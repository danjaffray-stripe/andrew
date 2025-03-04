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


1. **Set Up a Virtual Environment (optional but recommended)**:
```
python3 -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
```


