# Metrics Dashboard

## Overview
The Metrics Dashboard is a web application that collects, stores, and displays system metrics using Flask as the backend and Bootstrap for styling the frontend interface. The application updates CPU temperature and other system metrics every 5 seconds, showcasing them in a user-friendly analytics panel.

## Features
- Collects random CPU metrics every 5 seconds
- Stores metrics with timestamps in an SQLite database
- Displays metrics in a Bootstrap-styled interface
- Uses a RESTful API for data interaction

## Prerequisites
Before you begin, ensure you have met the following requirements:
- Python 3.6 or newer
- Flask
- SQLite
- psutil (for system metric collection)

## Installation

1. **Clone the Repository**:
   ```
   bash
   git clone https://github.com/yourusername/metrics-dashboard.git
   cd metrics-dashboard 
   ```


2. **Set Up a Virtual Environment (optional but recommended)**:
    ```
    python3 -m venv env
    source env/bin/activate  # On Windows use `env\Scripts\activate`
    ```

3. **Install Required Packages**:
    ```
    pip install -r requirements.txt
    ```

## Usage

1. **Run the Flask program**:

It contains 3 functions: 
- initdb(): creates the database
- a POST route to /metrics, which adds the metrics to the DB
- a GET route to /api/metrics which returns the most recent value in the DB

    ```
    python app.py
    ```

2. **Run the Metrics populator**:

   This sends a POST request to the metrics API which updates values every 5 seconds

    ```
    python metrics_populator.py
    ```

3. **Access the Dashboard**:
Open your web browser and navigate to http://127.0.0.1:5000/metrics to view the dashboard.

## Project Structure

```
.
├── app.py
├── metrics_populator.py
├── static/
│   └── scripts/
│       └── metrics.js
├── templates/
│   └── metrics.html
├── requirements.txt
├── README.md
└── database.db
```
