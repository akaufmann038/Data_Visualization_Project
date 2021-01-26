# Ford GoBike System Data Exploration
## by Alexander Kaufmann


## Dataset

Provide basic information about your dataset in this section. If you selected your own dataset, make sure you note the source of your data and summarize any data wrangling steps that you performed before you started your exploration.

This dataset contains information regarding rides in the ford GoBike system. The dataset has 183412 rows and 17 features per row. Upon exploring the dataset, I noticed that certain feature datatypes needed to be changed in order to create visualizations. I changed user_type and member_gender to categorical type. Additionally, since I was going to be using member_birth_year in my exploration, I decided to create a new column, 'age', to use in place of member_birth_year. Age simply had age values of every member assuming the data was recorded during the year 2010.


## Summary of Findings

Summarize all of your findings from your exploration here, whether you plan on bringing them into your explanatory presentation or not.

In my exploration, I wanted to focus on the duration_sec feature to see its distribution and how other features such as user_type, member_gender, and age affected it. Thus, to begin my exploration, I created a histogram of the duration variable. The visual showed a long tailed distribution, thus I created another visual with duration under a log scale. This portrayed a normal distribution for duration. It was initially clear that duration had a high frequency between 0 and 1000 seconds. As durations increased past this, the frequencies drastically decreased. Next, upon exploring the categorical datatypes, I found that there were far more user_types of subscriber type than customer type and far more male riders than female and riders of 'other' gender. I then plotted age and found a long tailed distribution with a peak in frequency betwen 10 to 35 years old. As the ages increased, the frequency drastically decreased from there.

Next, I looked at the relationship between age and duration and found that the rides with the longest durations were completed by riders between the ages 10 and 50. Due to the alpha value I added to the plot, I could also see that there was a very high concentration of rides completed by riders within the ages 10 and 60 within a range of 10,000 seconds. I wanted to see a more accurate depiction of the concentrated area in the scatter plot, so I depicted age vs duration using a heat map, zooming in on the high frequency area. This shows that there was the highest concentration of rides for riders between the ages 10 and 30 and within a range of 1,000 seconds. This added more clarity to the conclusions I drew from the original scatter plot. Next, I plotted user_type and duration and found that both customer and subscriber had similar distributions. I did the same with member_gender and duration and found similar distributions for female and male riders and a slightly more skewed upwards distribution for riders of 'other' gender. While these plots gave me some insight, I wanted a more precise depiction of the average durations for each categorical variable. Thus, I plotted user_type and duration and member_gender and duration using simple barplots. I found that on average customers had higher duration rides by more than twice as much as subscribers. For gender, I found that on average males and females had similar duration ridess while riders of 'other' gendr had the highest duration rides. I suspect that these differences in averages are due to the outliers with very high durations because all of the violin plot distributions look relatively the same. Then, I plotted user_type and age using a violin plot. I found that customer and subscriber riders had almost the same age distribution. The average age for both customer and subscriber fell in between 20 and 30 years old. I did the same with age and member_gender and found that female and male had similar distributions for age while gender had a slightly different shaped distribution between ages 30 and 50.

Finally, I did some multivariate exploration for the features of interest. When plotting age and duration with color variation for user_type, I found that customers and subscribers had a fairly even amount of high duration runs. The highest duration runs completed by the oldest riders were subscribers while the highest duration runs completed by the youngest riders were mostly customers. Then, I used the same plot with a color sceme for member_gender. I found that most of the high duration runs were completed by males and about half as many were completed by females. The least amount were completed by riders of 'other' gender, and these were concentrated around the age of 20. I plotted the same data using facetgrids and came to the same conclusions.


## Key Insights for Presentation

A main insight I displayed in my presentation was regarding rides of higher durations (20,000 seconds or higher). I found that most of the riders were male within the ages 10 to 40 and there were about half as many female riders in this duration range.

Additionally, I found that the majority of rides were completed by riders within the ages 10 and 35. These rides had a duration of 1000 seconds or less. Outside of these ranges of age and duration, the frequency decreases drastically.
