<div align="center">

# 🎓 Student Monitoring System

![PHP](https://img.shields.io/badge/PHP-8-777BB4?logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8-4479A1?logo=mysql&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![XAMPP](https://img.shields.io/badge/Server-XAMPP-FB7A24?logo=xampp&logoColor=white)
![License](https://img.shields.io/badge/License-Educational-yellow)

### A role-based web app for managing student attendance, grades, and study materials

Faculty manage student records, attendance, and grades — students log in to view their own progress and download materials, all through a simple PHP + MySQL backend.

</div>

---

## 📖 Overview

The **Student Monitoring System** is a PHP-based web application built to help faculty manage and monitor student attendance and grades efficiently, while giving students easy access to their own data.

It enables:
- 👨‍🏫 **Faculty** to add, update, and delete student records
- 📊 **Faculty** to insert and update subject-wise attendance and grades
- 📁 **Faculty** to upload subject-wise study materials
- 👩‍🎓 **Students** to view their own attendance, grades, and download materials
- 🔐 **Role-based, session-authenticated login** for both user types

---

## ✨ Features

**Faculty**
- ➕ Add, update, and delete student records
- 🗓️ Insert and update attendance (subject-wise)
- 📝 Insert and update grades/marks (subject-wise)
- 📤 Upload study materials (PDF / JPG / PNG) per subject

**Student**
- 🔑 Secure login with student credentials
- 📅 View subject-wise attendance
- 🏆 View grades/results
- 📥 Download uploaded study materials

**General**
- 🔒 Role-based login (Faculty / Student) with session-based authentication
- 📚 Subjects covered: Maths, SCP, PPS, HW, English, EVS
- 🖼️ Clean, icon-based dashboard UI

---

## 🛠️ Tech Stack

| Layer        | Technology                          |
|--------------|--------------------------------------|
| Backend      | PHP (mysqli, prepared statements)    |
| Database     | MySQL / MariaDB                      |
| Frontend     | HTML5, CSS3                          |
| Local Server | XAMPP / WAMP (Apache + MySQL)        |

---

## 📂 Project Structure

```
Project/
├── index.php                # Faculty dashboard
├── StudentHome.php           # Student dashboard
├── login.php                 # Role-based login
├── logout.php
├── config.php                # Database connection config
├── AddStudent.php / UpdateStudent.php / DeleteStudent.php
├── InsertAttendance.php / UpdateAttendance.php / Attendance.php
├── InsertGrade.php / UpdateGrade.php / Result.php
├── UploadMaterial.php / DownloadPage.php / download.php
├── Maths.php, SCP.php, PPS.php, HW.php, English.php, EVS.php   # Subject-wise pages
├── Style.css / student.css   # Stylesheets
├── Uploaded/                 # Uploaded study materials
├── sql.sql                   # Database schema + sample data
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- [XAMPP](https://www.apachefriends.org/) (or any Apache + MySQL/MariaDB + PHP stack)
- PHP 8+

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Samarth-patel25/Student-Monitoring-System.git
   ```

2. **Move the project into your server's document root**
   ```bash
   # Example for XAMPP on Windows
   Move the project folder into C:\xampp\htdocs\
   ```

3. **Create the database**
   - Start Apache and MySQL from the XAMPP control panel
   - Open [phpMyAdmin](http://localhost/phpmyadmin)
   - Create a new database (e.g., `student_monitoring`)
   - Import `sql.sql` into it

4. **Configure the database connection**

   Update `config.php` with your own database credentials (server, username, password, and database name).

5. **Run the project**

   Visit:
   ```
   http://localhost/Student-Monitoring-System/login.php
   ```

> ⚠️ **Note:** `sql.sql` contains sample faculty/student records for testing purposes. Replace or remove these before using the app beyond local development, and never commit real credentials to the repository.

---

## 🗄️ Database Schema

The system uses 5 main tables:

| Table        | Purpose                                                  |
|--------------|-----------------------------------------------------------|
| `students`   | Student records and login credentials                    |
| `faculties`  | Faculty login credentials                                 |
| `attendance` | Subject-wise attendance (Total / Present) per student     |
| `grades`     | Subject-wise marks (Total / Obtained) per student          |
| `material`   | Uploaded study material metadata (file path, subject)      |

---

## 🔐 Security Notes

This was built as an academic/learning project. Before using it beyond a local/demo environment, consider:
- Hashing all passwords with `password_hash()` (some sample records currently store plaintext)
- Moving DB credentials out of version control (`.env` or ignored config)
- Adding CSRF protection and stricter file-upload validation

---

## 📄 License

This project is open-source and free to use for educational purposes.

## 👤 Author

**Samarth Patel**
B.Tech CSE, Dharmsinh Desai University
