---
title:  "Ethically Aware Recommender Systems in Social Media"
linktitle:  "Ethically Aware Recommender Systems in Social Media"
date:   2020-06-15
categories: ["Computer Science", "Misc"]
tags: ["AI", "data science"]
---
*This post is based on an article I wrote some time ago; There may be some inconsistencies with the references, sorry.*

{{< image
    src="/img/sad_bird.jpg"
    alt="sad_bird" >}}


### Reccomender Systems
In a world where digital information is increasing every year, recommender systems are very important tools to handle the challenge of information overload. A recommender system is a type of information filtering system with the ability to filter information from a large amount of data generated dynamically, according to a given preference, observed behavior or interest from the user [1]. There are different techniques used in recommender systems, the most mature and famous one being collaborative filtering,  which is domain-independent, and works by creating a table (user X items) of the preferences for items by users, they matching users to potential items they may like based on the recommendation of other users in the neighborhood, i.e. users with similar preference, taste or observed behavior [2]. Collaborative filtering based techniques are widely used in social media [3], e.g. the video sharing social media Youtube uses a  variation of this technique to recommend new videos to its users [4] .


Recommender systems are a very efficient way of getting user engaged in social networks, due to its ability to tailor it's recommendations according to each specific user and one powerful way of advertising and promoting a sense of uniqueness to a service's clients. But despite its advantages, an unrestrained recommendation system is also a prominent cause of people getting involved and promoting extremism and misinformation, especially in social media "custom-made" information delivery, creating a “Filter Bubble” [5] . Therefore, I argue an actively ethical approach should be taken in the development of recommender systems, trying to actively mitigate the problems that a highly specialized user-tailored system can entail.  These problems and their potential harms to democracy will be addressed and discussed in greater detail in the following paragraphs. 

Nowadays, advertising is the main source of revenue for the biggest social media products, like Facebook, Google, Youtube, Twitter, etc. One of the main strategies social media uses to maximize this source of revenue is to increase the time a user spends in the service. Therefore, recommender systems are one of the most efficient ways to keep a user engaged in the service: it tailors the content of the product to the user's "tastes", explicit or not. In some way, recommender systems algorithms are built in a way to keep expanding the recommendations, i.e. to continuously recommend new content which relates to what a user might like, but the type of content itself is not evaluated. 

### Social Echo Chamber

One of the current biggest concerns about them is the hoisting of extremism on these platforms [11]. A Fortune experiment on the video social network Youtube [6] found that extremist or misinformation content more likely to be shown for the users because the algorithm knows that people who watch them are more likely to spend more time in the website. Another investigation from the Wall Street Journal, with the help of a former Youtube engineer [12], came to similar conclusions. Another example is the Twitter platform, in which ISIS supporters substantially used it to spread information about the extremist group. A recent 2018 study from MIT [13] corroborates these experiments, in which the researchers found that fake news spread faster in social media. Even though the misinformation spreading and accessing is not a fault of the algorithm itself only (it's a combination of the recommender system and current human/society characteristics), it is possible to minimize the possible harms by adopting an active strategy when developing such systems, taking into consideration the ethics of it [15]. One such example is a research article [8] published in the Distributed Computing and Internet Technology, which uses machine learning techniques such as K-Nearest-Neighbors (KNN) and Support Vector Machines (SVM) to identify radicalization on Twitter.

An equally significant aspect of having an unrestrained algorithm to decide what to show or not, is the emergence of an intellectual isolation in these websites, which is called a "filter bubble", term coined by Eli Pariser in his book [5]. Ryan Muldoon, associate professor of philosophy at University at Buffalo says that “Democracy demands a robust contest of ideas to thrive, and diversity is the best way of protecting the democratic foundation [of our society]” [14]. One of the fundamental aspects of democracy is the plurality of ideas and debate to reach a compromise, and the harms filter bubble poses far outweigh the possible benefits it has to our individual social lives [9]. This problem is recognized by the social media companies, and just currently is being scrutinized due to the lack of effort they do to prevent or at least minimize the harms, according to a Minister of the UK Parliament from the Home Affairs Select Committee [10]. However, it's also important to recognize that it is possible to minimize them greatly by adopting an active instance in the building of such recommender systems. The Project Redirect redirects Youtube searches and videos from certain users who are searching for extremist content, and instead of providing with more extreme content (as a default unrestrained recommender system would), it presents them with content intended to de-radicalize them.

{{< image
    src="/img/echo_chamber.png"
    alt="echo_chamber" >}}

Thus, most of the harms of having algorithms filter and suggest new information is becoming more and more common. The evidence is clear, albeit it is difficult to know how deep the damage can escalate if not restrained. The dangers of fake news and misinformation are becoming clear, especially with the influence social media had in last elections in the USA. Echo chambers getting more and more powerful, posing a great threat to our society with its intellectual isolation. On the other hand, the above-presented approaches to hinder the effect of recommender systems is evidence that the harms can be reduced. But palliative measures are not enough, given the dangers previously outlined. From the beginning of its conception, social media applications should adopt ethical standards and test throughout the recommender system in multiple scenarios. Ethics over profit.

### References

**[1]** C. Pan, W. Li. “Research paper recommendation with topic analysis”. In Computer Design and Applications IEEE 2010; 4, pp. V4-264.

**[2]** J.L. Herlocker, J.A. Konstan, L.G. Terveen, J.T. Riedl. “Evaluating collaborative filtering recommender systems” in ACM Trans Inform Syst 2004; 22(1):5–53.

**[3]** C.V. Batista Jr., M.A. de Oliveira. “Recommender systems in social networks” in JISTEM J.Inf.Syst. Technol. Manag. [Online]. 2011, vol.8, n.3 pp.681-716. Available: https://bit.ly/2RL4idV. 

**[4]** P. Covington, J. Adams, E. Sargin. “Deep Neural Networks for Youtube Recommendations.” In Proceedings of the 10th ACM Conference on Recommender Systems (RecSys '16). ACM, New York, USA: 191-198.

**[5]** E. Pariser, “The Filter Bubble: What the Internet Is Hiding from You.”. New York, USA: Penguin Press, 2011.

**[6]** D. Z. Morris, "How Youtube Pushes Viewers Towards Extremism", Fortune, 2018. [Online]. Available: https://for.tn/2DFlOsH

**[7]** S. Illing, "How social media became a weapon of war", Vox, 2018. [Online]. Available: https://bit.ly/2AYATY1

**[8]** S. Agarwal and A. Sureka, “Using KNN and SVM Based One-Class Classifier for Detecting Online Radicalization on Twitter,” in Distributed Computing and Internet Technology, 2015, pp. 431–442.

**[9]** D. Baer, "The ‘Filter Bubble’ Explains Why Trump Won and You Didn’t See It Coming", The Cut, 2018. [Online]. Available: https://bit.ly/2QMIWw2

**[10]** K. McCann, "Social media companies are 'grooming' users by recommending extremist content and failing to take it down", The Telegraph, 2018. [Online]. Available: https://bit.ly/2QxvjBi. 

**[11]** P. Chadwick, "Why fake news on social media travels faster than the truth", the Guardian, 2018. [Online]. Available: https://bit.ly/2G9XZOK

**[12]** J. Nicas, "How Youtube Drives People to the Internet’s Darkest Corners", WSJ, 2018. [Online].Available: https://www.wsj.com/articles/how-Youtube-drives-viewers-to-the-internets-darkest-corners-1518020478.

**[13]** S. Vosoughi, D. Roy and S. Aral, "The spread of true and false news online", Science, vol. 359, no. 6380, pp. 1146-1151, 2018.

**[14]** R. Muldoon, "Democracy depends upon diversity", University at Buffalo, 2018. [Online]. Available: [http://www.buffalo.edu/news/releases/2018/08/031.html](http://www.buffalo.edu/news/releases/2018/08/031.html).

**[15]** D. Paraschakis. Towards an Ethical Recommendation Framework, 2018. 10.1109/RCIS.2017.7956539. 
