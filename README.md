Download Link: https://assignmentchef.com/product/solved-cs313-assignment-3
<br>
<span class="kksr-muted">Rate this product</span>

Do the following using psql only: (no pgadmin)

Q1. create user and schema called lab3(instructions for creating user and database are given at the last section of this page)

Q2. create the following tables.The attributes with id mentioned are keys for the respective tables.:

<ul>

 <li>●  part – containing part-no ( id ), part-name, colour, weight</li>

 <li>●  supplier – containing supplier-no ( id ), sup-name, city, bank</li>

 <li>●  shipment – containing shipment-no ( id ),part-no, supplier-no, date, quantity, price (perunit)(Shipment contains data about parts supplied by various suppliers)Q3. Add one tuple in each table interactively using psql insert statement.Q4. Create a .sql file to load more data in these tables so that they have at least 3 parts, 2 suppliers, and 4 shipments for each part.(instructions for creating .sql file are given at the last section of this document)Q5. Execute the following queries.</li>

</ul>

<ul>

 <li>●  list supplier who have supplied red parts</li>

 <li>●  get total cost of shipments for all suppliers for making payments to them</li>

 <li>●  list suppliers who have supplied all parts.</li>

</ul>

<ol>

 <li>There will be no quiz question for this lab.</li>

</ol>

To create the user with password, run the below command :

$ CREATE USER youruser WITH ENCRYPTED PASSWORD ‘yourpass’;

EX : CREATE USER lab3 WITH ENCRYPTED PASSWORD ‘123’’;

To create the database and grant privileges to the created user, run the below commands:

​$ CREATE DATABASE yourdbname;

EX : CREATE DATABASE lab3;

$ GRANT ALL PRIVILEGES ON DATABASE yourdbname TO youruser;

Ex : GRANT ALL PRIVILEGES ON DATABASE lab3 TO lab3;

To login with a new user lab3.Close the terminal and open it again.Run the following command to connect to postgres:

$ psql -U lab3 (enter the password)

To Connect to the database lab3

$ c lab3;

( After connecting to the database ,you can start creating the tables )

Instructions for creating .sql file

<ol>

 <li>Use any text editor and create a file with extension as .sql</li>

 <li>Include the insert statements in the .sql file as it is.( with respect to Q 4).</li>

 <li>We have uploaded a sample .sql file on moodle for your reference.</li>

</ol>

Running .sql file in psql terminal

i path_to_sql_file

Example :

​( For linux &amp; mac )1. i /home/sysad/Downloads/insert.sql;

( note the / for directory separator in linux &amp; no spaces in file path )

( For windows )

2. i ‘C:\Users\admin\Desktop\Postgresql_demo\insert.sql’;