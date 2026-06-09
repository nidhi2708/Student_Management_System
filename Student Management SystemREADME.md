# ***Student Management System***



A database management system developed using Oracle SQL and PL/SQL for managing student records, courses, enrollments, marks, and attendance. The project demonstrates core database concepts along with advanced PL/SQL features such as stored procedures, functions, triggers, cursors, and exception handling.

### 

#### **Features:**



Manage student information

Manage course details

Track student enrollments

Record and maintain marks

Monitor attendance

Generate student performance reports

Automated grade calculation

Data validation using triggers

Exception handling for duplicate records

Cursor-based student record display



#### **Technologies Used:**



Oracle Database XE

Oracle SQL Developer

SQL

PL/SQL



#### **Database Schema:**



STUDENT

Column	Type

STUDENT\_ID	NUMBER

STUDENT\_NAME	VARCHAR2(50)

GENDER	VARCHAR2(10)

PHONE	VARCHAR2(15)

EMAIL	VARCHAR2(50)

DEPARTMENT	VARCHAR2(30)

COURSE

Column	Type

COURSE\_ID	NUMBER

COURSE\_NAME	VARCHAR2(50)

CREDITS	NUMBER

ENROLLMENT

Column	Type

ENROLLMENT\_ID	NUMBER

STUDENT\_ID	NUMBER

COURSE\_ID	NUMBER

ENROLLMENT\_DATE	DATE

MARKS

Column	Type

MARK\_ID	NUMBER

STUDENT\_ID	NUMBER

COURSE\_ID	NUMBER

MARKS	NUMBER

ATTENDANCE

Column	Type

ATTENDANCE\_ID	NUMBER

STUDENT\_ID	NUMBER

COURSE\_ID	NUMBER

ATTENDANCE\_PERCENT	NUMBER



#### **Entity Relationships:**



STUDENT

&#x20;  |

&#x20;  +---- ENROLLMENT ---- COURSE

&#x20;  |

&#x20;  +---- MARKS

&#x20;  |

&#x20;  +---- ATTENDANCE 



##### **PL/SQL Components Implemented:**



###### 1\. Stored Procedure



ADD\_STUDENT

Adds a new student record into the STUDENT table.



###### 2\. Function



CALCULATE\_GRADE

Calculates grades based on student marks.



Marks Range	Grade

90+	A

80-89	B

70-79	C

Below 70	D

###### 

###### 3\. Trigger



CHECK\_MARKS

Validates marks before insertion or update and prevents negative values.



Example:

INSERT INTO MARKS VALUES (10,101,201,-5);



Output:

ORA-20001: Marks cannot be negative



###### 4\. Exception Handling



SAFE\_ADD\_STUDENT

Handles duplicate student ID insertion attempts gracefully.



Output:

Student ID already exists



###### 5\. Cursor



DISPLAY\_STUDENTS

Displays student records using an explicit cursor.



###### Example Output:

101 - Rahul

102 - Priya

103 - Arjun

104 - Ananya

Sample Report Query

The project generates student performance reports by joining multiple tables.



##### **Sample Output:**



Student Name	Course Name	Marks	Attendance

Rahul	Database Management Systems	85	95

Rahul	Data Structures	92	90

Priya	Database Management Systems	78	80

Arjun	Operating Systems	88	92



#### **Learning Outcomes:**



Through this project, the following concepts were implemented and practiced:

Relational Database Design

Normalization

Primary Keys

Foreign Keys

SQL Joins

Stored Procedures

Functions

Triggers

Cursors

Exception Handling

Report Generation

Data Integrity and Validation



##### **Future Enhancements:**

Web-based front-end interface

Student login module

Faculty login module

Attendance dashboard

Performance analytics

Automated GPA calculation

Role-based access control



Author

Srinidhi Gadde

B.Tech Computer Science Engineering

Mahindra University

