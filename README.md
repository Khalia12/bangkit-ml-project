# Bangkit Machine Learning Project
Bangkit Machine Learning Project with Tensorflow to predict number of visitors in the next week based on number of visitors in previous weeks


<h3>Problem Framing</h3>
A hotel needs to determine how they should prepare for upcoming season or event, either for their promotion or internal hotel activities. In order to do so, the hotel needs to determine how many visitors will stay in their hotel later. Predictions will be made based on number of visitors per period
<h5>Ideal Outcome</h5>
Hotel can get better insight about how they should prepare budget and activities based on number of visitor prediction. This way the hotel can also save more money and time.
<h5>Success Failure Metric</h5>
System is succeed if average difference between prediction and number of visitors in the next week should not more that 100. Failure means big difference between prediction and number of visitors in the next week.
<h5>Preferrable Output</h5>
Unidimensional Time Series Regression to get single prediction based on number of visitors in several weeks
<h5>Heuristics</h5>
One of popular heuristic method which can be used for regression is Multivariate Adaptive Regression Spline (MARS) which predicts by brute-force search for pair of values which produces minimum sum of squares residual error. Evaluation after prediction is done to prevent overfitting by removing least effective result.

<h3>Dataset</h3>
Data is acquired from <a href="https://www.kaggle.com/jessemostipak/hotel-booking-demand">Hotel Booking Demands Datasets</a> by Jesse Mostipak from Kaggle which contains hotel booking data from 2015 to 2017.

<h3>Solution Approach</h3>
There are several methods that can be used to predict time series data, but we choose Long Short Term Memory (LSTM). LSTM is type of Recurrent Neural Network (RNN) which is designed to keep information from long term data to be used later in prediction.

We also use Mean Square Error (MSE) to measure our system accuracy. MSE shows square difference between our prediction and our desired result. Smaller MSE means better accuracy.

<h3>Hyperparameter Explanation</h3>
<h5>Time Step</h5>
Time step in our case means number of previous weeks which will be used to predict number of visitors in the next week. LSTM considerably able to predict well in our case and the most accurate prediction is acquired based on 3 weeks data

<h5>Batch</h5>
Batch size shows how many data is processed by system before system starts to update based on what it has learned. Bigger batch size will definitely shorten training time, but will also deteriorate accuracy. In our case it also inflicts overfitting (system did well in training but terrible in testing)

<h5>Epoch</h5>
Epoch shows how many times our data is trained. Bigger epoch slows down training time, but will increase accuracy. If epoch is too big, it will also inflicts overfitting.

<h5>Units</h5>
Units show number of nodes which is used to learn data. More units increase system ability to learn but may also inflicts overfitting.

