# Online Complaint Registration and Tracking System

## Project Overview
A web-based complaint management system built with HTML, CSS, JavaScript, Java Servlets, and MySQL.

---

## File Structure and Content

### HTML Files (html/)
- **index.html** - Home page with navigation and features
- **register.html** - Complaint registration form
- **track.html** - Track complaint by ID
- **admin-login.html** - Admin login page
- **admin-dashboard.html** - Dashboard template

### CSS (css/)
- **style.css** - Complete styling for all pages

### JavaScript (js/)
- **validation.js** - Form validation for registration
- **track.js** - Tracking functionality
- **admin-login.js** - Login validation
- **admin-dashboard.js** - Dashboard interactions

### Java Servlets (com/complaint/servlet/)
- **ComplaintServlet.java** - Handles complaint registration
- **TrackComplaintServlet.java** - Handles tracking
- **AdminLoginServlet.java** - Admin authentication
- **ViewComplaintsServlet.java** - Shows dashboard
- **UpdateComplaintServlet.java** - Updates complaint status
- **LogoutServlet.java** - Admin logout

### Utility (com/complaint/util/)
- **DBConnection.java** - Database connection management

### Configuration (WEB-INF/)
- **web.xml** - Deployment descriptor
- **lib/** - mysql-connector-j-9.6.0.jar

---

## How to Run

### Step 1: Setup Database
```sql
CREATE DATABASE complaint_system;
USE complaint_system;
-- Run the schema.sql file
```

### Step 2: Configure Database
Edit `com\complaint\util\DBConnection.java` and set your MySQL password:
```java
private static final String DB_PASSWORD = "your_password";
```

### Step 3: Deploy to Tomcat
Copy the `ComplaintSystem` folder to:
```
C:\Program Files\Apache Software Foundation\Tomcat 11.0\webapps\
```

### Step 4: Compile Java Files
Open Command Prompt in the ComplaintSystem directory:

**Compile Servlets:**
```cmd
javac -cp ".;C:\Program Files\Apache Software Foundation\Tomcat 11.0\webapps\ComplaintSystem\WEB-INF\lib\mysql-connector-j-9.6.0.jar;C:\Program Files\Apache Software Foundation\Tomcat 11.0\lib\servlet-api.jar" com\complaint\servlet\*.java
```

**Compile Database Connection:**
```cmd
javac -cp ".;C:\Program Files\Apache Software Foundation\Tomcat 11.0\webapps\ComplaintSystem\WEB-INF\lib\mysql-connector-j-9.6.0.jar;C:\Program Files\Apache Software Foundation\Tomcat 11.0\lib\servlet-api.jar" com\complaint\util\DBConnection.java
```

### Step 5: Start Tomcat
Navigate to Tomcat bin folder:
```cmd
cd C:\Program Files\Apache Software Foundation\Tomcat 11.0\bin
startup.bat
```

### Step 6: Access Application
Open browser and go to:
```
http://localhost:8080/ComplaintSystem/html/index.html
```

---

## Default Admin Login
- **Username:** admin
- **Password:** admin123

---

## Technologies Used
- Frontend: HTML, CSS, JavaScript
- Backend: Java Servlets
- Database: MySQL
- Server: Apache Tomcat 11
