# 🧠 DeepSeek-RAG: Retrieval-Augmented Generation on Wikipedia with DeepSeek Model

## 📖 Overview
This project implements a Retrieval-Augmented Generation (RAG) system based on the DeepSeek-R1-Distill-Qwen-14B model, specifically designed to answer questions using the Wikipedia dataset. 

## ⚙️ Technologies Used
LangChain: A framework for building applications powered by language models.
Chroma: A vector database for efficient document retrieval.
BM25 Retriever: A classic retrieval model for document ranking.
BGE-Embedding: Bi-directional Generative Embedding.
BGE reranker: A powerful reranking algorithm that refines retrieved document.

## 🛠️ Installation
To get started, install the required dependencies using pip:
```bash

```

## 📝 Example
Here's an example of how the system works:
```bash
rag = WikiRAG()
question = "When did Lincoln begin his political career?"
answer = rag.ask(question)
print(f"Question: {question}")
print(f"Answer: {answer}")
```

```bash
question：When did Lincoln begin his political career?
answer：
You are a professional assistant, please strictly follow the context of the source:
        [Source：datasets/rag_mini_wikipedia.txt，type：normal]
Lincoln began his political career in 1832, at age 23, with an unsuccessful campaign for the Illinois General Assembly, as a member of the Whig Party. He ran eighth in a field of 13 candidates.

[Source：datasets/rag_mini_wikipedia.txt，type：normal]
to the areas where it already existed, and placed on the 'course of ultimate extinction... .'"  Lincoln won the Republican Party nomination in 1860 and was elected president later that year. During his term, he helped preserve the United States by leading the defeat of the secessionist Confederate States of America in the American Civil War. He introduced measures that resulted in the abolition of slavery, issuing his Emancipation Proclamation in 1863 and promoting the passage of the Thirteenth Amendment

[Source：datasets/rag_mini_wikipedia.txt，类型：normal]
Lincoln had been practicing with the broad sword. Two years later, Lincoln entered law practice with William Herndon, a fellow Whig. In 1854, both men joined the fledgling Republican Party. Following Lincoln's death, Herndon began collecting stories about Lincoln and published them in Herndon's Lincoln. The first photograph ever taken of Mary Lincoln, a daguerreotype by Shepherd in 1846. On November 4 1842 Lincoln married Mary Todd, daughter of a prominent slave-owning family from Kentucky. The couple had

        Think through the steps and answer:When did Lincoln begin his political career?
        If context information is insufficient, specify the missing information. Finally, give a structured answer.</think>
Okay, so I need to figure out when Abraham Lincoln began his political career. I'll start by looking at the provided context from the source datasets. 

The first source mentions that Lincoln began his political career in 1832 at the age of 23, running for the Illinois General Assembly as a member of the Whig Party, but he was unsuccessful. That seems pretty straightforward. It clearly states the year he started, so that should be the answer.

Looking at the second source, it talks about Lincoln winning the Republican Party nomination in 1860 and being elected president that year. While this is important, it's about a later part of his career, not the beginning. So this doesn't add new information about when he started.

The third source discusses Lincoln practicing with a broad sword and entering law practice with William Herndon in 1854. It also mentions his marriage in 1842 and his involvement with the Republican Party in 1854. While this provides additional context about his personal life and later political activities, it doesn't directly answer when he began his political career.

Putting it all together, the first source is the most relevant because it explicitly states the year Lincoln started his political career. The other sources provide supplementary information but don't contradict or add to the specific question about the start date.
</think>

Abraham Lincoln began his political career in 1832 at the age of 23 when he ran for the Illinois General Assembly as a member of the Whig Party. 

**Answer:**  
Abraham Lincoln began his political career in 1832.
```
