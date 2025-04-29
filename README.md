About the Project

The Hospital Management System is a Java-based application designed to streamline hospital operations. It offers features for managing doctors, patients, and appointments efficiently. By integrating with a MySQL database, this system ensures secure and robust data handling.

📂 Project Structure

HospitalManagementSystem.java: Main program file that handles user interactions and menu options.

Doctor.java: Contains functionalities to manage and display doctors' data.

Patient.java: Provides functionalities to manage and display patients' data.

🚀 Features

Add new patients.

View the list of registered patients.

View the list of available doctors.

Book appointments between patients and doctors.

Validate doctors' availability during appointment booking.

🛠️ Technologies Used

Java (Core Java, JDBC for database connectivity)

MySQL (Relational database management system)

JDBC Driver (com.mysql.cj.jdbc.Driver)

⚙️ Setup Instructions

1. Clone the Repository

git clone <repository-link>

2. Configure the MySQL Database

Create a database named hospital.

Execute the following SQL scripts:

CREATE TABLE doctors (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    specialization VARCHAR(100)
);

CREATE TABLE patients (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    age INT,
    gender VARCHAR(10)
);

CREATE TABLE appointments (
    id INT PRIMARY KEY AUTO_INCREMENT,
    patient_id INT,
    doctor_id INT,
    appointment_date DATE,
    FOREIGN KEY (patient_id) REFERENCES patients(id),
    FOREIGN KEY (doctor_id) REFERENCES doctors(id)
);

Insert sample data into the doctors table:

INSERT INTO doctors (name, specialization) VALUES
('Dr. John Doe', 'Cardiologist'),
('Dr. Jane Smith', 'Dermatologist'),
('Dr. Emily Johnson', 'Pediatrician');

3. Update Database Credentials

Edit the following lines in HospitalManagementSystem.java:

private static final String username = "<your-username>";
private static final String password = "<your-password>";

4. Compile and Run the Application

javac -d . *.java
java HospitalManagementSystem.HospitalManagementSystem

📋 Usage

When you run the program, you will be presented with the following menu:

HOSPITAL MANAGEMENT SYSTEM
1. Add Patient
2. View Patients
3. View Doctors
4. Book Appointment
5. Exit
Enter your choice:

Choose the desired option to perform an action.

Follow the prompts to add patients, view records, or book appointments.

✨ Future Enhancements

Implement a graphical user interface (GUI) using JavaFX or Swing.

Add features to update and delete patient/doctor records.

Include a login system for administrators and doctors.

Generate comprehensive reports for appointments and records.

👨‍💻 Author

Developed by Abhishek. Contributions and suggestions are welcome to improve the project further.

