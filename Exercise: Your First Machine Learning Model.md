<h3> Step 1: Specify Prediction Target </h3>
<pre>
# Select the target variable, which corresponds to the sales price. Save this to a new variable called y. You'll need to print a list of the columns to find the name of the column you need.
# print the list of columns in the dataset to find the name of the prediction target
print(home_data.columns)
y=home_data.SalePrice
</pre>
<hr >
<h3> Step 2: Create X </h3>
<pre> 
# Create the list of features below
feature_names = ['LotArea','YearBuilt','1stFlrSF','2ndFlrSF','FullBath','BedroomAbvGr','TotRmsAbvGrd']

# Select data corresponding to features in feature_names
X = home_data[feature_names]
</pre>
<hr> 
<h3> have a look at the data and review it </h3>
<pre>
  # Review data
# print description or statistics from X
print(X.describe())

# print the top few lines
print(X.head())
</pre>
<hr>
<h3> Step 3: Specify and Fit Model </h3>
<pre> 
  # from _ import _
from sklearn.tree import DecisionTreeRegressor
#specify the model. 
#For model reproducibility, set a numeric value for random_state when specifying the model
iowa_model = DecisionTreeRegressor(random_state=1)

# Fit the model
iowa_model.fit(X,y)
</pre>
<hr> 
<h3> Step 4: Make Predictions </h3>
<pre>
predictions = iowa_model.predict(X)
print(predictions)
</pre>
<hr>



<h3> Think about your result </h3>
<pre> when i run the model on the 5 values i have seen that
the prediction results and sample results are exact same
  We use DecisionTree for this model
</pre>
