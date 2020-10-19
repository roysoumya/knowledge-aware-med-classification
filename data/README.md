## Data

This directory contains all the data files.

### Directory Structure
Please describe what each directory contains and how it links to the different sections of the paper.<br/>
Here we have three directories as follows:
* Adverserial ICHI: This directory consists of the modified ICHI datasets used for adverserial attacks. We do semantically adverserial attacks that is we replace certain words by other words such that the meaning of the sentences do not change. For example we replace year(s) by yr(s) for creating one of our modified dataset. This helps us understanding the robustness of our model as an user might use yr(s) instead of year(s).
* Adverserial Oshumed: This directory consists of the modified OSHUMED datasets used for adverserial attacks. We do semantically adverserial attacks that is we replace certain words by other words such that the meaning of the sentences do not change. For example we replace suggest(s) by recommend(s) for creating one of our modified dataset. This helps us understanding the robustness of our model as an user might use recommend(s) instead of suggest(s).
* Train_Test_Split: This directory consists of the ICHI and OSHUMED dataset splitted in test and train sets. The tests train split of the Oshumed dataset was done based on the TextGCN Paper.
