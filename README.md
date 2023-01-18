# FarmLink-RFM-Analysis
A customer segmentation/regression analysis using the RFM (Recency, Frequency, Monetary) model to determine if more donations can be earned based on the types of emails sent to different types of customers.

Credits to Andrew Kim, Manas Chithirala, Pulak Dugar, and Hailey Holcomb for this project.

## Step 1: Loading Datasets/Cleaning Data/Creating Variables
Using Deepnote, we uploaded the email list data received from FarmLink. We then added variables and generally cleaned up some inconsistencies before going in depth.

## Step 2: Creating the RFM Scale
Using the columns "Clicks" for Frequency, "lastgiftdate" for Recency, and "lifetodategiving" for Monetary, we created a 1-5 scale (1 being the worst and 5 being the best/highest priority customer) based on percentile groupings to categorize each person (note that Recency also has a 0 for the scale, due to the fact that customers who did not donate are also included in the data). The most important thing here is coding for reproducibility, in the event that future data is added.

## Step 3: RFM Categorization
Using the previously created scales, merge them into a full RFM and categorize each person based on their new 3 digit number in the column 'RFM'. Details of this categorization included in the main file.

## Step 4: Visualizations
Before going into analysis, we visualized the clusters in a 3D scatter plot and a 2D scatter plot (using K-means clustering). 

## Step 5: Regression modeling
Using the newly created customer segmented data, we created a clustered regression analysis to see whether there was some correlation between the number of times the donation button was clicked and the amount donated.

## Conclusion
In the end, using the data given, we concluded that there is not much benefit to specifying email type based on the type of customer. There is room for improvement in modeling, but is probably not productive given the current state of data. With more data, it may be possible to make this customer segmentation more useful.
