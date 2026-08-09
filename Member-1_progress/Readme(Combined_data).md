# Combined Dataset - Microplastic Prediction ML Model

## 1. Project Overview

This module contains the final machine learning pipeline for the Microplastic Water Quality Analytics project.

Multiple cleaned datasets are integrated to develop a machine learning model capable of predicting microplastic contamination in water samples.

The combined dataset integrates:

1. Water sample information
2. Location information
3. Polymer characteristics
4. Weather information

The final prediction target is:

`Microplastic_Count_per_m3`

---

# 2. Datasets Used

## Fact Water Samples

File:

`cleaned_fact_water_samples.csv`

Contains:

- Sample information
- Water quality measurements
- Microplastic concentration
- Polymer information
- Risk information

---

## Location Dataset

File:

`dim_locations_cleaned.csv`

Contains:

- Location ID
- Location name
- Water body type
- Latitude
- Longitude
- City
- State
- Nearby industry type

---

## Polymer Dataset

File:

`dim_polymers_cleaned.csv`

Contains:

- Polymer code
- Polymer name
- Toxicity score
- Degradation rate
- Other polymer characteristics

---

## Weather Dataset

File:

`weather_cleaned.csv`

Contains:

- Location ID
- Date
- Rainfall
- Wind speed
- Surface runoff index

---

# 3. Data Integration

The datasets are combined using common keys.

### Location Integration

`Location_ID`

is used to connect water samples with location information.

### Polymer Integration

`Dominant_Polymer`

is connected with:

`Polymer_Code`

### Weather Integration

Weather information is aggregated by:

- Location ID
- Month

The resulting weather information is merged with the water sample records.

---

# 4. Combined Dataset

The resulting file is:

`combined_ml_dataset.csv`

The combined dataset contains information from:

```text
Water Samples
      +
Locations
      +
Polymers
      +
Weather
