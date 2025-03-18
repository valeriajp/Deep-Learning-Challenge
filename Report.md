# Report Deep Learning Challenge

# **Overview**
Alphabet Soup, a nonprofit foundation, is looking for a tool that will assist it in choosing grant candidates that have the best likelihood of succeeding with their projects. Using the attributes in the given dataset and your understanding of machine learning and neural networks, you will develop a binary classifier that can forecast whether applicants will be successful if they are provided with funding from Alphabet Soup.

# **Data & Data Preprocessing**
The business team at Alphabet Soup granted access to a CSV that lists over 34,000 organizations that the company has funded throughout the years. Several columns in this collection include metadata about each organization, including:


- **EIN** and **NAME**—Columns for identification
- **APPLICATION_TYPE**—Alphabet Soup application type
- **AFFILIATION**—Affiliated sector of industry
- **CLASSIFICATION**—Government organization classification
- **USE_CASE**—Use case for funding
- **ORGANIZATION**—Organization type
- **STATUS**—Active status
- **INCOME_AMT**—Income classification
- **SPECIAL_CONSIDERATIONS**—Special considerations for application
- **ASK_AMT**—Funding amount requested

The results on the efficient use of funds were found in the column **´IS_SUCCESSFUL´**, which was used as the target variable (y).

Important preprocessing procedures included:

1. Since the ´EIN´ and ´NAME´ columns are neither targets nor features, they should be removed.
2. Lowering the distinct values in the columns labeled "CLASSIFICATION" and "APPLICATION_TYPE." A predetermined threshold was used to classify rare categories into a "Other" category.

# **Results, Compilation, Training & Model Evaluation**

Two models were created:

**First Model**

Summary of the first model:

<table style="border-collapse: collapse; width: 50%;">
  <tr style="background-color: #f2f2f2; text-align: left;">
    <th style="padding: 8px; border: 1px solid black;">Layer</th>
    <th style="padding: 8px; border: 1px solid black;">Output Shape</th>
    <th style="padding: 8px; border: 1px solid black;">Params</th>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">Dense_6 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 90)</td>
    <td style="padding: 8px; border: 1px solid black;">3,960</td>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">dense_7 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 50)</td>
    <td style="padding: 8px; border: 1px solid black;">4,550</td>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">dense_8 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 1)</td>
    <td style="padding: 8px; border: 1px solid black;">51</td>
  </tr>
</table>

The model employed "relu" activation functions, except for the output layer, which employed a sigmoid function. Following training on the preprocessed and cleaned data, the model's accuracy was 0.7233 and its loss was 0.5770 across 100 epochs.

Approximately 72.33% of the data can be explained by the model, according to this.

**Second Model (Optimization)**
Summary of the second model:


<table style="border-collapse: collapse; width: 50%;">
  <tr style="background-color: #f2f2f2; text-align: left;">
    <th style="padding: 8px; border: 1px solid black;">Layer</th>
    <th style="padding: 8px; border: 1px solid black;">Output Shape</th>
    <th style="padding: 8px; border: 1px solid black;">Params</th>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">Dense_18 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 90)</td>
    <td style="padding: 8px; border: 1px solid black;">3,960</td>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">Dense_19 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 50)</td>
    <td style="padding: 8px; border: 1px solid black;">4,550</td>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">Dense_20 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 1)</td>
    <td style="padding: 8px; border: 1px solid black;">51</td>
  </tr>
</table>


Except for the output layer, which employed a sigmoid function, the model's activation functions were "relu". This model was trained on the same preprocessed and cleaned data, and after 150 epochs, it achieved an accuracy of 0.7240 and a loss of 0.5907.

This small improvement in accuracy (72.40%) shows that the second model, which included more neurons and an extra layer, did not perform noticeably better than the first model. Even though it used more resources, the results were almost the same.

**Third Model (Optimization)**
Summary of the third model:

<table style="border-collapse: collapse; width: 50%;">
  <tr style="background-color: #f2f2f2; text-align: left;">
    <th style="padding: 8px; border: 1px solid black;">Layer</th>
    <th style="padding: 8px; border: 1px solid black;">Output Shape</th>
    <th style="padding: 8px; border: 1px solid black;">Params</th>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">Dense_24 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 80)</td>
    <td style="padding: 8px; border: 1px solid black;">3,520</td>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">Dense_25 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 30)</td>
    <td style="padding: 8px; border: 1px solid black;">2,430</td>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">Dense_26 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 1)</td>
    <td style="padding: 8px; border: 1px solid black;">31</td>
  </tr>
</table>

    Except for the output layer, which employed a sigmoid function, the model's activation functions were "relu". The data of the ASK_AMT variable, which included information on the amount of money requested from the organization for its projects, was arranged using bins in this model. Following 150 epochs of training, the model's accuracy was 0.7340 and its loss was 0.7339.

This suggests that roughly 73.40% of the data can be explained by the model.

**Fourth Model (Optimization)**
Summary of the fourth model:

<table style="border-collapse: collapse; width: 50%;">
  <tr style="background-color: #f2f2f2; text-align: left;">
    <th style="padding: 8px; border: 1px solid black;">Layer</th>
    <th style="padding: 8px; border: 1px solid black;">Output Shape</th>
    <th style="padding: 8px; border: 1px solid black;">Params</th>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">Dense_27 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 80)</td>
    <td style="padding: 8px; border: 1px solid black;">3,520</td>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">Dense_28 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 30)</td>
    <td style="padding: 8px; border: 1px solid black;">2,430</td>
  </tr>
  <tr>
    <td style="padding: 8px; border: 1px solid black;">Dense_29 (Dense)</td>
    <td style="padding: 8px; border: 1px solid black;">(None, 1)</td>
    <td style="padding: 8px; border: 1px solid black;">31</td>
  </tr>
</table>

Except for the output layer, which employed a sigmoid function, the model's activation functions were "relu". Following 150 epochs of training with the identical preprocessed and cleaned data (dropping variable ASK_AMT), this model produced an accuracy of 0.7287 and a loss of 0.5255.

The accuracy of this model is slightly higher (72.87%) than that of the second and third optimization models.

# **Summary & Conclusions**

1. Despite the dataset's high number of observations, more data could be required for in-depth analysis. Access to past data may also shed light on the sustained prosperity of groups that receive funding.

2. Reliability is demonstrated by the first model's ability to explain most of the target variable's results (72.33%) without overfitting.

3. Despite being more intricate and using more processing power, the improved models did not significantly outperform the original model. In order to get the best outcomes with the least amount of resources, it is crucial to optimize models.

Despite not achieving 75% accuracy, the first model seems to be the superior option because it successfully strikes a compromise between performance and simplicity.
