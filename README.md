## Anomaly_Detection

## Tracking point anomalies using LSTM architecture. 

The structure of the code is as follows:

1.	Fetches information from mysql table which tells from where data will be fetched. 
2.	The program then fetches data from the database and table from google’s BigQuery, where it has been stored. 
3.	It first checks if the model for the existing database is available or not. 
4.	If the model is not available, it creates a new model by having a series of data processing and transformations and ultimately passing through LSTM model architecture.

5.	But if the model is available it checks 2 things:
      
      a.	If the age of the model is more than 5 days old:
            Then it trains from the latest data and then updates the existing model- by adding the new weights to the old model.
      b.	If the age of the model is less than 5 days old
          	Then it predicts and outputs the result and displays anomaly. 
            
6.	Finally throwing the output in a dataframe format to a MySQL database. 
