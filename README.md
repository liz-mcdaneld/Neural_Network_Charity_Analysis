# Neural Network Charity Analysis

Neural Networks and Deep Learning Models

## Purpose

Alphabet Soup, a foundation, wants to predict where to make future investments. Machine learning and neural networks will be used to apply features on a provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. The initial file has 34,000 organizations and several columns that capture metadata about each organization from past successful fundings.

## Overview

-	Preprocessing Data for a Neural Network Model

-	Implement neural network models using TensorFlow.

-	Implement deep neural network models using TensorFlow.

-	Save trained TensorFlow models for later use.

-	Compile, Train, and Evaluate the Model

-	Optimize the Model

## Results

### Data Preprocessing

After preprocessing the data, the following questions can be answered:

#### What variable(s) are considered the target(s) for your model?

The targets of the model are checking to see if it is marked as successful in the DataFrame. This model would indicate that it has been successfully funded by AlphabetSoup.

#### What variable(s) are considered to be the features for your model?

The feature of the model is the ‘IS_SUCCESSFUL’ column.

![drop_is_successful](https://user-images.githubusercontent.com/103263248/191594763-a943d300-54fd-424d-8e2f-2bf587c4bf24.png)

#### What variable(s) are neither targets nor features, and should be removed from the input data?

The variables that are neither targets nor features and are removed from the data are the ‘EIN’ and ‘NAME’ columns. These will not increase the accuracy of the model, and their removal will help improve code efficiency. 

![drop_EIN](https://user-images.githubusercontent.com/103263248/191594814-2a98df9d-ca9f-4c45-8f15-d9f73db2a0d2.png)

![drop_EIN_NAME](https://user-images.githubusercontent.com/103263248/191594829-1bcc6e8f-f598-448a-ad49-32304c6d6c33.png)


### Compiling, Training, and Evaluating the Model

#### How many neurons, layers, and activation functions did you select for your neural network model, and why?

In the optimized model that was selected the following combination of layer provide the best results:

The first layer started with 80 neurons with a ‘relu’ activation. 
In the second layer, it dropped to 30 neurons and continued with the ‘relu’ activation. 
The third layer showed the ‘sigmoid’ activation seemed to be the good fit with 40 neurons. 
The fourth layer is the output layer with the ‘sigmoid’ activation.
This produced the best combination of loss to accuracy. 

#### Were you able to achieve the target model performance?

The target for the model was 75%. The best the model could produce is an accuracy of 72.5% 

![eval_model_ASC](https://user-images.githubusercontent.com/103263248/191594575-3622ceed-d399-43b5-8acc-68826e70d34a.png)

#### What steps did you take to try and increase model performance?

The data set was preprocessed, and columns were reviewed for necessity. Multiple attempts at model training were done in the AlphabetSoup_Optimization.ipynb file to find the best fit of neurons and layers. In the different attempts at model training, different activations, such as tanh, were tried. 


![attempt-one-opt-model-train](https://user-images.githubusercontent.com/103263248/191594120-6ff38ba3-fb52-4673-b4b4-2b8977c99667.png)

##### Attempt one's results:

![attempt-one-opt-model-train-eval](https://user-images.githubusercontent.com/103263248/191594200-8c2e1009-e683-4137-9451-4fc867f9b02e.png)


![attempt-two-opt-model-train](https://user-images.githubusercontent.com/103263248/191594518-08078966-24a3-45f4-840d-b63e1502a10a.png)

##### Attempt two's results:

![attempt-two-opt-model-train-eval](https://user-images.githubusercontent.com/103263248/191594434-61335fbc-b749-4093-a8ec-046270789d51.png)


![attempt-three-opt-model-train](https://user-images.githubusercontent.com/103263248/191594498-1ee3df4f-1dde-4823-982f-2116854c2187.png)

##### Attempt three's results:

![attempt-three-opt-model-train-eval](https://user-images.githubusercontent.com/103263248/191594535-40d3c4b6-c8de-4814-a9ae-d3c8b2eb89eb.png)

## Summary

The ‘relu’ and ‘sigmoid’ activations on the model training gave an accuracy of 72.5%. This is the best the model could produce after multiple attempts at different activations and neuron and layer combinations. The next step to optimize the mode and get better results would be to consider the random forest classifier as it is less effected by outliers. 
