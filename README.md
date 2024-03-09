# Spoken-SQuAD Language Model

This repository contains an Extractive Question Answering (EQA) language model specifically trained on the Spoken-SQuAD dataset. It leverages a fine-tuned version of `bert-base-uncased` to answer questions based on spoken language context, addressing various Word Error Rates (WERs) to mimic real-world spoken language processing challenges.

## Dataset

The model is trained on the Spoken-SQuAD dataset, an adaptation of the SQuAD dataset with simulated spoken language modifications. The dataset includes various versions to represent different levels of noise as WER (Word Error Rate), simulating real-life spoken language inaccuracies.

You can find the Spoken-SQuAD data files here: [Spoken-SQuAD Dataset Repository](https://github.com/chiahsuan156/Spoken-SQuAD)

## Model

The model, hosted on Hugging Face, is available at: [rein5/bert-base-uncased-finetuned-spoken-squad](https://huggingface.co/rein5/bert-base-uncased-finetuned-spoken-squad). It uses the `bert-base-uncased` model as its backbone, fine-tuned for the EQA task on the Spoken-SQuAD dataset.

## Installation

Before running the provided Jupyter notebook (`eqa-lm-spoken-squad.ipynb`), ensure you have the following dependencies installed:

- torch
- transformers
- datasets
- accelerate
- huggingface_hub
- evaluate
- tqdm
- numpy
- json

You can install these packages using pip:

```bash
pip install torch transformers datasets accelerate huggingface_hub evaluate tqdm numpy
```

## Running the Notebook
1. Clone this repository to your local machine or Jupyter environment.
2. Ensure you have Jupyter Notebook or JupyterLab installed.
3. Open `eqa-lm-spoken-squad.ipynb` and execute the cells sequentially.

   **Note**: The notebook requires the Spoken-SQuAD dataset files mentioned above. Please download them and update the paths in the notebook accordingly.

## Evaluation

The model is evaluated on three versions of the Spoken-SQuAD dataset, reflecting different WER levels to simulate various noise conditions in spoken language:

- No noise (22.73% WER)
- Noise V1 (44.22% WER)
- Noise V2 (54.82% WER)

### Results:
- **Test Set (NO NOISE - 22.73% WER)** - Exact Match: 64.23%, F1 Score: 74.29%
- **Test V1 Set (V1 NOISE - 44.22% WER)** - Exact Match: 40.72%, F1 Score: 54.94%
- **Test V2 Set (V2 NOISE - 54.82% WER)** - Exact Match: 28.50%, F1 Score: 41.41%

## Contributing

Contributions to this project are welcome! Please submit a pull request or issue to propose changes or additions.

