# Overview

This analysis report is for reviewing the performance of the neuro-network for the Alphabet soup.

## Data Preprocessing

* target is the `is_successsful` column, which is a binary classification target, either 1 or 0.
* features for this task are all the columns from the application_df without "EIN", "NAME" and the target column `is_successful`.

## Compilling, Training, Evaluating the Model

* for my neuro-network of the optimisation model, I use 3 hidden layers and set each layer number of neurons to be
86, 50, 24. But I specifically set the input layer, which the unit of neurons is equal to the total number of features. The number of neurons in each hidden layer is arbitary. Mainly random trying.
* After the 3 optimisation trails. I did not achieve the target model performance (which is >= 75%).
* My optimisations involves 3 stages, first is to increase the number of hidden layer from 2 hidden to 3. Then I increased the units of neuron per hidden layer and alter the activation functions. The last optimisation is to change the learning rate and increase the epochs from 100 to 200.

## Summary:

So after the 3 attempts of trying to optimise the model to reach >=75% of accuracy. Despite faliure, these results indicates that not always the changes will result in model improvement, in reality, it's common for model after several changes that no or little improvements, or even downtrending.
So for this task. in order to figure the better parameters, consider using the Keras-tuner to find the optimal params and hyperparameter would be used.
Also, for approches other than using deep-learning, another way for this task could be using random-forrest classifier. As this datasets contains many features that after encoding it result in sparse matrix, where decision-tree like model would be suitable for handeling high-dimension data, as well as feature importance selection which suitable for handeling sparse features.
