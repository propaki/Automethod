# mNamer
mNamer: A tool leveraging LLMs to auto-suggest descriptive method names from functional descriptions. It uses a multistage training approach to bridge semantic gaps, enhancing code quality
Datasets
This repository includes two key datasets:
# Dataset 1:
Method Names with English Functional Descriptions.
# Dataset 2:
Method Names with Chinese Functional Descriptions.
Each dataset is crucial for training and evaluating the models to ensure they perform effectively across linguistic boundaries.

# Corpus of Prompts
A curated corpus of prompts is provided to optimize ChatGPT's performance in generating accurate method names from functional descriptions. These prompts are tailored to encourage precise and contextually relevant outputs from the model.
# Supervised Fine Tuning (SFT) training corpus:
# Chinese-SFT-Training-Corpus.JSON
A JSON file to fine tune the LLM with quality conversations between two indviduals using samples (pair of functional description and method name) of Chinese axtracted by Best-Example process. 
# English-SFT-Training-Corpus.JSON
A JSON file to fine tune the LLM with quality conversations between two indviduals using samples (pair of functional description and method name) of English axtracted by Best-Example process.
# Source Code:
# Baseline Model
Source code for the baseline model (BiLSTM with attention and copying mechanism) applied to both Dataset 1 and Dataset 2 is available, serving as a comparative benchmark for the mNamer's performance.
# mNamer
The source code is the centerpiece of this repository, showcasing the application of BERT-based semantic model for both Semantic Driven Preprocessing and BERT-based RLHF in Postprocessing for LLMs to improve its method naming capabilities. This model represents a significant advancement in the field of automated method naming.

Getting Started
To get started with mNamer:
Install the required dependencies: pip install -r requirements.txt
Follow the instructions in the usage_instructions.md file for detailed steps on how to train and evaluate the models using the provided datasets and prompts.
Contribution
Contributions to LLM-MethodNamer are welcome. If you have suggestions for improvement or want to report bugs, please open an issue or submit a pull request.
