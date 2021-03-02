# IBM Coursera Advanced Data Science Capstone Project
Repository for the IBM Coursera Advanced Data Science Project

## Predict delays in US national flights

### Research Question
The U.S. Department of Transportation's (DOT) Bureau of Transportation Statistics (BTS) tracks the on-time performance of domestic flights operated by large air carriers from 1987. Data of 2019 flights was downloaded from their site (https://www.transtats.bts.gov/DL_SelectFields.asp?Table_ID=). This database contains scheduled and actual departure and arrival times reported by certified U.S. air carriers that account for at least one percent of domestic scheduled passenger revenues. The data is collected by the Office of Airline Information, Bureau of Transportation Statistics (BTS).

Using this data set, we ask ourselves:

**Can one predict delays in US domestic flights with data regarding origin and destination, taxi times, departure delay, seasonal features (period of the year, day of the week...), etc?**

### Content

 - Initial Data Exploration: notebook for exploratory analysis, checking features, missing values, graphics and insights for feature extraction.
 - ETL: here data is read from .csv files and stored in a pandas dataframe. Then, an unused column is dropped, duplicate and NaN rows are deleted along with rows of cancelled flights, a sample of the data set is randomly taken, and default column names are changed for the ease of typing. Finally, methods to export/read the data frame to/from HDF5 are defined.
 - Feature Engineering: In the first part we retrieve the data from some HDF5 file, change some column formats to their relevant data type and drop other columns that aren't needed for the subsequent analysis. Then, we create the new columns that we need: months, days, days of the week, delayed and status. Finally, we do some feature transformations.
 - Model Definition and Evaluation: Here we use different algorithms to train classical models such as Random Forest Classifier and Support Vector Machine, as well as one deep learning algorithm from the scikit-learn package: the Multi-Layer Perceptron Classifier. Finally, we explore some metrics to check how our models perform and do a brief discussion about the best models.
 - The Lightweight IBM Cloud Garage Method for Data Science, Architectural Decisions Document.
