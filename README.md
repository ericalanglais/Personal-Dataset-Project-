## Motivation
The question I wanted to explore was how hospital admissions varied across New York State. I decided to answer this question at the county-wide level, specifically those in the Upper and Mid-Hudson region valley: Dutchess, Orange, Putnam, Rockland, Ulster, and Westchester County. 
## Data 
To answer my question, I used the dataset "Hospital Inpatient Discharges (SPARCS De-Identified): Adult Prevention Quality Indicators (PQI) by County: Beginning 2009" from the New York State's Health Data website. I also paired this data with census data in R's package tidycensus. Because of the rates of admission had decimal points in them, they were treated as a character data type by R. I converted both rate observed and expected rate columns to integers, and then filtered out the NA values. Then, I filtered the data to keep only the rows that had the counties I wanted to look at, which were Dutchess, Orange, Putnam, Rockland, Ulster, and Westchester. Next, some entries had inconsistent capitalization of PQIs that led to R treating them as different types of admissions, so I made the data consistent by changing all instances of the words "Short-Term" and "Long-Term" to "Short-term" and "Long-term", respectively. Additionally, I changed the PQI name from "Chronic Obstructive Pulmonary Disease (COPD) or Asthma in Older Adults" to the shorter "COPD or Asthma in Older Adults." Lastly, I created a new column called "Prediction.Error" that subtracted the expected rate from the observed rate. 
## Prevention Quality Indicator 
<img width="1400" height="865" alt="image" src="https://github.com/user-attachments/assets/3ac27316-3830-4cda-ba6c-6d285ba0b009" />
&nbsp;
The first graph I created was a scatterplot of observed vs expected number of hospital admissions per 100,000 people across all conditions, which showed a very strong, linear  relationship.
I fit a linear model to the data, and the resulting equation was Predicted Observed Rate = 2.631606 + 0.897179 * Expected Rate, with an R-squared value of 0.9208, further verifying that there
is a good match between expected outcomes and observed outcomes. I noticed that certain counties seemed to have different trends --- counties like Ulster and Orange seem to have higher observed
rates compared to their expected, while counties like Putnam and Rockland seemed to have lower observed rates compared to their expected rates. Whether or not this disparity has anything to do
with median income is a question that lead me to do additional analysis, which I will upload at for the final submission! Along with the county difference, I noticed two different "groupings", 
so I plotted the same information with the colors being the specific conditions instead.

&nbsp;
<img width="1400" height="865" alt="image" src="https://github.com/user-attachments/assets/0ffc32b5-a2cb-4433-a03d-e8b2afdc62ee" />
&nbsp;
Because of the number of unique conditions, as well as the length of their names, this graph was messy. However, what I took away was that most of the points on the right forming a clump were
composite scores, which made sense that these numbers would be higher because they compiled, for example, all rates for chronic conditions. 

