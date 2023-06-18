# DL_Final_Project Landmark Classification
- Use Kaggle notebook to train
## Topic
-	Google Landmark Recognition 2021
- [Kaggle](https://www.kaggle.com/competitions/landmark-recognition-2021)
- ![image](https://github.com/wzray07/DL_Landmark/assets/77890790/6fefa5c9-b4f2-4228-83f1-2f0d9961fd28)
## Data Analyze
- Data Amount : 1580470
- Class of Data : 81313
- ![image](https://github.com/wzray07/DL_Landmark/assets/77890790/2a7f38d4-ff9e-47bd-a907-afaf5d629975) ![image](https://github.com/wzray07/DL_Landmark/assets/77890790/073ff5af-bd1d-411d-a19c-820375d1ef4e) ![image](https://github.com/wzray07/DL_Landmark/assets/77890790/2fe56bd1-cf20-4aa4-a470-1bc4a8fb834a)
##	Data Preprocess
-	81313 Class choose the most amount of 30000 classes.
-	Each class choose 10 images ( random ) => 300000 Images
  - Advantage : Data Balance.
  -	Disadvantage : Not Enough Data.
-	Batch Size: 64 
-	Resize to image : [64, 64]

##	Model & Training Parameter
-	**EfficientNet – B7**
  -	Parameters : 140,616,960
-	Loss : CrossEntropyLoss
-	Learning Rate : 1e-3
-	Optimizer : radam
- Epoch : 20
- ![image](https://github.com/wzray07/DL_Landmark/assets/77890790/f169c092-26ee-49b0-b4ab-1542b93e2251)

-	**ResNet 50**
  -	Parameters : 55,587,032
-	Loss : CrossEntropyLoss
-	Learning Rate : 1e-3
-	Optimizer : radam
- Epoch : 20
- ![image](https://github.com/wzray07/DL_Landmark/assets/77890790/719ffd11-1e8b-43e9-9b6e-8ba646516a8c)

##	Evaluation
###	GAP : Global average precision
- ![image](https://github.com/wzray07/DL_Landmark/assets/77890790/398bd009-97a4-47b7-8151-e81999cdee39)

-	N is the total number of predictions returned by the system, across all queries
-	M is the total number of queries with at least one sample from the training set visible in it (note that some queries may not depict samples)
-	P(i) is the precision at rank i. (example: consider rank 3 - we have already made 3 predictions, and 2 of them are correct. Then P(3) will be 2/3)
-	rel(i) denotes the relevance of prediciton i: it’s 1 if the i-th prediction is correct, and 0 otherwise

##	Result & Compare
![image](https://github.com/wzray07/DL_Landmark/assets/77890790/461d5c1d-fe19-4661-8323-e7fffb6bb1df)


## Ranking

![image](https://github.com/wzray07/DL_Landmark/assets/77890790/e74bc719-0985-4e98-91cb-adf09f9b7b75)

##	Summary & Discuss
-	Because of the training limit, we can’t train too many data and train more bigger model.
-	EfficientNet is more better than ResNet 50, But EfficientNet is more bigger than ResNet 50
-	The score in Leaderboard is not good.
-	We should think how to train more class and keep the data balanced






 

