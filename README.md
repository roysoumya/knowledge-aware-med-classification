# knowledge-aware-med-classification
Contains the codebase for our paper **Knowledge-Aware Neural Networks for Medical Forum Question Classification** that is accepted for publication at the 30th ACM International Conference on Information and Knowledge Management (CIKM 2021) [arXiv](https://arxiv.org/abs/2109.13141), [DOI](https://dl.acm.org/doi/10.1145/3459637.3482128)

The codebase is based on huggingface transformers Github [codebase](https://github.com/huggingface/transformers).

![Proposed Knowledge-aware BERT model](medbert-ichi.png)

### Running Bert-plus models

The code files in the form of self-contained Jupyter notebooks is available at: **src/ProposedKnowledgeAwareModel/**

### Experiments and Results
The BERT and MedBERT models were trained and evaluated on three datasets: CADEC and ICHI (Datasets provided in the data directory). 

### Annotated CADEC dataset
We annotate CADEC as a multi-label multi-class dataset, for the task of "Medical Forum Question Classification". Each data point is annotated by 0 and 1, across five information need categories. We also have an additional column, containing the extracted medical concepts using QuickUMLS tool. The annotated files can be found at **CADEC-Annotations/**




