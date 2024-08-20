# MANTRA: Minkowski-Aligned Neural Training for Robustness Against Adversaries


![Adversarial Attacks](https://img.shields.io/badge/Prompt-Injection-yellow.svg?style=plastic)
![Large Language Models](https://img.shields.io/badge/LargeLanguage-Models-green.svg?style=plastic)

## Abstract
Despite significant progress in defense mechanisms focused on textual manipulation, a thorough understanding of adversarial vulnerabilities in Large Language Models (LLMs) remains lacking. Geometric approaches have shown promise in unraveling the complexities of deep learning models. In this context, we introduce a novel geometric perspective to tackle adversarial challenges. Our proposed MANTRA framework utilizes vector embeddings (e.g., Word2Vec) and Minkowski geometry to identify and mitigate hidden adversarial vulnerabilities within the model's structure. This framework offers a mathematically rigorous foundation for enhancing LLM resilience against diverse attacks. Unlike traditional defenses, our approach reduces computational overhead by deriving bounds that depend solely on the distribution of adversarial prompts, rather than the original prompts. This advancement allows for a more in-depth exploration of the model’s black-box nature, paving the way for the development of more robust and secure language models.


## Quick Start
- **Get code**
```shell 
git clone https://github.com/Phani-61/mantra.git
```

- **Build environment**
```shell
cd Mantra
conda create -n Mantra python=3.9
conda activate Mantra
pip install -r requirements.txt
```

- **Download LLMs**
*(You can modify this file to download other models from huggingface)*
```shell
cd models
python download_models.py
cd ..
```

- **Mantra-Framework**
```shell
python mantra_framework.py
```

- **Get responses**
```shell
python get_mantra_response.py --evaluate duplicate_sentence_detection --path results/eval/llama3/static/momentum_1.0/token_length_150/target_0/0_5_20_normal.json
python get_mantra_response.py --evaluate summarization --path results/eval/llama3/static/momentum_1.0/token_length_150/target_0/0_5_20_normal.json
python get_mantra_response.py --evaluate grammar_correction --path results/eval/llama3/static/momentum_1.0/token_length_150/target_0/0_5_20_normal.json
python get_mantra_response.py --evaluate natural_language_inference --path results/eval/llama3/static/momentum_1.0/token_length_150/target_0/0_5_20_normal.json
python get_mantra_response.py --evaluate hate_detection --path results/eval/llama3/static/momentum_1.0/token_length_150/target_0/0_5_20_normal.json
python get_mantra_response.py --evaluate sentiment_analysis --path results/eval/llama3/static/momentum_1.0/token_length_150/target_0/0_5_20_normal.json
python get_mantra_response.py --evaluate spam_detection --path results/eval/llama3/static/momentum_1.0/token_length_150/target_0/0_5_20_normal.json
```

## Acknowledge
Some of our codes are built upon [llm-attack](https://github.com/llm-attacks/llm-attacks).
