# 🏥 Hospital Management System with IoT-Based Vitals Monitoring

A **Java-based Hospital Management System** with **MySQL** integration to efficiently manage patient, doctor, and appointment records. The system now includes an **IoT simulation module** that monitors patient vitals (heart rate and temperature) and **sends SMS alerts** if abnormal conditions are detected using **Twilio API**.


## ✨ Features

### Core Management System:
- **Add Patient**: Input patient details like name, age, and gender.
- **View Patients**: Display all registered patients.
- **Add Doctor**: Register doctors with name and specialization.
- **View Doctors**: List all doctors.
- **Book Appointment**: Schedule appointments between patients and doctors.

### IoT-Based Vitals Monitoring:
- **Vitals Class**: Represents vital signs data (heart rate, temperature) linked to patients.
- **IOTSimulator**:
  - Simulates vitals for a list of patients.
  - Periodically generates random heart rate and temperature values.
  - Inserts readings into the `Vitals` table in MySQL.
  - **Sends SMS alerts** if vitals are out of the normal range using Twilio.


## 🚨 Alert Criteria

SMS alerts are triggered when any of the following is true:
- **Heart rate** < 60 bpm or > 100 bpm
- **Temperature** < 36.1 °C or > 37.8 °C


## 🧰 Prerequisites

- **Java (JDK 8+)**
- **MySQL**
- **JDBC**
- **MySQL Connector/J**
- **Twilio Java SDK** (for SMS integration)
