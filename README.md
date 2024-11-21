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
            HAD-Using-Sensors/code/002_eda_phone_data.ipynb
            HAD-Using-Sensors/code/002_eda_watch_data.ipynb
#### Training
###### LSTM
            HAD-Using-Sensors/code/003_train_phone_data_lstm.ipynb
            HAD-Using-Sensors/code/003_train_watch_data_lstm.ipynb
###### GRU
            HAD-Using-Sensors/code/003_train_phone_data_gru.ipynb
            HAD-Using-Sensors/code/003_train_watch_data_gru.ipynb
            

## Code Contributors 
            1) Murthy L
            2) Moushumi Mahato
            3) Shashankgoud Patil

