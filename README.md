## Background 
## Motivating Question 
## Data
## Data Cleaning
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

