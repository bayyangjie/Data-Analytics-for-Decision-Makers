This analytics project focuses on understanding the booking habits of users on the Tripadvisor platform and to also bridge a link to users’ demographic information. It employs different analytical techniques in achieving the objectives of the analysis from visualizations to predictive analytics. In addition, it also emphasizes on data management and cleaning to ensure cleaned data is being used as input for achieving an accurate analysis output.

Visualization/Clustering
1. Tripadvisor can identify the number of bookings for the different periods of the year to understand which parts of the year have high demand for hotel bookings
2. Distribution of count of total hotel reviews by month
3. Distribution of member years on Tripadvisor to understand the spread of membership years of existing customers
4. Determine which hotel features contributes to a high star rating ( >=4)

Predictive: Using C&R tree method
1. What is the likely chance of a hotel receiving a 5 star rating ?

Techniques that could be employed
- Creating visualization plots: Bar charts were used to analyze the distribution in the variables required for the objectives mentioned earlier. 
- Clustering: The purpose of the clustering is to group similar data points. With specific data points clusters formed, the company can then focus on the specific characteristics of each cluster for targeted or personalized advertisements. 
- Predictive modelling: The specific tool used would be the C&R decision tree which is used to make predictions based on the values of input variables by splitting the dataset into training and testing data. 

Objective #1: Tripadvisor can identify the number of bookings for the different periods of the year to understand which parts of the year have high demand for hotel bookings
The barplot created shows the total booking counts for each quarter of the year. From the plot, we can see that overall, the difference in count of bookings for each quarter appears to be quite small. The first quarter of the year (Mar-May) has the highest number of bookings at 128 while the last quarter of the year (Dec-Feb) has the lowest at 124. Additionally, based on the cluster matrix table below, not only does it show that total bookings is the highest for period of Mar-May but the number of bookings is also higher during that period for each individual cluster.

Data Understanding/Treatment:
The variables are a mixed of different data types with categorical and numerical values. The roles are set as ‘input’ for all the fields as all the variables are used as inputs for making predictions/learning patterns
![Image 1](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%201.png)

Data values misalignment:
- In the columns from ‘Nr.rooms’ to the last column, it was found that the columns were shifted to the right by one column resulting in misalignment of the data to the correct column labels. Thus, also resulting in an extra column created at the end. There were a total of 96 affected rows in each of the affected column bringing the total affected cells to 576 as shown below. During verification of the data in the var.file node, it also shows that ‘User continent’ has incorrect values displayed, which further prompted further checking of the dataset.

Excel was used to shift the columns back into place so that the data values correspond with the appropriate column label as shown below. There are also no more unknown values that exist in the last column which was deleted thereafter.
Invalid values found in ‘User continent’ column:
![Image 2](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%202.png)

Before modifying dataset alignment in excel:
![Image 3](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%203.png)

After modifying dataset alignment in excel:
![Image 4](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%204.png)

Illogical values:
- As shown in the python .describe() output of ‘Member years’, there is an illogical value of ‘-1806’ which does not makes sense to the data. Since it happens only one specific row, it was removed from the dataset.

- Data audit below also shows the illogical value of ‘-1806’ in ‘Member years’ column as the minimum value.
![Image 7](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%207.png)

Before
![Image 5](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%205.png)

After
![Image 6](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%206.png)

Check for missing/NULL values:
Data audit shows no NULL or missing values in the dataset.
![Image 8](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/tree/main/Pictures#:~:text=1%20minute%20ago-,Picture%208.png,-Add%20files%20via)

Outliers:
The number of outliers for the respective columns shown below are very few and quite insignificant as compared to the total number of records of 504.
![Image 9](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%209.png)


1c)
As mentioned previously, clustering was performed and the dataset is categorized into 3 clusters of data points as shown below. Based on the description of the clusters, most of the records are in cluster 2 which makes up 71.4% of the entire dataset. Clustering quality as shown by the silhouette score is at a fair level. 
![Image 10](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%2010.png)


Visualization/Clustering
Objective #1: Tripadvisor can identify the number of bookings for the different periods of the year to understand which parts of the year have high demand for hotel bookings
The barplot created shows the total booking counts for each quarter of the year. From the plot, we can see that overall, the difference in count of bookings for each quarter appears to be quite small. The first quarter of the year (Mar-May) has the highest number of bookings at 128 while the last quarter of the year (Dec-Feb) has the lowest at 124. Additionally, based on the cluster matrix table below, not only does it show that total bookings is the highest for period of Mar-May but the number of bookings is also higher during that period for each individual cluster.

Cluster matrix:
![Image 11](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%2011.png)

![Image 12](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%2012.png)

Objective #2: Distribution of count of total hotel reviews by month
The distribution plot shown below displays the spread of total hotel reviews submitted by month. It shows that September has the highest count of hotel reviews followed by August. October has the lowest count of hotel reviews submitted.
 
![Image 13](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%2013.png)

Objective #3: Distribution of member years on Tripadvisor to understand the spread of membership years of existing customers
 
From the distribution plot, we can see that majority of customers (299) have been members with Tripadvisor around the range of 1 to 5 years. Only 1 customer has the highest membership years of 13. The company could place more focus on the majority group of customers by keeping them updated with the latest or new membership programs/benefits. This is to encourage them to extend their membership once it expires.

 ![Image 14](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%2014.png)

Objective #4: Determine which hotel features contribute to a high star rating ( >=4)
From the KMeans clustering output below, only hotels in cluster 2 have a star rating of 4 and above. There are some features that hotels in this cluster have that leads to a higher star rating. Firstly, as shown in the image below, hotels in cluster 2 have spa facilities while hotels in the other 2 clusters do not have.

Secondly, the number of rooms in the hotel could also play a part in the star rating of the hotel. As shown in the bottom image, hotels in clusters 2 have over 2600 rooms. Having more rooms to accommodate more bookings can means that more guests are able to book the hotel which can also lead to a higher chance of obtaining good star ratings too.
 
Contributing factors for lowest star rating of hotels in cluster 3:
Hotels in cluster 3 have the lowest star rating but this could be due to the absence of a casino, a facility/feature that hotels in the other two clusters have. A casino is a popular place for tourists, thus the benefits of having it can greatly affect a hotel’s rating. Although hotels in cluster 3 do have a tennis court, but it may not be appealing enough to garner higher ratings. This could also be due to the observation that most traveller types in this cluster as well as the entire dataset are couples, most might prefer to explore other types of facilities that the hotel has to offer.

 ![Image 15](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%2015.png)

                 
Predictive modelling
Objective: What is the likely chance of a hotel receiving a 5 star rating ?
The C&R tree can be used to determine what is the likely chance of a hotel receiving a 5 star rating based on the input of the other contributing factors.
Based on the C&R tree, the predictor importance shows that whether a hotel has a swimming pool or not has the greatest influence on the hotel star rating while the availability of a gym in a hotel has the lowest significance on the hotel star rating.

 ![Image 16](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%2016.png)

Here, the C&R decision tree is used to make a prediction on the hotel star rating based on the input of the different hotel features. The C&R tree map was plotted to determine which combination of the relevant input variables would produce the highest star rating for a hotel. The input variables used for plotting the tree are pool, gym, tennis court, spa, casino, free internet, number of rooms, user country and score. The algorithm used in the tree automatically discarded the variables that do not contribute significantly to improving the predictive accuracy. The final input variables used by the algorithm are number of rooms, gym, pool score and user country. The snapshots below show the flow in the decision tree.
 
![Image 17](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%2017.png)

![Image 18](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/blob/main/Pictures/Picture%2018.png)

Based on the tree diagram shown above, the prediction shows that in order for a hotel to receive a 5-star rating, the combination of feature characteristics that a hotel should have are as follows:
- a pool
- more than 1255 rooms (more than 4004 rooms OR total rooms must be at least between 3014 and or equals to 3957)

Discussion/Evaluation and Conclusion
Key pattern:

One key pattern observed is that number of rooms that a hotel has and having a pool are two factors that play a big part in the star rating of the hotel. This can be supported by observations from both the clustering output whereby hotels in cluster 2 that have the most rooms have the highest star ratings and the C&R tree chart where the hotels with 5-star ratings fall under the splitted path of ‘Pool=YES’ and room count of 3000 to 4000.

Limitations of analysis:

One limitation of the analysis is the relatively small sample size, which may impact the precision of the results. To enhance the analysis, more data could be collected from similar sources or expanding the dataset to include a broader population.
Another limitation of the analysis is the variety of hotel features listed. There are many other hotel features that could be considered which could affect the outcome of the hotel star rating. In this analysis, only specific features were considered. Thus, if a wider field of features could be utilised, a more accurate analysis could be achieved.
One such method to increase the collection and variety of data could be through the use of API calls whereby real time data can be extracted from the booking platform’s database to retrieve the additional data required for analysis.

Conclusion:

In conclusion, this study has shed light on the booking habits of users such as the frequent travelling periods of the year and hotel features that are of importance to users when booking. The clustering analysis provided valuable insights into the characteristics of the different clusters of data points, thereby providing a better understanding of the dataset as a whole. Through this analysis, Tripadvisor would be better able to recommend suitable hotels to users and bring about increased user traffic as well as membership rates on the platform.
![image](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/assets/153354426/ea3f2223-e9f6-4577-a793-fbb49d588595)



















