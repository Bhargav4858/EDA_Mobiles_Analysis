# 📱 Smartphone Market Price & Feature Analysis

## 📌 Project Overview

This project performs an end-to-end **Exploratory Data Analysis (EDA)**
on smartphone market data to understand how brand, hardware
specifications, camera features, display characteristics, operating
systems, and user ratings are associated with smartphone pricing.

The analysis starts with data cleaning and preprocessing, followed by
feature engineering, categorical transformation, non-visual analysis,
and visual exploration. The final stage summarizes the major pricing
patterns and business-oriented insights discovered from the dataset.

------------------------------------------------------------------------

## 🎯 Project Objective

The main objective of this project is to:

-   Analyze the distribution of smartphone brands and prices.
-   Identify the major factors associated with smartphone pricing.
-   Compare smartphone prices across brands and price segments.
-   Study the relationship between RAM, storage, battery, processor,
    camera, display, and price.
-   Analyze operating-system and processor patterns across brands.
-   Understand the relationship between customer ratings and smartphone
    prices.
-   Identify premium, mid-range, and budget market patterns.
-   Generate business insights that can support smartphone
    manufacturers, retailers, and consumers.

------------------------------------------------------------------------

## 📊 Dataset

**Dataset:** `Smart-Phones-Prices.csv`

### Initial Dataset

-   **Rows:** 1,020
-   **Columns:** 32

After duplicate removal and preprocessing:

-   **Rows:** 1,018
-   **Columns:** 43

The final dataset contains both original numerical/categorical variables
and engineered analysis-friendly features.

### Major Dataset Features

  -----------------------------------------------------------------------
  Category                            Features
  ----------------------------------- -----------------------------------
  Brand                               Brand

  Pricing                             Price

  Software                            Operating System, OS Version

  Processor                           Processor Brand, Processor Series,
                                      Processor Category

  Memory                              RAM, Internal Storage, RAM Tier

  Battery                             Battery Capacity, Fast Charging

  Display                             Screen Size, Refresh Rate,
                                      Resolution Width, Resolution
                                      Height, Notch Type

  Camera                              Primary Rear Camera, Rear Camera
                                      Count, Primary Front Camera, Front
                                      Camera Count

  Connectivity                        4G, 5G, Vo5G, NFC, IR Blaster

  Hardware                            Core Count, Clock Speed

  Other                               Dual SIM, Memory Card Support

  Customer Feedback                   Rating
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 🔄 Data Cleaning & Preprocessing

The following preprocessing steps were performed:

1.  Loaded the dataset using Pandas.
2.  Inspected dataset shape, data types, statistical information,
    duplicates, and missing values.
3.  Removed duplicate records.
4.  Checked for missing values.
5.  Combined processor brand and processor series into a single
    `Processor` feature.
6.  Removed unnecessary columns such as `Performance_Tier` and
    `memory_card_size`.
7.  Reordered columns for easier analysis.
8.  Standardized brand names such as `OPPO` and `POCO`.
9.  Removed the `RAM Tier` column because it contained mostly unknown
    values.
10. Corrected Apple devices to use `iOS` as the operating system
    category.
11. Replaced invalid zero values in camera-count columns with one
    camera.
12. Standardized OS version values.
13. Converted numerical fields containing units such as `mAh`, `W`, and
    `v` into numeric values for analysis.
14. Created simplified brand groups using the top six brands and an
    `Other` category.
15. Created standardized processor categories such as:
    -   Bionic
    -   Dimensity
    -   Exynos
    -   Helio
    -   Snapdragon
    -   Unisoc
    -   Google Tensor
    -   Kirin
    -   Other
16. Created analysis categories for price, RAM, storage, battery,
    charging power, screen size, camera specifications, processor speed,
    resolution, OS version, and ratings.

------------------------------------------------------------------------

## 🧩 Feature Engineering

Several categorical features were created using `pd.cut()` to make
comparisons easier.

### Price Categories

-   Budget
-   Mid-Range
-   Premium
-   Flagship
-   Luxury

### Other Categorized Features

-   RAM category
-   Storage category
-   Battery capacity category
-   Fast-charging category
-   OS-version category
-   Screen-size category
-   Rear-camera megapixel category
-   Front-camera megapixel category
-   Clock-speed category
-   Resolution-width category
-   Resolution-height category
-   Rating category

These engineered features make it easier to compare smartphone
positioning across different market segments.

------------------------------------------------------------------------

## 🔎 Exploratory Data Analysis

The project covers multiple dimensions of smartphone pricing and market
positioning.

### 1. Brand & Price Analysis

Analysis includes:

-   Brand frequency distribution
-   Price distribution
-   Price outlier detection
-   Price-segment distribution
-   Brand presence across price segments
-   Brand-wise price distribution
-   Average price by brand
-   Price variability by brand

### 2. Operating System Analysis

Analysis includes:

-   Operating-system distribution by brand
-   Average price by brand and OS
-   OS version versus price
-   Brand-level software positioning

### 3. Processor Analysis

Analysis includes:

-   Processor-category distribution
-   Processor versus price
-   Processor type and RAM relationships
-   Clock speed versus price
-   Brand-wise processor positioning

### 4. RAM Analysis

Analysis includes:

-   RAM distribution
-   RAM versus price
-   Brand-wise RAM pricing
-   RAM category versus price

### 5. Storage Analysis

Analysis includes:

-   Storage distribution
-   Storage versus price
-   Brand-wise storage pricing
-   Storage category versus price

### 6. Battery & Charging Analysis

Analysis includes:

-   Battery capacity versus price
-   Fast-charging power versus price
-   Brand-wise battery and charging patterns

### 7. Camera Analysis

Analysis includes:

-   Primary rear-camera megapixels versus price
-   Number of rear cameras versus price
-   Primary front-camera megapixels versus price
-   Number of front cameras versus price
-   Brand-wise camera positioning

### 8. Display Analysis

Analysis includes:

-   Resolution width versus price
-   Resolution height versus price
-   Screen-size categories
-   Notch type versus price
-   Brand-wise display positioning

### 9. Rating Analysis

Analysis includes:

-   Rating versus price
-   Average rating by brand
-   Rating category versus price
-   Brand-wise rating patterns

### 10. Correlation Analysis

A correlation matrix was created for important numerical variables
including:

-   Price
-   RAM
-   Storage
-   Battery capacity
-   Rear camera megapixels
-   Front camera megapixels
-   Clock speed
-   Rating

------------------------------------------------------------------------

## 📈 Key Insights

### 💰 Pricing

-   The dataset is concentrated mainly in the **mid-range smartphone
    segment**.
-   Premium, flagship, and luxury smartphones represent a smaller
    portion of the dataset.
-   The price distribution contains high-value outliers representing
    premium and luxury devices.

### 🏷️ Brand Positioning

-   Brands such as **Samsung, Xiaomi, Vivo, and OPPO** have substantial
    representation across multiple price segments.
-   Brands such as **Apple, Vertu, Royole, Leitz, and Huawei** appear
    more strongly in higher-priced segments within this dataset.
-   Brand-level pricing varies considerably, indicating that brand
    identity and product positioning are associated with price
    differences.

### 💾 RAM & Storage

-   Higher RAM configurations are generally associated with higher
    smartphone prices.
-   Storage capacity shows a strong positive relationship with price in
    the analysis.
-   Storage and RAM are among the most important hardware specifications
    associated with smartphone pricing.

### ⚙️ Processor

-   Premium and flagship processor categories are generally associated
    with higher-priced smartphones.
-   Processor family and clock speed show noticeable pricing differences
    across brands.

### 📷 Camera

-   Higher camera specifications are generally associated with higher
    prices, although the relationship is not uniform across all brands.
-   Some brands offer relatively high camera specifications at lower
    price points.

### 🖥️ Display

-   Display resolution and other display characteristics contribute to
    price differences.
-   Higher-resolution devices are frequently positioned in higher price
    categories, although brand-level exceptions exist.

### 🔋 Battery & Charging

-   Battery capacity contributes to smartphone price variation.
-   Fast-charging capability provides an additional differentiating
    feature, particularly in higher-specification devices.

### ⭐ Ratings

-   Smartphone ratings show a relatively weak positive relationship with
    price.
-   A higher price does not necessarily guarantee a proportionally
    higher customer rating.

### 📱 Operating System

-   Android is the dominant operating system in the dataset because it
    appears across many manufacturers and price segments.
-   iOS is associated with Apple devices in the cleaned dataset.

------------------------------------------------------------------------

## 💼 Business Recommendations

Based on the exploratory patterns:

1.  Smartphone manufacturers can prioritize **RAM and storage
    configurations** when designing products for higher price segments.
2.  Mid-range manufacturers can focus on delivering premium-like
    specifications at competitive prices.
3.  Retailers can use feature-based segmentation to improve product
    positioning and recommendations.
4.  Camera, battery, charging, and display features can be used as
    differentiators in competitive market segments.
5.  Brand positioning should be considered alongside hardware
    specifications because similar specifications can have substantially
    different prices across brands.
6.  Customer ratings should be considered as a separate
    customer-experience metric rather than assuming that higher-priced
    devices automatically receive better ratings.

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   **Python**
-   **Pandas** -- Data manipulation and analysis
-   **NumPy** -- Numerical operations
-   **Matplotlib** -- Data visualization
-   **Seaborn** -- Statistical visualization
-   **Jupyter Notebook** -- Development and analysis environment

------------------------------------------------------------------------

## 📂 Project Structure

``` text
Smartphone-Market-Analysis/
│
├── Mobiles_dataset_analysis.ipynb
├── Smart-Phones-Prices.csv
├── README.md



## 📌 Project Workflow

``` text
Raw Smartphone Dataset
        ↓
Data Understanding
        ↓
Data Cleaning
        ↓
Duplicate & Missing-Value Checks
        ↓
Feature Engineering
        ↓
Categorization & Standardization
        ↓
Exploratory Data Analysis
        ↓
Brand & Price Analysis
        ↓
Hardware Analysis
        ↓
Camera & Display Analysis
        ↓
OS & Rating Analysis
        ↓
Correlation Analysis
        ↓
Key Insights
        ↓
Business Recommendations
```

------------------------------------------------------------------------

## ⚠️ Limitations

-   This is an **exploratory analysis**, so observed relationships
    should not automatically be interpreted as causal relationships.
-   The dataset represents the products included in the source data and
    may not represent the entire smartphone market.
-   Brand representation is uneven, which can affect comparisons between
    brands.
-   Price can be influenced by factors not fully captured in the
    dataset, such as launch date, region, promotions, availability,
    brand strategy, and ecosystem.
-   Some preprocessing decisions involve assumptions, such as replacing
    zero camera counts with one.
-   Correlation measures association between variables and does not
    establish causation.

------------------------------------------------------------------------

## 🚀 Future Improvements

-   Build an interactive **Streamlit dashboard** for smartphone market
    exploration.
-   Develop a **smartphone price prediction model** using machine
    learning.
-   Create a **Value-for-Money Score** using price and specifications.
-   Add time-based analysis if historical smartphone launch/price data
    becomes available.
-   Compare brands using normalized specification scores.
-   Perform statistical hypothesis testing to validate important
    observed relationships.
-   Add interactive filters for brand, price range, processor, RAM,
    storage, camera, and operating system.

------------------------------------------------------------------------

## 👨‍💻 Author

**Vempa Bhargav Naidu**

B.Tech -- Computer Science and Engineering

**Skills:** Python \| SQL \| Pandas \| NumPy \| Matplotlib \| Seaborn \|
Power BI \| Data Analytics \| Machine Learning

------------------------------------------------------------------------

## ⭐ Conclusion

This project provides a structured analysis of smartphone pricing and
market positioning using real-world smartphone specification data. The
analysis highlights the importance of **storage, RAM, processor
capabilities, display specifications, camera features, battery/charging
technology, and brand positioning** in understanding smartphone prices.

The project demonstrates an end-to-end **Data Analytics / EDA
workflow**, from raw data preprocessing and feature engineering to
visualization, correlation analysis, insight generation, and business
recommendations.
