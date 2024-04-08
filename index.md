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
![image](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/assets/153354426/9f103f4b-d85f-4829-b4e3-d670afbd95ee)

After modifying dataset alignment in excel:
![image](https://github.com/bayyangjie/Data-Analytics-for-Decision-Makers/assets/153354426/b6346f4a-b9a1-47cd-b708-a1d2590f7f62)





