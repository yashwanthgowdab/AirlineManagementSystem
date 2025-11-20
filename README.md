✈️ Airline Management System
Java Swing | MySQL | Desktop Application

The Airline Management System is a Java-based desktop application that helps airline staff manage customers, flights, bookings, boarding passes, and ticket cancellations. It provides a clean and easy-to-use graphical interface built using Java Swing, with backend storage handled by MySQL.

🖥️ Features
✅ User Login

Staff login with credential validation.

Secure authentication through database lookup.

✅ Add Customer

Add new passenger records.

Stores name, nationality, address, passport number, contact details, etc.

Data is inserted into the MySQL database.

✅ Flight Information

Displays all flights with:

Flight code

Source

Destination

Date & time

Helps staff quickly check flight availability.

✅ Book Flight

Search flights using source/destination.

Select a customer and assign them to a flight.

Auto-generates unique ticket numbers.

Saves booking details in database.

✅ Journey Details

View all journey details for a specific passenger.

Shows route, flight number, date, and ticket information.

✅ Boarding Pass Generation

Automatically prepares a formatted boarding pass after booking.

Displays:

Passenger name

Flight number

Route

Date

Designed to resemble a real airline boarding pass.

✅ Cancel Ticket

Search for an existing booking.

Cancel ticket and delete booking record from database.

🛠️ Technologies Used
Technology	Purpose
Java	Core application logic
Java Swing	Graphical User Interface (GUI)
MySQL	Database for storing customers, flights, bookings
JDBC	Database connectivity
OOP Concepts	Structure and design
📁 Project Structure
AirlineManagementSystem/
 ├── src/
 │   ├── AddCustomer.java
 │   ├── BookFlight.java
 │   ├── BoardingPass.java
 │   ├── Cancel.java
 │   ├── FlightInfo.java
 │   ├── JourneyDetails.java
 │   ├── Login.java
 │   ├── Home.java
 │   ├── Conn.java        # Database connection class
 │   └── Main.java        # Entry point
 ├── .idea/
 ├── .git/
 └── README.md

⚙️ Setup & Installation
1. Install Requirements

Java JDK 8 or above

MySQL Server

IntelliJ / Eclipse / VS Code

2. Create Database

Create a MySQL database and import SQL tables if included.
Update the credentials inside Conn.java:

public class Conn {
    Connection c;
    Statement s;

    public Conn() {
        try {
            Class.forName("com.mysql.cj.jdbc.Driver");
            c = DriverManager.getConnection("jdbc:mysql://localhost:3306/airline", "root", "yourpassword");
            s = c.createStatement();
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}

3. Run the Application

Open project → Run Main.java.

📸 Screenshots

(Add screenshots of UI here after running your project)

![Home Screen]()
![Add Customer Screen]()
![Book Flight Screen]()
![Boarding Pass]()

🚀 Future Improvements

Add payment processing

Add seat selection UI

Add admin panel

Add flight scheduling module

Convert into a web-based Spring Boot version

📜 Author

Yashwanth Gowda B
Final Year Information Science Engineering
