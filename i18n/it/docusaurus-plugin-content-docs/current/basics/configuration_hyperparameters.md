---
sidebar_position: 100
---

# 🟢 LLM Settings


import Temperature from '../assets/temperature.svg';

<div style={{textAlign: 'center'}}>
  <Temperature style={{width:"500px",height:"300px",verticalAlign:"top"}}/>
</div>


# Introduzione

The output of LLMs can be affected by *configuration hyperparameters*, which control various aspects of the model, such as how 'random' it is. These hyperparameters can be adjusted to produce more creative, diverse, and interesting output. In this section, we will discuss two important configuration hyperparameters and how they affect the output of LLMs.

:::note
[for researchers] These are different from regular hyperparameters like learning rate, number of layers, hidden size, etc. 
:::

## Temperatura

La temperatura è un iperparametro di configurazione che può controllare la casualità dell'output del modello di linguaggio. Una temperatura alta produrrà risultati più creativi e meno prevedibili, mentre una temperatura bassa produrrà risultati più conservativi e comuni. Per esempio, se impostiamo la temperatura a 0.5, di solito il modello genererà un testo che è più prevedibile e meno creativo rispetto a se impostiamo la temperatura a 1.0.

## Top p

Top p, also known as nucleus sampling, is another configuration hyperparameter that controls the randomness of language model output. It sets a threshold probability and selects the top tokens whose cumulative probability exceeds the threshold. The model then randomly samples from this set of tokens to generate output. This method can produce more diverse and interesting output than traditional methods that randomly sample the entire vocabulary. For example, if you set top p to 0.9, the model will only consider the most likely words that make up 90% of the probability mass.

## Altri iperparametri rilevanti

Ci sono molti altri iperparametri che possono influire le performance del modello di linguaggio, come le penalità di frequenza e presenza. Non tratteremo di questo qui, probabilmente in futuro.

## How these hyperparameters affect the output

Temperature and top p can both affect the output of a language model by controlling the degree of randomness and diversity in the generated text. A high temperature or top p value produces more unpredictable and interesting results, but also increases the likelihood of errors or nonsense text. A low temperature or top p value can produce more conservative and predictable results, but may also result in repetitive or uninteresting text.

For text generation tasks, you may want to use a high temperature or top p value. However, for tasks where accuracy is important, such as translation tasks or question answering, a low temperature or top p value should be used to improve accuracy and factual correctness.

:::note
Sometimes more randomness can be helpful on tasks where accuracy is necessary when paired with [special prompting techniques](https://learnprompting.org/docs/intermediate/self_consistency).
:::




## Conclusioni

In summary, temperature, top p, and other model configuration hyperparameters are key factors to consider when working with language models. By understanding the relationship between these hyperparameters and the model output, practitioners can optimize their prompts for specific tasks and applications.

:::warning
Some models, like ChatGPT, **don't** let you adjust these configuration hyperparameters.
:::

By jackdickens382