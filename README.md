# Natural Disasters Map

An interactive web application for exploring natural disasters around the world, in particular earthquakes, wildfires, and floods.

The application retrieves data from external APIs and visualizes events on an interactive map using Leaflet. Users can select a time interval, browse events geographically, inspect their details, and sort the available data.

<img width="800" height="450" alt="demo" src="https://github.com/user-attachments/assets/c231f898-ba54-4b4f-9a3a-25b054aab217" />

## Features

- Display earthquakes, wildfires, and floods on an interactive world map
- Search for events within a selected date range
- Visualize events using geographic markers
- Cluster map markers when displaying large numbers of events
- View detailed information about individual events
- Browse events through a paginated list
- Sort events according to relevant properties, such as date or magnitude
- Automatically move and zoom the map to a selected event
- Reverse-geocode geographic coordinates where applicable

## Data Sources

The application retrieves disaster data from publicly available APIs:

- **USGS Earthquake Hazards Program** — earthquake locations, magnitudes, depths, and timestamps
- **NASA FIRMS / VIIRS** — satellite-detected active wildfire data
- **NASA EONET** — natural-event data used for flood information
- **OpenStreetMap Nominatim** — reverse geocoding of geographic coordinates

## Technologies

- **JavaScript**
- **HTML**
- **CSS / SCSS**
- **Leaflet**
- **Leaflet.markercluster**
- REST APIs / `fetch()`
- GeoJSON and CSV data processing

## How It Works

The user first selects a start and end date.

The application then retrieves disaster data for the selected interval from the corresponding external APIs. The received data is processed in JavaScript and displayed both geographically on a Leaflet map and, where applicable, in a sortable and paginated list.

Selecting an event from the list moves the map to its geographic location, while map markers provide additional information about each event.

## Running Locally

Clone the repository:

```bash
git clone https://github.com/luca012/natural_disasters_map.git
cd natural_disasters_map
```

Run a local HTTP server from the project directory. For example, with Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

Some functionality depends on the availability and usage limits of the external APIs.
