# deep-learning-challenge

## Overview
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. 

## Results
### Data Preprocessing

* What variable(s) are the target(s) for your model?
  * Target Variable: IS_SUCCESSFUL
* What variable(s) are the features for your model?
  * Feature Variable:
    * NAME—Identification columns
    * APPLICATION_TYPE—Alphabet Soup application type
    * AFFILIATION—Affiliated sector of industry
    * CLASSIFICATION—Government organization classification
    * USE_CASE—Use case for funding
    * ORGANIZATION—Organization type
    * STATUS—Active status
    * INCOME_AMT—Income classification
    * SPECIAL_CONSIDERATIONS—Special considerations for application
    * ASK_AMT—Funding amount requested
* What variable(s) should be removed from the input data because they are neither targets nor features?
  * Variable to be removed:
    * EIN—Identification columns
    * STATUS—Active status
    * SPECIAL_CONSIDERATIONS—Special considerations for application
* Compiling, Training, and Evaluating the Model
  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
    * The first 2 models (AlphabetSoupCharity, AlphabetSoupCharity_Optimization), were composed by 2 layers:
      * First Layer: 80 neurons
      * Second Layer: 30 Neurons
    * A third model (AlphabetSoupCharity_Optimization_Test) was created with the following parameters:
      * First Layer: 90 Neurons
      * Second Layer: 50 Neurons
      * Third Layer: 30 Neurons
    * The Activation Functions used for all the Models were:
      * relu
      * sigmoid
        
  * Were you able to achieve the target model performance?
    * Yes. The target was achieved in the Optimmized Model. The accuracy incresed from 72.51% to 78.82%
  * What steps did you take in your attempts to increase model performance?
    * The steps taken were to remove EIN, STATUS and SPECIAL_CONSIDERATIONS columns. These last 2 columns were removed based 
Both Model were ran with the same Compiling, Training and Evaluation Methods. The main difference between the First and Optimized model are:
  * In the First Model (AlphabetSoupCharity), the EIN and NAME column were dropped
  * In the Optimized Model (AlphabetSoupCharity_Optimization), EIN, STAUS and SPECIAL_CONSIDERETAIONS were dropped because there wasn't a lot of variation.
  * In the Third Model (AlphabetSoupCharity_Optimization_Test), the neurons and layers were increased.

Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
By increasing the number of layers the accuracy increased but not in a signifcant number. It would be recommended to test it with more lahyers and neurons to coonfirm if the accuracy rate keeps increasing.
