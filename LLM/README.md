---
description: https://www.youtube.com/watch?v=bCz4OMemCcA
layout: editorial
---

# Attention is All Your Need

## Recurrent Neural Networks (RNN)&#x20;

is sequential process, and need improvements.

* Slow computation for long sequences
*   Vanishing or exploding gradient

    d(`output`)/d(`input`) is a chain of  d(`next_state_function`)/d(`current_state_function`), so it may be too small if each gradient is < 1 or too large vice versa.&#x20;
* Difficulty in accessing information from long time ago, the last computation may not know much information after first computation, but as human we know they are more related.

## Transformer

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption><p>Transformer Model</p></figcaption></figure>

### &#x20;Input Embedding:&#x20;

1. Tokenize the input sentence (each token maybe more than single word)
2. Convert tokens into numbers that represent positions in a vocabulary training set
3. Embed a number to a vector of numbers that represnet meaning od the word (this is model-unique and may change along with the training process).  The _**size**_ of this is called the $$d_{model}$$.



<figure><img src=".gitbook/assets/image.png" alt=""><figcaption><p>Input Embedding</p></figcaption></figure>



### Positional Encoding

We want each token to carry some information about its position in the setence, so model can understand position relation of token.

An fixed vector of numbers (size is $$d_{model}$$) that represents the token position will be added to the embedding vector. Sum to the **Encoder input**.

The value in the position vector is caclulated by PE functions. PE only takes in position and 2i/2i+1, so it's not related to the token and can be applied to different sentences in one model.

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption><p>PE function</p></figcaption></figure>



### Multi-Head Attention

#### Self Attention

allows the model to relate words to each other

