## Overview
Vizualized trends in Spotify data using Amazon Quicksight. The goal of this project was to familiarize myself with Amazon Quicksight. Amazon QuickSight is a cloud-based business intelligence (BI) tool offered by Amazon Web Services (AWS). It allows users to easily analyze and visualize their data to gain valuable insights. With QuickSight, you can create interactive dashboards, perform ad-hoc analysis, and share insights across your organization. It offers features such as drag-and-drop functionality, integration with various data sources, machine learning-powered insights, and scalability to handle large datasets. Overall, QuickSight simplifies the process of data analysis and empowers users to make data-driven decisions efficiently. For this project I wanted to find out if there was any correlation between the duration of the songs in the top of the year lists provided by spotify and the year that they were popular. In the end, I found that the duration of the songs on average went down as the year progressed. 

## Steps 

### Step 1: Finding Data
I used Kraggle to find the dataset that I would eventually use for this project. I needed a dataset that showed the duration of songs and also the year that they got popular. I eventually settled on Spotify Top Hit Playlist by Joesphine [link](https://www.kaggle.com/datasets/josephinelsy/spotify-top-hit-playlist-2010-2022). 

### Step 2: Uploading Data to an S3 Bucket
Now that we have the data, we need to create an S3 bucket to store the csv so that QuickSight can access it. We also need to have a manifest.json file so that Quicksight knows how to interpret the data. Once we store both of these files we can move onto the next step. 

### Step 3: Using Amazon Quicksight
In order to access the data stored in the S3 bucket we need to give QuickSight permissions to our S3 bucket. Once we have given it permissions, we need to copy our S3 url from our manifest.json S3 file and paste it in when prompted by Amazon QuickSight. Now we can vizualize our data. 

### Step 4: Vizualizing the data
Vizualizing data is very easy in QuickSight because all we have to do is drag and drop the criteria that we want to see into the AutoGraph. In our case, we want the average duration in ms of the song and the date of the song. With that our graph is finished. 

## Graph
![image](https://github.com/sauravnakarmi/Vizualizng-Data-Using-Amazon-Quicksight/assets/70821330/571c65d7-d90c-438d-ac0e-6c9a800790cb)

## Insights
As you can see from the graph provided, there is a clear decline in the duration of what songs become popular throughout the years. This could be related to the decrease in attention span over the past couple of decades that has effected what type of media we consume as a society. We can also see there was a major drop in song duration during 2019, that has perisisted to this day, which is when the pandemic started. 

## Conclusion 
In conclusion, Amazon QuickSight emerges as a highly valuable business intelligence tool, offering unparalleled speed, simplicity, and scalability in data visualization and analytics. Its intuitive interface, coupled with seamless integration with various data sources and AWS services, empowers organizations to derive actionable insights swiftly. By democratizing data analysis and enabling users to create interactive dashboards without the need for extensive training or IT support, QuickSight facilitates informed decision-making across all levels of an enterprise. Moreover, its pay-as-you-go pricing model ensures cost-effectiveness, making it accessible to businesses of all sizes. Overall, Amazon QuickSight stands out as a transformative solution, streamlining the process of data exploration and visualization, and ultimately driving efficiency and innovation within organizations.
