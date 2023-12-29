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

