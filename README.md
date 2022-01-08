![Library](https://user-images.githubusercontent.com/64320724/148652760-a908cd62-fc4a-4d3a-a188-807c850c8f3c.JPG)
Create table Student (ID_Card varchar(20), Student_Name varchar(50), gender varchar(10), Branch varchar(20), Year varchar(20), Contact varchar(30), Fine varchar(20) default 'NA');
select * from student;

insert into student values('01','Rohan Singh','Male','Btech','2020','7126254532','')
insert into student values('02','Mohan Soni','Male','Btech','2021','9658741258','')
insert into student values('03','Deepansh Tiwari','Male','BCom','2021','7569853243','')
insert into student values('04','Pankaj Singh','Male','BCA','2020','8659325471','')
insert into student values('05','Sonal Tiwari','Female','Btech','2020','7569852147','')
insert into student values('06','Pooja Singh','Female','BCA','2021','8523654789','')
insert into student values('07','Raman kumar','Male','BPharma','2021','756987896','')
insert into student values('08','Deepak Singh','Male','Btech','2020','7569877896','')
insert into student values('09','Aman Soni','Male','BCA','2021','9963658753','')
insert into student values('10','Shreya Singh','Female','Btech','2020','9696587412','')

Create table Books (ID_Card varchar(20), Book_Name varchar(50), MRP varchar(10), Book_ID varchar(20), Page_Count varchar(20));
select * from books;

insert into Books values('Computational Thinking and Problem Solving','Rs 450', 'B1', '463')
insert into Books values('Computer Programming','Rs 350', 'B2', '523')
insert into Books values('Communicative English','Rs 250', 'B3', '376')
insert into Books values('Calculus and Matrix Algebra','Rs 650', 'B4', '776')
insert into Books values('Data Structures and Algorithms','Rs 450', 'B5', '544')
insert into Books values('Discrete Mathematics','Rs 480', 'B6', '644')
insert into Books values('Object-Oriented Programming','Rs 280', 'B7', '444')
insert into Books values('Operating Systems','Rs 480', 'B8', '494')
insert into Books values('Computer Networks','Rs 350', 'B9', '594')
insert into Books values('Database Management Systems','Rs 750', 'B10', '922')


Create table Borrow (Book_ID varchar(20), Issue_Date varchar(20), Submit_Date varchar(20));
select * from borrow;

insert into borrow values('B1', '28 december 2021', '28 january 2022');
insert into borrow values('B2', '25 december 2021', '25 january 2022');
insert into borrow values('B3', '21 december 2021', '21 january 2022');
insert into borrow values('B4', '22 december 2021', '22 january 2022');
insert into borrow values('B5', '20 december 2021', '22 january 2022');
insert into borrow values('B6', '23 december 2021', '23 january 2022');
insert into borrow values('B7', '24 december 2021', '24 january 2022');
insert into borrow values('B8', '26 december 2021', '26 january 2022');
insert into borrow values('B9', '26 december 2021', '26 january 2022');
insert into borrow values('B10', '20 december 2021', '20 january 2022');


select * from student inner join books on Student.book_Id = Books.book_Id;
select * from student inner join books on Student.book_Id = Books.book_Id inner join borrow on student.book_id = borrow.book_id;
select Student_name, Branch, Book_name, submit_date from student inner join books on Student.book_Id = Books.book_Id inner join borrow on student.book_id = borrow.book_id;
