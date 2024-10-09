# I320 Database Design: PSET-1 Report

### UT HR System, UT EMS Database, and HEB Supermarket Database Design
**Katie Shih & Shamiya Lin**  
**Instructor: Dr. Shounak Roychowdhury**

---

## Introduction
This report presents a detailed breakdown and design of three systems selected for PSET-1 of the I320 Database Design Programming course. The systems chosen are the **UT EMS Database**, the **UT HR System**, and the **HEB Supermarket Database**. This report is divided into two parts:

1. **Requirement Analysis**  
2. **ER Diagrams** for each system.  

The requirement analysis includes identifying key entities, relationships, and attributes. The ER diagrams visualize these relationships and form the basis for implementing databases in subsequent assignments.

---

## UT EMS (Emergency Medical Services) Database

We present the design of a **UT EMS (Emergency Medical Services) database**. This database keeps track of **ambulances**, **patients**, **diagnoses**, and **hospitals**. After analyzing the miniworld rules and the users’ needs, the requirements for this database were determined as follows:

- **HOSPITAL**  
Each hospital has a unique ID (HospitalID), a name (Name), a location (Address, separated into Street Address, City, Country, and Zip Code), and a capacity (Capacity, which tracks the number of beds). Each hospital may specialize in particular types of care (LocationCapabilities).

  - **Use Case**: When a hospital receives a patient from an ambulance, its availability (Capacity) is updated.

- **PATIENT**  
Each patient has a unique ID (PatientID), name (Name, including first and last names), date of birth (DOB), age (derived from DOB), gender, and address. The system also stores the patient’s contact information, emergency contact, and insurance details (InsuranceID).

  - **Use Case**: A patient makes an emergency call, and the system retrieves the patient’s medical records and insurance details for proper treatment.

- **EMERGENCY_CALL**  
Each call has a unique ID (EmergencyCallID), time of call (Time), caller information, and details about the emergency. The system tracks response times and calls for ambulances made by patients.

  - **Use Case**: A patient makes an emergency call, and the system finds the nearest ambulance and records the response time to ensure quick service.

- **AMBULANCE**  
Each ambulance has a unique ID (AmbulanceID), a driver’s name, location, and availability status. Ambulances have a capacity and are assigned maintenance schedules to maintain cleanliness and sterility.

  - **Use Case**: An ambulance is dispatched to pick up a patient, and its status is updated from “Available” to “On Duty.”

- **EMS_PERSONNEL**  
Each EMS personnel has a unique
