📂 Project Workflow
1️⃣ Data Loading

The dataset was loaded using Pandas.

data = pd.read_csv('BostonHousing.csv')
2️⃣ Data Cleaning

Missing values in the rm column were handled using the median value.

data['rm'] = data['rm'].fillna(data['rm'].median())
3️⃣ Feature Selection
X = data.drop(columns='medv')
y = data['medv']
4️⃣ Train-Test Split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=100
)
5️⃣ Model Training
linear_reg = LinearRegression()
linear_reg.fit(X_train, y_train)
6️⃣ Prediction
y_pred = linear_reg.predict(X_test)
7️⃣ Model Evaluation
R² Score
Mean Squared Error (MSE)
Root Mean Squared Error (RMSE)
📊 Visualization

Actual vs Predicted Housing Prices:

plt.scatter(y_test, y_pred)
plt.xlabel("Actual Prices")
plt.ylabel("Predicted Prices")
plt.title("Actual vs Predicted Housing Prices")
plt.show()

This visualization helps evaluate how closely the predictions match the actual housing prices.

📈 Results

The model achieved a good regression performance with an R² score of approximately 75%, meaning the model explained a large portion of the variation in housing prices.

📚 What I Learned

Through this project, I learned:

How Multiple Linear Regression works
The importance of preprocessing data
How to split datasets for training/testing
How to evaluate regression models
How to visualize prediction performance
🚀 Future Improvements
Feature scaling
Hyperparameter tuning
Trying advanced regression models
Using larger real-world housing datasets# Boston-House-prices

⭐ If you found this project interesting, feel free to star the repository!
