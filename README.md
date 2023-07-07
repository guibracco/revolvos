# revolvos
## The Earth Revolvos around the Sun.

---

**Predictive maintenance of Volvo Group truck fleet.**

With focus on sustainable service growth, analysed and processed large buckets of data on AWS cloud to formulate hypotheses regarding predictive maintenance. The data were then used in a regression model to measure the correlation of the variables with severe faults and fed into a machine learning model to predict when those faults were more likely to happen. How to anticipate when a truck was more likely to have a severe fault so that they could do maintenance before it happened, thus reducing downtime and, of course, loss of money.

After consulting, we decided to first go for a statistical regression and then try and build a machine learning model to predict the so-called red faults. It was the perfect learning opportunity because we have lots of data points, but especially because our stakeholders were highly technical for that approach, they were used to those models.

So we sliced the data and selected as many variables as possible to train and test our model. Our regression showed how much each variable affected red fault occurrence (the bigger the number, stronger the correlation) and we presented the results confirming our main hypothesis that vehicle activity would affect when a severe fault occurs.

But there was a caveat. When we ran our machine learning model, it could predict faults, but its precision was off. The confusion matrix showed that when it accurately predicted 657 red faults, it also wrongly predicted 457 red faults which were not actually severe. And when it predicted almost 180.000 non-red faults, it also wrongly predicted 18.000 non-red faults that were in fact severe, which was troubling, as the model never reached enough accuracy.

Looking back into the data, we realized that although they provided a generous amount of data, the timespan of the data collection was probably too narrow, comprising about only 6 months, which hindered the results. Mind that most of the trucks remained at service for at least 2 years, so the picture the data provided was limited in time. Our recommendation was to expand that timeline for a predictive model to be more accurate. We also suggested that they provided more information about causes for each of the features (or snapshots) that had pretty dramatic coefficients in the regression and how they correlated, taking them into consideration when doing maintenance checks.
