CODE:

form departments
{
	displayname = "Departments"
	success message = "Data Added Successfully!"
	Section
	(
		type = section
	 	row = 1
	 	column = 0   
		width = medium
	)
	department_name
	(
    	type = text
		displayname = "Department Name"
	 	row = 1
	 	column = 1   
		width = medium
	)
	mail_alias
	(
    	type = text
		displayname = "Mail Alias"
	 	row = 1
	 	column = 1   
		width = medium
	)
	
	actions
	{
		on add
		{
			submit
			(
   				type = submit
   				displayname = "Submit"
			)
			reset
			(
   				type = reset
   				displayname = "Reset"
			)
		}
		on edit
		{
			update
			(
   				type = submit
   				displayname = "Update"
			)
			cancel
			(
   				type = cancel
   				displayname = "Cancel"
			)
		}
	}
}


PROJECT STRUCTURE

employee-management-system/
│
├── app.py
├── config.py
├── requirements.txt
│
├── models/
│   ├── employee.py
│   └── department.py
│
├── routes/
│   ├── auth.py
│   ├── employee.py
│   └── department.py
│
├── templates/
│   ├── login.html
│   ├── dashboard.html
│   ├── employees.html
│   ├── add_employee.html
│   └── edit_employee.html
│
├── static/
│   ├── css/
│   ├── js/
│   └── images/
│
└── database/
    └── schema.sql

Employee Table

Column    	Type
id	        INT
name	     VARCHAR
email	    VARCHAR
phone	    VARCHAR
department_id 	INT
designation	  VARCHAR
salary	   FLOAT
joining_date	 DATE

Department Table

Column	  Type
id	      INT
department_name	 VARCHAR

Installation
Clone Repository
git  clone https://github.com

Create Virtual Environment
python -m venv venv

Activate Environment

Windows

venv\Scripts\activate

Linux/Mac

source venv/bin/activate
Install Dependencies
pip install -r requirements.txt

Configure Database

Create MySQL database:
  SQL
CREATE DATABASE employee_management;

Update database credentials in:

config.py

Run Application

python app.py

Application URL:

http://127.0.0.1:5000
