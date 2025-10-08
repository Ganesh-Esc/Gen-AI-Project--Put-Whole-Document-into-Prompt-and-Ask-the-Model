# Gen-AI-Project--Put-Whole-Document-into-Prompt-and-Ask-the-Model
# Understanding LLM Limitations: The Context Window Challenge

[![LangChain](https://img.shields.io/badge/LangChain-0086CB?style/for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNTYgMjU2Ij48cGF0aCBkPSJNMjI0IDQ4YTY0IDY0IDAgMCAwLTkwLjQ5IDBMMTE3LjI3IDY0SDEwNGE0MCA0MCAwIDEgMC00MCA0MGwtMTguNzUgMTguNzVBMTYgMTYgMCAwIDAgNDAgMTM2djY0YTMyIDMyIDAgMCAwIDMyIDMySDI0MGEzMiAzMiAwIDAgMCAzMi0zMmwzMi0zMmE2My44MSA2My44MSAwIDAgMC04MC04MCIgc3R5bGU9ImZpbGw6IzAwODZjYiIvPjwvc3ZnPg==)](https://www.langchain.com/)

A hands-on lab that explores a fundamental limitation of Large Language Models (LLMs): the **context window**. We will demonstrate why you can't simply put a whole document into a prompt and expect good results.

---

## 📖 Lab Overview

Large Language Models (LLMs) like GPT-4, Llama 3, and Mixtral have revolutionized natural language processing. However, they are not without their constraints. One of the most significant is the **context window length**—the maximum amount of text (measured in tokens) that a model can process at one time.

When dealing with lengthy documents for tasks like question-answering, a naive approach of feeding the entire text into the model's prompt will fail. This lab will demonstrate this limitation firsthand and explain why understanding the context window is essential for building effective, real-world LLM applications.

---

## 🔬 The Context Window Constraint

Think of the context window as the LLM's **short-term memory**. It's a fixed-size buffer that can only hold a certain amount of information.

* **What are the limits?** Different models have different limits. For example, GPT-3 has a context window of 4,096 tokens, while GPT-4 offers larger windows like 8,192 tokens.
* **What happens when you exceed the limit?**
    * **Truncation:** The input text is cut off. Any information beyond the token limit is completely ignored by the model, which can lead to incorrect or incomplete answers.
    * **Increased Cost & Latency:** Processing thousands of tokens is computationally expensive, leading to higher API costs and slower response times.

This limitation is especially critical for building a question-answering assistant. If the answer to a user's question lies in a part of the document that gets truncated, the model will fail, even though the information is technically "in" the source document.



---

## 🎯 Learning Objectives

After completing this lab, you will be able to:

1.  **Explain the Concept of Context Length:** Define what the context window is for LLMs and why it's a critical constraint.
2.  **Recognize the Limitations:** Demonstrate and understand the problems (e.g., information loss via truncation) that arise when inputting the entire content of a large document into a single prompt.

---

