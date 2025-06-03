# LSTM-vs-Distill-Bert
 This project aimed for testing the performance of LSTM and Transformers(Keeping in view of computation capacity, we used Distill Bert). Another reason was due to accuracy issues. 
 Our goal on each model was to have an accuracy of at least 60% on testing data.

 # About the Dataset
 The dataset contains text, each assigned a label with its corresponding genre and has one of the following labels
 'Promotion','Legal','Lyrical/Prose','Forum','Argumentation/Opinion','Instruction','News','Information/Explanation','Other'
 The dataset is contained both in English and Slovenian language, since the Solvenian dataset was quite low as compared to English, the Slovenian dataset was filtered out.
 Then applied deep learning-based classifiers to effectively predict the label of each text and performed the following tasks:
  •	Randomize the data and split it into training and testing sets.
  •	2 models were considered, one based on LSTM and another on transformers.
  •	Utilized pre-trained word embeddings in models.
  •	Fine-tuned the hyperparameters for optimal performance.
  •	Compared the performances of both models created in your experiments.
  •	Perform a qualitative analysis.
  •	Report the model performance on the testing set.
And at last, created a report summary of the complete processed for both model training and testing and also mention qualitative and quantitative analysis of both models’ performance.

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
