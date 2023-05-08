![image](https://user-images.githubusercontent.com/123495041/236913511-9f83bfea-4e56-49cd-8616-3161cfb3df4a.png)
# Classification_Spaceship_Titanic

## Project written as part of the course "Data Science after SDA bootcamp"

## The Kaggle Competition
The competition is organised by Kaggle and is in the GettingStarted Prediction Competition series. In this competition, you are supposed to predict predict which passengers were transported by the anomaly using records recovered from the spaceship’s damaged computer system. Submissions are evaluated on Classification Accuracy.
https://www.kaggle.com/competitions/spaceship-titanic/

## Technologies
Python 3.8.10

## Data
The dataset contains information on 12970 Spaceship Titanic passengers. Each observation contains information such as PassengerId,	HomePlanet,	CryoSleep,	Cabin,	Destination,	Age,	VIP,	RoomService,	FoodCourt,	ShoppingMall,	Spa,	VRDeck,	Name.

## Data mining
Prior to building the model, the data was analyzed to understand the relationship between the variables and the transportation of passengers.

![image](https://user-images.githubusercontent.com/123495041/236905705-affdb0fd-93b8-4d59-9c28-c509d994efcd.png)

![image](https://user-images.githubusercontent.com/123495041/236908524-1651ea9a-d446-4b99-89c0-0a0322d31113.png)

![image](https://user-images.githubusercontent.com/123495041/236908695-46d69aad-2ff5-45f7-a350-c8b37d53efbf.png)

## Missing values
![image](https://user-images.githubusercontent.com/123495041/236908853-1298e83f-6883-4816-87f3-6fd6b35456be.png)
As part of data processing, they were supplemented with missing values, primarily based on the information contained in the description of the competition data. For example, it could be concluded that if a person is in cryogenic sleep, they cannot spend money on additional services.
However, the relationship between age and any expenses on additional services
![image](https://user-images.githubusercontent.com/123495041/236908997-d4b7b1c6-976a-4ddc-9bd6-fd0c7fe1bb1b.png)

The remaining missing values were supplemented using the ImputationKernel method from the miceforest library.

## Models
Three models were used in the project: XGBoost, LightGBM and CatBoost. Each of the models was trained on data processed using two approaches to coding categorical variables

### Option 1: Ordinal Encoding
In the first approach, categorical variables were converted to numerical values using ordinal coding.

### Option 2: One-Hot Encoding
In the second approach, categorical variables were transformed using "one-hot" coding.

## Results
The best result was obtained for the CatBoost model using ordinal coding, achieving a classification accuracy of 81.7%.
The accuracy achieved based on the test data from kaggle was 80.8%, which translated into 192nd place out of 2641 teams on the leaderboard.
