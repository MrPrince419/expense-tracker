# Expense Tracker

A comprehensive financial management application built with Streamlit for tracking personal and business expenses with advanced analytics and administrative capabilities.

![Expense Tracker Dashboard](https://via.placeholder.com/800x400?text=Expense+Tracker+Dashboard)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Why Expense Tracker?](#why-expense-tracker)
- [Installation](#installation)
- [Usage](#usage)
- [User Guide](#user-guide)
- [Admin Guide](#admin-guide)
- [Data Security](#data-security)
- [Technical Architecture](#technical-architecture)
- [Contributing](#contributing)
- [License](#license)

## Overview

Expense Tracker is a web-based application that helps individuals and small businesses manage their finances by tracking income, expenses, and providing insightful analytics. Built with Python and Streamlit, it offers an intuitive interface for uploading financial data, visualizing spending patterns, and generating reports.

## Features

### User Features
- **Multi-format Data Import**: Upload financial data in CSV, Excel, JSON, TXT, or Parquet formats
- **Automatic Column Mapping**: Smart recognition and standardization of column names
- **Interactive Dashboard**: Visualize spending patterns, income vs. expenses, and category breakdowns
- **Data Cleaning Tools**: Remove duplicates and handle missing values
- **Export Capabilities**: Download filtered data in CSV or Excel formats
- **Transaction Management**: Add, edit, and categorize transactions
- **Monthly Trend Analysis**: Track spending patterns over time

### Admin Features
- **User Management**: View and manage user accounts
- **Activity Tracking**: Monitor login and upload activities
- **Engagement Analytics**: Track user engagement metrics
- **Data Completeness Scoring**: Assess the quality of user data
- **User Growth Charts**: Visualize user adoption over time
- **Statistical Reports**: Download comprehensive admin statistics

## Why Expense Tracker?

### The Problem

Managing personal and business finances often involves dealing with data scattered across multiple sources, making it difficult to get a comprehensive view of one's financial situation. Existing solutions are either too complex for casual users or too simplistic for meaningful financial analysis.

### Our Solution

Expense Tracker bridges this gap by providing:

1. **Simplicity with Power**: An intuitive interface that doesn't sacrifice analytical capabilities
2. **Data Flexibility**: Support for multiple data formats and automatic mapping of columns
3. **Meaningful Insights**: Visualizations and metrics that help users understand their spending habits
4. **Administrative Oversight**: Tools for organizations to manage and monitor user activity

### Impact

- **Financial Awareness**: Users gain deeper insights into their spending habits
- **Time Savings**: Automated data processing and visualization save hours of manual work
- **Better Decision Making**: Data-driven insights lead to better financial decisions
- **Organizational Efficiency**: Administrative tools help organizations manage financial data across teams

## Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/expense-tracker.git
   cd expense-tracker
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Create a `.env` file based on the provided `.env.example` (for admin credentials):
   ```bash
   cp .env.example .env
   ```

4. Edit the `.env` file with secure credentials for production use.

## Usage

### Running the Application

Start the application with Streamlit:

```bash
streamlit run app.py
```

This will launch the application on `http://localhost:8501` by default.

### Default Admin Credentials

For initial setup, use these credentials (remember to change them in production):
- **Email**: admin@example.com
- **Password**: Admin@123

## User Guide

### Registration and Login

1. Navigate to the signup tab on the homepage
2. Create a user account with a secure password
3. Login with your credentials

### Data Upload

1. Navigate to the Upload page
2. Use the file uploader to import your financial data
3. Review the automatic column mapping
4. Apply data cleaning options if needed

### Dashboard Analysis

1. Navigate to the Dashboard page
2. View key metrics (income, expenses, savings)
3. Explore visualizations:
   - Income vs. Expense chart
   - Spending breakdown by category
   - Monthly trends
   - Top spending categories

### Data Export

1. Navigate to the Upload page
2. Scroll to the Export section
3. Select your desired format (CSV or Excel)
4. Click the download button

## Admin Guide

### Admin Dashboard

Access the admin panel by logging in with admin credentials to manage:

1. **User Management**: View all registered users and their activity
2. **Engagement Stats**: Monitor user login and upload activities
3. **Data Completeness**: Track the quality of user data
4. **User Growth**: Visualize user adoption over time

### Downloading Statistics

1. Navigate to the bottom of the admin panel
2. Click the "Download Admin Stats" button
3. Stats will be saved as CSV with the current date

## Data Security

### Security Measures

- **Password Security**: Passwords are hashed using bcrypt
- **Secret Answers**: Secret answers for password recovery are hashed with SHA-256
- **Environmental Variables**: Sensitive configuration is stored in environment variables
- **Session Management**: Sessions timeout after periods of inactivity
- **Data Validation**: Input validation prevents injection attacks

### Privacy Considerations

- **Data Storage**: User data is stored locally and not shared with external services
- **Sensitive Data**: Sensitive files are excluded from version control via .gitignore
- **Activity Logging**: User activities are logged but personally identifiable information is minimized

## Technical Architecture

### Component Overview

- **Frontend**: Streamlit-based interactive interface
- **Authentication**: Custom auth system with bcrypt password hashing
- **Data Processing**: Pandas for data manipulation and analysis
- **Visualization**: Plotly and Altair for interactive charts
- **Storage**: File-based JSON storage for users and transaction data

### Directory Structure

```
expense-tracker/
├── app.py                # Main application entry point
├── auth.py               # Authentication and user management
├── utils.py              # Utility functions for data handling
├── requirements.txt      # Dependencies
├── .env.example          # Template for environment variables
├── .gitignore            # Git ignore rules
├── users.json            # User database (not in version control)
├── pages/                # Application pages
│   ├── 1_Upload.py       # Data upload and export functionality
│   ├── 2_Dashboard.py    # Analytics dashboard
│   └── admin_panel.py    # Admin functionalities
└── user_data/            # User transaction data (not in version control)
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## Contact

For questions or support, please open an issue on our GitHub repository or contact the maintainers directly at [![Email](https://img.shields.io/badge/Email-Support-blue?style=flat-square&logo=gmail)](mailto:PrinceUwagboe44@outlook.com).

---

*Last updated: April 18, 2025*