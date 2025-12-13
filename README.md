# 🏥 Online Healthcare Management System (Java Swing + MySQL)

**A desktop & optional web module** for hospital administration: patient registration, doctor management, appointment booking, and basic records.
Built with **Java Swing** (desktop UI), **JDBC / MySQL** (database), DAO pattern, transaction-handling, and GUI responsiveness (multithreading).

## ✨ Key Features

* **User Authentication** — Admin login with secure password hashing (bcrypt).
* **Admin Dashboard** — Central interface to manage doctors, patients, and appointments.
* **Patient Management** — Add / Edit / Delete patient profiles.
* **Doctor Management** — Add / Edit / Delete doctors, specializations.
* **Appointment Management** — Create / Update / Delete appointments, status tracking.
* **Search & Filtering** — Live search in tables (TableRowSorter).
* **Background Loading** — Multithreading used to load lists and refresh appointment data without freezing the UI.
* **Synchronization** — Critical sections and synchronized DAO operations to avoid concurrent write conflicts.
* **JDBC + Transactions** — PreparedStatements, proper commit/rollback, connection pooling-ready pattern.
* **Clean Architecture** — Model classes, DAO interfaces + Impl, UI frames separated for maintainability.

## 🧰 Technologies Used

**Frontend**

* Java Swing, AWT
* JDatePicker (date selection)
* FlatLaf (modern look & feel)
* JSP, HTML, CSS

**Backend**

* MySQL (database)
* JDBC (plain JDBC for DB access)
* DAO pattern (AppointmentDAO, UserDAO, etc.)
* Java Servlets

**Libraries / Tools**

* MySQL Connector/J (`mysql-connector-java-8.x.jar`)
* jBCrypt (`jbcrypt-0.4.jar`) — password hashing
* jdatepicker (`jdatepicker-1.3.4.jar`)
* FlatLaf (`flatlaf-3.4.jar`)
* IDE: NetBeans (project file included). Git & GitHub for version control.
* Server: Apache Tomcat 9


## 🤔 Features

*  Admin login (authenticate using email + password)
*  Manage Doctors: Add / edit / delete / list
*  Manage Patients: Add / edit / delete / list
*  Appointments: Create / Update / Delete / List with date-time picker
*  Search & Live filter for appointments
*  Background data loading (multithreading) so UI never freezes
*  Synchronized booking (prevents double-booking)
*  Secure password hashing using bcrypt
*  JDBC prepared statements (prevents SQL injection)
*  DAO layer and model classes for clean separation
*  
---

## 🚀 Servlets Used

### 🔹 LoginServlet
**Purpose:**  
- Authenticates users using database validation  
- Creates session on successful login  

**Key Concepts:**  
- `HttpServlet`
- `doPost()`
- `HttpSession`
- JDBC (`PreparedStatement`)

---

### 🔹 LogoutServlet
**Purpose:**  
- Logs out user securely  

**Functionality:**  
- Invalidates session  
- Redirects to login page  

---

### 🔹 DoctorServlet
**Purpose:**  
- Handles doctor management  

**Functionality:**  
- Accepts doctor details from JSP  
- Inserts data into MySQL  
- Forwards success message  

---

### 🔹 PatientServlet
**Purpose:**  
- Handles patient registration  

**Functionality:**  
- Receives patient data  
- Stores it in database  
- Displays confirmation  

---

## 🧾 JSP Pages Used

### 🔹 login.jsp
- User login interface  
- Sends data to `LoginServlet`  
- Displays error messages  

---

### 🔹 index.jsp (Dashboard)
- Main landing page after login  
- Displays navigation menu  
- Session-protected  

---

### 🔹 addDoctor.jsp / viewDoctor.jsp
- Add doctor details  
- View doctor list in tabular form  

---

### 🔹 addPatient.jsp / viewPatient.jsp
- Register patient  
- View patient records  

---

### 🔹 success.jsp
- Displays confirmation messages after operations  

---

## 🔐 Session Management

- Session created after successful login
- Session attribute: `username`
- Protected pages check session validity
- Logout destroys session using `session.invalidate()`

---

## 🗄️ Database Tables

- `user` – login credentials
- `doctor` – doctor details
- `patient` – patient details
- `appointments` – appointment records

---

## 🎨 UI Enhancement

- External CSS used (`style.css`)
- Card-based layout
- Gradient buttons
- Hover effects
- Professional healthcare theme

---

## ✅ Code Quality & Execution

- Clean package structure
- No SQL inside JSP
- Centralized DB connection
- Proper exception handling
- Modular servlets

---

## 🌟 Innovation / Extra Effort

- Session-based security
- UI enhancement using CSS
- MVC-ready structure
- Scalable design

-
