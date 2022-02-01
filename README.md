# Neural_Network_Charity_Analysis

## Data Preprocessing:
  - The variable that was the target for my model was the sucess of the applicant in question(IS_SUCCESSFUL)
  - The variables that were the features for my model were the application types(APPLICATION_TYPE), affiliated sector of industry(AFFILIATION), government organization        classification(CLASSIFICATION), use case for funding(USE_CASE), organization type(ORGANIZATION), active status(STATUS), income classification(INCOME_AMT), special consideration for application(SPECIAL_CONSIDERATIONS) and funding amount requested(ASK_AMT). 
  - The identification columns (EIN and NAME) were neither targets nor features and were removed from the data.


## Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - In my neural network I had two hidden layers with eight neurons in the first layer and five neurons in the second. The two activation functions were "relu" and the output was "sigmoid". The ratio of nodes in the layers are in line with common usage within neural network use. "Relu" was chosen because it is both simple to implement and effective at overcoming the limitations of otheractivation functions. "Sigmoid" was chosen to classify and choose between two alternatives(Is_SUCCESSFUL).  
![Screenshot (209)](https://user-images.githubusercontent.com/90067477/152052893-649e4273-6d76-449c-b9a1-4a9cf2b0ef1b.png)

Were you able to achieve the target model performance?
  - In my network I wasn't able to achieve the target performance of 75%. My initial accuracy score was 53% before optimization efforts. 

  - To optimize model performance I changed (in separate tests) the amount of nodes, hidden layers and activation features. 
  - Test one changed the output layer activation to "tanh". This raised the accuracy to 55%. 
  
   ![Screenshot (210)](https://user-images.githubusercontent.com/90067477/152054497-97cb6187-ed6f-425e-9ecc-223068ff4486.png)
   
  - Test two added a third hidden layer with three neurons. This test also raised the accuracy to 55%. 
  
  ![Screenshot (211)](https://user-images.githubusercontent.com/90067477/152055034-b3a4f19a-db3a-4395-bdf2-98201bc5c808.png)

  - Test three changed the epochs from 100 to 300. The accuracy remained at 53%. 
  ![Screenshot (212)](https://user-images.githubusercontent.com/90067477/152055827-66d42396-4147-42e8-bd63-499ae617de3d.png)
  
In addition to the above tests I chose to run an optimization program with kerastuner. Using that tool I was able to reach 73% accuracy. 

![Screenshot (213)](https://user-images.githubusercontent.com/90067477/152057008-1db616e5-8de9-43ef-b478-91d3ccf8626c.png)

## Summary: 
This dataset and testing needs more work. Removing features or adding more data to test could aid in optimizing the neural network; I would also recommend that anyone working with neural networks begin their project using the kerastuner. It saves a lot of time. 
With the parameters that were used in this model I believe that a Random Forest classifier would work well. It has a faster performance(an issue that I ran into multiple times with the neural network) and could help with not overfitting the data.    
