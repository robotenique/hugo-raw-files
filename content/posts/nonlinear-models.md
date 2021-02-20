---
title:  "Useful Nonlinear Models in Python"
linktitle:  "Useful Nonlinear Models in Python"
date:   2021-01-20
categories: ["Statistics", "Python"]
tags: ["data science", "python", "programming"]
---






# Exponential Decay
https://demonstrations.wolfram.com/KineticOrderOfDegradationReactions/
Degradation Reactions (chemistry)

- Sympy, Wolfram Alpha, pencil and paper

- Exponential & logistic growth















| {{< image
    src="/img/sleep2020_4.png"
    alt="sleep" >}} | 
|:--:| 
| *My sleep time (in minutes) over the year 2020* |



## Context

2020 was a long year. One of the habits I paid some attention in this year was to measure/improve my sleep quality. Sleeping is a key part of our life, important for recharging your mind, form long lasting memories and learning overall. According to recent research[^fn2]:


## Measurements

{{< image
    src="/img/sleep2020_2.png"
    alt="sleep" >}}


## Sleep Time


```python
avg_in_hours = df.total_hours_slept.dt.total_seconds().mean()/60/60
minute_part = (avg_in_hours % 1)*60
print(f"2020 Average Sleep time: {str(int(avg_in_hours))}h:{str(int(minute_part))}m")
```
[^fn2]: Golbert,  D.  C.,  Souza,  A.  C.,  Almeida-Filho,  D.  G.,and Ribeiro, S. (2017).  4.28 - sleep, synaptic plasticity, and memory.  InByrne,  J.  H.,  editor,Learning  and  Memory:  A  Comprehensive  Reference(Second Edition), pages 539 – 562. Academic Press, Oxford, second edition.
