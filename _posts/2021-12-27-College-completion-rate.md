---
layout: post
title: "How Long Does It Take To Finish College?"
subtitle: "An inspection on what factors will affect college completion rate "
background: '/img/posts/college/uw.jpg'
thumbnail: '/img/posts/college/hist2.jpg '
---
<div class="col-lg-8 col-md-10 mx-auto" markdown="1">

 College completion rate is tied to multiple factors and it is related more to my personal life since I am in my last academic year for master degree studying. I will inspect **gender, family income, race, tuition fee and SAT,ACT score** as if they would affect college completion rate.

<h3> Findings </h3>

 The linear regression model shows that 

 - <strong class="covid">Tuition fee</strong> is postively correlated with college completion rate.

 - <strong class="covid">SAT/ACT score</strong> is postively correlated with college completion rate. 
 
 -  <strong class="covid">Alien</strong> of all race categories has the highest college completion rate.

 <h3> Data  </h3>

 I am able to retrieve the data from College Scorecard University/College level data about school and its student cohorts and I mainly focus on the latest dataset which is from 2016 to 2017.

![map](/img/posts/college/output_3_1.png "map") 
![histogram](/img/posts/college/output_4_0.png "histogram")
![distribution](/img/posts/college/his_1.jpg "distribution")

There is a huge difference between different states and the range is from 0 to 700.  <strong class="covid">California</strong> contains the most numbers of institutions in the whole country. However, it is hard to compare the difference between the majority of the states. The distribution of institutions are not even,  <strong class="covid">majority of the states</strong> only have less than or about 200 institutions.  <strong class="covid">6 states</strong> have more than 300 institutions. And among them, state of California has around 700. 

![SAT](/img/posts/college/line_2.jpg "SAT")

And the test score reflects on the academic ability that a student is capable of. Thus, a student having a higher test score, student will likely to perform well in the college level. According to the graph, the correlation between the two is really high. It indicates that when a student has a higher SAT score, he will be likely to have a higher score in ACT as well. 

![Race](/img/posts/college/his2.jpg "Race")

In order to show the comparison more clear between four cohorts. State of Massachusetts and state of Rhode Islands are chosen to be on the graph. Since these two states have relatively the highest completion rate in all groups comparing to other states. And it shows that <strong class="covid">alien</strong> and<strong class="covid"> white</strong> cohorts have the higher completion rate.

![Tuition](/img/posts/college/hist2.jpg "Tuition")

The graph shows a high linear correlation between the two. But surprisingly, it shows a positive correlation which can be interpreted as the higher the tuition fee is, the higher college completion rate the state will have. It would be strange because if the tuition fee is high, less people will be able to afford it, thus less completion rate due to this reason. Some further analysis is needed from the linear regression.

Last but not least, the regression model is tested and the R square of the model is 69.3 percent and it means that these regressors could represent almost <strong class="covid">70% </strong>of the dependent variable. 

The p value for average SAT score is 0.751, which is larger than 0.05 and it might not be a suitable independent variable for completion rate. It might due to the reason that SAT score illustrates the ability prior to college and individual could change a lot during the 4 years of development. Therefore, the SAT score is not really helpful for the model. 

However, all the other regressors are <strong class="covid">significant</strong>. The coefficient for tuition is positive and it might be the reason that a higher tuition fee is due to the quality of the college; it might select the students who are already more suitable to embrace the more intense competition. And the dummy variables show that alien cohort, comparing to white cohort, aliens will have a higher completion rate and black cohort as well as unknow cohort will have a lower completion rate comparing to the white cohort.

<br/><br/>

> Python pacakges that are used:
> - pandas
> - matplotlib
> - seaborn
> 
> <a href="/pdf/store.pdf" target="_blank">Python code</a>
</div>






