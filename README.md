# Human Activity Detection Using Phone and Watch Sensors
## Dataset
[WISDM Smartphone and Smartwatch Activity and Biometrics Dataset](https://archive.ics.uci.edu/dataset/507/wisdm+smartphone+and+smartwatch+activity+and+biometrics+dataset)

## Dataset Summary
| Metric                         | Value                                  |
|--------------------------------|----------------------------------------|
| Number of subjects             | 51                                     |
| Number of activities           | 18                                     |
| Minutes collected per activity | 3                                      |
| Sensorspolling rate            | 20Hz                                   |
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



## Data Preprocessing
    code/001_data_collection_preprocessing_phone_data.ipynb
    code/001_data_collection_preprocessing_watch_data.ipynb
## EDA
    code/002_eda_phone_data.ipynb
    code/002_eda_watch_data.ipynb
## Feature extraction
Performs signal processing and generates processed dataset in dataset/ folder

    code/003_feature_extraction.ipynb

## Training
Note: It is prerequisite to execute above feature extraction since Logistic regression, Random forest and KNN works on feature extracted dataset.

### 1. Logistic regression
    code/004_1_train_logisticregression_phone.ipynb
    code/004_1_train_logisticregression_watch.ipynb

### 2. KNN
    code/004_3_train_knn_phone.ipynb
    code/004_3_train_knn_watch.ipynb

### 3. Random forest
    code/004_2_train_randomforest_phone.ipynb
    code/004_2_train_randomforest_watch.ipynb
    code/004_2_train_randomforest.ipynb

### 4. LSTM
    code/004_4_train_lstm_phone.ipynb
    code/004_4_train_lstm_watch.ipynb
    code/004_4_train_lstm.ipynb
### 5. GRU
    code/004_5_train_gru_phone.ipynb
    code/004_5_train_gru_watch.ipynb
    code/004_5_train_gru.ipynb
## Results

### Single Sensor

#### 1. Logistic regression
| Sensors               | Accuracy(%)|
|-----------------------|------------|
| Phone Accelerometer   |  39.57     |
| Phone Gyroscope       |  40.56     |
| Watch Accelerometer   |  73.06     |
| Watch Gyroscope       |  65.08     |

#### 2. KNN
| Sensors               | Accuracy(%)|
|-----------------------|------------|
| Phone Accelerometer   |  59.29     |
| Phone Gyroscope       |  44.20     |
| Watch Accelerometer   |  62.64     |
| Watch Gyroscope       |  57.03     |

#### 3. Random forest
| Sensors               | Accuracy(%)|
|-----------------------|------------|
| Phone Accelerometer   |  72.99     |
| Phone Gyroscope       |  63.81     |
| Watch Accelerometer   |  85.60     |
| Watch Gyroscope       |  76.60     |

#### 4. LSTM
| Sensors               | Accuracy(%)|
|-----------------------|------------|
| Phone Accelerometer   |  25.75     |
| Phone Gyroscope       |  49.37     |
| Watch Accelerometer   |  74.97     |
| Watch Gyroscope       |  76.57     |

#### 5. GRU
| Sensors               | Accuracy(%)|
|-----------------------|------------|
| Phone Accelerometer   |  30.10     |
| Phone Gyroscope       |  53.03     |
| Watch Accelerometer   |  78.38     |
| Watch Gyroscope       |  80.80     |

### Multi Sensors

#### 1. Random forest
| Sensors                        | Accuracy(%)|
|--------------------------------|------------|
| Phone Accel & Gyro             |  81.04     |
| Watch Accel & Gyro             |  90.26     |
| All 4 Sensors                  |  93.17     |
| All 4 Sensors (15 activities)¹ |  96.12     |

#### 2. LSTM
| Sensors                        | Accuracy(%)|
|--------------------------------|------------|
| Phone Accel & Gyro             |  52.79     |
| Watch Accel & Gyro             |  85.19     |
| All 4 Sensors                  |  85.11     |
| All 4 Sensors (15 activities)¹ |  89.32     |

#### 3. GRU
| Sensors                        | Accuracy(%)|
|--------------------------------|------------|
| Phone Accel & Gyro             |  58.18     |
| Watch Accel & Gyro             |  88.14     |
| All 4 Sensors                  |  88.06     |
| All 4 Sensors (15 activities)¹ |  92.27     |

¹ dropping "eating chips", "eating pasta", "eating sandwich" activities.


## Conclusion
   This project focused on analysing the WISDM dataset to classify human activities using a range of machine learning and deep learning models. Among the tested approaches, the Random Forest classifier stood out as the top performer, delivering the highest accuracy and computational efficiency. Its robust handling of feature importance and generalization across the dataset made it a reliable choice for this task.  
 
   Deep learning models, particularly LSTM and GRU, also showed strong potential. These models worked well in capturing temporal patterns and dependencies inherent in sequential data, showing their suitability for activity recognition tasks. However, further optimization through hyperparameter tuning and architectural adjustments could enhance their performance and fully leverage their strengths.  
 
   Future directions for this work could include integrating ensemble techniques to combine the strengths of different models, developing hybrid frameworks that utilize both traditional machine learning and deep learning, and employing more advanced preprocessing steps to improve data quality. These efforts could drive better performance, greater adaptability and deeper insights into human activity classification.


## Code Contributors
            1) Murthy L
            2) Moushumi Mahato
            3) Shashankgoud Patil

