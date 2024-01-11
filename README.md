# **Forecasting Demand for Optimized Inventory Planning**
------------

## **Business Case-Study**

Historical data must be used to create a machine learning model to reliably forecast the demand for 14 days. Use the period starting on 30 June 2018 00:00:00, the day after the last date from the transaction files. 

The solutions submitted will be assessed and compared based on their monetary value 
for the retailer. The monetary value is determined by the predicted revenue and an 
overstocking fee for overestimating the demand for any product. The demand prediction 
for every product is therefore compared with the actual number of orders within the same 
time frame.

------------

## **Dataset Description**

1) **Orders Dataset**: It have 5 features 
  
  a) time
  
  b) transactID
  
  c) itemID
  
  d) order
  
  e) sales price


2) **Items Dataset**: It have 8 features:
  
  a) itemID
  
  b) brand	
  
  c) manufacturer	
  
  d) customer rating	
  
  e) category1	
  
  f) category2	
  
  g) category3	
  
  h) recommended retail price


3) **Infos Dataset**: It have 3 features:
  
  a) itemID	
  
  b) simulationPrice	
  
  c) promotion


4) **DMC_2020_solution Dataset**: It have 4 features

  a) itemID	
  
  b) price	
  
  c) demand prediction	
  
  d) revenue
  
-----------
For Time series Forecasting (TSF) we need time and demand prediction features only
<br/>

<pre>	
date	      demand prediction
2018-01-01	450931
2018-01-02	117876
2018-01-03	37034
2018-01-04	320165
2018-01-05	3049527
...	...
2018-06-25	1260087
2018-06-26	946622
2018-06-27	2263096
2018-06-28	144532
2018-06-29	1182259
</pre>

It has 180 rows × 1 column

---------
## **Graph Analysis**

It is not seasonal from the below graph

![image](https://github.com/Bamit-2021/Forecasting-Demand-for-Optimized-Inventory-Planning/assets/77608956/85e3cbd8-625d-4b61-9d4a-9aded79cfe8e)

It is stationary from the below graph so we do not need differencing.

![image](https://github.com/Bamit-2021/Forecasting-Demand-for-Optimized-Inventory-Planning/assets/77608956/4f8222f4-d853-484c-97e5-74d0a8cba757)

----------------
## **Model : ARIMA(AutoRegressive Integrated Moving Average)**

![image](https://github.com/Bamit-2021/Forecasting-Demand-for-Optimized-Inventory-Planning/assets/77608956/7d4b936f-87d7-435f-9f9b-5bbea4ec7863)

--------------

### **Next 14 Days Prediction of Demands:**

From the above graph, we can see that the daywise prediction of demands is getting good results from 30-06-2018 to 13-07-2018.

```
2018-06-30	1.129260e+06
2018-07-01	6.899962e+05
2018-07-02	1.098518e+06
2018-07-03	8.169385e+05
2018-07-04	9.082161e+05
2018-07-05	1.023671e+06
2018-07-06	7.346322e+05
2018-07-07	1.123810e+06
2018-07-08	7.297089e+05
2018-07-09	1.034994e+06
2018-07-10	8.885879e+05
2018-07-11	8.457368e+05
2018-07-12	1.062438e+06
2018-07-13	7.281683e+05
```

-------------------
## **More information**
Visit this python file for more detailed analysis [Inventory_Planning.ipynb](https://github.com/anjanikmr39/Forecasting-Demand-for-Inventory-Planning/blob/master/Inventory_Planning.ipynb)
