# Optional BERT checkpoint

This folder is prepared for a HuggingFace-style BERT sentiment model.

Included:

- `config.json`
- `tokenizer.json`
- `tokenizer_config.json`
- `training_history.json`

Not included in Git by default:

- `model.safetensors`

To enable real BERT inference in the Streamlit app, copy your trained weight file here:

- `models/bert/model.safetensors`
