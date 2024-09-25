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

##### It can be inferred that data is in an upward trajectory trends influcencing seasonilty.
