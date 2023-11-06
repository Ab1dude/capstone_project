# Space-Program-Capstone_Project
## Editing the file
Its a markdown file in this repository
Classification Project:
We will predict if the Falcon 9 first stage will land successfully or not. Therefore if we can determine if the first stage will land, we can determine the cost of a launch.

Models Used:
LogisticRegression, KNN, DecisionTreeClassifier, XGBClassifier (Best), SVM & RandomForestClassifier

Project Overview:

• Defined a series of helper functions that will help us use the API to extract information using identification numbers in the launch data.

• Started requesting rocket launch data from SpaceX API with the URL link 'https://api.spacexdata.com/v4/launches/past'. Requested and parsed the SpaceX launch data using the GET request. Created a Pandas dataframe from the dictionary launch_dict

• Filtered the dataframe to only include Falcon 9 launches.

• Dealt with missing values in column 'PayloadMass' using the .mean() and then .replace() function to replace np.nan values in the data with the mean

• Explored data to find some patterns in the data and determine what would be the label for training supervised models.

• Exploratory Analysis using libraries like Pandas, Seaborn and Matplotlib

• Feature Engineering: Based on obtaining some preliminary insights about how each important variable would affect the success rate, selected the features that will be used in success prediction in the future module.

• Launch Sites Locations Analysis with Folium, Marked all launch sites and the success/failed launches for each siteon a map. Then calculated the distances between a launch site to its proximities.

• Machine Learning Prediction: Standardized the data, splitted into training data and test data, found best Hyperparameters for SVM, Decision Tree, KNN and Logistic Regression, and then got which of the method performs best using test data among all classification models.

Main Highlights:
• Used Standard Scaler for Feature Scaling, One Hot Encoding to convert categorical variables to Numerical Variables.

• Dealt with null values:

⦾ Used "mean" to fill null values in 'PayloadMass' variable

⦾ Used "mode" to fill null values in 'LandingPad' categorical variable

⦾ Performed Bivariate analysis majorly to get some useful insights from the variables with the help of catplot, barplot, lineplot, and scatterplot

⦾ During Accuracy Comparison of different algorithms on training data, best algorithm is RandomForest with a score of 1.0.

⦾ While during Accuracy comparison of different algorithms on test data, best Algorithm is XGBClassifier with a score of 88.89
