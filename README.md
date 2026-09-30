# ServiceNow Metro Ticket Generating System

A ServiceNow-based Metro Ticket Generating System designed to simplify metro ticket booking through the Service Catalog. The system allows users to select stations, choose journey type and passenger count, calculate the applicable fare, select a payment mode, and generate a QR-based metro ticket.

## Project Overview

The Metro Ticket Generating System provides a simple digital workflow for metro ticket booking using ServiceNow.

The system is implemented using ServiceNow Service Catalog, Catalog Client Scripts, Catalog UI Policies, Service Portal widgets, and Update Sets.

## Objectives

- Provide a simple metro ticket booking interface.
- Allow users to select source and destination stations.
- Support single and return journeys.
- Allow selection of number of passengers.
- Calculate fare dynamically based on route and passenger count.
- Provide different payment mode options.
- Generate a QR code for the metro ticket.
- Maintain the complete ServiceNow configuration through an Update Set.

## Technologies Used

- ServiceNow
- Service Catalog
- Service Portal
- Catalog Client Scripts
- Catalog UI Policies
- Service Portal Widget
- JavaScript
- Update Sets
- GitHub

## Main Features

### 1. Metro Ticket Booking

Users can book a metro ticket by providing:

- Starting station
- Destination station
- Journey type
- Number of passengers
- Payment mode

### 2. Station Selection

The system supports the following stations:

- Ameerpet
- Madhapur
- LB Nagar
- Uppal Stadium
- Jubilee Hills
- Panjagutta
- Kukatpally

### 3. Journey Types

Two journey types are supported:

- Single Journey
- Return Journey

### 4. Passenger Selection

Users can select between 1 and 5 passengers.

### 5. Dynamic Fare Calculation

Fare is calculated automatically based on the selected source, destination, journey type, and number of passengers.

For a single journey:

`Fare = Route Fare × Number of Passengers`

For a return journey:

`Fare = Route Fare × 2 × Number of Passengers`

### 6. Payment Mode

The system provides the following payment options:

- UPI
- Card
- Others

### 7. QR Ticket Generation

After submitting the ticket form, the system generates a QR code using a Service Portal widget.

The QR code contains a ticket reference URL and is displayed to the user before final confirmation.

## ServiceNow Components

The project uses the following ServiceNow components:

### Catalog Item

**Book A Metro Ticket**

### Catalog Variables

- Starting From
- Going To
- Type of Journey
- No of Passengers
- Amount for Single Journey
- Amount Including Return
- Mode of Payment
- Enter Payment Mode

### Catalog Client Scripts

- Fare auto-calculation
- QR Generation

### Catalog UI Policy

- Fields Visibility

### Catalog UI Policy Action

- Enter Payment Mode

### Service Portal Widget

**Metro QR Widget**

The widget displays the generated QR code to the user.

## Fare Calculation

The system contains route-based fare values for supported metro stations.

| Route | Fare |
|---|---:|
| Ameerpet - Panjagutta | ₹20 |
| Ameerpet - Madhapur | ₹30 |
| Ameerpet - Jubilee Hills | ₹20 |
| Ameerpet - Kukatpally | ₹30 |
| Ameerpet - LB Nagar | ₹50 |
| Ameerpet - Uppal Stadium | ₹60 |
| Panjagutta - Jubilee Hills | ₹20 |
| Panjagutta - Madhapur | ₹30 |
| Panjagutta - Kukatpally | ₹40 |
| Panjagutta - LB Nagar | ₹50 |
| Panjagutta - Uppal Stadium | ₹60 |
| Jubilee Hills - Madhapur | ₹30 |
| Jubilee Hills - Kukatpally | ₹40 |
| Jubilee Hills - LB Nagar | ₹50 |
| Jubilee Hills - Uppal Stadium | ₹60 |
| Madhapur - Kukatpally | ₹40 |
| Madhapur - LB Nagar | ₹50 |
| Madhapur - Uppal Stadium | ₹50 |
| Kukatpally - LB Nagar | ₹60 |
| Kukatpally - Uppal Stadium | ₹70 |
| LB Nagar - Uppal Stadium | ₹30 |

The fare calculation also supports reverse routes.

## Project Workflow

```text
User opens Book A Metro Ticket
          ↓
Select Starting Station
          ↓
Select Destination Station
          ↓
Select Journey Type
          ↓
Select Number of Passengers
          ↓
System Calculates Fare
          ↓
Select Payment Mode
          ↓
Submit Ticket
          ↓
QR Code Generation
          ↓
Metro Ticket QR Display
## Update Set

The complete ServiceNow configuration is preserved in the project Update Set.

**Update Set:** Metro Ticket Generating System Project

The exported Update Set XML is available in:

`ServiceNow/Metro Ticket Generating System Project.xml`

The XML can be imported into another ServiceNow instance to restore the project configuration.

## Testing

The project was tested for:

- Source and destination station selection
- Single journey fare calculation
- Return journey fare calculation
- Passenger-based fare calculation
- Payment mode selection
- Field visibility
- QR code generation
- Ticket submission

### Sample Test

**Route:** Ameerpet → Madhapur  
**Journey:** Single  
**Passengers:** 2

Calculated fare:

`₹30 × 2 = ₹60`

For a return journey with 2 passengers:

`₹30 × 2 × 2 = ₹120`

## Repository Structure

```text
ServiceNow-Metro-Ticket-Generating-System/
│
├── README.md
│
└── ServiceNow/
    └── Metro Ticket Generating System Project.xml
```

## Installation / Import

To use the project in another ServiceNow instance:

1. Open the ServiceNow instance.
2. Navigate to **System Update Sets**.
3. Import the exported Update Set XML.
4. Open the imported Update Set.
5. Preview the Update Set.
6. Commit the Update Set.
7. Verify the **Book A Metro Ticket** Catalog Item.
8. Test the ticket booking workflow through the Service Portal.

## Future Enhancements

- Real-time metro station data integration.
- Online payment gateway integration.
- Database-based fare management.
- User ticket history.
- Ticket cancellation functionality.
- Live metro route and station information.
- Improved QR ticket validation.

## Project Repository

The complete ServiceNow project configuration and Update Set are maintained in this repository.

## Author

**Amreen**

B.Tech – Information Technology
