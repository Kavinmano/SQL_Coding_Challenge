# PetPals - The Pet Adoption Platform

## Overview
PetPals is a comprehensive Pet Adoption Platform designed to manage pets, shelters, donations, adoption events, and participants. This project includes an SQL schema and queries to support the platform's functionality.

## Database Schema
The platform contains the following tables:

### 1. Pets
- `PetID` (Primary Key, INT): Unique identifier for each pet.
- `Name` (VARCHAR): Name of the pet.
- `Age` (INT): Age of the pet.
- `Breed` (VARCHAR): Breed of the pet.
- `Type` (VARCHAR): Type of pet (e.g., Dog, Cat).
- `AvailableForAdoption` (BIT): Indicates availability for adoption (0 for not available, 1 for available).

### 2. Shelters
- `ShelterID` (Primary Key, INT): Unique identifier for each shelter.
- `Name` (VARCHAR): Name of the shelter.
- `Location` (VARCHAR): Location of the shelter.

### 3. Donations
- `DonationID` (Primary Key, INT): Unique identifier for each donation.
- `DonorName` (VARCHAR): Name of the donor.
- `DonationType` (VARCHAR): Type of donation (Cash, Item).
- `DonationAmount` (DECIMAL): Amount donated (for cash donations).
- `DonationItem` (VARCHAR): Item donated (for item donations).
- `DonationDate` (DATETIME): Date and time of the donation.

### 4. AdoptionEvents
- `EventID` (Primary Key, INT): Unique identifier for each event.
- `EventName` (VARCHAR): Name of the event.
- `EventDate` (DATETIME): Date and time of the event.
- `Location` (VARCHAR): Location or venue of the event.

### 5. Participants
- `ParticipantID` (Primary Key, INT): Unique identifier for each participant.
- `ParticipantName` (VARCHAR): Name of the participant.
- `ParticipantType` (VARCHAR): Type of participant (Shelter, Adopter).
- `EventID` (Foreign Key, INT): References `EventID` from the AdoptionEvents table.

## Tasks Implemented

### 1. Database Initialization
- Script to create and initialize the PetPals database.
- Handles cases where the database and tables already exist.

### 2. SQL Queries
- Retrieve available pets for adoption.
- Retrieve participant names and types for a specific adoption event.
- Update shelter information with a stored procedure.
- Calculate total donation amount per shelter.
- Retrieve pets without owners.
- Calculate total donation amount per month and year.
- Retrieve distinct breeds for pets aged between 1-3 years or older than 5 years.
- Retrieve pets and their shelters where pets are available for adoption.
- Count total participants for events in a specific city.
- Retrieve unique breeds for pets aged between 1 and 5 years.
- Retrieve pets not adopted.
- Retrieve adopted pets with adopters' names.
- List shelters with count of available pets for adoption.
- Find pairs of pets from the same shelter with the same breed.
- List all combinations of shelters and adoption events.
- Find the shelter with the highest number of adopted pets.

## Usage
1. Clone the repository and import the SQL script.
2. Execute the script to create tables and insert necessary data.
3. Run the SQL queries provided to interact with the data.

## How to Run
- Import `petpals_sql.sql` into your MySQL server.
- Run the stored procedure and queries as needed.





