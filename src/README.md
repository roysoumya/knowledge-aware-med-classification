### Directory Structure
* ProposedKnowledgeAwareModel: Contains the codes for reproducing the MedBERT architecture
* transformers: Contains the modified code from the ***huggingface/transformers*** Github codebase. We modify under the directory 'src/transformers'
* Text Classification: Contains of the codes used for Medical Text Classification for the Baseline Models. They were trained using the train set and evaluated using the test set provided in the data directory.
  * Baseline Models: It consists the codes for basic Machine Learning Models and Heirarchical Attention Network. The Machine Learning Models used were Naive Bayes, Support Vector Machine and Logistic Regression. For taking care of the imbalance in the datasets we used SMOTE. The Hierarchichal Attention network was used for extracting the Word and Sentence Attentions of various datapoints.
