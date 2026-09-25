This project explores parameter-efficient fine-tuning of Phi-2 for dialogue summarization using LoRA (Low-Rank Adaptation). I compared the base Phi-2 model against two LoRA configurations: a default setup targeting the query, key, value, and dense layers, and a lighter configuration targeting only the query and value projection matrices.


Both fine-tuned models improved over the vanilla Phi-2 model across ROUGE metrics. The default LoRA configuration achieved the strongest performance, while the Q/V-only setup reduced the number of trainable parameters by roughly 50% with only a modest reduction in training time and some loss in summarization quality.

**Key Results**

Default LoRA: ~20.97M trainable parameters, ~49 min training time

Q/V-only LoRA: ~10.49M trainable parameters, ~46.6 min training time

 - Both configurations outperformed the base Phi-2 model on ROUGE

 - Default LoRA produced the best overall summarization performance
