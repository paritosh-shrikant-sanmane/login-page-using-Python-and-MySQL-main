# login-page-using-Python-and-MySQL


@@@@@ HOW TO RUN THIS PROJECT @@@@@


It's a GUI project using python tkinter and MySQL database.

Make sure you already have installed all the modules used in this project. Please see the requirement.txt file for all the requirements.


Steps to follow after installing all the modules. Otherwise this application will not work properly.

->Create a database with this name, "student_database"
->create a table with this name, "student_register"


USE this code to create the table under the "student_database" database

create table student_register(
   f_name VARCHAR(50) NOT NULL,
   l_name VARCHAR(50) NOT NULL,
   email VARCHAR(100) NOT NULL,
   question VARCHAR(50) NOT NULL,
   answer VARCHAR(100) NOT NULL,
   password VARCHAR(50) NOT NULL,
   PRIMARY KEY ( email )
);

Create a Dedicated MySQL User and Grant Privileges
I suggest to create a specific MySQL user exclusively for this project and grant the necessary privileges. Please perform the following steps:

1. Log in to MySQL:
You’ll need to have administrative access to your MySQL server. You can log in using the MySQL command-line client:

mysql -u root -p
Replace root with your MySQL username if it’s different, and you’ll be prompted for the MySQL root password.

2. Create a New User:
To create a new MySQL user, you can use the `CREATE USER` command. Replace `username` and `password` with your desired username and password:

CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
This creates a user called `username` that can only connect from the local machine. If you want to allow connections from any host, replace `localhost` with `%`.

3. Grant Privileges:
You can use the `GRANT` statement to assign privileges to the user. Here’s how to grant various privileges:

Grant all privileges on a specific database:
GRANT ALL PRIVILEGES ON database_name.* TO 'username'@'localhost';
Grant specific privileges (e.g., GRANT CREATE, ALTER, DROP, INSERT, UPDATE, INDEX, DELETE, SELECT, REFERENCES, RELOAD) on a specific database:
GRANT SELECT, INSERT, UPDATE, DELETE ON database_name.* TO 'username'@'localhost';
Replace `database_name` with the name of the database you want to grant access to.

Grant all privileges on all databases (not recommended for security reasons):
GRANT ALL PRIVILEGES ON *.* TO 'username'@'localhost';

4. Apply Privileges:
After granting privileges, you need to apply the changes using the FLUSH PRIVILEGES command:

FLUSH PRIVILEGES;
5. Exit MySQL:
Now you can exit the MySQL Client:

exit;

Done!

if you still need help. don't shy to ask, I'll happy to help you.

Email: paritoshsanmane123@gmail.com
