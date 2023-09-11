# Utilizing Transformers for Translating Sentences from English to French

The goal of this assignment was to train an English to French translation model using the OPUS book translation dataset using the PyTorch Lightening framework.

## Requirements
1. Speeding up Transformers
2. Achieve a final loss of less than 1.8 during training

## Introduction to Data - [Opus Books](https://huggingface.co/datasets/opus_books)
   
The opus_books dataset, offered by Hugging Face, is an integral component of the OPUS (Open Parallel Corpus) initiative. The overarching objective of OPUS is to curate and furnish top-tier parallel corpora. This particular dataset places its emphasis on parallel textual content derived from books. As such, it stands as a valuable asset for the training and assessment of machine translation models, as well as for various other natural language processing endeavors.

## Efficient Training of Transformers
The Transformer model has become widely acclaimed in the realm of natural language processing (NLP) owing to its exceptional performance across diverse tasks. Nonetheless, training sizable Transformer models can demand substantial computational resources and time. To tackle these hurdles, this repository delves into a range of advanced training methodologies aimed at enhancing both the efficiency and effectiveness of the training process.

## Automated Mixed Precision
Automated Mixed Precision (AMP) is a technique that combines both 16-bit and 32-bit floating-point arithmetic to expedite training while preserving model accuracy. This approach leverages hardware acceleration to accelerate training without compromising model performance.
  ![image](https://github.com/Paurnima-Chavan/transformers-s16/assets/25608455/6584748d-8acf-4aae-8b25-55a3b2909339)

## Dynamic Padding
Dynamic padding is a strategy that enhances input sequence padding during training. Instead of uniformly padding all sequences to match the length of the longest sequence in the entire batch, adaptive padding individually pads each batch to the length of its longest sequence. This minimizes unnecessary computations and accelerates the training process.
  ![image](https://github.com/Paurnima-Chavan/transformers-s16/assets/25608455/cbccd42c-6514-4c2f-b303-b5f39fc84d83)


## Parameter Sharing
Parameter consolidation involves the sharing of model parameters among layers or components within the model. This can lead to a reduction in the overall number of parameters, resulting in improved memory efficiency and the potential for enhanced model generalization.
  ![image](https://github.com/Paurnima-Chavan/transformers-s16/assets/25608455/061841e6-b55c-442f-baf9-7ca3d6745d63)


## One-Cycle Learning Rate Policy
The One-Cycle Learning Rate Policy is a dynamic learning rate schedule that adjusts the learning rate throughout training to facilitate faster convergence and superior final performance. This policy entails a gradual increase and subsequent decrease in the learning rate during the training process.

## Model Training
Attained a loss of 1.499 within 20 epochs.
  ![image](https://github.com/Paurnima-Chavan/transformers-s16/assets/25608455/3b8a28d7-7cb8-400d-97b0-0fb6975f671b)
