---
title:  "Sleep - 2020"
linktitle:  "Sleep - 2020"
date:   2021-01-20
categories: ["Statistics"]
tags: ["data science"]
---

| {{< image
    src="/img/sleep2020_4.png"
    alt="sleep" >}} | 
|:--:| 
| *My sleep time (in minutes) over the year 2020* |



## Context

2020 was a long year. One of the habits I paid some attention in this year was to measure/improve my sleep quality. Sleeping is a key part of our life, important for recharging your mind, form long lasting memories and learning overall. According to recent research[^fn2]:

> The mechanisms underlying the intimate connection between sleep and learning are becoming increasingly clear. By detoxifying the brain, replenishing metabolites, and homeostatically rescaling synaptic weights, prelearning sleep enables the acquisition of new memories during subsequent waking. 

Even though research clearly indicates the importance of good sleep, for both quality of life and productivity, there's still part of the tech community that glorifies sleep deprivation, crunching long hours programming with not enough sleep, and still prides themselves for adopting such erratic behavior. Research experiments even indicate that sleep deprivation cut developers productivity by half[^fn1], but it's still common to see posts of developers glorifying low sleep time (as if it were a personal quality), and it's something a lot of people ignore until it becomes a real problem, for example a cross-sectional study[^fn3] concluded that:

> (...) fluctuating amounts of sleep and irregular bedtimes and wake-up times, put people at an increased risk for obesity, high cholesterol, high blood pressure, high blood sugar, and other health problems. And for each hour of sleep variability, these risks went up by as much as 27 percent.

For these and other reasons in 2020 I started to monitor and collect data about my sleep patterns, with the help of the Mi Band 4 that keeps track of my sleep. It's difficult to know exactly how your sleep pattern relates to the "recommended" if you don't have any data to compare it against. In the Mi Band you can, thanks to GDPR, export all your data in CSV format, filtering by time of measurement. Sure, Mi Band has an app that shows some of this information, but I was curious and wanted to perform a deeper analysis than the one provided by the app. Hopefully in the end of 2021 I re-run this analysis and compare how my sleep behavior changed from one year to another.

## Measurements

The data collected is about daily sleep, so in the exported CSV I have information regarding the hour I started to sleep, the hour I woke up and the total sleep time. Enough to say that the measurements aren't perfect (measurement error can still occur), and there's some period when I didn't had any sleep data:

- September 2020: No sleep data was collected in this period. IIRC it was because I lost the charging dock of the Mi Band (but found later after some time);
- December 2020: In the middle of the month my wristband broke, so I couldn't use the Mi Band while I was waiting for a new wristband I bought to arrive, but this happened only on January 2021.

Here are the counts by each month of 2020. One can see that there's no month number 9 (September) and December measurements is only half of the total amount of days in the month. Except these two months I got decent and consistent measurements throughout the rest of the year.
{{< image
    src="/img/sleep2020_2.png"
    alt="sleep" >}}


## Sleep Time

The amount of sleep we need differs depending on your age and other personal factors (some people need less sleep time, some more). Taking my age into account, according to the Journal of the National Sleep Foundation[^fn4] adults sleep range (ages 18 to 64) is 7-9 hours of sleep.

I first checked my sleep time distribution, shown here in minutes slept instead of hours:

{{< image
    src="/img/sleep2020_1.png"
    alt="sleep" >}}

The first thing I noticed was the distribution had a peak in the 0 minutes slept point, which doesn't make a lot of sense. I attributed this to measurement errors in the Mi Band 4 and removed them from the dataset to not pollute the rest of the analysis. Next thing I did was to calculate my 2020 average sleep time:

```python
avg_in_hours = df.total_hours_slept.dt.total_seconds().mean()/60/60
minute_part = (avg_in_hours % 1)*60
print(f"2020 Average Sleep time: {str(int(avg_in_hours))}h:{str(int(minute_part))}m")
```

> 2020 Average Sleep time: 7h:44m

Which is a pretty good number. My objective is to have at least 7 hours of sleep, but the goal is to sleep 7 hours and 30 minutes each night. However I felt this number might've been skewed by specific sleep behaviors I have, and investigated the top days of sleep time (where I've slept the most) and bottom days of sleep times.

The top 5 sleep times:

| date                | weekday   | start               | stop                | total_hours_slept   |
|:--------------------|:----------|:--------------------|:--------------------|:--------------------|
| 2020-01-19 00:00:00 | Sunday    | 2020-01-18 21:59:00 | 2020-01-19 10:56:00 | 0 days 12:57:00     |
| 2020-07-12 00:00:00 | Sunday    | 2020-07-11 22:51:00 | 2020-07-12 11:28:00 | 0 days 12:37:00     |
| 2020-01-11 00:00:00 | Saturday  | 2020-01-11 00:23:00 | 2020-01-11 12:49:00 | 0 days 12:26:00     |
| 2020-01-12 00:00:00 | Sunday    | 2020-01-11 23:05:00 | 2020-01-12 11:14:00 | 0 days 12:09:00     |
| 2020-02-24 00:00:00 | Monday    | 2020-02-23 23:07:00 | 2020-02-24 10:59:00 | 0 days 11:52:00     |

Wow, I almost slept 13 hours in a single day! 🧐 But the pattern here is clear: most of these top days are either Saturday or Sunday, indicative that I sleep more on the weekends (and I can personally confirm this hypothesis).

The bottom 5 sleep times:

| date                | weekday   | start               | stop                | total_hours_slept   |
|:--------------------|:----------|:--------------------|:--------------------|:--------------------|
| 2020-03-29 00:00:00 | Sunday    | 2020-03-28 23:20:00 | 2020-03-29 02:45:00 | 0 days 03:25:00     |
| 2020-01-18 00:00:00 | Saturday  | 2020-01-18 04:19:00 | 2020-01-18 08:09:00 | 0 days 03:50:00     |
| 2020-07-07 00:00:00 | Tuesday   | 2020-07-06 23:51:00 | 2020-07-07 04:19:00 | 0 days 04:28:00     |
| 2020-11-02 00:00:00 | Monday    | 2020-11-02 00:22:00 | 2020-11-02 05:07:00 | 0 days 04:45:00     |
| 2020-01-13 00:00:00 | Monday    | 2020-01-13 01:47:00 | 2020-01-13 07:06:00 | 0 days 05:19:00     |

Some of the data in the bottom sleep times is a little bit strange. For example the first row indicates I started sleeping at 23h10 but woke up at 2h45 in the morning, and didn't went back to sleep. I don't remember being awake from 2 in the morning and don't going back to sleep, either I have a bad memory of this event or is another measurement error. The other bottom sleep time measurements make more sense, even though I can't find a clear pattern here.

I investigated further the sleep time distribution  per day of the week, measured in total minutes slept (7 hours = 420 minutes):

{{< image
    src="/img/sleep2020_3.png"
    alt="sleep" >}}

And the pattern here is very clear. There's an evident difference of sleep time in Saturday and Sunday (which the top sleep time weekdays were indicating): I usually sleep much more on the weekends than on the usual business days. I've read some articles that suggest that having different sleep patterns for different days isn't good, so it's something I should pay attention this following year.  In the business days the sleep schedule is more uniform, and I also couldn't find any meaningful monthly pattern.


## Sleep Hours

I wanted to analyze when I usually go to sleep and at which time I wake up. Before I dive into the numbers themselves, I'll digress a little about how to actually get these average values of sleep times.

### Mean of Circular Quantities

How would you calculate the average hour a task starts? The usual (arithmetic) mean won't give you plausible results, because hours of the day are *circular*. After 23h the next hour is 00h, not 24h. For example, if we take the arithmetic mean of `[22h, 23h, 00h]` we get `15h`, but if you went to sleep at 22h, 23h and 00h in three subsequent days you wouldn't say that in these days the average time you went to sleep was 15h, would you?

The correct way to calculate the mean here is to map the hours to angles and use the methodology of mean of circular quantities. The idea is that, once you converted the values to angles in the unit circle (in the range $[0, 2\pi[$), you map each angle $\theta$ to its point in the cartesian coordinates $p$ where:

$$p = (cos \theta, sin \theta)$$

And you average out separately each component, then take the arctangent of the resulting angle. If you have $\theta_1, ..., \theta_n$ angles, the mean is calculated as:

$$\overline{\theta} = atan2\left(\sum_{i=1}^n sin\ \theta_i, \sum_{i=1}^n cos\ \theta_i\right)$$

Another method is to calculate this mean using complex numbers, which is the way I calculated in the code, based on a snippet I found on [Rosetta Code](https://rosettacode.org/wiki/Averages/Mean_angle#Python).

### Average Start and Stop times

Using the aforementioned method I calculated the average hour I usually go to sleep and when I wake up, for each day of the week:

| weekday   | start_hour_avg   | stop_hour_avg   |
|:----------|:-----------------|:----------------|
| Monday    | 23:42:40         | 07:46:00        |
| Tuesday   | 23:41:10         | 07:44:36        |
| Wednesday | 23:40:43         | 07:44:34        |
| Thursday  | 23:29:41         | 07:48:04        |
| Friday    | 23:51:16         | 07:40:27        |
| Saturday  | 00:11:59         | 09:09:57        |
| Sunday    | 00:58:34         | 10:25:59        |


- The data shows a consistent pattern of sleep time on the business days: ~23h40 is my usual sleep time, and I usually wake up at ~7h40 in the morning;
- On the weekends there's a shift in sleep time: Instead of going to bed at 23h40 I tend to stay awake more time;
- Besides that, I also wake up later on the weekends, not only because I go to sleep later, but also because I have longer sleep times on Saturday and Sundays as we've already seen in the last section.


## Conclusion + Code

Overall I'm pretty happy with the sleep patterns I had in 2020. I have a very good sleep time and (mostly) consistent sleep hours, which yield me good quality of sleep (my inference here). About my weekend sleep patterns I'm not sure if I need (and want to) commit to change them and make them more consistent with the usual business days. I think it would be wise to make the Friday-Saturday sleep transition more consistent with the rest of the week, but I developed a habit of watching movies/tv series on Fridays that I don't know if it's worth to change it. ¯\\\_(ツ)_/¯

For 2021 my goals are to, at least, keep some of this consistency and sleep time, but I don't have anything more ambitious in mind regarding my sleep habits. You can check the notebook with the code I used to generate the plots and the tables in [Google Colab](https://colab.research.google.com/drive/1lsxZwF863tmyddXV54mXdt7Qn0CFEHul?usp=sharing) (raw data not provided).



[^fn1]: Fucci,  D.,  Scanniello,  G.,  Romano,  S.,  and  Juristo,  N.(2018).   Need  for  sleep:  the  impact  of  a  night  of  sleep  deprivation  on novice developers’ performance.CoRR, abs/1805.02544.
[^fn2]: Golbert,  D.  C.,  Souza,  A.  C.,  Almeida-Filho,  D.  G.,and Ribeiro, S. (2017).  4.28 - sleep, synaptic plasticity, and memory.  InByrne,  J.  H.,  editor,Learning  and  Memory:  A  Comprehensive  Reference(Second Edition), pages 539 – 562. Academic Press, Oxford, second edition.

[^fn3]: Huang,   T.   and   Redline,   S.   (2019).Cross-sectional and prospective associations of actigraphy-assessed sleep regula-rity with metabolic abnormalities: The multi-ethnic study of atherosclero-sis.Diabetes Care.

[^fn4]: National Sleep Foundation Recommends New Sleep Times | Sleep Foundation. (2021). Retrieved 20 January 2021, from https://www.sleepfoundation.org/press-release/national-sleep-foundation-recommends-new-sleep-times