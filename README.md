# AlphabetSoup
### Deep Learning using Neural Networks

# Background
From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received various amounts of funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

Using your knowledge of machine learning and neural network model building, you must create a binary classifier that is capable of predicting whether or not an applicant will be successful if funded by Alphabet Soup using the features collected in the provided dataset.

## Pre-Processing

**1) What variable(s) are considered the target for your model?**
  The Target for the model is the "Is-Successful" column; It signifies if the money was use effectively
  
**2) What variable(s) are considered to be the features for your model?**
    The Features of this Model are the Name, Application Type, Affiliation, Classification, Use_case, Organization, Income Amount, and Ask Amount

**3) What variable(s) are neither and should be removed from the input data?**
    EIN (Employer identificaiton) was dropped because the numbers could confuse the system into thinking its significant
    Special Considerations was dropped because there was only a small percentage of cases that had any special consideration, and special considerations cannot be quantified.
    Status was dropped because all rows were the same (1)
    
## Creating the Model
**How many neurons and layers did you select for your neural network model?**
  After testing multiple configurations, I achieved success with 3 Hidden layers; with various Neurons. After trying multiple configurations with only two hidden layers, adding a third layer using the sigmoid activation was able to achieve the desired result of over 75% accuracy.
  WE kept the Epochs at 100, because adding or subtracting Epochs didnt have a significant change in the accuracy result.


**Were you able to achieve the target model performance? What steps did you take to try and increase model performance?**
In order to achieve the desired results, I had to manipluate the data in different ways. Here are a few of the things that I attempted:

1) I played with dropping various columns; Which had some effect on the outcome; I mistakenly dropped the Name column, assuming that each row was unique; I realized my mistake and converted that column into data; this had the biggest impact on my accuracy score.

2) I attempted to manipluate the Ask_Amount information into buckets to see how much the amount would change my accuracy; in the end playing with the Ask_Amount as a feature resulted in decreased accuracy.

3) Added a third hidden layer, which ultimately allowed me to get past my 73% accuracy barrier.

**If you were to implement a different model to solve this classification problem, which would you choose? Why?**
Being a classificaiton issue, i feel that Random Forest Machine Learning could be used to solve this problem. This is because the Random Forest L can break down the dataset and the voting process could give similar results.
