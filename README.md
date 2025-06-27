# <div align="center">🎓 Course Registration System</div>

<div align="center">
  
![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=28&duration=3000&pause=1000&color=00D9FF&background=00000000&center=true&vCenter=true&width=800&lines=Modern+Elective+Course+Management+Platform;Java+Spark+%7C+MongoDB+%7C+Responsive+Web+Design;Secure+Authentication+%7C+Admin+Dashboard;Student+Portal+%7C+Real-time+Enrollment+Tracking)

</div>

---

## 🌟 **Project Overview**

A sophisticated web-based platform for managing elective course registrations, featuring:
- **Student Portal** for course browsing and enrollment
- **Admin Dashboard** for comprehensive system management
- **Real-time** seat availability tracking
- **Secure** authentication system

```mermaid
graph TD
    A[Student] -->|Browse| B(Courses)
    A -->|Enroll| C[My Courses]
    D[Admin] -->|Manage| B
    D -->|Monitor| E[Enrollments]
    B --> F[(MongoDB)]
    C --> F
    E --> F

🚀 Key Features
<div align="center">
👨‍🎓 Student Experience
Feature	Description	Tech Used
🔐 Secure Login	Password-protected access with session management	Java Spark Sessions
📚 Course Catalog	Browse available electives with real-time seat data	MongoDB Aggregation
🎯 Smart Enrollment	One-click course registration with instant confirmation	AJAX, Java Spark
📱 Responsive Design	Fully functional on all devices	Flexbox, Media Queries
👨‍💼 Admin Capabilities
Feature	Description	Tech Used
⚙️ Course CRUD	Full lifecycle course management	MongoDB Driver
👥 User Management	View/delete student accounts	Java Spark Routes
📊 Enrollment Insights	Filter students by course selection	MongoDB Queries
📈 Capacity Monitoring	Visual seat availability tracking	Chart.js Integration
</div>
🛠️ Technical Architecture
java
// Core System Architecture
public class CourseRegistrationSystem {
    private SparkServer server;
    private MongoDatabase db;
    
    public void initialize() {
        configureRoutes();
        setupDatabase();
        startServer();
    }
    
    private void configureRoutes() {
        // Authentication endpoints
        post("/login", AuthController::handleLogin);
        
        // Course management
        get("/courses", CourseController::getAllCourses);
        post("/enroll", EnrollmentController::processEnrollment);
    }
}
Tech Stack
<div align="center">
Layer	Technology
Frontend	HTML5, CSS3, JavaScript, Bootstrap
Backend	Java Spark Framework
Database	MongoDB (NoSQL)
Authentication	Session-based Security
Build Tool	Maven
Deployment	Render/Heroku
</div>
📸 System Screenshots
<div align="center" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1rem;">
🔐 Secure Login Portal
https://github.com/user-attachments/assets/8d685a92-1e6e-4760-9d8c-9028f49f1c47

⚙️ Admin Dashboard
https://github.com/user-attachments/assets/cf42c01b-3b88-4bc6-aac9-6472a478dd2c

📚 Student Course View
https://github.com/user-attachments/assets/7c6f45b6-576c-4495-a316-71a2c516559e

📊 Enrollment Management
https://github.com/user-attachments/assets/43451d42-5965-47bd-a76f-6bde6e044b2f

</div>
🧩 Database Schema
javascript
// Courses Collection
{
  _id: ObjectId,
  code: "CSE201",
  title: "Web Development",
  description: "Modern web technologies",
  seats: 30,
  enrolled: ["student1@email.com"]
}

// Students Collection
{
  _id: ObjectId,
  name: "Abishek Kumar",
  email: "24mcab07@kristujayanti.com",
  password: "$2a$10$...", // bcrypt hash
  enrolledCourses: ["CSE201"]
}
🚧 Setup & Installation
bash
# Clone repository
git clone https://github.com/ALLURIABISHEK/Course-Registration.git
cd Course-Registration

# Install dependencies
mvn clean install

# Configure environment
cp .env.example .env
# Edit MongoDB URI in .env

# Run application
mvn exec:java -Dexec.mainClass="org.example.Main"
Requirements:

Java JDK 11+

MongoDB 4.4+

Maven 3.6+
