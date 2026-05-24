# methane-emission-estimation

**Type:** Master's Thesis Project  
**Author:** Andrii Baranichenko  
**Technologies:** Python, AWS (EC2, S3), Pandas, NumPy, Matplotlib, Xarray  

---

## 🛰️ Project Overview
This project focuses on building an **inverse model** for estimating methane emissions from satellite observations.  
The workflow involves **data retrieval, preprocessing, filtering, normalization, and visualization** of atmospheric methane concentration fields.

The study was conducted as part of a master's thesis at the National Technical University of Ukraine *"Igor Sikorsky Kyiv Polytechnic Institute"*.

---

## ⚙️ Features
- Processing of **Sentinel-5P satellite data** (methane concentration).  
- Application of data filtering and normalization techniques.  
- Implementation of an **inverse modeling approach** for emission estimation.  
- Visualization of methane distribution and model outputs.  
- Deployment of computations on **AWS EC2** and storage on **AWS S3**.

---

## 📐 Data Pipeline & Architecture

The project leverages the **Integrated Methane Inversion (IMI)** platform deployed on AWS to process high-resolution satellite data.

```text
[ S5P TROPOMI Satellite Data ] (Resident on AWS Cloud)
               │
               ▼
   [ AWS EC2 Instance (IMI AMI) ] ◄── Configured & Managed by me
               │
               ├─► Generates ~1.6 TB of intermediate outputs
               │
               ▼
        [ AWS S3 Bucket ] (Data Storage)
               │
               ▼
[ Custom Python Pipeline (My Code) ] 
 ├─ Libraries: Xarray, Pandas, Geopandas, Matplotlib
 ├─ Steps: Data retrieval, regional aggregation, filtering, and normalization
 └─ Output: Temporal/spatial emission analysis & visualizations
```

---

## 🧩 Repository Structure
```text
methane-emission-estimation/
├─ src/notebooks                 # Python scripts for preprocessing, modeling, and visualization
├─ data_samples/         # Example input datasets (small-sized for demonstration)
├─ docs/                 # Diagrams, result plots, and explanations
├─ requirements.txt      # Python dependencies
└─ README.md

