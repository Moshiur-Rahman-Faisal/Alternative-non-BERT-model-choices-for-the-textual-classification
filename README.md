# Alternative non-BERT model choices for the textual classification in low-resource languages and environments

Natural Language Processing (NLP) tasks in non-dominant and low resource languages have not experienced significant progress. Although pre-trained BERT models are available, GPU-dependency, large memory requirement, and data scarcity often limit their applicability. As a solution, this paper proposes a fusion chain architecture comprised of one or more layers of CNN, LSTM, and BiLSTM and identifies precise configuration and chain length. The study shows that a simpler, CPU-trainable non-BERT fusion CNN + BiLSTM + CNN is sufficient to surpass the textual classification performance of the BERT-related models in resource-limited languages and environments. The fusion architecture competitively approaches the state-of-the-art accuracy in several Bengali NLP tasks and a six-class emotion detection task for a newly developed Bengali dataset. Interestingly, the performance of the identified fusion model, for instance, CNN + BiLSTM + CNN, also holds for other lowresource languages and environments. Efficacy study shows that the CNN + BiLSTM + CNN model outperforms BERT implementation for Vietnamese languages and performs almost equally in English NLP tasks experiencing artificial data scarcity. For the GLUE benchmark and other datasets such as Emotion, IMDB, and Intent classification, the CNN + BiLSTM + CNN model often surpasses or competes with BERT-base, TinyBERT, DistilBERT, and mBERT. Besides, a position-sensitive self attention layer role further improves the fusion models’ performance in the Bengali emotion classification. The models are also compressible to as low as ≈ 5× smaller through pruning and retraining, making them more viable for resource-constrained environments. Together, this study may help NLP practitioners and serve as a blueprint for NLP model choices in textual classification for low-resource languages and environments.

## Dataset

Dataser link: [**Kaggle**](https://www.kaggle.com/datasets/moshiurrahmanfaisal/bangla-ekman-six-emotion-dataseti)


## Embedding

Word embedding with `fastText` and context embedding with `BERT` was used. 




## Model Accuracy

From the dataset 80% data was used for training and 20% for testing.

#### Proposed models fusion models with self-attention.

| **Deep Neural Network Models** | **Accuracy (%)** 
| :-------- | :------- 
| CNN + attention + BiLSTM + CNN | 86.83%
| CNN + attn. + LSTM + CNN | 86.91% 


#### Transformer models from Hugging Face

|**BERT Models** | **Accuracy (%)** 
| :-------- | :------- 
| mBERT | 86.62%
| Bangla BERT | 86.17% 

Also the model comparison was done in `GLUE` benchmark dataset. 



## Referance

#### Read the paper for more details:
[Alternative non-BERT model choices for the textual classification in low-resource languages and environments](https://aclanthology.org/2022.deeplo-1.20) (Mustavi Maheen et al., DeepLo 2022)

