# Course-Registration
A web-based application that allows students to browse and register for elective courses, with an admin panel for course and user management. Built with Java Spark backend and MongoDB database.
Course Registration System
Overview
A web-based application that allows students to browse and register for elective courses, with an admin panel for course and user management. Built with Java Spark backend and MongoDB database.

Key Features
Student Features
🔐 Secure Authentication

Student registration with email verification

Password-protected login

📚 Course Management

Browse available elective courses

View course details (name, code, description, available seats)

Enroll in available courses

View currently enrolled courses

👤 User Profile

View personal information

Track course selections

Admin Features
⚙️ Course Management

Add new courses with details (title, code, description, seats)

Delete existing courses

View all available courses

👥 Enrollment Management

View students enrolled in each course

Remove students from courses

Monitor seat availability

👤 User Management

View all registered students

Delete student accounts

Track student course selections

Technical Specifications
Backend: Java Spark framework

Database: MongoDB (NoSQL)

Frontend: HTML5, CSS3, JavaScript

Authentication: Session-based

Responsive Design: Works on desktop and mobile devices

Database Structure (MongoDB Collections)
courses Collection
javascript
{
  courseName: "Web Development",
  courseCode: "CSE201", 
  description: "Learn HTML, CSS, and JavaScript",
  seatsAvailable: 30
}
students Collection
javascript
{
  name: "John Doe",
  email: "john@example.com",
  password: "hashed_password", 
  selectedCourse: "CSE201"
}
Setup Instructions
Prerequisites:

Java JDK 11+

MongoDB installed locally

Maven for dependency management

Installation:

bash
git clone [repository-url]
cd course-registration-system
mvn clean install
Configuration:

Update MongoDB connection string in MongoConnection.java

Configure email settings in EmailService.java

Running:

bash
mvn exec:java -Dexec.mainClass="org.example.Main"
Screenshots
(Add screenshots of your interface here)

Future Enhancements
Email notifications for course registration

Course waitlisting system

Student dashboard with academic progress

Faculty access portal
