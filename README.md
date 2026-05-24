# WebGIS Project

Repository ini berisi aplikasi **WebGIS interaktif** berbasis Leaflet untuk menampilkan layer WIUP, Kawasan Hutan KLHK, project polygon dari Supabase, upload KML, pencarian project/perusahaan, pilihan basemap, minimap, serta tools drawing/measurement.

> Fokus repository ini adalah menjaga aplikasi tetap ringan, langsung bisa dijalankan di browser, dan mudah dipahami oleh developer lain.

## ✨ Fitur Utama

- Peta interaktif menggunakan **Leaflet**.
- Beberapa pilihan basemap: OpenStreetMap, Google Satellite, Google Terrain, Google Street, Topographic, dan MapLibre Streets.
- Layer WIUP berbasis vector tile.
- Layer Kawasan Hutan KLHK melalui Esri Leaflet.
- Layer project dari Supabase REST API.
- Filter layer berdasarkan status project.
- Pencarian berdasarkan kode project dan perusahaan.
- Upload file KML langsung dari browser.
- Minimap dan drawing tools menggunakan Leaflet MiniMap serta Leaflet Geoman.
- Pengukuran area, jarak, radius, dan koordinat marker.

## 🧰 Tech Stack

| Kategori | Teknologi |
| --- | --- |
| Frontend | HTML, CSS, JavaScript |
| Map Engine | Leaflet |
| GIS Plugin | Leaflet VectorGrid, Esri Leaflet, Leaflet Omnivore, Leaflet Geoman |
| Spatial Utility | Turf.js |
| Data Source | Supabase REST API, MapTiler, KLHK ArcGIS REST Service |

## 📁 Struktur Repository

```text
webgis-main/
├── index.html              # Struktur halaman aplikasi
├── style.css               # Styling UI peta dan sidebar
├── script.js               # Logic peta, layer, search, upload KML, dan drawing tools
├── package.json            # Script development lokal
├── .editorconfig           # Konsistensi format editor
├── .gitignore              # File/folder yang tidak perlu masuk Git
├── README.md               # Dokumentasi utama repository
├── docs/
│   ├── DEVELOPMENT.md      # Catatan teknis untuk developer
│   └── PROJECT_STRUCTURE.md# Penjelasan struktur project
└── .vscode/
    ├── extensions.json     # Rekomendasi extension VS Code
    └── settings.json       # Setting workspace VS Code
```

## 🚀 Cara Menjalankan Project

### Opsi 1 — Langsung dari Browser

Buka file `index.html` di browser modern seperti Chrome, Edge, atau Firefox.

### Opsi 2 — Menggunakan Local Server

```bash
npm install
npm run dev
```

Aplikasi akan berjalan melalui local static server.

## 🔐 Catatan Konfigurasi

Project ini menggunakan beberapa endpoint dan API key publik di sisi frontend, antara lain MapTiler dan Supabase publishable key. Untuk production, sebaiknya pindahkan konfigurasi sensitif ke environment variable atau backend proxy.

## 🗺️ Data Layer

| Layer | Sumber | Keterangan |
| --- | --- | --- |
| WIUP | MapTiler Vector Tile | Ditampilkan sebagai vector grid |
| Kawasan Hutan KLHK | ArcGIS REST Service KLHK | Ditampilkan sebagai tiled map layer |
| Projects | Supabase REST API | Ditampilkan sebagai GeoJSON layer |
| KML Upload | File lokal user | Dibaca menggunakan Leaflet Omnivore |

## 🧪 Quality Check

Gunakan perintah berikut untuk validasi cepat JavaScript:

```bash
npm run check
```

## 👩‍💻 Author

Developed and maintained by **Alifya Dhiva**.
