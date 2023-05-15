# Flight Delay Analysis & Prediction
This is my first ever data analysis project. For this project, I analyzed over 11 million rows of airplane data using SQLIite, Python &amp; R. The Workflow includes data cleaning, preprocessing, exploratory analysis, visualization, and machine learning models to understand factors affecting delays, improve operational efficiency, and enhance customer satisfaction.



### Languages
1. Python
2. R
3. SQLite
![tabkes](https://github.com/oolwinds/airplanedelays/assets/130780065/9414e516-d9b2-4a26-ad1e-9d2e53affec2)

![dbtool](https://github.com/oolwinds/airplanedelays/assets/130780065/fa8938cd-95c2-4cb5-a80e-6e7b4c7090d7)

### Data Analysis 
The initial stage involved thorough exploratory data analysis (EDA). We used SQLite to manage our large dataset and perform complex queries to extract valuable insights. The analysis included the relationship between departure and arrival delays, the busiest and least busy airports, and the effect of these parameters on flight delays.
![q2](https://github.com/oolwinds/airplanedelays/assets/130780065/76223900-875f-4e6d-a774-c28b7cab4ccc)

We used SQL case statements to create dummy variables, which helped simplify categorical data and made it more suitable for machine learning algorithms. We also used SQL to filter and aggregate data, making it easier to visualize and interpret.

It was noted that busy airports tend to suffer more delays, likely due to high traffic and potential infrastructure constraints. Factors such as the day of the week, the age of the aircraft, and the specific airport can significantly influence the occurrence and duration of flight delays.

### Data Preprocessing
The next step was data preprocessing where we filtered out any rows that could potentially distort our results. We focused on instances where both departure and arrival delays were more than 0, with no diversions or cancellations. This data was then transformed into a more manageable data frame for further analysis. The preprocessing step also involved creating dummy variables for categorical features, making the data ready for machine learning models.

### Network Analysis with Python (NetworkX)

In order to model and analyze the network structure of flight routes, we utilized NetworkX, a Python package for the creation, manipulation, and study of complex networks. NetworkX allowed us to generate a visual representation of our flight data, effectively converting airports into nodes and flights into edges. This graph-based approach provided valuable insights into the connectivity and interdependencies among different airports, crucial for understanding the cascading effect of flight delays.

The NetworkX graph (Figure 11) was instrumental in our study of the propagation of flight delays across the network. It also served as an efficient tool for identifying high-traffic airports that could potentially be the primary contributors to widespread flight delays.
![q4network](https://github.com/oolwinds/airplanedelays/assets/130780065/58767c41-0c07-4fd2-bcfd-941392bfce1d)

### Interactive Data Visualization with R (Shiny) 

To make our analysis more accessible and interactive, we incorporated R Shiny, a web application framework for R, into our workflow. Shiny enabled us to build user-friendly, interactive dashboards for data visualization.

Our Shiny application allowed users to interactively explore various aspects of our data, such as the distribution of departure and arrival delays, the busiest and least busy airports, and more. Figure 6 in our report were generated using this Shiny application, enabling us to dive deeper into the relationship between various factors and flight delays. The interactive nature of Shiny apps facilitated a more intuitive understanding of these complex models, making our analysis more understandable to a wider audience.

These tools, combined with traditional data analysis and machine learning techniques, formed the backbone of our workflow. Together, they allowed us to perform a thorough investigation into the factors contributing to flight delays, and to develop reliable predictive models for future delays.
![shiny](https://github.com/oolwinds/airplanedelays/assets/130780065/c8d615cc-3560-432d-8160-9b2c48cc4d47)


### Machine Learning Models 

Our main objective was to predict departure delays, hence we utilized several machine learning models for this purpose.

### Regression

In Python, we used a Linear Regression model and a Random Forest Regression model to predict departure delay. The models were trained on 70% of the data and tested on the remaining 30%. The accuracy of these models was then evaluated using metrics such as the R2 score and mean squared error (MSE).

In R, we used a Ridge Regression model and a Random Forest model for the same purpose. We again split the data into a 75% training set and a 25% testing set. Hyperparameters were tuned, and cross-validation was used to optimize the models.

### Classification 

In addition to regression models, we also used several classification models to predict whether a flight would be delayed or not. These models included Logistic Regression, Support Vector Machines, Gradient Boosting, Random Forest, and Penalised Logistic Regression. The performance of these models was evaluated using ROC curves.

![q5](https://github.com/oolwinds/airplanedelays/assets/130780065/ea60559c-3d91-44e3-99ea-13e763472cab)

### Results & Conclusion

Both in Python and R, the Random Forest model showed superior performance in predicting flight delays. This was established by comparing the models using their accuracy and MSE values. It was found that Random Forest and Gradient Boosting classification models were able to perfectly distinguish between delayed and non-delayed flights.

In conclusion, this project involved comprehensive data analysis, preprocessing, and machine learning model implementation to predict flight delays. Several factors were identified that contribute to flight delays, and it was found that these delays can be predicted with a high degree of accuracy using machine learning models.

It's worth noting that while the analysis provides valuable insights and accurate predictions, there are inevitable outliers due to the unpredictable nature of many factors influencing flight schedules. Therefore, while our models perform well on historical data, they should be continuously updated and evaluated with new data to maintain their predictive power.

Please refer to the original repository for the full analysis, including all graphs and figures. The Git workflow was utilized throughout the project to maintain code versions and ensure smooth collaboration.
