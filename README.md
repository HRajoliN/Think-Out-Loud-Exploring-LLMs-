<div align="center">
  <h1>🗣 Let's Think Out Loud: Large Language Model Exploration</h1>
</div>

---

In this exploration, we aim to delve deeply into the details and concepts within the realm of Large Language Models (LLMs). This journey is not about having all the answers upfront but about thinking out loud, openly sharing ideas, revisiting thoughts, and refining our understanding as we progress. Mistakes and course corrections are not just expected but embraced as part of the process.

This repository is a collaborative space where every comment, suggestion, or insight is valuable and can lead to meaningful discoveries. Together, let’s embark on this exciting adventure into the world of LLMs and uncover their incredible potential.

Let’s get started,

---

## 📌 How Does LLM Generate an Answer?

LLMs leverage the **autoregressive method**, where the next token in a sequence is predicted based on all previously generated tokens. This approach enables LLMs to generate text step-by-step, with each token conditioned on the context of prior tokens, allowing coherent and contextually relevant outputs. Actually, the words come from:

<div style="text-align: center; line-height: 1.8;">
   💥  <strong>Auto:</strong> "Self" – It refers to the fact that the model relies on its own previous outputs (or previous values in a sequence) to make predictions. <br>
   💥  <strong>Regressive:</strong> "Based on dependencies" – Each prediction depends on the values that came before it in the sequence.
</div>
<br>

> *Example: The LLM wants to answer this question "What is the capital of France?"*
> <p align="center">
> <img src="Figures/LLM_auto_reg.png" alt="LLM Autoregressive Process" width="600">
> </p>
> The above figure illustrates the autoregressive process step by step:  

>  1. **Step 1**: The input prompt *"What is the capital of France?"* is fed into the LLM, which predicts the first token: **"It"**.  
> >    - Context so far: *"What is the capital of France? It"*.  

>  2. **Step 2**: The model takes the updated context and predicts the next token: **"is"**.  
> >    - Updated context: *"What is the capital of France? It is"*.  

>  3. **Step 3**: With the expanded context, the model generates the next token: **"Paris"**.  
> >    - Final context: *"What is the capital of France? It is Paris"*.

<div style="text-align: center; line-height: 1.8;">
   ✅  <strong>Token-by-Token:</strong> Predictions are made one word at a time. <br>
   ✅  <strong>Context Matters:</strong> Each prediction uses the original prompt + previous outputs as input.
</div>
