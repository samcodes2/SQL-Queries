# SQL1
Learning Structured Query Language
--Sql Server 2014 Express Edition
--Batches are separated by 'go'

select @@version as 'sql server version'
create table Customer
(
    Id int Primary Key identity(1,1),
    Firstname varchar(50),
    Lastname varchar(50),
    Age int
    )
--each variable is a column    
--varchar means variable with 50 character limit

insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Joey','Blue',40);
insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Barry','Bonds',50);
insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Mike','Schmidt',40);
insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Cookie','Burnt',25);    
insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Mike','Andy',50);    
insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Terry','Fun',30);
insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Terry','Muffin',33);    
insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Terry','Muffin1',30);    
insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Terry','Muffin2',30);    
insert into dbo.Customer (Firstname, Lastname, [Age])
    values('Terry','Muffin3',30);     
--select *
--from Customer

select id,FirstName,LastName,Age
from Customer
where FirstName = 'Terry'
and LastName = 'Fun'

--ok let's keep going

select id,FirstName,LastName,Age
from Customer
where FirstName = 'Terry'
and LastName like 'Muffin%'
--the '%' gives anything with 'Muffin'

select id,FirstName,LastName,Age
from Customer
where FirstName = 'Terry'
and LastName like 'Muffin_'
--the '_' gives anything with 'Muffin', but it MUST have the additional character too

update Customer
Set Age = 20
where FirstName = 'Terry'
and LastName = 'Fun'

--adding a column
alter table Customer
add City varchar(50)

update Customer
Set City = 'Santa Barb'
where FirstName = 'Terry'


update Customer
Set City = 'Erie'
where FirstName = 'Terry'
and LastName = 'Fun'

update Customer
Set City = 'Amherst'
where id = 4

select * from Customer
