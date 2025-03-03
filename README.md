# sbb3_todo

## 📌 Project Overview
sbb3_todo is a **Java-based To-Do Web Application** that allows users to register, log in, add tasks, and mark them as completed. It is built using **Servlets, JSP, JDBC, and MySQL**.

## 📁 Folder Structure
```
sbb3_todo/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── beans/
│   │   │   │   ├── Register.java
│   │   │   │   ├── Task.java
│   │   │   ├── factory/
│   │   │   │   ├── DBConn.java
│   │   │   ├── dao/
│   │   │   │   ├── ToDoDAO.java
│   │   │   │   ├── ToDoDAOImpl.java
│   │   │   ├── servlets/
│   │   │   │   ├── RegisterServlet.java
│   │   │   │   ├── LoginServlet.java
│   │   │   │   ├── AddTaskServlet.java
│   │   │   │   ├── MarkTaskCompletedServlet.java
│   │   │   │   ├── LogoutServlet.java
│   ├── webapp/
│   │   ├── Register.html
│   │   ├── Login.jsp
│   │   ├── ViewTasks.jsp
│   │   ├── WEB-INF/
│   │   │   ├── web.xml
├── pom.xml  (if using Maven)
├── README.md
```

## 🚀 Technologies Used
- **Java (JDK 17)**
- **Servlets & JSP**
- **MySQL (JDBC for database connectivity)**
- **Apache Tomcat (Web Server)**
- **Eclipse IDE**

## 🔧 Setup Instructions
### **1️⃣ Install Required Software**
- **Java Development Kit (JDK 17)**
- **Apache Tomcat 8.5**
- **MySQL 8 / XAMPP**
- **Eclipse IDE**


### **4️⃣ Configure MySQL Database**
1. Open **MySQL Workbench** or **phpMyAdmin**.
2. Create a database:
```sql
CREATE DATABASE sbb3_todo;
```
3. Run the following SQL to create tables:
```sql
CREATE TABLE register (
    regid INT PRIMARY KEY,
    fname VARCHAR(20),
    lname VARCHAR(20),
    email VARCHAR(50),
    pass VARCHAR(20),
    mobile BIGINT,
    address VARCHAR(50)
);

CREATE TABLE tasks (
    taskid INT,
    taskname VARCHAR(50),
    taskdate VARCHAR(10),
    taskstatus INT CHECK (taskstatus IN (1,2,3)),
    regid INT,
    PRIMARY KEY (taskid, regid),
    FOREIGN KEY (regid) REFERENCES register(regid)
);
```

### **5️⃣ Run the Project on Tomcat**
1. Right-click on the project → **Run As** → **Run on Server**.
2. Select **Apache Tomcat** and click **Finish**.
3. Open a browser and go to:
   - **Registration Page:** `http://localhost:8080/sbb3_todo/Register.html`
   - **Login Page:** `http://localhost:8080/sbb3_todo/Login.jsp`

## 📜 Features
✅ **User Registration & Login**
✅ **Add New Tasks**
✅ **View All Tasks**
✅ **Mark Tasks as Completed**
✅ **Logout Functionality**



