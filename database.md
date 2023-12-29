views vs materialized views.

select * from accounts

create view view_200_300 AS SELECT * FROM accounts WHERE balance <= 300 and balance >=200;
select * from view_200_300;
update accounts SET balance = 900 WHERE id=4;
select * from view_200_300;

why view? use it when you run a query alot like the between query, this view is a macro to the query. it doesnt cache but runs in the background; main purpose is to make queries shorter and compact.

materialized view
this takes a snapshot from the data 


create materialized view materialized_view AS SELECT * FROM accounts WHERE balance <=500 AND balance >=400;
select * from materialized_view;
update accounts SET balance = 600 WHERE id=7;
select * from materialized_view;

select * from accounts;


to be able to see updated data refresh the view.
refresh materialized view materialized_view;

CREATE TABLE accounts (
    id SERIAL PRIMARY KEY,
    owner VARCHAR(255) NOT NULL,
    balance DECIMAL(10, 2) NOT NULL,
    currency VARCHAR(3) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE OR REPLACE FUNCTION add_entries_to_accounts()
RETURNS VOID AS $$
DECLARE
    i INT := 1;
BEGIN
    WHILE i <= 50000 LOOP
        INSERT INTO accounts (id, owner, balance, currency, created_at)
        VALUES (
            DEFAULT,                        -- Assuming id is a serial or identity column
            'Owner ' || i,                  -- Sample owner value
            random() * 1000,                -- Sample balance value (adjust as needed)
            'USD',                          -- Sample currency value
            now() - (i || ' days')::INTERVAL -- Sample created_at value
        );
        
        i := i + 1;
    END LOOP;
END;
$$ LANGUAGE PLPGSQL;

select add_entries_to_accounts();