---
layout: post
title: "Can Ridesharing Services Completely Replace Public Transportation?"
subtitle: "Is Uber a complement or substitute service to public ‘L’ ridership in Chicago?"
background: '/img/posts/uber/uber.jpg'
---
<div class="col-lg-8 col-md-10 mx-auto" markdown="1">

In 2018, The Chicago Transit Authority (CTA) reported that bus ridership in the city of Chicago <strong class="uber">decreased by 2.8%</strong> and rail ridership <strong class="uber">decreased by 1.9% </strong>compared to the previous year. 

 We seek to understand whether ridesharing services serve as a complement or a substitute to public transportation in Chicago and what environmental and social factors impact the effects using data from ridesharing rides in Chicago over the course of eight months and daily weather data. 


<h3> Findings </h3>

The model created using the data shows 

- A <strong class="covid">positive significant</strong> relationship between the number of daily ridesharing rides picked up near rail stations with the amount of daily riders on the CTA rail. 

- Ridesharing services can be serving as a <strong class="covid">complement</strong> to public ‘L’ ridership in Chicago.

- On average, there is a <strong class="covid">252877</strong> passenger-increase in L rail ridership during weekdays and there is a <strong class="uber">82288</strong> passenger-decrease in L rail ridership during holidays and weekends.

More imporantly, 
- Cities can further <strong class="covid">encourage these complementary effects</strong> by making ridesharing trips with pick up or drop off public transportation stops tax free rather than adding additional taxes.

- It helps cities understand the effects of ridesharing services on public transportation and how to <strong class="covid">most efficiently structure both systems to maximize the economic and social wellbeing of the city</strong>. 

 ![Train](/img/posts/uber/CTA L Train.png "Train")

 <h3> People </h3>

 > - Catherine Peterson 
 > - Charles Mrkvicka 
 > - Daniel Nesslein
 > - Nick Kang

 <h3> Data </h3>

![Data](/img/posts/uber/data.png "data")

We used ridesharing and transit data from the Chicago Data Portal that was recorded from November 2018 through June 2019 and included details of pickups, dropoffs, and trip lengths. In addition, we analyzed a data set of the daily ridership of the Chicago L rail. 

![comparison](/img/posts/uber/ridersharing_vs_LOL _rail.png "comparison")

From the graph, during late December, we see a large decrease in ridesharing and L rail rides. If ridesharing and the L rail are <strong class="covid">complements</strong>, we assume that most ridesharing pickups near an L rail station are for people getting on or off the L rail. For consumer privacy reasons, our dataset of ridesharing trips classified pickup and dropoff locations into a series of <strong class="covid">census tract points</strong>. We created a <strong class="covid">buffer of 0.005 degrees</strong> (approximately <strong class="covid">500 meters</strong>) around each L rail stop in Chicago and selected the census tract points that intersected with the buffer to distinguish which rides were picked up or dropped off near an L stop.

![zone](/img/posts/uber/pickup_dropoff.png "zone")

These trips are of interest to our model because if ridesharing serves as a complement to public transportation, <strong class="covid">people will get picked up near an L stop to be taken to their final destination. Additional pickups within the buffer should thus increase public transportation ridership</strong>.

We conrtsucted a regression model and the main purpose is to test the hypothesis whether ridesharing service is a complemnet to public transportation. By analyzing the effect of ridesharing pickups near L stations, we see that these ridesharing rides have a <strong class="covid">positive effect</strong>on daily L ridership, explaining that ridesharing services serve as a <strong class="covid">complement</strong> to the L rail. 

Other social and economic variables not included in our model could further explain the effects in the future such as population, unemployment rate, and costs of owning a car including gas, parking, and insurance. Our model was further limited due to the dataset using census tract points rather than exact coordinates. Using exact coordinates would allow the model to use a more accurate count of rides located near L stops. We also acknowledge that our model includes only 242 days of a single year which may explain why we were able to create a model with such a high adjusted R-squared. 

</div>



