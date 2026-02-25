# 🍎 Apple Maps Tile Downloader  
Frontend + Cloudflare Worker Proxy

## 📌 Project Overview

This project is a web-based Apple Maps satellite tile downloader built with **Leaflet.js** and integrated with a **Cloudflare Worker proxy**.

It allows users to:

- 🔍 Search any location (via OpenStreetMap Nominatim API)  
- 🗺️ Draw a bounding box directly on the map  
- 📡 Download Apple Maps satellite tiles for the selected area  
- 🧩 Automatically stitch tiles together on a canvas  
- 🖼️ Export the final image as a high-resolution PNG  

The tool is fully client-side (HTML + JavaScript) and uses a Cloudflare Worker to proxy Apple tile requests securely.

---

## 🛠 Tech Stack

### Frontend
- HTML5  
- Vanilla JavaScript  
- Leaflet.js  
- Leaflet Draw  

### Map Services
- OpenStreetMap  
- Nominatim (Geocoding API)  

### Proxy Layer
- Cloudflare Workers  

---

## ⚙️ Features

### 1️⃣ Location Search
Uses OpenStreetMap’s Nominatim API to geocode any location and center the map instantly.

### 2️⃣ Bounding Box Selection
Users can draw a rectangle on the map to define the exact download region.

### 3️⃣ Tile Coordinate Conversion
Implements Web Mercator tile calculation:
- Converts longitude/latitude to XYZ tile coordinates
- Supports custom zoom levels

### 4️⃣ Batch Tile Download
Downloads Apple satellite tiles using parameters:
- `style`
- `size`
- `scale`
- `zoom`
- `version`
- `accessKey`

Tiles are stitched into a single canvas dynamically.

### 5️⃣ PNG Export
Exports the final stitched image.

---

## 🧠 Technical Highlights

- Web Mercator projection tile math implementation
- Canvas-based tile stitching
- Async image loading with Promise handling
- Custom error handling UI
- Secure tile fetching via Cloudflare Worker proxy
- Fully client-side architecture

---

## 🚀 How It Works

1. Search for a location  
2. Draw a rectangle over the desired area  
3. Enter Apple Maps parameters (zoom, version, access key, etc.)  
4. Click **Download**  
5. Export the stitched image as PNG  

---

## 📷 Use Cases

- GIS experimentation  
- Satellite imagery research  
- Tile coordinate system learning  
- Map stitching demonstration  
- Web Mercator implementation practice  

---

## ⚠️ Disclaimer

This project is for educational and research purposes only.  
Please ensure compliance with Apple Maps' terms of service before using any downloaded imagery.
