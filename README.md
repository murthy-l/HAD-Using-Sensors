# Human Activity Detection Using Phone and Watch Sensors
## Dataset
[WISDM Smartphone and Smartwatch Activity and Biometrics Dataset](https://archive.ics.uci.edu/dataset/507/wisdm+smartphone+and+smartwatch+activity+and+biometrics+dataset)

## Dataset Summary
| Metric                     | Value                     |
|----------------------------|---------------------------|
| Number of subjects         | 51                        |
| Number of activities       | 18                        |
| Minutes collected per activity | 3                   |
| Sensor polling rate        | 20Hz                      |
| Smartphone used            | Google Nexus 5/5X or Samsung Galaxy S5 |
| Smartwatch used            | LG G Watch               |
| Number of raw measurements | 15,630,426               |

18 activity are recorded and coded as follow

| Activity                   | Code |
|----------------------------|------|
| Walking                    | A    |
| Jogging                    | B    |
| Stairs                     | C    |
| Sitting                    | D    |
| Standing                   | E    |
| Typing                     | F    |
| Brushing Teeth             | G    |
| Eating Soup                | H    |
| Eating Chips               | I    |
| Eating Pasta               | J    |
| Drinking from Cup          | K    |
| Eating Sandwich            | L    |
| Kicking (Soccer Ball)      | M    |
| Playing Catch w/Tennis Ball| O    |
| Dribbling (Basketball)     | P    |
| Writing                    | Q    |
| Clapping                   | R    |
| Folding Clothes            | S    |

## Prerequisites :
python >= 3.8

    pip install -r requirements.txt

## Execution Steps:

#### Data Preprocessing
            code/001_data_collection_preprocessing_phone_data.ipynb
            code/001_data_collection_preprocessing_watch_data.ipynb
#### EDA
            code/002_eda_phone_data.ipynb
            code/002_eda_watch_data.ipynb
#### Feature extraction
Performs signal processing and generates processed dataset in dataset/ folder

            code/003_feature_extraction.ipynb

#### Training
Note: Prerequisite to execute above feature extraction since Logistic regression, Random forest and KNN works on feature extracted dataset.

###### Logistic regression
            code/004_1_train_logisticregression_phone.ipynb
            code/004_1_train_logisticregression_watch.ipynb

###### Random forest
            code/004_2_train_randomforest_phone.ipynb
            code/004_2_train_randomforest_watch.ipynb

###### KNN
            code/004_3_train_knn_phone.ipynb
            code/004_3_train_knn_watch.ipynb



###### LSTM
            code/004_4_train_lstm_phone.ipynb
            code/004_4_train_lstm_watch.ipynb
###### GRU
            code/004_5_train_gru_phone.ipynb
            code/004_5_train_gru_watch.ipynb
#### Results

###### Logistic regression
| Sensor                | Accuracy |
|-----------------------|----------|
| Phone Accelerometer   |  0.4472  | 
| Phone GyroScope       |  0.4001  |
| Watch Accelerometer   |  0.7150  |
| Watch GyroScope       |  0.6126  |

###### Random forest
| Sensor                | Accuracy |
|-----------------------|----------|
| Phone Accelerometer   |  0.8399  | 
| Phone GyroScope       |  0.6249  |
| Watch Accelerometer   |  0.8331  |
| Watch GyroScope       |  0.7332  |

###### KNN
| Sensor                | Accuracy |
|-----------------------|----------|
| Phone Accelerometer   |  0.6385  | 
| Phone GyroScope       |  0.4529  |
| Watch Accelerometer   |  0.62811 |
| Watch GyroScope       |  0.5216  |



###### LSTM
| Sensor                | Accuracy |
|-----------------------|----------|
| Phone Accelerometer   |          | 
| Phone GyroScope       |          |
| Watch Accelerometer   |          |
| Watch GyroScope       |          |
| Phone Accel & Gyro    |          |
| Watch Accel & Gyro    |          |
| All 4 sensor          |          |

Special case where 15 actions were classified
| Sensor                | Accuracy |
|-----------------------|----------|
| All 4 sensor          |          |

###### GRU
| Sensor                | Accuracy |
|-----------------------|----------|
| Phone Accelerometer   |          | 
| Phone GyroScope       |          |
| Watch Accelerometer   |          |
| Watch GyroScope       |          |
| Phone Accel & Gyro    |          |
| Watch Accel & Gyro    |          |
| All 4 sensor          |          |

Special case where 15 actions were classified
| Sensor                | Accuracy |
|-----------------------|----------|
| All 4 sensor          |          |

## Code Contributors 
            1) Murthy L
            2) Moushumi Mahato
            3) Shashankgoud Patil

