# Data-Structures-Algorithms-Group-Project
Group Project

# QuickSpot
Where we help you find parking easily and effectivly 

# Table of Contents 
1. Introduction
2.File Architecture
3.Installation and Usage
4.First time install
5.Usage 
6.Further Improvments
7.Resources used 
8.Credits

# Introduction
QuickSpot is a prototype web application designed to simulate how a smart parking detection system can work using location-based data.
The app allows users to:
View real-time available parking spots in a given area.
Filter parking spots by type (regular, electric, or truck).
Simulate booking and cancelling a parking spot.
Explore a small dataset of parking locations across key points in Madrid, such as IE Tower, Sol, Gran Vía, Retiro, and Atocha.
This version runs on a Flask web server using Folium for map visualization and Ngrok for public tunneling (so you can access the app via a live web link in Google Colab or Jupyter).
The project focuses on data simulation, user experience testing, and functional proof of concept, rather than production deployment.

# File Architechture
/QuickSpot/
 ├── code/
 │    ├── quickspot_app.ipynb        # Main notebook containing Flask + Folium app
 │
 ├── resources/
 │    ├── mock_data.csv              # Example of parking data
 │    ├── images/                    # Screenshots or diagrams (optional)
 │
 ├── README.md                       # Installation and documentation file
 └── requirements.txt                 # Python libraries required for setup

. Components
Flask: Used to serve the app and handle routes (main web server).
Folium: Generates interactive maps using Leaflet.js.
PyNgrok: Opens a public HTTPS tunnel to make the app viewable in environments like Colab or Kaggle.
Haversine Function: Calculates the distance between the user’s location and each available parking spot.
Dataset (Mock Data): Contains simulated parking spots with status (available, booked), type (regular, electric, truck), and coordinates.

# Installation 

First Time Install
1. Clone or Download the Repository
git clone https://github.com/quickspot/quickspot.git
cd QuickSpot

2. Install Required Libraries
Make sure you have Python 3.9+ installed, then run:

pip install flask pyngrok folium

3. Verify Installation
Once dependencies are installed, open the quickspot_app.ipynb file in Google Colab or Jupyter Notebook.

# Usage 
1. Select a Reference Point
Choose a starting location (e.g., “IE Tower”, “Sol”, “Retiro”, etc.).

2. Apply Filters

Use the filters on the left panel to:
Choose type of spot (regular, electric, truck).
Set maximum distance in meters.
Select mode: nearest single spot or top-K available list.

3. View Available Spots

The map displays spots color-coded by availability:
 Green: Electric available
 Blue: Truck available
 Orange: Regular available
 Red: Booked
 Purple: Your booked spot

4. Book or Cancel

Click “Book this spot” to reserve a parking space.
If already booked, the popup will show “Cancel reservation.”
The app automatically updates the map and highlights your route from origin to selected spot.

# Features
Real-time simulated parking map (Folium + Flask)
Booking and cancellation of spots
Filtering by type and distance
Multiple reference points around Madrid
Interactive HTML map auto-updating without refresh
Anonymous, local simulation (no user login required)
