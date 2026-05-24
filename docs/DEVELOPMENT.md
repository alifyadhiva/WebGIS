# Development Notes

Dokumen ini berisi catatan teknis agar project lebih mudah dikembangkan oleh developer berikutnya.

## Alur Aplikasi

1. `index.html` memuat dependency CDN dan struktur UI utama.
2. `style.css` mengatur tampilan peta, sidebar, legend, dropdown, search, dan control Leaflet.
3. `script.js` melakukan inisialisasi map, basemap, layer GIS, search index, upload KML, serta drawing/measurement tools.

## Komponen Penting

- `baseLayers`: daftar basemap yang tersedia.
- `wiupLayer`: vector tile WIUP dari MapTiler.
- `kLHKLayer`: tiled layer Kawasan Hutan dari KLHK.
- `projectsLayers`: grouping project berdasarkan status.
- `searchIndex`: index pencarian project/perusahaan.
- `onEachProjectFeature`: popup dan interaksi setiap feature project.

## Rekomendasi Pengembangan Berikutnya

- Pisahkan konfigurasi API ke file khusus seperti `config.js`.
- Modularisasi `script.js` menjadi beberapa file, misalnya `map.js`, `layers.js`, `search.js`, dan `kml.js`.
- Tambahkan screenshot aplikasi pada README.
- Tambahkan deployment workflow bila akan dipublikasikan ke GitHub Pages, Netlify, atau Vercel.
