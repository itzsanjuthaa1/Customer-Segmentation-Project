# 🎯 Customer Segmentation Intelligence Dashboard

> **B.Tech IT Portfolio Project** — Machine Learning · Python · Streamlit · Plotly

A production-quality customer segmentation system that clusters 5,000+ customers using **K-Means** clustering, provides a fully interactive **Streamlit dashboard**, and ships a **standalone HTML dashboard** that works directly in any browser — no Python required.

---

## 📸 Dashboard Preview

| Feature | Detail |
|---|---|
| Algorithm | K-Means Clustering |
| Optimal K | Found via Elbow Method + Silhouette Score |
| Dataset | 5,000 realistic customer records |
| Segments | Up to 5 distinct customer personas |
| Charts | 8+ interactive Plotly visualisations |
| Export | CSV, Summary CSV, Business Report TXT |

---

## 🗂️ Project Structure

```
customer_segmentation/
├── app.py                              # Streamlit dashboard
├── customer_segmentation.py           # ML pipeline (core logic)
├── generate_dataset.py                # Dataset generation script
├── customer_segmentation_dashboard.html  # Standalone HTML dashboard
├── requirements.txt
├── README.md
└── data/
    ├── customer_dataset.csv           # Raw dataset (5,000 records)
    └── customer_segmented.csv         # Output with cluster labels
```

---

## ⚙️ Installation

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/customer-segmentation.git
cd customer-segmentation
```

### 2. Create a Virtual Environment (Recommended)
```bash
python -m venv venv
source venv/bin/activate        # macOS / Linux
venv\Scripts\activate           # Windows
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

---

## 🚀 Running the Project

### Option A — Streamlit Dashboard (recommended)
```bash
streamlit run app.py
```
Then open **http://localhost:8501** in your browser.

### Option B — Run ML Pipeline Only
```bash
python customer_segmentation.py
```
Prints KPIs, segment summary, and saves `data/customer_segmented.csv`.

### Option C — Standalone HTML (no Python needed)
Simply open `customer_segmentation_dashboard.html` in **any modern browser**. No server, no dependencies.

### Option D — Regenerate Dataset
```bash
python generate_dataset.py
```

---

## 🧠 ML Methodology

### Feature Engineering
Seven features are used for clustering:
- **Age** — demographic signal
- **Annual Income** — purchasing power
- **Purchase Frequency** — engagement depth
- **Average Order Value** — transaction quality
- **Total Spending** — lifetime value proxy
- **Customer Tenure** — loyalty signal
- **Online Purchase Ratio** — channel preference

All features are **StandardScaler**-normalised before clustering.

### Optimal K Selection
1. **Elbow Method** — plot inertia vs. K; identify the "elbow" where marginal gain diminishes.
2. **Silhouette Score** — quantifies cluster cohesion and separation (range −1 to +1; higher is better).
3. The K with the **highest silhouette score** is selected automatically.

### Dimensionality Reduction
**PCA (2 components)** is applied for scatter-plot visualisation only — clustering is performed in the full 7-dimensional feature space.

---

## 📊 Customer Segments

| Segment | Description | Key Trait |
|---|---|---|
| 💎 Premium Buyers | High income + high spending | Upsell & VIP programmes |
| 🤝 Loyal Mid-Tier | Long tenure + consistent spend | Retention & cross-sell |
| 🚀 Young Actives | High frequency + digital-first | Social commerce |
| 💡 Value Seekers | Budget-conscious, price-driven | Promotions & bundles |
| ⚠️ At-Risk | Declining engagement | Win-back campaigns |

---

## 📈 Dashboard Features

### KPI Cards
- Total Customers · Average Spending · Average Income · Retention Rate · Top Revenue Segment

### Filters
- Age Group · Gender · Region · Product Category · Segment

### Visualisations
1. Segment Distribution (Donut Chart)
2. Elbow Method & Silhouette Analysis (Dual-axis Line Chart)
3. PCA Scatter Plot (Customer Clusters in 2D)
4. Revenue by Segment (Horizontal Bar Chart)
5. Income vs. Spending (Scatter + Size by Frequency)
6. Age Distribution by Segment (Histogram)
7. Regional Breakdown (Stacked Bar)
8. Product Preference Heatmap

### Segment Profiles
- Auto-generated business descriptions per cluster
- Actionable retention, upselling, and loyalty strategies

### Exports
- Full filtered dataset (CSV)
- Segment analytics summary (CSV)
- Business recommendations report (TXT)

---

## 🌐 GitHub Deployment

```bash
git init
git add .
git commit -m "Initial commit: Customer Segmentation Dashboard"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/customer-segmentation.git
git push -u origin main
```

> The **standalone HTML file** can also be deployed to **GitHub Pages** with zero configuration:
> `Settings → Pages → Deploy from branch → main / root`

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Language | Python 3.10+ |
| Data | Pandas · NumPy |
| ML | Scikit-learn (KMeans, PCA, StandardScaler, silhouette_score) |
| Visualisation | Plotly Express · Plotly Graph Objects |
| Web Framework | Streamlit |
| Standalone UI | Vanilla HTML · CSS · Plotly.js |

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you'd like to change.

---

*Built with ❤️ as a B.Tech IT Portfolio Project*
