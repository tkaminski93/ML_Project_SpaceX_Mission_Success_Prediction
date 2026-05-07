# IBM Applied Data Science Capstone Project

## 🚀 Executive summary
The primary goal of this project is to predict whether the first stage of a SpaceX Falcon 9 rocket will land successfully. SpaceX offers launch prices at $62 million, whereas other providers cost upward of $165 million. Much of these savings are possible because SpaceX reuses the first stage. Therefore, determining if a landing will be successful allows us to estimate the actual cost of a launch.

## 🛠️ Technologies & Tools
- **Languages:** Python 3.x
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Folium, Plotly Dash, Scikit-learn.  
- **Data Sources:** SpaceX API and Wikipedia Web Scraping.  
- **Environment:** IBM Skills Network / Jupyter Notebooks.

## 📋 Project Methodology & Notebooks
**1. Data Collection & Preparation**
- [1_Complete_the_Data_Collection_API](/Notebooks/1_Complete_the_Data_Collection_API.ipynb): Data extraction from the SpaceX API, focusing specifically on Falcon 9 launches. Missing values were replaced by column means, resulting in a dataset of 90 rows and 17 columns.  
- [2_Data_Collection_with_Web_Scraping](/Notebooks/2_Data_Collection_with_Web_Scraping.ipynb): Extracting historical records from Wikipedia using BeautifulSoup to supplement API data.  
- [3_Data_Wrangling](/Notebooks/3_Data_Wrangling.ipynb): Cleaning and formatting data to prepare it for exploratory analysis. 

**2. Exploratory Data Analysis (EDA)**
- [4_Complete_the_EDA_with_SQL](/Notebooks/4_Complete_the_EDA_with_SQL.ipynb): Querying the dataset using SQL (IBM DB2) to answer technical questions about payload mass, launch sites, and mission outcomes.  
- [5_EDA_with_Visualization](/Notebooks/5_EDA_with_Visualization.ipynb): Utilizing Matplotlib and Seaborn to identify correlations between flight numbers, payload mass, and launch site success rates.
![Payload Mass vs. Flight Number](/Images/payloadmass_vs_flightnumber.png)
*A scatterplot showing the relationship between Payload Mass and Flight.*

**3. Interactive Visual Analytics**
- [6_Interactive_Visual_Analytics_with_Folium](/Notebooks/6_Interactive_Visual_Analytics_with_Folium.ipynb): Building interactive maps to visualize launch site clusters and proximity to critical infrastructure like railways and highways.
![Proximity to Critical Infrastructure](/Images/proximity_to_critical_infrastructure.png)
*A folium map showing the proximity to critical infrastructure.*  
- [7_Build_an_Interactive_Dashboard_with_Plotly_Dash](/Notebooks/7_Build_an_Interactive_Dashboard_with_Ploty_Dash.py): Creating a web-based dashboard to analyze the impact of payload mass on landing success for specific sites.
![Success vs. Specific Sites](/Images/success_vs_specific_sites.png)
*The picture below shows a pie chart when launch site CCAFS SLC-40 is chosen in the dropdown menu on the website. *
![Class vs. Payload Mass](/Images/class_vs_payloadmass_.png)
*The picture below shows a scatter plot  when the payload mass range is set to be from 0kg to 9600kg.* 

**4. Predictive Modeling**
- [8_Machine_Learning_Prediction](/Notebooks/8_Machine_Learning%20Prediction.ipynb): Implementing and optimizing classification models including Logistic Regression, SVM, Decision Tree, and KNN. Models were tuned using GridSearchCV to find the best hyperparameters.
![Model Performance](/Images/model_performance.png)
*The picture shows a horizontal bar chart of the performance of various models.*

## 📈 Results & Discussion
The analysis confirmed that specific features, such as payload mass and orbit type, correlate with launch outcomes. For instance, heavy payloads often show higher success rates for LEO and ISS orbits.  Model Performance: All four machine learning algorithms yielded similar accuracy on the test set.  Best Model: The Decision Tree algorithm was identified as the best-performing model based on a GridSearchCV score of 0.863.  

## 🏁 Conclusion

This project successfully developed a predictive model for Falcon 9 first-stage landings. By leveraging a Decision Tree classifier, we can provide data-driven estimations of launch costs, offering a significant competitive advantage in the aerospace market.

---

Author: Tomasz

Senior Quality Engineer | Data Science Certified