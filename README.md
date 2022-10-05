# Neural_Network_Charity_Analysis
## Overview
AlphabetSoup, a Charity Foundation whom has donated over $10B in the past 20 years, wants to employ Deep Learning data analyzing algorithms to evaluate the impact of each of its donations and be able to determine which charities are high risk, or worth donating to. This exercise is an introduction to an advanced form of machine learning that recognizes patterns and features in input-data and provides a clear quantitative output. Using TensorFlow, neural network models will be implemented to develop a learning model that will accurately predict sound investments for the foundation


### Data Environment:
- TensorFlow2.0 programming
- python
- Google Colabortory



## Results

#### Data Preprocessing
* The Target variable for my model was the ‘Is_successful’ values
* The Features variable for my model were:
    * For  Optimization Trial 1 & Trial 2:
        * Status
        * Ask_Amount
        * Application_Type
        * Income_Amt
        * Classification
        * Special_Considerations
    * For Optimization Trial 3 & Trial 4:
        * Status
        * Ask_Amount
        * Application_Type
        * Income_Amt
* EIN & NAME were Feature variables that had no influence on the success of an Alphabet Soup Charity donation, and could be dropped from the dataset.

#### Compiling, Training, and Evaluating the Model
* Trial 1 model parameters tested:
    * Accuracy = 69%
    * 2  Layers
        * 1st: 20
        * 2nd: 10
    * Epoch = 50
* Target Model Performance: Failed 
* Trial 2 model parameters tested:
    * Accuracy = 53%
    * 3  Layers
        * 1st: 20
        * 2nd: 20
        * 3rd: 10
    * Epoch = 50
* Target Model Performance: Failed 
* Trial 3 model parameters tested:
    * Accuracy = 58%
    * 3 Layers
        * 1st: 50
        * 2nd: 30
        * 3rd:10
    * Removed Features:
        * Classification
        * Special_Considerations
    * Epoch = 50
* Target Model Performance: Failed 
* Trial 4 model parameters tested:
    * Accuracy = 53%
    * 2  Layers
        * 1st: 80
        * 2nd: 30
    * Removed Features:
        * Classification
        * Special_Considerations
    * Epoch = 50
* Target Model Performance: Failed 


Steps I took to try increase model performance involved trying to reduce the nodes to see if the initial nodes were too high, after the initial model of 2 layers of 80:30 nodes with 53% Accuracy, failed in Deliverable 2.
- Trial 2, I increased the number of layers to 3 and reduced the nodes to 20:20:10. After taken into account the size of the dataset, I proposed more layers would reach target performance.
- Trial 3, the dataset was again, precessed and additional feature variables were dropped, Classification & Special_Considerations. The nodes for the 3 layers were increased to 50:30:10. After considering that the input data may have unnecessary features the dataset was reprocessed and Special_Considerations and Classifications were determined to have a low influence.
- Trial 4, The same reprocessed data was used again, but the layers were reduced back to 2 layers with 80:30 nodes to mimic the higher accuracy score obtained in Optimization Trial 1

## Summary:
On a few random reruns of the code I was able to achieve 69-71% Accuracy but the average of the runs of the code in total (12xs) was concentrated around 58%, the average loss metric was between .87 and 1. And, The processing time for the deep learning models were not time favorable. To the extent, the dataset had a large number of value points in comparison to the few number of Feature variables, I would propose using a more traditional supervised machine learning model like the RandomForest classifiers. This specific dataset was not so complex for the necessary use of a Neural network. The processing time could have been savored and the weak learning algorithm and multiple decision tress would have been more suitable for the caliber of the input data. 
