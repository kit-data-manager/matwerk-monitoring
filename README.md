# MatWerk Monitoring Dashboard

## Introduction

The **MatWerk Monitoring Dashboard** is a web-based tool designed to provide real-time monitoring and visualization of usage metrics for various MatWerk services developed by KIT. Built with Flask and Jinja2, it serves as a centralized platform for tracking KPIs and analyzing user engagement.

This project is adapted from the RPDM Dashboard Template and incorporates additional features to support MatWerk services.

## Features

- **Visualization of Usage Metrics**: Includes user distribution, plugin usage, and user growth charts.
- **Interactive Dashboards**: Dynamic and customizable visualization using Plotly.
- **Support for Multiple Services**: Metrics for services like EVOKS, Mapping Service, and FAIRDOScope.
- **Customizable UI**: Easily modify the dashboard layout and style to meet project requirements.

---

## Project Structure

### Core Components

1. **Backend**:
   - **`app.py`**: 
     - The main Flask application file.
     - Defines routes for different service metrics (e.g., `/monitoring`, `/monitoring/mapping-service`).
     - Fetches plots and tables dynamically from the `data` directory.

2. **Frontend**:
   - **Templates**:
     - **`index.html.j2`**: Main dashboard page.
     - **`evoks-metrics.html.j2`**: EVOKS service metrics page.
     - **`mapping-service-metrics.html.j2`**: Mapping service metrics page.
   - **Static Files**:
     - **`static/js/plotting.js`**: JavaScript functions for fetching and rendering plots and tables.
     - **`static/styles`**: CSS files for customizing the dashboard's appearance.

3. **Data**:
   - JSON files storing sample data for metrics such as user distribution and plugin usage.

4. **Configuration**:
   - **`requirements.txt`**: Lists dependencies for running the application.
   - **`dashboard.settings.js`**: Configures the visibility of dashboard components and UI customization.

5. **Deployment**:
   - **`run.sh`**: Script to activate the virtual environment and start the Flask application.
