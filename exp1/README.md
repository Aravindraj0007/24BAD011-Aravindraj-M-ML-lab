# Machine Learning Lab - Experiment 1
## Data Analysis and Visualization

This notebook contains exploratory data analysis (EDA) and visualization exercises on multiple datasets using Python libraries.


---

## 🎯 Overview

This experiment demonstrates fundamental data analysis techniques including:
- Data loading and exploration
- Statistical analysis
- Data visualization
- Correlation analysis
- Feature engineering

---

## 📦 Requirements

The following Python libraries are required:

```python
numpy
pandas
matplotlib
seaborn
```

Install them using:
```bash
pip install numpy pandas matplotlib seaborn
```

---

## 📊 Datasets

### Dataset 1: E-commerce Sales Data (`data.csv`)
- **Source**: [Kaggle - E-commerce Data](https://www.kaggle.com/datasets/carrie1/ecommerce-data)

### Dataset 2: Diabetes Data (`diabetes.csv`)
- **Source**: [Kaggle - Pima Indians Diabetes Database](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

### Dataset 3: Housing Data (`Housing.csv`)
- **Source**: [Kaggle - Housing Price Prediction](https://www.kaggle.com/datasets/harishkumardatalab/housing-price-prediction)

### Dataset 4: Marketing Campaign Data (`marketing_campaign(1).csv`)
- **Source**: [Kaggle - Customer Personality Analysis](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)

---

## 🔍 Analysis Performed

### Dataset 1 - E-commerce Sales
- ✅ Data inspection (`head()`, `tail()`, `info()`, `describe()`)
- ✅ Missing value analysis
- ✅ **Bar Chart**: Top 10 products by quantity sold
- ✅ **Line Chart**: Sales trend visualization

### Dataset 2 - Diabetes
- ✅ Data exploration (`head()`, `tail()`)
- ✅ **Histogram**: Glucose level distribution
- ✅ **Boxplot**: Age distribution

### Dataset 3 - Housing
- ✅ Data inspection and missing value check
- ✅ **Scatter Plot**: Area vs Price relationship
- ✅ **Heatmap**: Feature correlation matrix

### Dataset 4 - Marketing Campaign
- ✅ Data exploration and statistical summary
- ✅ Missing value analysis
- ✅ Feature engineering (Age calculation from Year_Birth)
- ✅ **Bar Chart**: Age distribution
- ✅ **Boxplots**: Age, Income, and Total Spending distributions
- ✅ **Histogram**: Income distribution
- ✅ Custom feature creation (Total_Spending)

---

## 🚀 Setup Instructions

1. **Clone or download** this repository
2. **Prepare datasets**: Ensure all CSV files are in the correct path:
   - `data.csv`
   - `diabetes.csv`
   - `Housing.csv`
   - `marketing_campaign(1).csv`
   
   > **Note**: Update the file paths in the notebook if your datasets are in different locations

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Open the notebook**:
   ```bash
   jupyter notebook ML_exp1.ipynb
   ```
   Or use VS Code with Jupyter extension

---

## 💻 Usage

1. Open `ML_exp1.ipynb` in Jupyter Notebook or VS Code
2. Run cells sequentially from top to bottom
3. Modify file paths if your datasets are located elsewhere
4. Each dataset section is clearly marked with comments

---

## 📈 Key Visualizations

- **Bar Charts**: Product sales, age distribution
- **Line Charts**: Sales trends
- **Histograms**: Glucose levels, income distribution
- **Boxplots**: Age, income, and spending outlier detection
- **Scatter Plots**: Area-price relationships
- **Heatmaps**: Feature correlation analysis


---

## 📝 Notes

- Some datasets may contain missing values - check using `df.isnull().sum()`
- Ensure proper encoding when loading CSV files (e.g., `encoding='latin1'`)
- Adjust figure sizes for better visualization if needed
- The Age column in the marketing dataset is calculated as `2026 - Year_Birth`



*Last Updated: January 2026*
