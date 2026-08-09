**Data Cleaning & Preprocessing**

Before starting the analysis and machine learning process, we cleaned and checked all the datasets to make sure the data was reliable, consistent, and ready to use.

**1. Weather Data (`dim_weather`)**

- Checked the dataset for missing values and duplicate records.
- Converted the `Date` column into the correct date format.
- Checked rainfall, wind speed, and runoff values for invalid or negative entries.
- Cleaned the `Location_ID` values by removing unnecessary spaces and inconsistencies.
- Checked for duplicate records for the same location and date.
- Looked for unusual values and possible outliers in the weather measurements.
- Created date-related fields such as year, month, and day for further analysis.

**2. Water Sample Data (`fact_water_samples`)**

- Checked the data for missing values and duplicate records.
- Verified that each `Sample_ID` was unique.
- Converted the `Timestamp` column into the correct date and time format.
- Checked water-quality measurements for invalid values.
- Verified that pH values were within a reasonable range.
- Checked microplastic counts and particle sizes for unusual values.
- Standardized fields such as `Risk_Level`, `Dominant_Polymer`, and `Dominant_Morphology`.
- Prepared the data for further analysis and machine learning.

**3. ML Predictions (`ml_predictions`)**

- Checked for missing and duplicate records.
- Verified the data types of the prediction-related columns.
- Checked that the predicted risk categories were consistent.
- Validated numerical prediction and confidence values.
- Cleaned inconsistent categorical values.
- Made sure the dataset was ready to be used for evaluating and displaying machine learning predictions.

**4. Polymer Data (`dim_polymers`)**

- Checked for missing values and duplicate records.
- Verified that each polymer had a unique identifier.
- Cleaned polymer names and text fields.
- Removed unnecessary spaces and formatting inconsistencies.
- Checked the polymer categories for consistency.
- Made sure the polymer data could be correctly linked with the water sample data.

**5. Location Data (`dim_locations`)**

- Checked for missing and duplicate records.
- Verified that each `Location_ID` was unique.
- Cleaned location names and text fields.
- Checked geographical information for incorrect or unusual values.
- Removed unnecessary spaces and formatting issues.
- Made sure the location IDs were consistent with the other datasets.

**Overall Data Quality Checks**

For all the datasets, we performed common quality checks such as:

- Checking for missing values
- Removing duplicate records
- Correcting data types
- Checking for invalid values
- Standardizing text and categorical fields
- Checking identifier uniqueness
- Validating dates and numerical ranges
- Looking for potential outliers
- Checking consistency between related datasets

