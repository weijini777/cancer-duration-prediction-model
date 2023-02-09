# Cancer Duration Prediction Model

This model predicts the general duration of a cancer related study based on the study's title name and brief summary

## How does it work?
1. I retrieved all the data from [ClinicalTrials.gov](https://clinicaltrials.gov/ct2/home), a database full of medical studies.
2. Parsed through the XML Tree, and took the relevant data I needed for the model which are the "title", "summary", "start date", "completion date", "NCT ID".
3. Turned all of the data into a pandas dataframe for furthur analysis 
4. Preprocessed the title and summary through converting to base form -> tokenization -> vectorization
5. Set up a LSTM neural network model that we will use for training the data
6. Train our designated train data to create prediction model
7. Test our designated test data and yield the accuracy of the model

## Ways to improve
Use a larger dataset: I only imported 10,000 cases, I can download and use the entire ClinicalTrials.gov data set
Optimize the LSTM neural network
Introduce more feautures besides just title and summary 
