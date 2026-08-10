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
