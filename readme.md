# Geospatial Analysis: NDVI Field Explorer 🛰️

A professional demonstration project focusing on **Remote Sensing (RS)** and **Geospatial Data Science**. This full-stack application serves as a practical implementation of satellite imagery processing, specifically designed for monitoring vegetation health (NDVI) using **Sentinel-2 L2A** (Bottom-of-Atmosphere) data.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Visit%20App-brightgreen)](https://ndvi-field-analyzer.onrender.com) 
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

---

## 🎓 Academic & Professional Context

This project was developed to demonstrate advanced workflows in **Geoinformatics** and **Earth Observation**. The primary goal was to bridge the gap between raw satellite data acquisition and meaningful spatio-temporal analysis through a custom-built web interface.

### Key Analytical Concepts Implemented:
* **Radiometric Processing:** Integration with the Copernicus Data Space Ecosystem to fetch Sentinel-2 L2A products.
* **Vegetation Indices:** Automated calculation of the **Normalized Difference Vegetation Index (NDVI)** to assess biomass and plant vigor.
* **Spatio-Temporal Filtering:** Advanced cloud detection using the **Scene Classification Layer (SCL)**. The algorithm performs a spatial intersection check to filter out cloudy pixels specifically within the user-defined area of interest (AOI).

---

## 🛠️ Tech Stack & Skills Demonstrated

The architecture reflects a modern **Geospatial Engineering** approach:

* **Geospatial Backend (Python 3.11):**
    * **SentinelHub API:** Automated data retrieval from Copernicus services.
    * **Rasterio & NumPy:** Efficient processing of multi-spectral raster arrays.
    * **Shapely:** Geometric operations and AOI polygon processing.
    * **Flask:** RESTful API development for geospatial data delivery.
* **Frontend / GIS Visualization:**
    * **Leaflet.js:** Interactive mapping and vector data handling (drawing tools).
    * **Chart.js:** Dynamic visualization of time-series vegetation trends.

---

## 🚀 Key Features

* **Polygon-Based Analysis:** Allows users to define precise AOIs for targeted spatial queries.
* **Intelligent Data Cleaning:** Automated rejection of low-quality images based on local cloud coverage within the AOI.
* **Interactive Time-Series:** Visualizing seasonal changes in vegetation health over a selected period.
* **Multi-Layer Visualization:** Seamless overlay of NDVI rasters with adjustable opacity over base maps.
* **Report Generation:** Exporting analytical results into a portable HTML format for documentation.

---

## ⚙️ Getting Started (Local Development)

### Prerequisites
* Python 3.11+
* [Copernicus Data Space Ecosystem](https://dataspace.copernicus.eu/) credentials.
  
### Installation & Setup

1.  **Clone the repo**
    ```sh
    git clone [https://github.com/Frenzi11/ndvi-web-app.git](https://github.com/Frenzi11/ndvi-web-app.git)
    cd ndvi-web-app
    ```
2.  **Create a virtual environment**
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```
3.  **Install Python packages**
    ```sh
    pip install -r requirements.txt
    ```
4.  **Set up environment variables**
    * Create a file named `.env` inside the `backend` folder.
    * Add your Copernicus API credentials to it:
        ```
        CDSE_CLIENT_ID='your-client-id-goes-here'
        CDSE_CLIENT_SECRET='your-client-secret-goes-here'
        ```
5.  **Run the application**
    * Navigate to the backend directory and start the Flask server:
        ```sh
        cd backend
        flask run
        ```
    * Open your browser and go to `http://127.0.0.1:5000`

---

## License

Distributed under the MIT License. See `LICENSE` for more information.
