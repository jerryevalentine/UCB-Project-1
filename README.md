# UCB-Project-1

## Data Source ##
https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data?resource=download

## Datasets ##

### Prefered dataset ###
- We will first need to determine the feasibility of using the car sales dataset.
- Need to check for nulls and use regular expressions to search for any garbage (corrupt data, data that should not be in the cell, etc.).  If the car sales is not appropriate then we will evaluate the credit card fraud dataset.
- Note the dataset has a 10 usability score, which I believe is the highest.  This notebook is for due dillegence and also providing the metadata for the dataset.

-https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data/data

-https://www.kaggle.com/datasets/kelvinkelue/credit-card-fraud-prediction

## Criteria for inclusion: ##
-Sufficiently large (558,837 records)
-Loads in about 15 seconds on mny computer
-11% of the Transmission records are null

-https://www.kaggle.com/code/yusupibrahim/selling-price-predic-with-stacked-gen-r2-0-96 provides good example code

## Kaggle Data Card ##

About Dataset

Dataset Description:
The "Vehicle Sales and Market Trends Dataset" provides a comprehensive collection of information pertaining to the sales transactions of various vehicles. This dataset encompasses details such as the year, make, model, trim, body type, transmission type, VIN (Vehicle Identification Number), state of registration, condition rating, odometer reading, exterior and interior colors, seller information, Manheim Market Report (MMR) values, selling prices, and sale dates.

Key Features:
Vehicle Details: Includes specific information about each vehicle, such as its make, model, trim, and manufacturing year.

Transaction Information: Provides insights into the sales transactions, including selling prices and sale dates.

Market Trends: MMR values offer an estimate of the market value of each vehicle, allowing for analysis of market trends and fluctuations.

Condition and Mileage: Contains data on the condition of the vehicles as well as their odometer readings, enabling analysis of how these factors influence selling prices.

Potential Use Cases:

Market Analysis: Researchers and analysts can utilize this dataset to study trends in the automotive market, including pricing fluctuations based on factors such as vehicle condition and mileage.

Predictive Modeling: Data scientists can employ this dataset to develop predictive models for estimating vehicle prices based on various attributes.

Business Insights: Automotive industry professionals, dealerships, and financial institutions can derive insights into consumer preferences, market demand, and pricing strategies.

Format: The dataset is typically presented in tabular format (e.g., CSV) with rows representing individual vehicle sales transactions and columns representing different attributes associated with each transaction.

Data Integrity: Efforts have been made to ensure the accuracy and reliability of the data; however, users are encouraged to perform their own validation and verification processes.

Update Frequency: The dataset may be periodically updated to include new sales transactions and market data, providing fresh insights into ongoing trends in the automotive industry.