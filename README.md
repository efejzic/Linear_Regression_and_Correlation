# Linear Regression and Correlation

**Introduction**

The North Carolina State Center for Health Statistics and Howard W. Odum Institute for Research in Social Science at the University of North Carolina at Chapel Hill make publicly available birth and infant death data for all children born in the state of North Carolina. The dataset, spanning from 1968 to the present, encompasses a wide record of data collection. Within the extensive dataset that comprises of 120,300 entries from 2001, we will focus on a random sample of 800 births, from which a subset of 80 records has been selected for this case study.

**Objectives**

The objectives of this unit are to understand how to formulate a single predictor linear regression model and to visualize that potential linear relationship. Additionally, this report will be able to compute and interpret the Grubbs to identify any potential outliers, remove those outliers, if necessary, compute coefficient of correlation and regression analysis.

**Data Description of Variables**

![image](https://github.com/user-attachments/assets/8731fd0b-2c0f-46ed-8815-8f8b2f21b79f)

**Data**

**File Name**: LDS_C02_NCBIRTH800

For analysis: A simple random sample (SRS) of 80 births from the 2001 North Carolina birth registry with variable columns renamed as ID_S, tgrams_S, and weeks_S.

![image](https://github.com/user-attachments/assets/38a3979b-1856-4a0c-8b91-aea4e4f6401a)

![image](https://github.com/user-attachments/assets/65f0d86d-89c4-4498-98e9-f174f36c33ca)

![image](https://github.com/user-attachments/assets/651e28c1-9cbe-4187-96fe-5fc609d417ab)

![image](https://github.com/user-attachments/assets/478a2283-5730-46c1-8fba-da3d3f678aa1)

**Results and Discussion**

_Preliminary Descriptive Statistics_

LDS_C02_NCBIRTH800

![image](https://github.com/user-attachments/assets/19b86fff-f2d7-4acf-9f4d-be37f8d9d8ec)

_Box plot_

![image](https://github.com/user-attachments/assets/8a375e94-7ffd-4847-8053-3ec8a3d9929a)

* With an SRS of 80, variable TGRAMS (or child weight in grams) has an IQR of 616.6 g, with the 3rd quartile as 3593.4 g and the 1st quartile as 2976.8 g. The median is 3302.8 g.

![image](https://github.com/user-attachments/assets/f3f8e9e8-3e5f-4bfb-91c8-9b589241ba50)

* With an SRS of 80, variable WEEKS (or weeks of gestation) has an IQR of 2 weeks, with the 3rd quartile as 40 weeks and the 1st quartile as 38 weeks. The median is 39 weeks.

_Histogram_

![image](https://github.com/user-attachments/assets/f7a7a1db-d004-4082-bdab-44de07bfe2bc)

* With a count of 80, the skew for variable TGRAMS is -0.079563, a negative number indicating a leftward skew, and the kurtosis is 0.872930, indicating a peak when compared to a normal distribution. The 95 percent confidence interval of the mean falls between 3149.5 g and 3411.3 g. The mean is reported at 3280 grams and the standard deviation is 588.2.

![image](https://github.com/user-attachments/assets/4d556691-4856-4af8-ac09-c9f92553671f)

* With a count of 80, the skew for variable WEEKS is -1.19838, a negative number indicating a leftward skew and showing more distribution of the tail towards data concentrated on the higher end. The kurtosis is 2.82994, indicating a peak when compared to a normal distribution and more extreme values. The 95 percent confidence interval of the mean falls between 38.155 and 39.95 weeks. The mean reported is 38.63 weeks and the standard deviation is 2.113.

_Outlier Test and Handling_

LDS_C02_NCBIRTH800

![image](https://github.com/user-attachments/assets/2ec8f26c-102f-4a3d-9249-cb02bc2fbf1d)

* The G value for TGRAMS is 3.12 and the p value is 0.105. The min is 1445.85 grams and max is 4734.45 grams. The p value suggests that the outlier is not statistically significant at the 0.05 significance level.

![image](https://github.com/user-attachments/assets/c5cb3e03-8e59-4d60-9aaa-3b875f38423a)

* The G value for WEEKS is 4.08 and the p value is 0.001. The min is 30 weeks and the max is 42 weeks. The results of the outlier test suggest that there is an outlier within the dataset for variable WEEKS.

* The Grubbs test has identified an outlier of 30 for the variable WEEKS. The outlier will remain unchanged and within the dataset as it is a relevant data point. A baby born at 30 weeks is considered very preterm and will require a long NICU stay, but their vital organs are much more developed and they usually weight about 3 pounds, or 1360 grams (Bird, 2022). In this dataset, the baby born at 30 weeks weighed 1445.85 grams, given the relevance and its alignment with known characteristics of babies born at 30 weeks, we fail to reject the null hypothesis at the significance level of 0.05.

_Scatter plot_

LDS_C02_NCBIRTH800

![image](https://github.com/user-attachments/assets/68dab2b7-a8fc-4db3-9c87-a8be1689cbfc)

* The matrix plot assesses the relationship between several pairs of variables at once. On the Y axis is the variable WEEKS, or weeks of gestation, and on the X axis is the variable TGRAMS, or child weight in grams. The visual reflects that lower weeks of gestation and lower child weight in grams indicate correlation between the two variables. When weeks of gestation is a higher number, than child weight in grams also reflects a higher weight. Although correlation seems to be reflected, there is no indication for linearity.

_Correlation_

LDS_C02_NCBIRTH800

![image](https://github.com/user-attachments/assets/0622f92c-1bde-4b44-b8ff-63653e1fd801)

![image](https://github.com/user-attachments/assets/068b67d8-a1fc-4d31-b1ca-19480050ff92)


_Regression Analysis_

LDS_C02_NCBIRTH800

![image](https://github.com/user-attachments/assets/bbb92885-d2b8-4d88-b084-7b104e5a02e5)

![image](https://github.com/user-attachments/assets/62a77ebc-a0a5-4f9a-ba8b-ca4d74cc9bf1)

![image](https://github.com/user-attachments/assets/b51212a8-3093-4dfd-aacc-1a6576ca340b)

![image](https://github.com/user-attachments/assets/18f5af0b-92ee-429d-a488-bed36ee698c2)

_Correlation Assumptions_

1. For each value of X there is a normally distributed subpopulation of Y values.

2. For each value of Y there is a normally distributed subpopulation of X values.

3. The joint distribution of X and Y is a normal distribution called the bivariate normal distribution.

4. The subpopulations of Y values all have the same variance.

5. The subpopulations of X values all have the same variance.

(Daniel, 2018).

**Null hypothesis:** There is no linear relationship between the two variables. p = 0

**Alternative Hypothesis:** There is a linear relationship between the two variables. p ≠ 0

(Frost, n.d).


* The Pearson correlation evaluates the relationship between two continuous variables (X and Y or variables TGRAMS and WEEKS, respectively). The p value indicates the strength of the relationship of evidence against the null hypothesis, which states that the variables are not linearly correlated. The p value concluded in the Pearson correlation is 0.000, indicating sufficient evidence to reject the null hypothesis. The sample data supports the notion that a significant relationship between the variables exists in the population.

* The correlation coefficient 0.464, greater than 0 indicating a moderate positive relationship between the variables implies that as one variable increases, the other tends to increase as well, although not necessarily linear. The level of statistical significance is 0.05. Since the p value is less than the significance level, it can be concluded that there is a statistically significant association between the response variable (TGRAMS) and the predicator variable (WEEKS). The continuous predicator (WEEKS) is significant, so it can be concluded that the coefficient for the predictor does not equal zero.

_Residual (error) Analysis_

LDS_C02_NCBIRTH800

![image](https://github.com/user-attachments/assets/d8ec4592-b7b8-45ef-bd8e-5f44ba147e2e)

* The difference between the observed value of Y and the predicted value of Y is also referred to as a residual (Daniel, 2018). As aforementioned, it can be concluded that there is a statistically significant association between the response variable (TGRAMS) and the predicator variable (WEEKS). As one variable increases, the other tends to increase as well, although not necessarily always in a linear fashion. We can observe from the Normal Probability Plot, that as percent along the Y axis increases, Residual values along the X axis also increase. Regression assumes that the residuals follow a normal distribution, and that the degree of scattering is the same for all fitted values (Frost, n.d). In the Versus Fits visualization, we can observe residuals centering on zero, indicating the predications are correct on average rather than systematically too high or low.

_Conclusion_

The null hypothesis of the Grubbs test states that all data values come from the same population, while the alternative hypothesis suggests that the smallest or largest data value may be an outlier. With a significance level set at 0.05, the Grubbs test was conducted on the two variables TGRAMS and WEEKS. The results indicate that there is no outlier for TGRAMS, but an outlier of 30 weeks, the smallest amount in the dataset, for variable WEEKS. Upon further investigation into the validity of the outlier, I decided to leave the data point representing a baby born at 30 weeks unchanged and within the dataset as it is a relevant data point. A baby born at 30 weeks is considered very preterm and will require a long NICU stay, but their vital organs are much more developed and they usually weight about 3 pounds, or 1360 grams (Bird, 2022). In our dataset, the baby born at 30 weeks weighed 1445.85 grams, which aligns with expectations for their gestational age. Therefore, we fail to reject the null hypothesis at the significance level of 0.05. Additionally, we have sufficient evidence to reject the null hypothesis of the Pearson correlation and concluding that there is a statistically significant association between the response variable (TGRAMS) and the predictor variable (WEEKS).

**References**

![image](https://github.com/user-attachments/assets/28862519-c908-414f-98fa-6381f87f3537)







