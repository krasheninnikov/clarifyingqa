# ClarifyingQA dataset from the paper "Assistance with large language models"

The ClarifyingQA dataset consists of four-turn dialogues of the form (vague input question, clarifying question, clarification, answer), as well as clear questions that were intended by the vague input question. 
The first and last turns of the dialogues are provided from [AmbigQA](https://nlp.cs.washington.edu/ambigqa/) dataset (which itself is based on the [Natural Questions](https://ai.google.com/research/NaturalQuestions) dataset), and the second and the third turns we collected ourselves.

## Data collection

A subset of AmbigQA (611 vague, 1771 corresponding clear questions) is labeled as follows.
For each vague question which we treat as an input, we ask a human labeler to 
1) ask a clarifying question aimed to understand what is meant by the vague question, and 
2) respond to that clarifying question as if the intent behind the vague question was to ask one of the clear questions corresponding to it in AmbigQA. 


## Data structure
The dataset can be found at ``data/clarifyingqa.csv``, and has the following columns:
- **Id**: id matching that of the corresponding vague question in AmbigQA
- **Vague Question**: vague question [this is from AmbigQA]
- **Clear Question**: one of the clear questions that corresponds to the above vague question [this is from AmbigQA]
- **Clarifying Question**: a clarifying question human annotators asked to find out what is meant by the vague question [this is labeled by our annotators]
- **Clarification**: the response to the clarifying question given that the intent behind the vague question was to ask the clear question [this is labeled by our annotators]
- **Answers**: semicolon separated possible answers to the clear question [this is from AmbigQA]