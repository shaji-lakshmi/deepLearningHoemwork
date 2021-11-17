# Deep Learning Homework: Charity Funding Predictor

**Purpose:** 
The purpose of this project is to use neural networks to predict the success of applicatns that are funded by the non-profit foundation AlphabetSoup.

**Processing The Data**:
    What variable(s) are considered the target(s) for your model?
    * I used the "IS_SUSCESSFUL" variable as my target
    What variable(s) are considered to be the features for your model?
    * All variables aside from "IS SUCESSFUL" was utilized as features for model
    What variable(s) are neither targets nor features, and should be removed from the input data?
    * I removed the columns titled "EIN" and "NAME" were removed from the inpud data
    
  * Compiling, Training, and Evaluating the Model
    How many neurons, layers, and activation functions did you select for your neural network model, and why?
    * I started my neural network model with two hidden layers and utilizing 'relu' and 'sigmoid' activation functions.
    * Defined my neurons in the following way:
         num_first = len(X_train_scaled[0])*2
         num_second = 50
    Were you able to achieve the target model performance?
     I wast not able to achieve the target model performance. The result that I yeilded was the following:
     268/268 - 1s - loss: 0.5591 - accuracy: 0.7290 - 1s/epoch - 4ms/step
     Loss: 0.5591133236885071, Accuracy: 0.7289795875549316
    * What steps did you take to try and increase model performance?
      
     **For my first attempt at optimizationa**, I tried to reduce my neurons significantly by reducing my inputs to the following:
         num_first = 80
         num_second = 10
     I kept the same amount of layers and same activation functions. I yielded the following result: 
     268/268 - 0s - loss: 0.5530 - accuracy: 0.7299 - 395ms/epoch - 1ms/step
     Loss: 0.5529734492301941, Accuracy: 0.729912519454956
     
     **For my second attempt at optimizationa**,  I added an additional layer and same activation functions. My inputs are defined below:
        num_first = 80
        num_second = 10
        num_third = 2
     I yielded the following result: 
     268/268 - 0s - loss: 0.5541 - accuracy: 0.7284 - 407ms/epoch - 2ms/step
     Loss: 0.5540666580200195, Accuracy: 0.7283964753150946
     
     **For my third attempt at optimizationa**, I tried to reduce my neurons further by defining my inputs to the following:
        num_first = 15
        num_second = 10
     I added an additional layer and same activation functions. I yielded the following result: 
     268/268 - 0s - loss: 0.5519 - accuracy: 0.7305 - 369ms/epoch - 1ms/step
     Loss: 0.551887571811676, Accuracy: 0.7304956316947937
     
   **Summary**: 

   Even with my attempts to optimize the neural networks, I was short of 75%.

