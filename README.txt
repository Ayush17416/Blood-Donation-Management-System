Blood Donation Management System
Overview
This project is a simple Blood Donation Management System that uses Java with JDBC to interact with a MySQL database. The system allows users to manage information about donors, hospitals, and blood drives.
Requirements
To run this project, you need to have the following installed:
•	Java Development Kit (JDK): Version 8 or higher.
•	Apache Maven: For managing project dependencies and building the project.
•	MySQL Database: A running MySQL server with access credentials.
•	IntelliJ IDEA: Recommended IDE for Java development.
Database Setup
1.	Create a Database:
o	Create a new database in MySQL named blood_donation.
2.	Create Tables:
o	Run the following SQL scripts to create necessary tables:
CREATE TABLE donors (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    blood_type VARCHAR(10) NOT NULL,
    location VARCHAR(100) NOT NULL
);

CREATE TABLE hospitals (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    location VARCHAR(100) NOT NULL
);

CREATE TABLE blood_drives (
    id INT AUTO_INCREMENT PRIMARY KEY,
    location VARCHAR(100) NOT NULL,
    date DATE NOT NULL
);
3.	Configure Database Connection:
o	Update the DB_URL, USER, and PASSWORD constants in the JDBCConnector.java file to match your MySQL setup.
Project Setup
1.	Clone the Repository:
git clone <repository-url>
cd web
2.	Navigate to Project Directory: Ensure you are in the project directory where the pom.xml file is located.
3.	Install Dependencies: Run the following command to install project dependencies:
mvn install
Running the Project
1.	Open IntelliJ IDEA:
o	Open the project in IntelliJ IDEA.
2.	Run the Main Class:
o	Find the JDBCConnector class in the src/main/java/com/jdbc/connector directory.
o	Right-click on the class and select Run 'JDBCConnector.main()'.
3.	Testing Functionality:
o	Uncomment the lines in the main method of JDBCConnector to test adding donors, retrieving all donors, and other operations as needed.
Note
Ensure that your MySQL server is running and accessible with the provided credentials before running the project.
License
This project is licensed under the MIT License - see the LICENSE file for details.

