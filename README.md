# Deep-Learning-Challenge

# **Background**
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received access to a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:
- **EIN** and **NAME**—Identification columns
- **APPLICATION_TYPE**—Alphabet Soup application type
- **AFFILIATION**—Affiliated sector of industry
- **CLASSIFICATION**—Government organization classification
- **USE_CASE**—Use case for funding
- **ORGANIZATION**—Organization type
- **STATUS**—Active status
- **INCOME_AMT**—Income classification
- **SPECIAL_CONSIDERATIONS**—Special considerations for application
- **ASK_AMT**—Funding amount requested
- **IS_SUCCESSFUL**—Was the money used effectively

# **Instructions**
**Step 1: Preprocess the Data**
Using your knowledge of Pandas and scikit-learn’s ![image](https://github.com/user-attachments/assets/4350877e-7c20-4f7f-bb1e-0c93c965fcaf), you’ll need to preprocess the dataset. This step prepares you for Step 2, where you'll compile, train, and evaluate the neural network model.
Start by uploading the starter file to Google Colab, then using the information we provided in the Challenge files, follow the instructions to complete the preprocessing steps.
1. From the provided cloud URL, read in the ![image](https://github.com/user-attachments/assets/47fc36f9-c5e3-48d8-abc7-bf4ed7bf0910) to a Pandas DataFrame, and be sure to identify the following in your dataset:
   - What variable(s) are the target(s) for your model?
   - What variable(s) are the feature(s) for your model?
2. Drop the ![image](https://github.com/user-attachments/assets/1215f82c-ad53-4368-8a4a-b367b0e54312) and ![image](https://github.com/user-attachments/assets/df715fd4-bc75-44c2-896f-61b8c54441e9) columns.
3. Determine the number of unique values for each column.
4. For columns that have more than 10 unique values, determine the number of data points for each unique value.
5. Use the number of data points for each unique value to pick a cutoff point to combine "rare" categorical variables together in a new value, ![image](https://github.com/user-attachments/assets/3d69f23d-5da8-4579-a122-6abea7ee4e1d), and then check if the replacement was successful.
6. Use ![image](https://github.com/user-attachments/assets/c24fad01-1f0d-448a-a4ce-bbed8052b9bb) to encode categorical variables.
7. Split the preprocessed data into a features array, ![image](https://github.com/user-attachments/assets/8acdbb84-bbda-4994-901b-077264d34c94), and a target array, ![image](https://github.com/user-attachments/assets/8d9e7882-eca4-4eb4-a4ee-b7a3eda0bc30). Use these arrays and the train_test_split function to split the data into training and testing datasets.
8. Scale the training and testing features datasets by creating a ![image](https://github.com/user-attachments/assets/1fc51d46-48b7-4107-9583-558d3f04face) instance, fitting it to the training data, then using the ![image](https://github.com/user-attachments/assets/650e939a-9a8a-4f0d-8af1-cb6c899611c8)
 function.

**Step 2: Compile, Train, and Evaluate the Model**
Using your knowledge of TensorFlow, you’ll design a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup-funded organization will be successful based on the features in the dataset. You’ll need to think about how many inputs there are before determining the number of neurons and layers in your model. Once you’ve completed that step, you’ll compile, train, and evaluate your binary classification model to calculate the model’s loss and accuracy.

1. Continue using the file in Google Colab in which you performed the preprocessing steps from Step 1.
2. Create a neural network model by assigning the number of input features and nodes for each layer using TensorFlow and Keras.
3. Create the first hidden layer and choose an appropriate activation function.
4. If necessary, add a second hidden layer with an appropriate activation function.
5. Create an output layer with an appropriate activation function.
6. Check the structure of the model.
7. Compile and train the model.
8. Create a callback that saves the model's weights every five epochs.
9. Evaluate the model using the test data to determine the loss and accuracy.
10. Save and export your results to an HDF5 file. Name the file ![image](https://github.com/user-attachments/assets/2e1d01e6-b6fe-4f77-a025-f10dff0deb78).

**Step 3: Optimize the Model**
Using your knowledge of TensorFlow, optimize your model to achieve a target predictive accuracy higher than 75%.

Use any or all of the following methods to optimize your model:
- Adjust the input data to ensure that no variables or outliers are causing confusion in the model, such as:
    - Dropping more or fewer columns.
    - Creating more bins for rare occurrences in columns.
    - Increasing or decreasing the number of values for each bin.
    - Add more neurons to a hidden layer.
    - Add more hidden layers.
    - Use different activation functions for the hidden layers.
    - Add or reduce the number of epochs to the training regimen.

**Note**: If you make at least three attempts at optimizing your model, you will not lose points if your model does not achieve target performance.

1. Create a new Google Colab file and name it ![image](https://github.com/user-attachments/assets/765a1ce6-35e9-4e7d-970a-65d3e703c104).
2. Import your dependencies and read in the ![image](https://github.com/user-attachments/assets/7b516427-d6af-43b9-bbb6-b5e5c4916cc1) to a Pandas DataFrame from the provided cloud URL.
3. Preprocess the dataset as you did in Step 1. Be sure to adjust for any modifications that came out of optimizing the model.
4. Design a neural network model, and be sure to adjust for modifications that will optimize the model to achieve higher than 75% accuracy.
5. Save and export your results to an HDF5 file. Name the file ![image](https://github.com/user-attachments/assets/5478de98-5159-4203-91e8-4576a896befb).

**Step 4: Write a Report on the Neural Network Model**
For this part of the assignment, you’ll write a report on the performance of the deep learning model you created for Alphabet Soup.

The report should contain the following:
1. Overview of the analysis: Explain the purpose of this analysis.
2. Results: Using bulleted lists and images to support your answers, address the following questions:
- Data Preprocessing
    - What variable(s) are the target(s) for your model?
    - What variable(s) are the features for your model?
    - What variable(s) should be removed from the input data because they are neither targets nor features?

- Compiling, Training, and Evaluating the Model
    - How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - Were you able to achieve the target model performance?
    - What steps did you take in your attempts to increase model performance?
3. **Summary**: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

**Step 5: Copy Files Into Your Repository**
Now that you're finished with your analysis in Google Colab, you need to get your files into your repository for final submission.
1. Download your Colab notebooks to your computer.
2. Move them into your Deep Learning Challenge directory in your local repository.
3. Push the added files to GitHub.

# **Requirements**
**Preprocess the Data (30 points)**
- Create a dataframe containing the ![image](https://github.com/user-attachments/assets/cc81297f-78ff-4993-bfa7-d20348a02851) data, and identify the target and feature variables in the dataset (2 points)
- Drop the ![image](https://github.com/user-attachments/assets/7e96d7e7-6b86-411f-9eef-f63075ff3b40) and ![image](https://github.com/user-attachments/assets/c319c278-ad2f-45b8-8cb9-09651886fe95) columns (2 points)
- Determine the number of unique values in each column (2 points)
- For columns with more than 10 unique values, determine the number of data points for each unique value (4 points)
- Create a new value called ![image](https://github.com/user-attachments/assets/6d281dd8-25f6-4ddb-959f-87631b19e48e) that contains rare categorical variables (5 points)
- Create a feature array, ![image](https://github.com/user-attachments/assets/1dc354dc-7024-42fd-bbb6-2c78ce78fc61), and a target array, ![image](https://github.com/user-attachments/assets/8bb9087c-9b97-4f64-bbff-6d9bcc8ea66c) by using the preprocessed data (5 points)
- Split the preprocessed data into training and testing datasets (5 points)
- Scale the data by using a ![image](https://github.com/user-attachments/assets/516e334f-1928-4e64-8e86-4d5e730fd1e6) that has been fitted to the training data (5 points)

**Compile, Train and Evaluate the Model (20 points)**
- Create a neural network model with a defined number of input features and nodes for each layer (4 points)
- Create hidden layers and an output layer with appropriate activation functions (4 points)
- Check the structure of the model (2 points)
- Compile and train the model (4 points)
- Evaluate the model using the test data to determine the loss and accuracy (4 points)
- Export your results to an HDF5 file named ![image](https://github.com/user-attachments/assets/8c1934d2-b986-4cf2-ba13-16927e02af57) (2 points)

**Optimize the Model (20 points)**
- Repeat the preprocessing steps in a new Jupyter notebook (4 points)
- Create a new neural network model, implementing at least 3 model optimization methods (15 points)
- Save and export your results to an HDF5 file named ![image](https://github.com/user-attachments/assets/c1a4dade-51eb-4edd-9f03-6f15a1242074) (1 point)

**Write a Report on the Neural Network Model (30 points)**
- Write an analysis that includes a title and multiple sections, labeled with headers and subheaders (4 points)
- Format images in the report so that they display correction (2)
- Explain the purpose of the analysis (4)
- Answer all 6 questions in the results section (10)
- Summarize the overall results of your model (4)
- Describe how you could use a different model to solve the same problem, and explain why you would use that model (6)

# **References**
IRS. Tax Exempt Organization Search Bulk Data Downloads.[https://www.irs.gov/](https://www.irs.gov/)
