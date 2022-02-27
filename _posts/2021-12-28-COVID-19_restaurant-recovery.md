---
layout: post
title: "The Recovery of U.S Restaurant Industry In 2021"
subtitle: "How well the restaurant industry is recovering in 2021 with the impact of COVID-19?"
background: '/img/posts/restaurant_covid/res.jpg'
---
<div class="col-lg-8 col-md-10 mx-auto" markdown="1">
U.S Restaurant industry of all could be affected by the pandemic the most due to the nature of the industry. It would be interesting to see how well the restaurant industry is recovering from Covid-19, more importantly, what is helping its recovery?


### **Data**

Data of restaurant open for seated dinner is released by OpenTable. It is collected from restaurants of its own platform. The data is starting from Jan 28th, 2020 to  Oct 28th, 2021. Over 50 restaurants are recorded and the result is calculated into a percentage by comparing its year over year comparison. 

For example, of all restaurants that are recorded on OpenTable, the number of restaurants that are open for seated dinner on Jan 28th, 2019 is divided by the number of restaurants that are open for seated dinner on Jan 28th, 2020 and 2021. 0 % means that the same amount of restaurants are open on that day comparing to the same day in 2019. 

### **Findings**

By comparing time series data of restaurant open for seated dinner, COVID-19 positive test cases and vaccination, I am
able to 
- Identify <strong class="covid">crucial moments</strong> when the recovery happens in different states.

- Discover that the U.S restaurant industry is <strong class="covid">slowly recovering </strong> from the pandemic, but the <strong class="covid"> impact of it is severe</strong>. 

- <strong class="covid">Vaccinations</strong> greatly boost the confidence for owners to reopen but the policy of mask order during the pandemic does not seem to affect the industry significantly.

![U.S restaurant industy in recovery overivew](/img/posts/restaurant_covid/fig_1.png "U.S restaurant overview")

From the figure, the daily test positive cases does not show a dramatic increase, it does indicate that it is the start of the pandemic season. Then at the end of 2020, the restaurant industry is taking another hit while the whole country is experiencing its worst impact. Throughout the whole 2020, the trend of daily positive test cases is <strong class="covid">increasing</strong> and the trend of restaurants reopen is <strong class="uber">decreasing</strong>. There is no doubt that the whole industry is <strong class="covid">heavily damaged</strong> by the virus since the daily open percentage is never even close to what it was in 2019 at any given day in 2020. However, the trend changes in 2021 with <strong class="covid">help of vaccinations</strong>. By comparing all three line charts, the pandemic has another peak in September but the recovery of the industry is more stable comparing to last year. It could be the reason that more than half of people are vaccinated and are confident that the virus can be under control over the time. 
</div>
<div class="col-md-6 smallimg" markdown="1">
![California](/img/posts/restaurant_covid/fig_2.png "California")
</div>
<div class="col-md-6 smallimg" markdown="1">
![Texas](/img/posts/restaurant_covid/fig_3.png "Texas")
</div>
<div class="col-lg-8 col-md-10 mx-auto">
<p>
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
    View Code Snippets
  </button>
</p>
<div class="collapse" id="collapseExample">
  <div class="card card-body" markdown="1">
    ```
    # California
    fig = plt.figure(figsize=(30,18))

    spec = gridspec.GridSpec(ncols=2, nrows=2, width_ratios=[7,1], wspace=0.001,hspace=0.05)
    ax0 = fig.add_subplot(spec[0])
    ax1 = fig.add_subplot(spec[1])
    ax2 = fig.add_subplot(spec[2])
    ax3 = fig.add_subplot(spec[3])

    y = p_t5['population']/1000000
    y1 = [covid_tc.loc['2021/10/28']['California']/1000000,covid_tc.loc['2021/10/28']['Texas']/1000000
    ,covid_tc.loc['2021/10/28']['Florida']/1000000, covid_tc.loc['2021/10/28']['Illinois']/1000000
      ,covid_tc.loc['2021/10/28']['Georgia']/1000000]

    for state in top_5_tc:
      s = top_5_tc[0]
      ax0.plot(res.index, res[state],color='dimgrey', linewidth=1)
      ax0.plot(res.index, res[s],color='crimson', linewidth=3.5)
      ax0.axhline(y=0, color='crimson', alpha = 0.5, linewidth=5, linestyle = ':') 
      ax0.text('2020/5/5', 100 , 'California',
           fontsize=25,color= 'crimson',  weight='bold')
      ax0.text('2020/5/5', 85 , 'Daily Restaurants open for reservations',
           fontsize=15,color= 'dimgrey',  weight='bold')
      ax0.text('2020/5/5', 75 , 'percentage comparing to 2019',
           fontsize=15,color= 'dimgrey',  weight='bold')
      ax0.text('2020/1/15', 5 , '0%', fontsize=20 ,color= 'dimgrey', weight='bold')
      ax0.text('2021/9/1', 100 , 'Population:', fontsize=20 ,color= 'dimgrey', weight='bold')
      ax0.text('2021/9/1', 90 , '37,254,519', fontsize=20 ,color= 'crimson', weight='bold')
      ax1.barh(p_t5.index,p_t5['population']/1000000, color='darkgrey')
      ax1.barh(s,p_t5.loc[s][0]/1000000, color='crimson')
      ax2.plot(covid_nc.index, covid_nc[state],color='dimgrey' , linewidth=1)
      ax2.plot(covid_nc.index, covid_nc[s],color='crimson' , linewidth=3.5) 
      ax2.text('2020/5/5', 60000 , 'Daily Covid Confirmed Positive Test',
           fontsize=18,color= 'dimgrey',  weight='bold')
      ax2.text('2021/6/10', 60000 , 'Total Confirmed Positive Test:',
         fontsize=20,color= 'dimgrey',  weight='bold')
      ax2.text('2021/8/15', 57000 , '4,885,289',
           fontsize=20,color= 'crimson',  weight='bold')
      ax3.barh(state,covid_tc[state]/1000000, color='darkgrey')
      ax3.barh(s,covid_tc[s]/1000000, color='crimson')
    
    for a in [ax0, ax1, ax2, ax3]:
    
      a.spines['top'].set_visible(False)
      a.spines['right'].set_visible(False)
      a.spines['bottom'].set_visible(False)
      a.spines['left'].set_visible(False)
      a.set_yticks([])
      a.xaxis.set_major_locator(mdates.MonthLocator())
    
    for i, v in enumerate(y):
      ax1.text(v , i, r_t5[i], color='white', fontweight='bold', fontsize=13, ha='right', va='center')

    for i, v in enumerate(y1):
      ax3.text(v , i, top_5_tc[i] , color='white', fontweight='bold', fontsize=13, ha='right', va='center')
    
    ax0.axvspan(dt.date(2020, 3, 1), dt.date(2020, 5, 1), facecolor='crimson', alpha=0.2)
    ax0.axvspan(dt.date(2020, 11, 1), dt.date(2021, 3, 1), facecolor='crimson', alpha=0.2)
    ax2.axvspan(dt.date(2020, 3, 1), dt.date(2020, 5, 1), facecolor='crimson', alpha=0.2)   
    ax2.axvspan(dt.date(2020, 11, 1), dt.date(2021, 3, 1), facecolor='crimson', alpha=0.2)

    plt.savefig('fig_2.png')
    plt.show()
    ```
  </div>
</div>
</div>
<div class="col-md-6 smallimg" markdown="1">
![Nebraska](/img/posts/restaurant_covid/fig_4.png "Nebraska")
</div>
<div class="col-md-6 smallimg" markdown="1">
![Rhode Island](/img/posts/restaurant_covid/fig_5.png "Rhode Island")
</div>

<div class="col-lg-8 col-md-10 mx-auto" markdown="1">
Considering the difference of population in different states, I have picked two states from <strong class="covid">top 5 most populated states</strong> that have corresponding restaurant open data and those two are <strong class="covid">California</strong> and <strong class="covid">Texas</strong>. I have also picked two states from the <strong class="uber">bottom 5 least populated states</strong> that have corresponding restaurant open data and those two are <strong class="uber">Nebraska</strong> and <strong class="uber">Rhode Island</strong>. All four states’ restaurants open trend comparing to their daily positive test cases. From bar plots of all four graphs, they indicate that population rank is almost the <strong class="covid">same</strong> as the test positive cases rank. It could mean that more people are in a state, more infected case there is. It could also mean that none of them impose any effective methods to stop the pandemic. 

All four states’ industries suffer a big drop at the start of the pandemic even though positive test cases does not show a drastic increase right away. And during the <strong class="covid">winter in 2020</strong>, the restaurant industry of all four states are at another bottom. However, having less population seems to have a faster recovery speed for the industry especially during the year of 2020. In 2021, however, four different states show different patterns due to various reasons.  Except California, the other three states show that the restaurant industry is recovering to almost the same level as in 2019, which can be considered to be <strong class="covid">back to normal</strong>. By having the most population of all  states in the country, <strong class="covid">California</strong> restaurant industry is still slowly climbing back to the normal stage.

![The mask order](/img/posts/restaurant_covid/fig_6.png "The mask order")

Another potential reason could be <strong class="policy">policy</strong> imposed by different states. Figure shows<strong class="covid"> the difference of vaccination rate and mask order in four different states</strong>. California, having the most population and the most vaccinated population, is still the slowest for the recovery process; it is also the only state that imposes Mask Order throughout the whole time. It is clear that the vaccination rate in all four states has over 50% and it provides a <strong class="covid"> huge boost</strong> for the restaurant industry. On the other hand, the mask order does not seem to affect the industry recovery at all, rather it shows the state of the pandemic. More importantly, the difference between California and Texas shows that there are some other reasons that delay the restaurant recovery. 

 <br/><br/>
 

> Python pacakges that are used:
> - pandas
> - matplotlib
> - seaborn
> 
> <a href="/pdf/project_python_code.pdf" target="_blank">Python code</a>
</div>



