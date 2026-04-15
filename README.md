# Airline Data Management and Analysis using Power BI
## Project Overview

This project focuses on analyzing airline operations data to gain insights into flight performance, passenger trends, and ticket booking behavior using Power BI.

The objective is to transform raw data into meaningful insights and build an interactive dashboard to support better decision-making in airline operations.

## Objective
 - Analyze airline operations data
 - Understand passenger distribution across airlines
 - Identify booking trends
 - Build an interactive Power BI dashboard
## Datasets Used
 1.Flight Information
  Fields: FlightID, FlightNumber, Airline, Destination, Status
 2.Passenger Information
  Fields: PassengerID, FlightID, SeatNumber
 3.Ticket Information
  Fields: TicketID, FlightID, BookingStatus
## Data Preparation
 - Performed data cleaning using Power Query
 - Removed duplicate records
 - Handled missing values
 - Corrected data types
## Data Modeling
 - Created relationships using FlightID
 - Established one-to-many relationships:
 - Flight to Passenger
 - Flight to Ticket
## Data Transformation
1.Created a conditional column:
 "Best" for On-Time flights
 "To Be Improved" for delayed or cancelled flights
2.Extracted flight numbers using transformation techniques
## DAX Calculations
TotalPassengers_SelectedFlight =
CALCULATE(
    COUNTROWS(Passenger_Information),
    ALL(Passenger_Information[FlightID])
)

TotalTicketsBooked =
CALCULATE(
    COUNTROWS(Ticket_information),
    Ticket_information[BookingStatus] = "Confirmed"
)
## Dashboard Features
  - Bar chart showing passengers by airline
  - Donut chart showing booking status distribution
  - Table showing flights by airline and destination
  - Slicers for airline, destination, and status
  - KPI cards for total passengers, tickets, and flights
##  Advanced Features
 - Implemented Row-Level Security (RLS) for controlled data access
 - Configured scheduled refresh for automatic data updates
## Key Insights
 - Airline A has the highest number of passengers
 - Phoenix has the highest number of flights
 - Some routes show delays and performance issues
 - Booking data highlights operational patterns
## Tools and Technologies
 - Power BI
 - Power Query
 - DAX (Data Analysis Expressions)
## Project Outcome

This project demonstrates the use of Power BI for data modeling, transformation, and visualization to generate actionable business insights in the airline industry.

## Project Files
 - Power BI Dashboard (.pbix)
 - Dataset files
 - Documentation
## Demo

[Watch Project Video] (https://drive.google.com/file/d/1cyvkklZeJ9D4wahq00LICVfFCIXkSO1M/view?usp=sharing)
.
