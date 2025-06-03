# LSTM-vs-Distill-Bert
 This project aimed for testing the performance of LSTM and Transformers(Keeping in view of computation capacity, we used Distill Bert). Another reason was due to accuracy issues. 
 Our goal on each model was to have an accuracy of at least 60% on testing data.

 ### Dataset Overview and Project Workflow

- The dataset contains text samples labeled with one of the following genres:
  - `Promotion`
  - `Legal`
  - `Lyrical/Prose`
  - `Forum`
  - `Argumentation/Opinion`
  - `Instruction`
  - `News`
  - `Information/Explanation`
  - `Other`

- The original dataset includes samples in both **English** and **Slovenian**.
- Due to a significantly smaller portion of Slovenian samples, only the **English** dataset was used for training and evaluation.

### Data Processing and Modeling Steps

- Randomized and split the dataset into **training** and **testing** sets.
- Implemented **two deep learning models**:
  - One based on **LSTM**
  - One based on **Transformer** architecture (DistilBERT)
- Used **pre-trained word embeddings** to enhance model understanding.
- Performed **hyperparameter tuning** for optimal model performance.
- Conducted a **comparative evaluation** of both models.
- Performed **qualitative analysis** of predictions to interpret model behavior.
- Evaluated and reported **quantitative performance metrics** on the testing set.
- Compiled a **comprehensive summary report** covering:
  - Data preprocessing  
  - Model training  
  - Testing results  
  - Qualitative and quantitative analysis of both models

###  Models Information
Two models were utilized in this project:
- **LSTM**
- **DistilBERT**

###  Architecture Used
- **LSTM:** BiLSTM (128 + 64 units)
- **DistilBERT:** Pre-trained transformer model

###  LSTM Model Details
- **Vocabulary Size:** 10,000  
- **Max Sequence Length:** 300  
- **Embeddings:** Pre-trained GloVe vectors (300D)  
- **Architecture:**  
  - BiLSTM layers with 128 and 64 units  
  - Batch Normalization  
  - Dropout layers  
  - Dense Softmax output layer  

###  Training Details
- **Loss Function:** `sparse_categorical_crossentropy`  
- **Optimizer:** Adam (learning rate = 0.0005)  
- **Epochs:** 40 (with Early Stopping)
