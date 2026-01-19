# Aadhaar Service Stress & Data Quality Analytics (UIDAI Hackathon)

This project performs a holistic analysis of UIDAI Aadhaar **Enrolment**, **Demographic Updates**, and **Biometric Updates** datasets to identify:
- High-demand service hotspots (district/pincode level)
- Service load concentration patterns
- Time-based trends and stress spikes
- Early warning signals for abnormal behaviour (data quality / operational surges)

The final output includes:
✅ A reproducible Python notebook (Google Colab)  
✅ A consolidated dataset for reporting  
✅ An interactive Power BI dashboard for insights and monitoring  

---

## 🧩 Problem Statement
Aadhaar services experience uneven demand across regions and time. Some districts/pincodes face consistently high enrolment and update workloads, while sudden spikes in update patterns may indicate temporary surges, operational bottlenecks, or potential data quality concerns.

This project aims to convert raw Aadhaar activity into actionable operational intelligence using a unified stress monitoring framework.

---

## 📌 Key Idea: Service Stress Index
We propose a **Service Stress Index** to quantify combined Aadhaar service load:

**Service Stress Index = (0.6 × Total Updates) + (0.4 × Total Enrolments)**

Where:
- Total Updates = Demographic Updates + Biometric Updates  
- Total Enrolments = Enrolment across age groups  

This provides a scalable indicator for identifying high-load zones.

---

## 📂 Datasets Used (UIDAI)
This project uses the official UIDAI datasets provided for the hackathon:

1. **Aadhaar Enrolment Dataset**
   - date, state, district, pincode
   - age_0_5, age_5_17, age_18_greater

2. **Aadhaar Demographic Update Dataset**
   - date, state, district, pincode
   - demo_age_5_17, demo_age_17_

3. **Aadhaar Biometric Update Dataset**
   - date, state, district, pincode
   - bio_age_5_17, bio_age_17_

---

## 🛠️ Tech Stack
- **Python** (Pandas, NumPy, Matplotlib)
- **Google Colab / Jupyter Notebook**
- **Power BI Desktop**
- GitHub for version control and documentation

---

## 🔎 Methodology (High Level)
1. Extract and load all dataset files
2. Standardize columns and parse dates
3. Clean and preprocess data (types, nulls, duplicates)
4. Merge datasets on:
   - `date`, `state`, `district`, `pincode`
5. Engineer KPIs:
   - Total Enrolments
   - Total Updates
   - Update-to-Enrolment Ratio
   - Service Stress Index
6. Detect stress spikes using rolling trend signals
7. Export final dataset for Power BI dashboarding

---

## 📊 Power BI Dashboard (Report)
The Power BI dashboard includes:
- Executive KPIs (Enrolments, Updates, Stress Index)
- Trend analysis over time
- Top districts/pincodes by service stress
- Hotspot ranking table with filters
- Anomaly signal monitoring view

---

## 🚀 How to Run
### Option A: Run Notebook in Google Colab
1. Open the notebook:
   - `UIDAI_DATA_HACKATHON_CODE.ipynb`
2. Upload the dataset ZIP files in Colab
3. Run all cells from top to bottom
4. Output generated:
   - `final_uidai_service_stress.csv`

### Option B: Open Power BI Report
1. Open `PowerBi report.pbix`
2. Refresh data source if required
3. Explore visuals using state/date filters

---

## 📌 Results / Outputs
- District and pincode-level hotspot rankings
- Stress index trends across the timeline
- Update-heavy service load dominance patterns
- Anomaly signal framework for early warning monitoring

---

## 📁 Repository Structure
├── UIDAI_DATA_HACKATHON_CODE.ipynb
├── PowerBi report.pbix
├── final_uidai_service_stress.csv (generated)
└── README.md


---

## 🔮 Future Scope
- Forecast stress index using time-series models
- Cluster regions based on service behaviour
- Integrate service centre capacity/staffing data
- Automated alerting system for anomaly spikes

---

## 👤 Author / Team
Built for the UIDAI Data Hackathon submission.

If you'd like to collaborate or discuss improvements, feel free to connect.
