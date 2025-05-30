# Student and Faculty Portal (Flex)

## Project Overview

The "Student and Faculty Portal" is a **console-based Java application** designed to centralize and streamline information management for students and faculty members within a university setting. Inspired by established university portals like `flexstudent.nu.edu.pk` and `flex.nu.edu.pk`, this system aims to provide easy and secure access to essential academic and personal data for various user types through a command-line interface.

The primary objective is to create a robust system that caters to the distinct needs of students (both undergraduate and graduate) and faculty members (visiting and permanent), while also offering common functionalities for seamless interaction.

## Features

This portal is structured to serve two primary user roles: **Students** and **Faculty Members**, with a set of common functionalities accessible to both. The application interacts with a database to manage all user and academic data.

### Common Features (Students & Faculty)

* **Secure Authentication:** Users can securely log in to the system using their unique ID and password.
* **Session Management:** Functionality to sign out securely.
* **Password Management:** Users have the ability to change their passwords.
* **Personal Profile View:** Access to essential personal details, including ID Number, Name, Email Address, Contact Information, CNIC, and Address.

### Student Side Features

Students are categorized into two types: **Undergraduate** and **Graduate** students. Each student is assigned a unique ID for system login.

* **Academic Performance Tracking:**
    * View individual course marks.
    * Check attendance records for enrolled courses.
    * View current Grade Point Average (GPA).
    * Generate and print a complete academic transcript of all grades.
* **Course Management:**
    * Browse available courses for enrollment.
    * Enroll in new courses for the current semester.
    * Drop existing courses they are currently enrolled in.
    * View a comprehensive list of courses they are currently studying.
* **Financial Management:**
    * Access and print fee challans for paying university dues.
    * View detailed fee information.

### Faculty Side Features

Faculty members are categorized into two types: **Visiting Faculty** and **Permanent Faculty**. Each faculty member has a unique login and password.

* **Student Management (Course-Specific):**
    * **Attendance Management:** Add and see attendance records for students in their assigned courses.
    * **Marks Management:** Upload and edit students' Quiz, Mid, and Final marks for their courses.
    * **Course Roster Management:** Add or remove students from courses they teach.
* **Multi-Course Assignment:** Faculty members are not limited to teaching a single course and can be assigned to multiple courses concurrently.
* **Teaching Assistant (TA) Assignment:** Permanent faculty members have the unique ability to assign a Teaching Assistant (TA) to their courses.
* **Grade Generation:** Faculty can generate grades for students.

## Technologies Used

This project is implemented as a console application using the following technologies:

* **Java:** The core programming language.
* **JDBC (Java Database Connectivity):** Used for connecting to and interacting with a relational database. The code includes SQL queries for various operations like `SELECT`, `UPDATE`, and `INSERT`.
* **Relational Database:** An external database system (e.g., MySQL, PostgreSQL, SQLite) is required to store all application data, including user information, courses, marks, and attendance.

## Usage

Once the application is running, you will interact with it through the console:

1.  **Main Menu:** The application will present a welcome menu.
2.  **User Type Selection:** You will be prompted to choose whether you are a 'Faculty' or a 'Student'.
3.  **Login:** Enter your email and password to log in.
    * *Note: Initial mock users are created in `populateDatabase()`. You might need to check the code or database to find default credentials.*
4.  **Role-Specific Menu:** After successful login, you will be directed to either the `FacultyMenu` or `StudentMenu` with a list of available actions.
5.  **Interact:** Enter the number corresponding to the action you wish to perform (e.g., "1" to Upload Marks for Faculty, "1" to Check Attendance for Student).
6.  **Logout/Exit:** Select the logout option (e.g., "8" for Faculty, "11" or "0" for Student) to end your session or exit the application.
