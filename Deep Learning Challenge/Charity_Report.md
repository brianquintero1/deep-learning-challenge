For this part of the assignment, you’ll write a report on the performance of the deep learning model you created for Alphabet Soup.

The report should contain the following:

1. Overview of the analysis: Explain the purpose of this analysis.
    **The purpose of this assignment is to create a binary classifier using machine learning and neural networks on behalf of a nonprofit foundation. The classifier will be used as a tool to help the organization, Alphabet Soup, to predict whether applicants will be successful if funding is extended to them by Alphabet Soup.**

2. Results: Using bulleted lists and images to support your answers, address the following questions:

    - Data Preprocessing
        * What variable(s) are the target(s) for your model?
            **The target variable for my model is the binary 'IS_SUCCESSFUL' column found in the application_df.**
        * What variable(s) are the features for your model?
            **The variables used as features for the model were selected after dropping non-beneficial columns used as identifiers, 'EIN' and 'NAME'. The final feature variables are all the remaining columns from the application_df, also excluding the target variable. There were 9 remaining feature variables 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', 'ASK_AMT,**
        * What variable(s) should be removed from the input data because they are neither targets nor features?
            **The variables that should be removed from the input data are the two identifers 'EIN' and 'NAME'.**

    - Compiling, Training, and Evaluating the Model
        * How many neurons, layers, and activation functions did you select for your neural network model, and why?
            **This neural network model uses 80 neurons in hidden_nodes_layer1 and 30 neurons in hidden_nodes_layer2.The activation functions used for these two layers was the Rectified Linear Unit (ReLU) activation function. ReLu activation is a great choice for this binary classifier model because it produces sparse activations by outputing zeros for any negative input, which contributes to faster training and improved performance. It is useful when using hidden nodes because it is able to learn complex patterns in the data while keeping the model computationaly efficient.**
            
            **The output layer used the sigmoid activation which is appropriate for binary classification because it converts the final output to a probability score between 0 and 1. The model generated 3520 trainable parameters for the first hidden layer and 2430 parameters for the second hidden layer.**
        * Were you able to achieve the target model performance?
            **No, I did not achieve the target model performance of 0.75 accuracy. My model had a success rate of 0.726**
        * What steps did you take in your attempts to increase model performance?
            **I removed columns and made modifications to the training of the model to include other factors such as epochs, batch size, and verbosity**

3. Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
    **My deep learning model had an accuracy of around 73% in predicting successfully. I believe that modifying the model with additional data cleanup and hyperparamenter tuning, such as experimenting with different batch sizes or performing more iterations, would result in a better outcome. Another option is using more hidden layers which would help the model learn from more complex representations of the data. The only thing to keep in mind is not overfitting the model.**