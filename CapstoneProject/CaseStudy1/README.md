# Cyclistic: Google Data Analytics Case Study
## By Sean Teams

<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/CyclisticImage.png"
width="600"></center>  
</p>

## Ask
What is our business task? Our director of marketing at Cyclistic beleives that our future success,
as well as profits depends on maximizing the number of annual memberships. We would wish to gain greater
insight as to how we can convert casual members into annual members. After coming to our data driven 
conclusions we should forward our plan to shareholders and executives for approval.
Questions we will attempt to answer in this analysis:
- How do annual members and casual riders use Cyclistic bikes differently?
- Why would casual riders buy Cyclistic annual memberships?
- How can Cyclistic use digital media to influence casual riders to become members? 

## Prepare
The Data we are using for this study is an aggregated dataset from April2021-April2022 of all users in Chicago on 
5,824 bicycles linked to 692 docking stations. All pertinent identifiable information has been removed to
protect the privacy and safety of our customers. Data was downloaded in 12 zip files as CSV. 
Data was cleaned and converted to .xlsx using GoogleSheets.
Raw CSV's can be found here:

https://divvy-tripdata.s3.amazonaws.com/index.html

Converted and saved to .xlsx on GoogleSheets:

https://docs.google.com/spreadsheets/d/17PRkKdoOxplCeMKx-h2xYo883Jlf73SjdkrrpvU0zZs/edit?usp=sharing

Data License Agreement, Motivate International Inc:

https://ride.divvybikes.com/data-license-agreement

## Process
Data was organized under 15 columns(ride ID #, ride type, start/end time, ride length, day of the week
starting point(location,latitude/longitude), ending point(location, latitude/longitude), and member/casual rider.
Duplicate rows were removed, as well as NA or incomplete rows before final analysis. 
New columns for ride length and day of week were added. 

## Analyze
Final analysis was completed in RStudio. RStudio allows us to work on larger datasets, over 212,970 rows. 
The script used for analysis can be found in the directory above.
An initial summary can be seen below:
<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/InitialSummary.jpg?raw=true"
width="600"></center>  
</p>  
Here we can see a mean ride length of 19 minutes with a max of over 4 hours, and most popular day being Saturday(7).
<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/BoxPlotTripDurationByDay.png?raw=true"
width="600"></center>  
</p> 
After cleaning our data, here we can see the ride length quartile distributions of each day as a boxplot with a marked increase on Friday and Saturday.
<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/CasualMemberStartTotals.jpg"</center>  
</p>  
Let's take a look at our member totals.
<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/Deeper.jpg?raw=true"</center>  
</p>  
***Comedic Interlude***
