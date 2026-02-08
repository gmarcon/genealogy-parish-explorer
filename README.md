# Parish Explorer

A lightweight, browser-based single-page tool designed to help genealogical researchers track their progress in searching source parishes, particularly useful for tracking migrations.

## Features

- **Interactive Map**: Built with [Leaflet.js](https://leafletjs.com/), featuring modern OpenStreetMap and historical layers (e.g., Bavaria 1808 Uraufnahme).
- **Location Management**:
  - Add, edit, and delete research locations.
  - Distinguish between standard locations and Parishes (using church icons).
  - Track research status with color-coded markers:
    - ⚪ **Not Started** (Grey)
    - 🟡 **In Progress** (Yellow)
    - 🟢 **Documented Find** (Green)
    - 🔴 **Ruled Out** (Red)
- **Search**: integrated location search using OpenStreetMap's Nominatim.
- **Data Persistence**:
  - Data is automatically saved to the browser's Local Storage.
  - **Export/Import**: Save your project as a `.json` file and restore it later.
  - **Shareable URLs**: Project state is encoded in the URL for easy sharing.
- **Resource Linking**: Add and manage external links to sources like Meyers Gazetteer, GOV, Matricula Online, ...

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, Safari).
- Internet connection (for loading map tiles and libraries).

### Installation
No installation is required. This is a single-file application that can be opened directly in your web browser.

1. Clone or download this repository.
2. Open `parish-explorer.html` directly in your web browser.

## Usage

1. **Create a Project**: Click the "New Project" button to start fresh.
2. **Add Locations**:
   - Use the search bar to find a place.
   - Click "Add Location" from the search result popup.
   - Or double-click anywhere on the map to add a custom location.
3. **Edit Details**:
   - Click on a marker and select "Edit Details".
   - Set the location type (e.g., set to "Parish" to show a church icon).
   - Update the research status.
   - Add links to sources.
4. **Save/Share**:
   - Your work is saved automatically to your browser.
   - Use the "Export JSON" button to download a backup.
   - Copy the URL to share your current map state with others.

## Data Format

The application uses a JSON structure to store project data:

```json
{
  "title": "My Research Project",
  "description": "Project description...",
  "locations": [
    {
      "name": "Village Name",
      "coordinates": [48.123, 11.456],
      "type": "parish",
      "status": "documented_find",
      "description": "Findings summary...",
      "sources": [
        {
          "name": "Source Name",
          "url": "https://example.com"
        }
      ]
    }
  ]
}
```

## Technologies

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Mapping**: Leaflet.js
- **Icons**: FontAwesome
