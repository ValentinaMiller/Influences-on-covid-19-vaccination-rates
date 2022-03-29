# University Data Science Project: Influences on Covid Vaccination Rates

## 1. Introduction

Since the first cases of COVID-19 appeared in Wuhan in December 2019, the
disease has spread worldwide and become a global pandemic. More than 400
million infected people have been registered globally, including more than 5.8
million fatalities with a presumably high number of unreported cases [1].
To counteract the outbreak of the disease, regulations and lockdowns were
imposed by many governments, which in turn imposed many restrictions on
daily life. Despite this, the pandemic has not yet been stopped and the hopes
of many people lie in vaccines, which were first developed at the end of 2020.
Vaccination could slow down the infection, or at least weaken the symptoms
of the disease, leading to fewer hospitalizations and thus keeping the health-
care system intact. Many countries have launched their vaccination campaigns
during the spring of 2021. At first, only vulnerable groups were able to get
vaccinated, but toward the middle of the year, the vaccine was released to the
entire population in most countries.
Although vaccines are promising, vaccination coverage varies widely across
countries. The reasons for this have not yet been conclusively clarified. In many
countries, vaccination is not mandatory, but the government encourages people
to get vaccinated. Therefore, it could be that trust in the government has an
impact on vaccination rates, along with other socio-economic factors.
The current study thus aims to investigate which socio-economic factors have
an influence on vaccination rates for COVID-19.

## 2. Methodology

In the second part we visualized and analyzed that data. This needed to be done
in such a way that the underlying relationships between the variables would be
observable. For that we plot each of our measures with our target variable,
which is the vaccination rate, on a two dimensional scatter plot that has the
respective measure on the x-axis and the vaccination rate on the y-axis. This
lets us visualize the relationship of each measure with the target variable. One
important indicator of that relationship is the correlation coefficient. We expect
some degree of linearity between a factor and the vaccination rate if that factor
has an influence on the vaccination process. For that reason the correlation
coefficient is a good measure to quantify the relationship. Additionally we
visualize the correlation by fitting a linear regression line on the points of each
plot. That way a high degree of correlation will be easily observable by a high
concentration of points close to the regression line.
In the last step we calculated a p-value for each of the plots. The p-value
indicates the probability of two random variables producing a dataset with the
given correlation value. Given a dataset it gives us the probability of that data
being produced by two independent random variables. In general a p-value of
0.05 and below is considered to be statistically significant. For that reason we
only considered measures that had a value in that range to be influencing the
vaccination rates.
We performed the analysis using a Python based stack including the packages
Jupyter-Lab, Matplotlib, Sklearn, Scipy, Pandas and Seaborn.
Please have a look at the pipeline for the code.

## 3. Results (relevant influences only)

Figure 1 reveals a high positive linear correlation between the share of people
fully vaccinated and the gross domestic product per capita with a correlation
coefficient of 0.701 and p-value of 7.54·10 −15 , meaning it is very likely that these
two variables are correlated. The same is shown by Figure 2 for the relationship
between the share of people fully vaccinated and the life expectancy. These two
variables have an even higher correlation coefficient of 0.782 and also a small
p-value of 1.29·10 −07 .
Figure 3 shows a negative linear correlation between the share of people fully
vaccinated and the working hours of employees with a correlation coefficient of
-0.48. The correlation is slightly weaker than for the previous two factors, but
the small p-value of 0.006 indicates that correlation is very likely.
For the following factors, shown by figures 4-9, the p-value was always higher
than 5%, which makes a correlation between the share of people fully vaccinated
and the respective factors very unlikely.


![Figure 1: Correlation between share of population vaccinated against COVID-
19 and GDP per capita](gdp.png) 
Correlation Coefficient and p-Value:
0.7006793183652773, 7.542031256159133e-15


![Figure 2: Correlation between share of population vaccinated against COVID-
19 and life expectancy](life_expectancy.png)


Correlation Coefficient and p-Value: 
0.7815731285293231, 1.288725407220812e-07


![Figure 3: Correlation between share of population vaccinated against COVID-
19 and working long hours](working_hours.png)


Correlation Coefficient and p-Value:
-0.4823137806158691, 0.005999820173321409

## 4. Discussion

The ongoing COVID-19 pandemic has cost the lives of many people and also
damaged the economies of many countries. In addition to strict regulations by
governments, which in turn restrict daily life, vaccination is one way to mitigate
the effects of the pandemic, making a high vaccination rate desirable.
The current investigation therefore examined which factors have an influ-
ence on vaccination rates. The results show that there are three factors that
have a relevant influence on the vaccination rate: the GDP per capita, the life
expectancy as well as the percentage of people working more than 45hours per
week. The higher the GDP per capita and the life expectancy the higher is
the vaccination rate. However, the more people work long working hours in a
country the lower is the vaccination rate of a country. The other factors did not
have a statistically relevant influence.
The limitations of this study were a limited number of data points due to a
limited number of countries. Moreover, data on socio-economic factors is hard
to quantify, because some of the indices were collected by asking people about
their attitudes and these findings are not entirely reliable.
It is important to mention that the GDP per capita and the life expectancy
have a high relation among each other, they represent wealth. This is reasonable
because a lot of poor countries have limited access to vaccines and therefore not
even the possibility to get vaccinated even if they would want to. The more
money a country has, the more it can spend on its health system. It was also
shown that countries in which employees work longer have a lower vaccination
rate. This could be because in poorer countries people earn less money and
therefore have to work more to make a living. That’s why another valuable
investigation would be to look into the influences of vaccination rates for groups
of countries separately, for example, to examine which socio-economic factors
are of relevance within a group of richer countries with a high GDP versus within a group of poorer countries with a lower GDP.

## 5. data and data sources 
### secondary & tertiary education, trust in government, unemployment, better life index
https://data.oecd.org

### GDP per capita:
https://www.kaggle.com/nitishabharathi/gdp-per-capita-all-countries

### COVID-19 vaccination rate:
https://www.kaggle.com/rsrishav/covid-vaccination-dataset

### Covid-19 deaths per 1000000 inhabitants
https://www.kaggle.com/uniquekale/covid-19-data-analysis-2021/data

### political regimes
https://sites.psu.edu/dictators/

## 5. How to install and run the project

<ol>
    <li><code>pip install -r requirements.txt</code></li>
    <li><code>jupyter-notebook pipeline.ipynb</code></li>
</ol>


[Learn more about creating GitLab projects.](https://docs.gitlab.com/ee/gitlab->
