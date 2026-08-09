**cleaned_fact_water_samples.ipynb**
---------------------------------------------------------------------------------------------------------------------------------

* Cleaned and prepared the water sample dataset for analysis.
* Explored the main water quality parameters such as pH, turbidity, temperature, and dissolved oxygen
* Analyzed microplastic concentration and particle size across the samples.
* Looked at the different polymer types and microplastic morphologies found in the dataset.
* Compared microplastic levels across different locationsto identify areas with higher contamination.
* Analyzed the different risk levels in the water samples.
* Created visualizations to better understand the patterns and relationships in the data.
* Added a correlation heatmap to see how water quality parameters relate to microplastic concentration.
* Added time-based analysis to observe changes in microplastic levels over time.
* The cleaned dataset and visualizations are now ready for the next stage of the project, including dashboard development and further analysis


------------------------------------------------------------------------------------------------------------------------------------
**weather 
Analysis outcome**

* Rainfall has a strong effect on surface runoff, with a correlation of about 0.93.
* Light rain gives an average runoff of around 1.62.
* Moderate rain increases the average runoff to around 6.87.
* Heavy rain produces much higher runoff, around 19.23 on average.
* The highest recorded runoff is about 23.18.
* Wind speed has very little connection with runoff, with a correlation of only about 0.03.
* This suggests that rainfall is the main weather factor affecting runoff in our dataset.
* More rainfall can lead to more runoff, which may carry microplastics from land into nearby water bodies.
* Overall, heavy rainfall periods may have a higher potential risk of microplastic transport.
-------------------------------------------------------------------------------------------------------------------------------------------------------

Analysis Outcome
* PVC has the highest toxicity score in the dataset, making it one of the most concerning polymers.
* Polystyrene also has a relatively high toxicity score.
* Polypropylene has the lowest toxicity score among the polymers analyzed.
* PVC takes around 1000 years to degrade, which is the longest degradation time in the dataset.
* Polypropylene and Polystyrene take around 500 years to degrade.
* Polyethylene and PET take around 450 years to degrade.
* Polyamide (Nylon) has the shortest degradation time, at around 40 years.
* The scatter plot shows the relationship between toxicity and degradation time for different polymers.
* The results show that some microplastics can remain in the environment for hundreds of years.
* PVC is a major concern because it combines high toxicity with a very long degradation time.
* Overall, identifying the polymer type helps us understand its possible environmental impact and persistence.

   -------------------------------------------------------------------------------------------------------------------------------------------------------


**Analysis Outcome**

* The predicted microplastic count is very close to the actual count.
* The model shows a very strong correlation with the actual microplastic count, around 0.995.
* The average number of microplastic particles in a sample is around 371.
* The average prediction error is around 5%, which shows that the model gives fairly accurate results.
* Samples with higher microplastic counts generally have higher contamination risk scores.
* The contamination risk score has a strong relationship with the actual microplastic count, with a correlation of about 0.994.
* Most predictions have small errors, while only a few samples have noticeably higher errors.
* Out of 1000 samples, 896 were considered normal and 104 were detected as anomalies.
* The model confidence mainly shows how sure the model is about its prediction and does not directly indicate the amount of microplastics.
* Overall, the results show that the system can predict microplastic counts fairly accurately and can also help identify samples with higher contamination risk.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
