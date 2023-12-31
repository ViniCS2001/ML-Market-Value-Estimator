This project uses ML models with the Random Forest Algorithm in order to predict/estimate the market values of football players based on their statistics.

### Prerequisites
You must have Scikit Learn, Pandas (for Machine Learning Model) and Flask installed.

### Project Structure
This project has four major parts :
1. RF_Model.ipynb & RF_Model2.ipynb - These files contain code for our Machine Learning models to predict the market value of football players using Random Forest Model with different input parameters.
2. app.py - This contains Flask APIs that receives employee details through GUI or API calls, computes the predicted value based on our model and returns it.
3. request.py - This uses requests module to call APIs already defined in app.py and displays the returned value.
4. templates - This folder contains the HTML template to allow user to enter the stats and displays the predicted market value.

### Running the project
1. Ensure that you are in the project home directory. Create the machine learning model by running below command -
```
python model.py
```
This would create a serialized version of our model into a file RF_model_app.pkl

2. Run app.py using the below command to start Flask API
```
python app.py
```
By default, flask will run on port 5000.

3. Navigate to URL http://localhost:5000

You should be able to view the homepage as below :
![ML_UI](https://github.com/ViniCS2001/ML-Market-Value-Estimator/assets/97949821/c01d11dc-ecf8-4adc-8429-c60fe58ceb6b)


Enter valid numerical values in all input boxes and hit Predict.

If everything goes well, you should be able to see the predicted salary value on the HTML page!

4. You can also send direct POST requests to Flask API using Python's inbuilt request module
Run the below command to send the request with some pre-populated values -
```
python request.py
```
