# Notes

## What is Machine Learning?
Programming computers so they can learn from data without being explicitly programmed. 

## Why use Machine Learning?
__Machine Learning__ is great for
* turning existing solutions for problems to less code and better performance 
* complex problems
* adapt to new data
* lots of data

## Types of Machine Learning Systems
There is
1. supervised vs. unsupervised
    * __supervised:__ classification, regression
    * __semi-supervised:__ usually a lot of unlabeled data and little label data
    * __unsupervised:__ cluster, visualization and dimensionally reduction, association rule learning, anamoly detection
    * __reinforcement learning__: The learningn system (aka agent) must learn by itself what is the best strategy (called policy) to get the most reward over time
2. online vs. batch
    * __online__: the system learns incrementally, data is feed to the model one by one instance of in "mini-batches"
        * _learning rate_: controlls how fast a model can adapt to the changes in the data
    * __batch__: the system is incapable of learning incrementally, it needs the whole data at once to be trained
        * _offline learning_: Train the system -> launch it -> retrain the model if new data available
3. instance-based vs. model-based
    * __instance based__: the system learns the examples (data) by heart, then generalizes to new cases using a similarity measure
    * __model-based__: Build a model that learns patterns in the data and use it to make predictions
        * _utility/cost function_: measure how good/bad your model performs and use this measure to maximize/minimize the correct/false predictions

## Main Challenges of Machine Learning
### Bad Data
1. Insufficient Quantity of Training Data
    * Data matters more than the algorithms -> __Better to have no data than to analyse "wrong" data!__
    * One question that came up very quickly to me is: __"Is more data always better"__? Quick Google Search got me to an [article](https://harbourfronts.com/machine-learning-is-more-data-always-better/) which makes the plausible statement of __data freshness__ (not sure if this term really exists, but I think it makes the idea clear). Resume: Older data that may not really be relevant for your business and therefore may hurt model performance. 
    * Another point I want to mention, is how easy/cheap or hard/expensive it is for your business to get new data (let's call it __data gathering costs__). This should definetly be considered at the project planning phase before any machine learning project starts. It should be considered at what point are potential gains in the model by gathering new data more important than the costs produced by the process of getting new data.
2. Nonrepresentative Training Data
    * __Sampling noise__: Nonrepresentative data as a result of chance
    * __Sampling bias__: Nonrepresentative data as a result of a flawed sampling method. 
3. Poor-Quality Data
    * Outliers, errors and noise will make it harder for a model to make good predictions. Discuss how to deal with missing data or wrong data / outliers. 
4. Irrelevant Features
    * Feature Engineering can be done by __feature selection__, __feature extraction__ or __feature creation__.
### Bad Models
1. Overfitting the Training Data
The model performs well on the training data but bad on the test data. Usually when the model is to complex and the model may learn the data by hard or adapt to noise in the data itself. Solutions may be
* Use a simpler model
* Gather more data
* Reduce the noise in the data
A common method to make a model simpler or to reduce the risk of overfitting is called __regularization__. This is a so called __hyper-parameter__ (a parameter of the learning algorithm and not the model itself), this means it has to be set prior to training and remains constant during training (usually).
2. Underfitting the Training Data
The model performs bad on the training and the test data. Usually the model is to simple to capture the underlying patterns in the data. Fix this with
* A more complex model
* Better features
* Reducing the contraints on the model (reduce hyper-paramter shrinkage)

### Testing and Validation



