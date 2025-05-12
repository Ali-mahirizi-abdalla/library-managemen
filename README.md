# Library Management System Database

![Library Database ER Diagram](/docs/erd.png)

A complete relational database solution for managing all aspects of a modern library system, including book inventory, member management, loans, and staff operations.

## Features

- **Comprehensive Book Tracking**: Manage books, authors, publishers, and physical copies
- **Member Management**: Track patrons with membership status and contact information
- **Loan System**: Handle book checkouts, returns, and overdue items
- **Reservation System**: Allow members to reserve unavailable books
- **Fine Management**: Automatically track and manage late fees
- **Staff Administration**: Manage library employees with hierarchy support
- **Audit Logging**: Track all database changes for security and accountability

## Database Schema

The database consists of 11 interrelated tables with proper constraints:

1. **Core Entities**:
   - `books` - Book metadata and information
   - `authors` - Writer information
   - `publishers` - Publishing companies
   - `book_copies` - Physical inventory items

2. **User Management**:
   - `members` - Library patrons
   - `staff` - Library employees

3. **Operational Tables**:
   - `loans` - Book borrowing records
   - `fines` - Late return penalties
   - `reservations` - Book hold requests

4. **Support Tables**:
   - `book_authors` - Many-to-many relationship table
   - `audit_log` - Change tracking system

## Entity-Relationship Diagram

[View Full ER Diagram](/docs/erd.png)

Key Relationships:
- Books to Authors (Many-to-Many via book_authors)
- Books to Copies (One-to-Many)
- Members to Loans (One-to-Many)
- Loans to Fines (One-to-One)

## Installation

### Prerequisites
- MySQL Server 8.0+
- MySQL Workbench (recommended)

### Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/library-management-db.git
   cd library-management-db# library-managemen