# 29187409-TravelBookingSystem

## Overview

The Travel Booking System is designed to manage travel bookings, customer information, and itinerary details for a travel agency. This project includes the creation of a database schema, the insertion of sample data, and the development of PL/SQL procedures to handle booking management, customer registration, and itinerary tracking.

## Features

- **Booking Management:** Add, update, delete, and search for bookings.
- **Customer Registration:** Register new customers.
- **Itinerary Tracking:** Track travel itineraries.

## Database Schema

### Bookings Table

| Column        | Data Type  | Constraints                              |
|---------------|------------|------------------------------------------|
| BOOKING_ID    | Number     | Primary Key                              |
| CUSTOMER_ID   | Number     | Foreign Key References Customers(CUSTOMER_ID) |
| ITINERARY_ID  | Number     | Foreign Key References Itineraries(ITINERARY_ID) |
| BOOKING_DATE  | Date       | Not Null                                 |
| DEPARTURE_DATE| Date       | Not Null                                 |
| RETURN_DATE   | Date       | Not Null                                 |
| STATUS        | Varchar2(50) | Not Null                                 |

### Customers Table

| Column        | Data Type   | Constraints                              |
|---------------|-------------|------------------------------------------|
| CUSTOMER_ID   | Number      | Primary Key                              |
| FIRST_NAME    | Varchar2(50)| Not Null                                 |
| LAST_NAME     | Varchar2(50)| Not Null                                 |
| EMAIL         | Varchar2(100)| Not Null                                |
| PHONE_NUMBER  | Varchar2(15)| Not Null                                 |
| ADDRESS       | Varchar2(255)| Not Null                                |

### Itineraries Table

| Column         | Data Type   | Constraints                              |
|----------------|-------------|------------------------------------------|
| ITINERARY_ID   | Number      | Primary Key                              |
| DESTINATION    | Varchar2(100)| Not Null                                |
| DEPARTURE_DATE | Date        | Not Null                                 |
| RETURN_DATE    | Date        | Not Null                                 |
| TRANSPORTATION | Varchar2(100)| Not Null                                |
| ACCOMMODATION  | Varchar2(100)| Not Null                                |

## Getting Started

### Prerequisites

- Oracle SQL Developer
- Oracle Database

### Installation and Working

1. **Create a New Database Connection in Oracle SQL Developer**:
   - Open Oracle SQL Developer.
   - Click on the `+` button to create a new connection.
   - Enter the connection details (username, password, hostname, port, SID/service name).
   - Test the connection and save it.

2. **Create the Database Schema**:
   - Open a new SQL Worksheet.
   - Create 3 tables one table is for creating the table schema and the next is to create table for bookings as well as itineraries.
   - Follow and ensure to give correct data type.

3. **Populate the Database with Sample Data**:
   - Open a new SQL Worksheet.
   - Insert the sample values into customer table, bookings table and itineraries table.
   - Execute and view the table to ensure whether all the inserted values are present.

4. **Develop PL/SQL Procedures**:
   - Open a new SQL Worksheet.
   - Create procedures for each table for insertion, updation and deletion.
   - Now test the working of procedures by performing sample insert, update, delete on them.
