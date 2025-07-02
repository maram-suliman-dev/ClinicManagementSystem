# Clinic Management System

This is a simple medical clinic management system created as a learning project using C# and SQL Server with Entity Framework Core (Code First).

## Overview
The project allows managing doctors, patients, and their appointments. It was built step-by-step using the Code First approach, where I started by writing C# classes and generated the database from the code.

## Main Tables
- **Doctors**: stores doctor's name and specialty.
- **Patients**: stores patient information such as name and phone number.
- **Appointments**: connects each patient with a doctor and stores the appointment date.

## Tech Stack
- C# (.NET Core)
- Entity Framework Core (Code First)
- SQL Server
- Visual Studio

## How It Works
1. I created three main classes: `Doctor`, `Patient`, and `Appointment`.
2. Then I created a DbContext class called `ClinicContext` to manage the connection.
3. I used `Add-Migration` and `Update-Database` to generate the tables in SQL Server.
4. Finally, I tested the system by inserting sample doctors, patients, and appointments.

## Example Code

```csharp
var doctor = new Doctor { Name = "Dr. Aisha", Specialty = "Dermatology" };
var patient = new Patient { FullName = "Maram", Phone = "91234567" };
var appointment = new Appointment
{
    AppointmentDate = DateTime.Now,
    DoctorId = doctor.Id,
    PatientId = patient.Id
};
