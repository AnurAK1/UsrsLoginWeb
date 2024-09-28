## Forecasting no of Users Logging In for a website.
### 💡Objective
##### To forecast number of users that will login to handle resources.In this project, it has been showcased the main concept of forecasting using ARIMA model. ARIMA model is one of the forecasting methods used mainly for time series analysis and predictive analysis.In Data Science, ARIMA model is one of the important model methodogy used for creating highly impactful models that generates solutions based on time series analysis. The data that has been used for this project is taken from Kaggle.
###  💡Data Introduction
##### On describing the data in jupyter notebook python , plot for increasing years with number of users suggest that there are yearly increase in number of users logging in from 2019 - 2022. Business organisation that wanted to quantify how business is performing , this shows that the business performance is going in an upward directions with increase in users logging in yearly.The average number of users on yearly basis has been increased from 2019 that sugests us that business performance could rise and organisation's performance might increase with increase in web traffic.
![image](https://github.com/user-attachments/assets/6e32df6e-9ccc-48b9-a85a-f090ec76d687)
|  |Year|Average number of users|
|:-:|----|        :--:            |
|0  |2019|54.405479               |
|1  |2020|65.453552               |
|2  |2021|76.164384               |
##### With increase in Web traffic, load to the website will also increase that might increase in overall cost of handling websites in cloud.Business might need a right amount of scaling provisioned inorder to meet the demand of the web users.

###  💡Data Trend Analysis to forecast
##### The plot below , signifies the yearly trend with number of users logging in on a daily basis.
![yearly_trend](https://github.com/user-attachments/assets/a0b53a05-a203-4baa-adcf-8ce210adc26b)
##### With respect to plot and data that was updated on recent years, it was found that there was number of users that logging in for the year 2021-22 was changing frequently in up down trajectory, and similar trends was found with other years/Months with change in numbers. With this finding we can conclude that the data is not distributed in a trend and might be influenced with seasonality. In order to forecast that data we will need to proceed with checking the seasonality in the data.
![Daily_trend](https://github.com/user-attachments/assets/3584eac9-9b13-48bd-8e26-31b588d5559d)
##### Decomposing the data multiplicatively and additively will define on what trend users are logging in to websites. It will also gives us trend in which the data is flowing on, it defines that the users are influenced by seasonality while logging in to the website. As there is a data changes its trajectory in upward direction on yearly , keeping decomposition factor to year will give data trends. The plot below shows yearly seasonality trends, when data is being decomposed multiplicatively and additively keeping the factors of little more than year.
###### Title : Seasonal Multiplicative decomposing data trend
![Mutiplicative](https://github.com/user-attachments/assets/28a50f94-790d-4bba-aaab-2c3bc428b5a5)

###### Title : Seasonal Additive decomposing data trend
![additive](https://github.com/user-attachments/assets/97970d23-3902-471d-a8c1-7a496ed33dc5)

##### It can be inferred that data is in an upward trajectory trends, influcencing seasonilty. In addition ad fuller test indicates the data present are stationary or non - stationary. Stationary data signifies that the mean and variance present in the data do not change over time. After conducting Ad Fuller test, it was found that data is non - stationary in nature and differencing will be required. Differencing will make data stationary as shown in the plot below.
![1st Diff](https://github.com/user-attachments/assets/5256bbae-e85a-4360-a48e-ce15f6a8b5ad)
##### Since the p value for 1st Differencing identified as 5.674175568009798e-26  for Ad Fuller test ,by rejecting the null hypothesis we can come to a conclusion that data is stationery and can proceed with generating the predictive Model.

###  💡Constructing Predictive Model for Forecasting
##### In Order to generate ARIMA model for Forecasting we will need Autocorrelation factor or ACF and Partial Autocorrelation PACF. On generating the ACF plot and values for 1st differencing data, it was identified repetitive high on 7th Lag signifying seasonality.
![ACF](https://github.com/user-attachments/assets/acb8207d-c71b-4a7a-8f06-5ae5f9d0a220)
##### Whereas PACF gives negative high on 5th, 6th and 13th Lag which results in PACF value close to 5,6 or 13.
![PACF](https://github.com/user-attachments/assets/6bb451fd-7266-4c3f-bfb7-bdd9cc793cc8)
##### With differencing as 1st Differencing on Data and ACF keeping as 1 and PACF starting with 4 gives a decent ARIMA model summary that justifies the model suitablity for finding forecast on WebUsers login.
##### Data Preparation in training and testing phases can be acheived by splitting the data in 80-20% giving total observation for Training and Testing with 878 and 219. Developing the ARIMA Model in training dataset and plotting the 
