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
<!-- Comedic Interlude -->
Here we can see very consistent usage of our members with a spike in usage for both casuals and members beginning in June, or more broadly, summer. This trend peaks in July and begins to falloff about ~20% per month to a low in December. Casual riders tend to mostly use our bikes in the summer while our members use the bikes more regularly throughout all months. 
<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/RideByMonthCasualVsMember.png?raw=true"
width="600"></center> 

This is an interesting chart, we can see that Casual members prefer to ride on the weekends, and members ride consistently throughout the week.
We can draw a few assumptions from this data. Casual members ride for leisure and our full subscription users ride to and from work or school as their main source of transportation. We can also see that docked bikes are the preferred mode of transportation for both types of riders.
<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/RideByDay.png?raw=true"
width="600"></center> 

Here we can see monthly totals and bike usage with an overwhelming prefererence for both casuals and members for docked bikes, with peak docked usage in August. We have 0 classic bike usage for May till November. Bike theives, availability, preference, repairs, regulations, data input errors? We would need to investigate and provide more analysis as to why this sudden and sustained dropoff in usage for classic bikes appears, which we are unable to do at the time of this report. Until we do, we are unable to get an accurate comparison between classic and docked bicycles.
<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/RideByMonth.png?raw=true"
width="600"></center> 

On this graph we can see a comparison between ride times of Casuals and Members for each Month. This confirms and strengthens our argument that Casuals use our bikes primarily for leisure on Fridays and Saturdays in the summer, while our Members are primarily using it for routine transportation. The spike in February can be explained by the lack of classic bikes we noticed in our previous graph affecting the overall trend. We can see consistent usage by our members for shorter duration trips(<~20minutes) during all months of the year. While our casuals use the bikes primarily during the summer months and for longer durations(>~30minutes) until the weather begins to cool. 
<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/AverageTripMemberVsCasual.png?raw=true"
width="600"></center> 

## Act
What is to be done? We can make several digital marketing appeals to our potential customers.

(To my prospective employers, these are not my charts, I'm using them to show you my thought process.)
<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/2018-Obesity-Prevalence.png?raw=true"
width="600"></center>

### Appeal to Health: 
Above we can see a discouraging trend, this chart was done pre-covid/'New Normal' sedentary lifestyle. We could make a targetted ad campaign to potential customers in Chicago based around creating a positive emotional state. We can push the positive health benefits of riding a bicycle to stay healthy as well as viewing all the wonderful attractions and fresh air Chicago has to offer. 'Not only will you look good, you will feel good, too!'

<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/LetThemEatBicycles.jpg?raw=true"
width="600"></center>

### Appeal to Emotion:

Gas prices are a non-partisan issue. Look around you, any object that got to where you are by truck, train, boat, or plane. Fuel is one of their main inputs, so when gas prices go up, the cost of everything goes up. Transportation is a must have, not a want, and as gas continues to rise in price we are naturally positioned to gain more and more marketshare. We can appeal to peoples already negative outlook on the issue and remind them, there is a cheaper way. 'Gas prices got you down? Try Cyclistic!'

<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/FedCurrencyInCirculationM1.jpg?raw=true"
width="800"></center>

<p align="center">  
<img src="https://github.com/evilusean/CourseraGoogleDataAnalyst/blob/main/CapstoneProject/CaseStudy1/InflationGetFeducated.jpg?raw=true"
width="600"></center>

### Appeal to Frugality:

Although this may seem counterintuitive to get more customers, we should increase prices. 
Everything is getting more expensive due to the increase in gas prices, people almost expect it at this point.
Since we are already positioned to gain marketshare as prices increase, we should take advantage of this fact.
With an expected 18month lag from policy decision(money printing) until it trickles down to main street, we have our timeframe.
How much? Well, 1.8 trillion in M1 currency supply to 2.2 trillion is an increase of 20%, which is what we can expect to see in inflation. 
What we could do is raise prices in the range of 20-40% while grandfathering any old customers which would increase their brand loyalty.
We could concurrently run an ad campaign offering 20% off for 3 months of a yearly subscription, with the new price. So it will give the appearance of a bargain, whilst increasing our profits and hedging us against future inflation.
We should also consider raising our own employee's salary in the range of 15-25% to compensate, the increased cost of overhead can be offset by our increased prices on new subscribers. This would increase employee morale which would boost our productivity, and loyalty. 

Another option we could employ is offering weekend passes, at a fraction of the cost of a regular subscription. Through our analysis, we have seen that the most popular days are Friday, Saturday, and Sunday. This would help us sign on new formerly casual customers, to a more permanent plan. Obviously we would need to look into availability of bicycles, and see if we have the excess capacity to allow for this. 
