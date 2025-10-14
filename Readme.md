# 🌍 Satellite Image Growth Analysis using Google Earth Engine and Machine Learning

## 📘 Project Overview

This project focuses on collecting, preprocessing, and analyzing satellite imagery to monitor and **predict growth patterns** (such as vegetation or urban expansion) using **Google Earth Engine (GEE)** and **unsupervised machine learning** techniques.

The workflow begins with **data collection from Google Earth Engine**, storage and management via **Google Cloud**, and proceeds through a **multi-layered K-Means segmentation** approach to extract meaningful patterns from satellite images. The final stage involves **analyzing growth metrics** and **predicting future growth trends** based on the segmented image data.

---

## 🧠 Key Features

- Automated satellite data collection via **Google Earth Engine (GEE)**
- Cloud storage management through **Google Cloud Storage** and **Google Drive**
- Image preprocessing (normalization, filtering, and enhancement)
- Multi-layered **K-Means image segmentation**
- Growth trend analysis and prediction using segmented data
- Fully integrated workflow using **Google Colab**

---

## ⚙️ Project Architecture

1. **Data Collection**
   - Create a project in **Google Cloud Console**.
   - Enable the **Google Earth Engine API**.
   - Authenticate your account and fetch imagery using the **GEE Python API**.
   - Export data to **Google Cloud Storage** or directly to **Google Drive**.

2. **Image Preprocessing**
   - Load satellite images from Drive or Cloud Storage into Colab.
   - Apply preprocessing techniques such as resampling, normalization, and denoising using libraries like `rasterio` and `numpy`.

3. **Segmentation (Multi-layered K-Means)**
   - Perform multi-stage clustering on pixel values for enhanced segmentation.
   - Each layer refines the segmentation, improving object boundary clarity.
   - Visualize segmentation results and compare them with raw imagery.

4. **Growth Analysis & Prediction**
   - Analyze pixel-class changes over time.
   - Compute growth rate and trend metrics.
   - Optionally train regression or ML models to forecast future growth patterns.

---

## 🧩 Dependencies

Most modules are **preinstalled in Google Colab**, so setup is minimal.  
However, you need to install the following extra dependencies:

```bash
pip install rasterio

```

Other common libraries used (already available in Colab):

* `geemap`
* `ee` (Earth Engine Python API)
* `numpy`
* `matplotlib`
* `sklearn`
* `pandas`

---

## 🚀 Running the Project

1. **Clone this Repository**

   ```bash
   git clone https://github.com/Risav27/Mangrove-Growth-Monitoring.git
   cd Mangrove-Growth-Monitoring
   ```

2. **Authenticate Google Earth Engine**

   ```python
   import ee
   ee.Authenticate()
   ee.Initialize()
   ```

3. **Run Data Collection Notebook**
   Execute the notebook: `data_collection.ipynb`

   * Fetch data from GEE.
   * Export to Google Cloud Storage or Drive.

4. **Run Image Processing & Segmentation Notebook**
   Execute the notebook: `image_segmentation.ipynb`

   * Load the imagery.
   * Preprocess and apply multi-layered K-Means.
   * Visualize the results.

5. **Run Growth Analysis Notebook**
   Execute the notebook: `growth_prediction.ipynb`

   * Perform temporal analysis and compute growth trends.
   * Predict future growth based on past data.

---

## ☁️ Google Cloud Setup

1. Visit [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project and enable **Google Earth Engine**.
3. Link **Google Cloud Storage** or **Google Drive** for data export.
4. Set environment variables or authentication tokens in Colab when prompted.

---

## 📊 Output

* Segmented image layers (visualized with distinct color codes)
* Growth trend graphs and metrics
* Optional predictive visualizations showing expected growth areas

---



## 🙌 Acknowledgements

* [Google Earth Engine](https://earthengine.google.com/) for satellite data and processing tools
* [Google Cloud Platform](https://cloud.google.com/) for scalable data storage
* [Google Colab](https://colab.research.google.com/) for interactive experimentation and ML development

````
