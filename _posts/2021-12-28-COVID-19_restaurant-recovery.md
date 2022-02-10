---
layout: post
title: "The recovery of U.S Restaurant industry in 2021"
subtitle: "How well the restaurant industry is recovering in 2021 with the impact of COVID-19?"
background: '/img/posts/restaurant_covid/res.jpg'
---
## U.S Restaurant industry of all could be affected by the pandemic the most due to the nature of the industry. It would be interesting to see how well the restaurant industry is recovering from Covid-19, more importantly, what is helping its recovery?


 <br/><br/>

### **Data**

Data of restaurant open for seated dinner is released by OpenTable. It is collected from restaurants of its own platform. The data is starting from Jan 28th, 2020 to  Oct 28th, 2021. Over 50 restaurants are recorded and the result is calculated into a percentage by comparing its year over year comparison. 

For example, of all restaurants that are recorded on OpenTable, the number of restaurants that are open for seated dinner on Jan 28th, 2019 is divided by the number of restaurants that are open for seated dinner on Jan 28th, 2020 and 2021. 0 % means that the same amount of restaurants are open on that day comparing to the same day in 2019. 

### **Findings**

By comparing time series data of restaurant open for seated dinner, COVID-19 positive test cases and vaccination, I am
able to 
- Identify **crucial moments** when the recovery happens in different states.
- Discover that the U.S restaurant industry is **slowly recovering** from the pandemic, but the **impact of it is severe**. 
- **Vaccinations** greatly boost the confidence for owners to reopen but the policy of mask order during the pandemic does not seem to affect the industry significantly.

![U.S restaurant industy in recovery overivew](/img/posts/restaurant_covid/fig_1.png "U.S restaurant overview")

From the figure, the daily test positive cases does not show a dramatic increase, it does indicate that it is the start of the pandemic season. Then at the end of 2020, the restaurant industry is taking another hit while the whole country is experiencing its worst impact. Throughout the whole 2020, the trend of daily positive test cases is **_increasing_** and the trend of restaurants reopen is **_decreasing_**. There is no doubt that the whole industry is **_heavily damaged_** by the virus since the daily open percentage is never even close to what it was in 2019 at any given day in 2020. However, the trend changes in 2021 with **_help of vaccinations_**. By comparing all three line charts, the pandemic has another peak in September but the recovery of the industry is more stable comparing to last year. It could be the reason that more than half of people are vaccinated and are confident that the virus can be under control over the time. 

| 
--- | ---
![California](/img/posts/restaurant_covid/fig_2.png "California") | ![Texas](/img/posts/restaurant_covid/fig_3.png "Texas")

| 
--- | ---
![Nebraska](/img/posts/restaurant_covid/fig_4.png "Nebraska") | ![Rhode Island](/img/posts/restaurant_covid/fig_5.png "Rhode Island")

Considering the difference of population in different states, I have picked two states from **_top 5 most populated states_** that have corresponding restaurant open data and those two are **_California_** and **_Texas_**. I have also picked two states from the **_bottom 5 least populated states_** that have corresponding restaurant open data and those two are **_Nebraska_** and **_Rhode Island_**. All four states’ restaurants open trend comparing to their daily positive test cases. From bar plots of all four graphs, they indicate that population rank is almost the **_same_** as the test positive cases rank. It could mean that more people are in a state, more infected case there is. It could also mean that none of them impose any effective methods to stop the pandemic. 

All four states’ industries suffer a big drop at the start of the pandemic even though positive test cases does not show a drastic increase right away. And during the **_winter in 2020_**, the restaurant industry of all four states are at another bottom. However, having less population seems to have a faster recovery speed for the industry especially during the year of 2020. In 2021, however, four different states show different patterns due to various reasons.  Except California, the other three states show that the restaurant industry is recovering to almost the same level as in 2019, which can be considered to be **_back to normal_**. By having the most population of all  states in the country, **_California_** restaurant industry is still slowly climbing back to the normal stage.

![The mask order](/img/posts/restaurant_covid/fig_6.png "The mask order")

Another potential reason could be **_policy_** imposed by different states. Figure shows **_the difference of vaccination rate and mask order in four different states_**. California, having the most population and the most vaccinated population, is still the slowest for the recovery process; it is also the only state that imposes Mask Order throughout the whole time. It is clear that the vaccination rate in all four states has over 50% and it provides a **_huge boost_** for the restaurant industry. On the other hand, the mask order does not seem to affect the industry recovery at all, rather it shows the state of the pandemic. More importantly, the difference between California and Texas shows that there are some other reasons that delay the restaurant recovery. 

 <br/><br/>

> Python pacakges that are used:
> - pandas
> - matplotlib
> - seaborn
> 
> Python code 

