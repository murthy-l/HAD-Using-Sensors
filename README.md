# Human Activity Detection Using Phone and Watch Sensors
## Dataset
[WISDM Smartphone and Smartwatch Activity and Biometrics Dataset](https://archive.ics.uci.edu/dataset/507/wisdm+smartphone+and+smartwatch+activity+and+biometrics+dataset)

## Dataset Summary
| Metric                         | Value                                  |
|--------------------------------|----------------------------------------|
| Number of subjects             | 51                                     |
| Number of activities           | 18                                     |
| Minutes collected per activity | 3                                      |
| Sensor polling rate            | 20Hz                                   |
| Smartphone used                | Google Nexus 5/5X or Samsung Galaxy S5 |
| Smartwatch used                | LG G Watch                             |
| Number of raw measurements     | 15,630,426                             |

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
            code/004_6_train_lstm.ipynb
###### GRU
            code/004_5_train_gru_phone.ipynb
            code/004_5_train_gru_watch.ipynb
            code/004_6_train_lstm.ipynb
#### Results

###### Logistic regression
| Sensor                | Accuracy |
|-----------------------|----------|
| Phone Accelerometer   |  46.80   | 
| Phone Gyroscope       |  40.20   |
| Watch Accelerometer   |  72.45   |
| Watch Gyroscope       |  61.39   |

###### Random forest
| Sensor                | Accuracy |
|-----------------------|----------|
| Phone Accelerometer   |  83.51   | 
| Phone Gyroscope       |  63.49   |
| Watch Accelerometer   |  82.75   |
| Watch Gyroscope       |  73.66   |

###### KNN
| Sensor                | Accuracy |
|-----------------------|----------|
| Phone Accelerometer   |  64.68   | 
| Phone Gyroscope       |  44.87   |
| Watch Accelerometer   |  63.23   |
| Watch Gyroscope       |  52.26   |



###### LSTM
| Sensor                | Accuracy |
|-----------------------|----------|
| Phone Accelerometer   |  25.75   | 
| Phone Gyroscope       |  49.37   |
| Watch Accelerometer   |  74.97   |
| Watch Gyroscope       |  76.57   |
| Phone Accel & Gyro    |  52.79   |
| Watch Accel & Gyro    |  85.19   |
| All 4 sensor          |  85.11   |

Special case where 15 activities* were classified
| Sensor                | Accuracy |
|-----------------------|----------|
| All 4 sensor          |  89.32   |

###### GRU
| Sensor                | Accuracy |
|-----------------------|----------|
| Phone Accelerometer   |  30.10   | 
| Phone Gyroscope       |  53.03   |
| Watch Accelerometer   |  78.38   |
| Watch Gyroscope       |  80.80   |
| Phone Accel & Gyro    |  58.18   |
| Watch Accel & Gyro    |  88.14   |
| All 4 sensor          |  88.06   |

Special case where 15 activities* were classified
| Sensor                | Accuracy |
|-----------------------|----------|
| All 4 sensor          |  92.27   |

* dropping "eating chips", "eating pasta", "eating sandwich" activities.

## Code Contributors 
            1) Murthy L
            2) Moushumi Mahato
            3) Shashankgoud Patil

