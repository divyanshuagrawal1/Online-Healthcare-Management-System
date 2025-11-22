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

**Backend**

* MySQL (database)
* JDBC (plain JDBC for DB access)
* DAO pattern (AppointmentDAO, UserDAO, etc.)

**Libraries / Tools**

* MySQL Connector/J (`mysql-connector-java-8.x.jar`)
* jBCrypt (`jbcrypt-0.4.jar`) — password hashing
* jdatepicker (`jdatepicker-1.3.4.jar`)
* FlatLaf (`flatlaf-3.4.jar`)
* IDE: NetBeans (project file included). Git & GitHub for version control.

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
