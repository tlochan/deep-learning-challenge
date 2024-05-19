# deep-learning-challenge
Neural Network Analysis of Funding Application Success

Overview of the analysis: In this analysis on behalf of the Alphabet Soup Charity, we sought to leverage machine learning to determine which potential ventures would be most successful if funded by the nonprofit. Looking at 34,000 past funding events, we sought to evaluate which characteristics were most useful in predicting future organizations worthy of funding.
 
Results: 

  Data Preprocessing
* The target of the model is IS_SUCCESSFUL—Was the money used effectively? IN other words, which past organizations used the funding successfully.
* Feature variables include: NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION,
        USE_CASE, ORGANIZATION, STATUS,INCOME_AMT,SPECIAL_CONSIDERATIONS, & ASK_AMT
* Here we used metadata centered on the organization itself and also parameters 
            of the funding 
* Name of the company was originally omitted, and EIN was omitted in both 
           versions of the model

Compiling, Training, and Evaluating the Model
* The original version of the neural network had 2 Hidden layers (5 neurons/relu 
          for both) and 1 Output Layer (1 neuron/sigmoid) -- the thinking here was to 
          integrate all of the metadata into a binary classifier of successful or not
* This model only reached 73% accuracyafter 100 epochs, which didn't reach our 
          target efficacy
* ![model1]('./model1.png')
*The second, optimized version of the neural network added Name as a feature 
          varaible and binned less data as 'Other' for the application and classification 
          columns. My logic was to give more data points to the model to evaluate.
* The second layer was given 2 more Neurons, and I also added 2 Hidden Layers
       (7 Neurons/Sigmoid) & (5 Neurons/Sigmoid) to make the neural net more robust
* After these improvements, the model achieved 75.6% accuracy
* ![model2]('./model2.png')

   Summary: 
   Based on my analysis, the Keras Sequential Model was successfully deployed to predict whether an organization would successfully implement funding from Alphabet Soup. With an Accuracy of 75%, this model is a useful tool in predicting whether potential new entires would be fruitful endeavors but not one we should rely too heavily on. 

   Another type of model that would be useful for this type of classification is a Random Forest. This type of supervised machine learning excels at dealing with numerical and categorical features to output a binary target. 
   
