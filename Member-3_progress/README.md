# InsightX -- Microplastic Detection & Environmental Analytics Dashboard

## 1. Project Overview

InsightX is a data analytics and interactive dashboard project developed
for HackMatrix 2026 -- Round 2. The project integrates water-quality,
microplastic, weather, polymer, location, and machine-learning datasets
into a structured data model and interactive dashboard.

The objective is to transform environmental datasets into meaningful
insights related to water quality, microplastic contamination,
environmental conditions, pollution patterns, and machine-learning
performance.
## 2. Problem Statement

Microplastic pollution in drinking-water sources is a significant
environmental concern. Water-quality information is often distributed
across multiple datasets and reports, making analysis and monitoring
difficult.

InsightX provides a centralized analytical solution that combines data
cleaning, data modeling, analysis, machine learning, and interactive
dashboard visualization.
## 3. Solution Overview

The project follows an end-to-end data analytics workflow:

**Data Collection → Data Cleaning → Data Modeling → Data Analysis →
Machine Learning → Dashboard Development → Insights**

The dashboard provides an integrated view of water quality, microplastic
contamination, environmental conditions, locations, polymers, risk
levels, and machine-learning results.
## 4. Datasets and Data Model

The project uses cleaned datasets covering weather, water samples,
microplastics, polymers, locations, and machine-learning predictions.

### Main Tables

  -----------------------------------------------------------------------
  Table                               Description
  ----------------------------------- -----------------------------------
  `dim_weather`                       Weather, rainfall, and runoff
                                      information

  `fact_water_samples`                Water-quality, microplastic,
                                      polymer, morphology, and risk
                                      information

  `ml_predictions`                    Machine-learning prediction outputs

  `dim_polymers`                      Polymer characteristics, toxicity,
                                      and degradation information

  `dim_locations`                     Geographic and location-related
                                      information
  -----------------------------------------------------------------------

A structured data model was created in Power BI by establishing
relationships between the relevant tables. This enables information from
multiple datasets to be analyzed together.
## 5. Data Import and Preparation

The datasets were imported into the project and prepared for analysis
and dashboard development.

The preparation process included:

-   Importing the required datasets
-   Checking missing values
-   Checking duplicate records
-   Correcting data types
-   Correcting date and time fields
-   Validating numerical values and ranges
-   Standardizing text and categorical fields
-   Checking identifier consistency such as `Sample_ID` and
    `Location_ID`
-   Checking unusual values and outliers
-   Preparing cleaned datasets for analysis and visualization
## 6. Data Modeling and Power BI Development

After data cleaning, a structured Power BI data model was developed.

The dashboard development process included:

-   Importing cleaned datasets
-   Creating new calculated columns
-   Creating calculated tables where required
-   Creating measures for KPIs and analysis
-   Establishing relationships between tables
-   Building a connected data model
-   Creating visualizations based on the modeled data
-   Applying consistent dashboard design and formatting

The relationships between the tables allow the dashboard to combine
environmental, water-quality, microplastic, polymer, location, and
machine-learning information.
## 7. Dashboard Development

The dashboard was developed progressively to provide both
dataset-specific analysis and an overall project view.

### 7.1 Individual Dataset Dashboard

Initially, individual dashboards were created for the separate datasets
to understand their structure, variables, and key information.

### 7.2 Executive Overview

An Executive Overview was developed to provide a consolidated summary of
the project.

It presents key measures and high-level insights from the integrated
datasets.

### 7.3 Water Quality Analysis

Line charts and other visualizations were created to analyze
water-quality trends across the available data.

The analysis helps identify changes and patterns in water-quality
measurements.

### 7.4 Microplastic Analysis

The dashboard includes analysis of microplastic-related information,
including:

-   Microplastic concentration
-   Microplastic counts
-   Polymer distribution
-   Particle characteristics
-   Morphology
-   Risk levels
-   Location-wise patterns

### 7.5 Environmental Conditions Analysis

Weather and environmental conditions were analyzed using the available
weather dataset.

The dashboard includes:

-   Average rainfall
-   Maximum rainfall
-   Average wind speed
-   Rainfall and runoff patterns
-   Relationships between environmental conditions and water-related
    measurements

### 7.6 Machine-Learning Performance

Visualizations were created to present machine-learning model
performance.

The evaluation includes:

-   Accuracy
-   Precision
-   Recall
-   F1 Score
-   Confusion Matrix
## 8. Data Analysis and Key Findings

The analysis covers water quality, microplastic concentration, particle
size, polymer types, morphology, risk levels, locations, and
weather-related patterns.

Documented findings include:

-   Rainfall and surface runoff show a strong correlation of
    approximately 0.93.
-   Average runoff is approximately 1.62 for light rain, 6.87 for
    moderate rain, and 19.23 for heavy rain.
-   Wind speed has a very weak relationship with runoff, with a
    correlation of approximately 0.03.
-   PVC has the highest toxicity score in the analyzed polymer data and
    a degradation time of approximately 1000 years.
-   Predicted microplastic count has a correlation of approximately
    0.995 with actual count, with an average prediction error of
    approximately 5%.
-   The contamination risk score has a correlation of approximately
    0.994 with actual microplastic count.
-   The location dataset covers 10 monitoring locations.

## 9. Machine Learning

A location-based classification module was developed using
`dim_locations_cleaned.csv`.

### Model Details

-   **Target:** `Water_Body_Type`
-   **Features:** Latitude, Longitude, City, State, Nearby Industry Type
-   **Algorithm:** Random Forest Classifier
-   **Preprocessing:** Feature selection, one-hot encoding, and
    train/test split
-   **Evaluation Metrics:** Accuracy, Precision, Recall, F1 Score, and
    Confusion Matrix

The location model is described as a demonstration model because the
location dataset does not directly contain microplastic contamination
measurements.
## 10. Dashboard Design

The dashboard was designed with a clean and consistent visual structure
to make complex environmental data easier to interpret.

The design includes:

-   KPI cards
-   Interactive charts
-   Line charts
-   Distribution charts
-   Risk-level visualizations
-   Location-wise analysis
-   Machine-learning performance charts
-   Interactive filters and slicers
-   Consistent formatting and styling
-   Separate dashboard sections for different analytical areas

## 11. Technology Stack

  Technology         Purpose
  ------------------ -----------------------------------------------------
  Power BI           Data modeling and interactive dashboard development
  Python             Data processing and analysis
  Pandas             Data preparation and manipulation
  NumPy              Numerical operations
  Jupyter Notebook   Data analysis and machine-learning workflow
  Matplotlib         Data visualization
  Seaborn            Data visualization
  Scikit-learn       Machine-learning implementation
  Excel / CSV        Structured project datasets
  APIs               External data sources where applicable

## 12. Project Workflow

``` text
Raw Datasets
     |
     v
Data Import
     |
     v
Data Cleaning and Preprocessing
     |
     v
New Columns, Tables and Measures
     |
     v
Data Modeling
     |
     v
Table Relationships
     |
     v
Data Analysis
     |
     +--------------------+
     |                    |
     v                    v
Water Quality       Microplastic Analysis
     |                    |
     +----------+---------+
                |
                v
Environmental Conditions Analysis
                |
                v
Machine-Learning Performance Analysis
                |
                v
Power BI Dashboard Development
                |
                v
Interactive Insights
```
## 13. Repository Structure

A typical project structure can be organized as follows:

``` text
InsightX/
|
├── datasets/
│   ├── raw/
│   └── cleaned/
|
├── notebooks/
│   └── analysis_and_ml/
|
├── powerbi/
│   └── InsightX_Dashboard.pbix
|
├── reports/
│   └── project_documentation/
|
└── README.md
```

## 14. Team Roles

  -----------------------------------------------------------------------
  Role                                Responsibility
  ----------------------------------- -----------------------------------
  Data Cleaning and Preprocessing     Clean, validate, and prepare
                                      project datasets

  Data Analysis and Visualization     Perform analysis, identify trends,
                                      and create visualizations

  Machine Learning                    Prepare data, train and evaluate
                                      models, and generate predictions

  Dashboard Development               Build the interactive dashboard and
                                      present project insights
  -----------------------------------------------------------------------
## 15. Future Scope

The project can be extended with:

-   Real-time water-quality monitoring
-   IoT sensor integration
-   Real-time weather and API integration
-   Real-time contamination alerts
-   Predictive contamination mapping
-   GIS integration
-   Mobile application integration
-   Automated notifications
-   Automated reporting

## 16. Repository and Links

**GitHub Repository:**\
https://github.com/Keerthi2412/Microplastic-Detection-Environmental-Analytics-Dashboard

**Live Dashboard:**\
Add deployment link here.

**Demo Video:**\
Add demo video link here.

## 17. Conclusion

InsightX provides a centralized approach for analyzing microplastic
pollution and environmental data. By combining cleaned datasets,
calculated columns, tables, measures, relationships, a structured data
model, environmental analysis, machine learning, and interactive Power
BI visualizations, the project converts complex datasets into meaningful
insights.

The dashboard supports analysis of water quality, microplastic
contamination, environmental conditions, locations, polymers, risk
levels, and machine-learning performance, providing a consolidated
platform for environmental data analysis and decision support.
