# openstreetmap

This project visualizes the street network of a specified location using OpenStreetMap data. It leverages OSMnx to fetch the street network and Folium to display it on an interactive map.

# Requirements
To run this project, you need Python and the following libraries:
osmnx
folium
geopandas

# How It Works
Location Definition: A location (e.g., city, neighborhood) is defined as a string (in this example, "Kharar, Punjab, India").
Download Street Network: Using OSMnx, the street network for the specified location is fetched from OpenStreetMap with ox.graph_from_place, specifying network_type='drive' to include only drivable roads.
Convert to GeoDataFrames: The street network graph is converted into GeoDataFrames for nodes and edges, making it easier to work with the geometries for mapping.

# Map Creation: A Folium map is created, centered around the average coordinates of the edges.
Add Streets to Map: Each edge (representing a street) is added to the Folium map as a PolyLine, allowing for customization of color, width, etc.
Save to HTML: The final interactive map is saved as an HTML file named kharar.html.

# Usage
Set the Location: Update place_name with the desired location (e.g., a city or neighborhood name).
Run the Code: Execute the script to fetch the street network, create the map, and save it as an HTML file.
View the Map: Open the generated kharar.html file in a web browser to view the interactive map.

# Notes
Ensure that the location string matches a recognizable area on OpenStreetMap.
Modify network_type to other options such as 'all', 'bike', 'walk', or 'all_private' to customize the types of streets included in the network.
