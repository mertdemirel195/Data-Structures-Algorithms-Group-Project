# QuickSpot
Where we help you find parking easily and effectively.

# TABLE OF CONTENTS
1. Introduction
2. File Architecture
3. Installation
4. Usage
5. Further Improvements
6. Resources Used
7. Credits

# INTRODUCTION
QuickSpot is a prototype web application designed to simulate how a smart parking detection system can work using location-based data. 

The app allows users to:

- View real-time available parking spots in a given area.
- Filter parking spots by type (regular, electric, or truck).
- Simulate booking and cancelling a parking spot.
- Explore a small dataset of parking locations across key points in Madrid, such as IE Tower, Sol, Gran Vía, Retiro, and Atocha.

This version runs on a Flask web server using Folium for map visualization and Ngrok for public tunneling (so you can access the app via a live web link in Google Colab or Jupyter).

The project focuses on data simulation, user experience testing, and functional proof of concept, rather than production deployment.

# FILE ARCHITECTURE
/QuickSpot/

 ├── code/
 
 │    ├── quickspot_app.ipynb &emsp;&emsp; # Main notebook containing Flask + Folium app
 
 │
 
 ├── resources/
 
 │    ├── mock_data.csv &emsp;&emsp;&emsp;&emsp;&ensp;&nbsp;   # Example of parking data
 
 │    ├── images/ &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&ensp; # Screenshots or diagrams (optional)
 
 │
 ├── README.md &emsp;&emsp;&emsp;&emsp;&emsp;&nbsp;&nbsp; # Installation and documentation file
 
 └── requirements.txt &emsp;&emsp;&emsp;&emsp;&nbsp;&nbsp;&nbsp; # Python libraries required for setup

## Components
- Flask: Used to serve the app and handle routes (main web server).
- Folium: Generates interactive maps using Leaflet.js.
- PyNgrok: Opens a public HTTPS tunnel to make the app viewable in environments like Colab or Kaggle.
- Haversine Function: Calculates the distance between the user’s location and each available parking spot.
- Dataset (Mock Data): Contains simulated parking spots with status (available, booked), type (regular, electric, truck), and coordinates.

# INSTALLATION 
1. Clone or Download the Repository
   - git clone https://github.com/quickspot/quickspot.git
   - cd QuickSpot

3. Install Required Libraries
   - Make sure you have Python 3.9+ installed, then run:

&emsp;&emsp;&emsp;&emsp; pip install flask pyngrok folium

3. Verify Installation
   
&emsp;&emsp; Once dependencies are installed, open the quickspot_app.ipynb file in Google Colab or Jupyter Notebook.
&emsp;&emsp; Once all dependencies are installed, you can run the project in two different ways:

Option A – Run in Visual Studio Code

Open Visual Studio Code.

Go to File → Open Folder → QuickSpot.

Open the file MVPHarutYFinal.ipynb or quickspot_app.ipynb.

If prompted, select the Python 3 interpreter.

Run all cells (or press ▶ Run All).

Wait for the message:

# USAGE 
1. Select a Reference Point
   
&emsp;&emsp; Choose a starting location (e.g., “IE Tower”, “Sol”, “Retiro”, etc.).

3. Apply Filters

&emsp;&emsp; Use the filters on the left panel to:

&emsp;&emsp;&emsp;&emsp; - Choose type of spot (regular, electric, truck).

&emsp;&emsp;&emsp;&emsp; - Set maximum distance in meters.

&emsp;&emsp;&emsp;&emsp; - Select mode: nearest single spot or top-K available list.

3. View Available Spots

&emsp;&emsp; The map displays spots color-coded by availability:

&emsp;&emsp;&emsp;&emsp; - Green: Electric available
 
&emsp;&emsp;&emsp;&emsp; - Blue: Truck available
 
&emsp;&emsp;&emsp;&emsp; - Orange: Regular available
 
&emsp;&emsp;&emsp;&emsp; - Red: Booked
 
&emsp;&emsp;&emsp;&emsp; - Purple: Your booked spot

4. Book or Cancel

&emsp;&emsp; - Click “Book this spot” to reserve a parking space.

&emsp;&emsp; - If already booked, the popup will show “Cancel reservation.”

&emsp;&emsp; - The app automatically updates the map and highlights your route from origin to selected spot.

## Features
- Real-time simulated parking map (Folium + Flask).
- Booking and cancellation of spots.
- Filtering by type and distance.
- Multiple reference points around Madrid.
- Interactive HTML map auto-updating without refresh.
- Anonymous, local simulation (no user login required).

# FURTHER IMPROVEMENTS
- [ ] Payment features for paid parking spaces.
- [ ] City-wide geographic coverage (focus is on targeted pilot zones only).
- [ ] Integration with private parking garages.
- [ ] Integration with existing navigation systems (open in Google Maps or Apple Maps).

# RESOURCES USED
- Rstudio
- Flask
- Folium
- Ngrok

# CREDITS
This project was created for our Algorithms and Data Structures course at IE University. QuickSpot was created by:
- Ibtihal Nasri
- Nadia Gherab
- Clara Nogales
- Jiaxin Chen
- Mert Demirel
- Harutyun Yeranyan
