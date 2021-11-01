# knowledge-aware-med-classification
Contains the codebase for our paper **Knowledge-Aware Neural Networks for Medical Forum Question Classification** that is accepted for publication at the 30th ACM International Conference on Information and Knowledge Management (CIKM 2021) [arXiv](https://arxiv.org/abs/2109.13141), [DOI](https://dl.acm.org/doi/10.1145/3459637.3482128)

The codebase is based on huggingface transformers [Github codebase](https://github.com/huggingface/transformers). The lcf_ichi and lcf-associated codes is based on ABSA-Pytorch [Github codebase](https://github.com/songyouwei/ABSA-PyTorch/blob/master/models/lcf_bert.py)

![Proposed Knowledge-aware BERT model](medbert-ichi.png)

### Running Bert-plus models

The code files in the form of self-contained Jupyter notebooks is available at: **src/ProposedKnowledgeAwareModel/**
Please go through the notebook, which produces at the end a 'run_ichi.py'. 

```
python ./examples/ichi/run_ichi.py --model_type bert --model_name_or_path bert-base-uncased --do_lower_case --do_train --do_eval --data_dir ./data/ichi_dataset --max_seq_length 256 --per_gpu_eval_batch_size=16 --per_gpu_train_batch_size=16 --learning_rate 1e-4 --num_train_epochs 2 --output_dir ./tmp/ichi_bert_base_new --overwrite_output_dir
```

### Experiments and Results
The BERT and MedBERT models were trained and evaluated on two datasets: CADEC (multi-label) and ICHI (multi-class) (Datasets provided in the data directory). 

### Annotated CADEC, a multi-label medical forum question classificaton dataset
We annotate CADEC as a multi-label multi-class dataset, for the task of "Medical Forum Question Classification". Each data point is annotated by 0 and 1, across five information need categories. We also have an additional column, containing the extracted medical concepts using QuickUMLS tool. The annotated files can be found at **CADEC-Annotations/**

### ICHI, a multi-class medical forum question classification dataset
We obtain the ICHI data from rakshajalan/ECIR-2018 [Github codebase](https://github.com/rakshajalan/ECIR-2018/tree/master/ECIR-18_medical_question_classification/Dataset), and keep the same train-test data split.

## Citing MedBERT
If you use the labeled CADEC dataset or use MedBERT model, please cite the paper: 

```
@inproceedings{10.1145/3459637.3482128,
author = {Roy, Soumyadeep and Chakraborty, Sudip and Mandal, Aishik and Balde, Gunjan and Sharma, Prakhar and Natarajan, Anandhavelu and Khosla, Megha and Sural, Shamik and Ganguly, Niloy},
title = {Knowledge-Aware Neural Networks for Medical Forum Question Classification},
year = {2021},
isbn = {9781450384469},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3459637.3482128},
doi = {10.1145/3459637.3482128},
abstract = {Online medical forums have become a predominant platform for answering health-related
information needs of consumers. However, with a significant rise in the number of
queries and the limited availability of experts, it is necessary to automatically
classify medical queries based on a consumer's intention, so that these questions
may be directed to the right set of medical experts. Here, we develop a novel medical
knowledge-aware BERT-based model (MedBERT) that explicitly gives more weightage to
medical concept-bearing words, and utilize domain-specific side information obtained
from a popular medical knowledge base. We also contribute a multi-label dataset for
the Medical Forum Question Classification (MFQC) task. MedBERT achieves state-of-the-art
performance on two benchmark datasets and performs very well in low resource settings.},
booktitle = {Proceedings of the 30th ACM International Conference on Information &amp; Knowledge Management},
pages = {3398–3402},
numpages = {5},
keywords = {online health communities, clinical text classification},
location = {Virtual Event, Queensland, Australia},
series = {CIKM '21}
}
```
