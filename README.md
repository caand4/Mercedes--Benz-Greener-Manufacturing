# Mercedes Benz Greener Manufacturing

## Scenario
Since the first automobile, the Benz Patent Motor Car in 1886, Mercedes-Benz has stood for important automotive innovations. These include the passenger safety cell with a crumple zone, the airbag, and intelligent assistance systems. Mercedes-Benz applies for nearly 2000 patents per year, making the brand the European leader among premium carmakers. Mercedes-Benz is the leader in the premium car industry. With a huge selection of features and options, customers can choose the customized Mercedes-Benz of their dreams.

## Code Interpretation

#Import libraries and loading datasets
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/ca3c54d9-66b4-44a1-bd86-c0a9f52c32fd)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/a531f965-dba1-4c6c-a9ad-bcbedba9e2b6)
Check the shape for train and test dataset and view dataset.
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/609c8128-f126-4edd-a661-50de75dd9082)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/3693cd5a-0a1b-48c6-9efc-58482b72823c)

Drop the ID column in both train and test dataset. Remove variables where the variance is equal to zero and check for columns with null and unique values.
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/f9de567f-32b4-4602-9baa-8d8bb011bac4)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/7d3e59f9-e5ea-41ae-8566-c58d7b0d809c)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/bf033ae3-69f9-4294-80da-6119cd44b42c)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/5268137d-da61-4f71-88d0-0d44889592da)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/91502add-123e-4523-9ee0-2441cff4ccb7)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/3a5c271e-25d7-4d08-8127-9b77b8bacc36)

Label Encoding:

Check for columns having dtype: Object. Perform label encoder on those columns.

![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/1ff41cf8-b7c2-4ad4-bd1c-bb33955e9660)

Dimensionality Reduction:
Using PCA components with 98% variance will be retained. Separate X and y from the dataset and perform test train split to get the train and validation data. Apply n_components and experienced_variance_ratio on the PCA. Transform the following using pca for xgboost:
	X_train  training data (pca_fit_transform_X_train)
X_val  validation data(y_train)
test_df test data(pca_transform_X_test)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/445ab4fd-d3bf-4e8c-bb80-11eb16fdb485)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/04ae3271-03fa-46db-bb44-62cace9857af)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/f4b00ddf-d118-46d8-8445-cae86fc0ef3b)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/aeaa05ea-e5af-4ccd-887a-d19492ed4ca2)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/2db14c91-ca5e-4f71-8ac4-f63270e00583)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/56ea9952-0e66-4c0f-ae55-3b62365ce8d1)

Xgboost:
Build an xgboost model for linear regression and fit X_train and y_train in the model. Predict on pca_transform_X_test. Check RMSE for the model.
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/579c85f9-8841-455e-8bdd-d303faa1a0fc)
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/e2f25747-a324-4945-ab3b-a6d45ab4ae42)
A helpful task would be to create a different model and compare RMSE as highlighted below:
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/5059e5d1-6487-4999-abbd-96d68da5ca36)
























## Visualization
![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/514fd115-5f8e-4c3e-b3b9-b2ed8bb8f181)
This first image shows a comparison of the variance with all n_components.

![image](https://github.com/caand4/Mercedes--Benz-Greener-Manufacturing/assets/80293132/322697f7-d60c-4871-b66d-78c3d378b65f)
This second image shows how many of the components experience the 98% variance.




