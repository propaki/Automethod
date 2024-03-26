# Replication package for paper : "Automated Suggestion of Method Names According to Functional Descriptions"

# Overview:
mNamer introduces a novel approach to automatically suggest high-quality Java method names using Large Language Models (LLMs). Leveraging the advanced understanding capabilities of LLMs for natural language descriptions of method functionalities, mNamer combines specialized pre-processing and customized post-processing techniques, including semantics-driven analysis and reinforcement learning from human feedback. This method aims to align generated names with established naming conventions, enhancing code readability and maintainability.
Datasets
This repository includes two key datasets:
# Datasets:
There are two datasets are used to evalatute the approach
- English Dataset: Method Names with English Functional Descriptions (Dataset of Baseline).
- Chinese Dataset: Method Names with Chinese Functional Descriptions. The Dataset organized from [Java 11 API Reference](https://www.apiref.com/java11-zh/java.base/module-summary.html)
Each dataset is crucial for training and evaluating the models to ensure they perform effectively across linguistic boundaries.
# Corpus of Prompts: 
Included in the "OptiPrompts" folder is a carefully curated corpus of prompts, comprised of text files, designed to enhance the performance of ChatGPT in accurately generating Java method names based on functional descriptions. These prompts are crafted to elicit precise and contextually relevant responses from the model, adhering to a well-designed template that aligns with the naming conventions and requirements specific to Java methods.
# Supervised Fine Tuning (SFT) training corpus:
The Chinese-SFT-Training-Corpus.JSONL and English-SFT-Training-Corpus.JSONL files in the "SFT-Training-Corpus" folder are specifically tailored for fine-tuning the Large Language Model (LLM) to enhance its capability in generating method names from functional descriptions in Chinese and English. It contains a collection of high-quality conversation samples between two individuals. Each sample comprises a pair: a functional description and the corresponding method name, meticulously extracted through the Best-Example process. This corpus aims to improve the model's accuracy and fluency in handling Chinese language inputs, ensuring the generation of contextually appropriate and conventionally accurate method names.
# Baseline Model
Source code for the baseline model (BiLSTM with attention and copying mechanism) applied to both Dataset 1 and Dataset 2 is available, serving as a comparative benchmark for the mNamer's performance.
# mNamer
fine-tuned ready to chat ChatGPT4 extention availabe at https://chat.openai.com/g/g-T58v7ELEM-mnamer
The source code is the centerpiece of this repository, showcasing the application of BERT-based semantic model for both Semantic Driven Preprocessing and BERT-based RLHF in Postprocessing for LLMs to improve its method naming capabilities. This model represents a significant advancement in the field of automated method naming.

Getting Started
To get started with mNamer:
Install the required dependencies: pip install -r requirements.txt
Follow the instructions in the usage_instructions.md file for detailed steps on how to train and evaluate the models using the provided datasets and prompts.
Contribution
Contributions to LLM-MethodNamer are welcome. If you have suggestions for improvement or want to report bugs, please open an issue or submit a pull request.
