# SQL1
Learning Structured Query Language

#making a table
create table Customer
(
    Firstname varchar(50),
    Lastname varchar(50),
    Age int
    )
#varchar means this column variable has up to 50 characters

insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Joey','Blue',40);
insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Barry','Bonds',50);
insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Mike','Schmidt',40);
            
select *
from Customer
#takes all data
