# Bus Booking System

This is a simple Java console application for bus reservation.  
It uses **JDBC** to connect and store booking details in a MySQL database.

## Features

- View available buses
- Book a seat for a specific bus and date
- Checks seat availability before booking

## Technologies Used

- Java
- JDBC (Java Database Connectivity)
- SQL Database (MySQL)

## Database Setup

This project uses MySQL for storing bus and booking details.

### Steps:

1. **Create Database and Tables:**
   ```sql
   create database busresv;
   use busresv;

   create table bus(
     id int primary key,
     ac boolean,
     capacity int
   );

   insert into bus values(1,1,22);
   insert into bus values(2,1,48);
   insert into bus values(3,0,52);

   create table booking(
     passenger_name varchar(50),
     bus_no int,
     travel_date date
   );
   ```

2. **Update JDBC Connection:**
   - In your Java DAO classes, use:
     ```
     jdbc:mysql://localhost:3306/busresv
     ```
   - Username/password as per your MySQL setup.

## How to Run

1. **Compile:**
   ```
   javac BusDemo.java
   ```

2. **Run:**
   ```
   java BusDemo
   ```

## File Structure

- `BusDemo.java` : Main program
- `Booking.java` : Booking logic
- `BusDAO.java` : Bus data access (JDBC)
- `BookingDAO.java` : Booking data access (JDBC)

## Author

Thanish