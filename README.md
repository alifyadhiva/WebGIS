# WebGIS Project

This repository contains an interactive WebGIS application built with Leaflet for displaying WIUP layers, KLHK forest areas, project polygons from Supabase, KML uploads, project and company search, multiple basemap options, minimap support, and drawing or measurement tools.

The project is designed to remain lightweight, browser-friendly, and easy to understand for other developers.

## Main Features

- Interactive map interface powered by Leaflet
- Multiple basemap options including OpenStreetMap, Google Satellite, Google Terrain, Google Street, Topographic, and MapLibre Streets
- WIUP layer using vector tiles
- KLHK forest area layer using Esri Leaflet
- Project polygon layer from Supabase REST API
- Layer filtering based on project status
- Search functionality for projects and companies
- Direct KML file upload from the browser
- Minimap and drawing tools using Leaflet MiniMap and Leaflet Geoman
- Area, distance, radius, and coordinate measurement tools

## Tech Stack

| Category | Technology |
| --- | --- |
| Frontend | HTML, CSS, JavaScript |
| Map Engine | Leaflet |
| GIS Plugins | Leaflet VectorGrid, Esri Leaflet, Leaflet Omnivore, Leaflet Geoman |
| Spatial Utility | Turf.js |
| Data Source | Supabase REST API, MapTiler, KLHK ArcGIS REST Service |

## Repository Structure

```text
webgis-main/
├── index.html
├── style.css
├── script.js
├── package.json
├── .editorconfig
├── .gitignore
├── README.md
├── docs/
│   ├── DEVELOPMENT.md
│   └── PROJECT_STRUCTURE.md
└── .vscode/
    ├── extensions.json
    └── settings.json
```

## Getting Started

### Option 1 — Open Directly in Browser

Open the `index.html` file using a modern browser such as Chrome, Edge, or Firefox.

### Option 2 — Run with Local Server

```bash
npm install
npm run dev
```

The application will run using a local static server.

## Configuration Notes

This project uses several public frontend endpoints and API keys, including MapTiler and Supabase publishable keys. For production environments, sensitive configurations should be moved to environment variables or a backend proxy.

## Data Layers

| Layer | Source | Description |
| --- | --- | --- |
| WIUP | MapTiler Vector Tile | Rendered as vector grid |
| KLHK Forest Area | KLHK ArcGIS REST Service | Rendered as tiled map layer |
| Projects | Supabase REST API | Rendered as GeoJSON layer |
| KML Upload | Local user file | Processed using Leaflet Omnivore |

## Development

Use the following command to start local development:

```bash
npm run dev
```

## License

This project is intended for educational and development purposes.
