# 🧠 Customer Segmentation using Deep Embedded Clustering (DEC)

This repository provides a detailed overview of our final year B.Tech project focused on customer segmentation using a novel machine learning approach — Deep Embedded Clustering (DEC). This technique is capable of automatically identifying meaningful groups of customers based on purchasing behavior using both feature learning and clustering.

---

## 📑 Abstract

The increasing volume of customer data in e-commerce has made it essential to adopt advanced analytical techniques to understand customer behavior. Traditional clustering techniques like K-Means, DBSCAN, and Hierarchical Clustering often struggle with high-dimensional or sparse data. To address these challenges, we proposed a model based on Deep Embedded Clustering (DEC) which utilizes deep autoencoders for dimensionality reduction followed by soft clustering. This project compares the results of traditional methods against DEC to demonstrate its performance and segmentation quality.

---

## 📊 Dataset

The dataset used in this project is the **Brazilian E-Commerce Public Dataset by Olist** from Kaggle, which includes:

- Customer data
- Order information
- Product and seller information
- Payment and review details

The dataset was preprocessed and merged into a single customer-centric dataset using Pandas.

---

## ⚙️ Tools Used

- Python
- Google Colab
- Pandas, NumPy
- Scikit-learn
- TensorFlow, Keras
- Matplotlib, Seaborn, Plotly

---

## 🧪 Methodology

### 🔹 Data Preprocessing
- Merged multiple CSV files using `customer_id` as the primary key.
- Removed null values and outliers using Z-score and IQR methods.
- Encoded categorical data and scaled features using `StandardScaler`.

### 🔹 Feature Engineering
- Derived **RFM (Recency, Frequency, Monetary)** features from the transaction data.

### 🔹 Clustering Techniques
- Implemented and evaluated:
  - K-Means Clustering
  - DBSCAN
  - Hierarchical Clustering
  - **Deep Embedded Clustering (DEC)**

### 🔹 Deep Embedded Clustering (DEC)
- Built an autoencoder for feature extraction.
- Latent features were clustered using a custom clustering layer.
- The model was optimized using Kullback-Leibler divergence loss.

---

## 📈 Results

### 🧪 Evaluation Metrics

| Model         | Silhouette Score | Calinski-Harabasz Index |
|---------------|------------------|--------------------------|
| K-Means       | 0.585            | 2601.45                  |
| DBSCAN        | 0.628            | 2293.41                  |
| Hierarchical  | 0.512            | 2425.78                  |
| RFM Only      | 0.521            | 2556.72                  |
| **DEC**       | **0.672**        | **2734.89**              |

The results show that DEC produced the highest silhouette score and CH index, indicating well-separated and cohesive clusters.

---

## 🖼 Sample Output Visualizations

- Cluster Distribution Pie Chart
- t-SNE/UMAP Plot for latent space
- Dendrogram from hierarchical clustering
- Boxplots for RFM features by cluster

All visuals are available in the `images/` folder.

---

## 📂 Directory Structure

```bash
customer-segmentation-dec/
├── data/                       # Raw and processed datasets
├── notebooks/                 # Jupyter notebooks
├── images/                    # Output plots and diagrams
├── saved_models/              # Trained DEC model (.h5)
├── docs/                      # Project report and presentation
├── requirements.txt           # Python dependencies
└── README.md                  # This file
```

---

## 📄 How to Run

1. Clone this repository:
```bash
git clone https://github.com/<your-username>/customer-segmentation-dec.git
cd customer-segmentation-dec
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Open and run the notebooks in Google Colab or Jupyter:
- `notebooks/1_data_preprocessing.ipynb`
- `notebooks/2_rfm_analysis.ipynb`
- `notebooks/3_dec_model.ipynb`

---

## 👨‍👩‍👧‍👦 Team Members

- Narra Manasa (21BQ1A05G4)
- Pothina Trisha (21BQ1A05I5)
- Patibanda Bhavana (21BQ1A05H4)
- Polisetty Sai Ganesh (21BQ1A05I4)

**Guide**: Mr. K. Mohan Krishna, Associate Professor, VVIT

---

## 📜 License

This project is licensed under the MIT License.

---

## 📧 Contact

For queries or contributions, please reach out to any of the contributors or submit an issue on GitHub.
