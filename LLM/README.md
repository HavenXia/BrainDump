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

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption><p>Transformer Model</p></figcaption></figure>

&#x20;
