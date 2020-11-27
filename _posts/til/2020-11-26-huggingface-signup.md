---
title:  "Joining the Hugging Face Community"
description: "Signing up to Hugging Face"
category: til
tags: huggingface
---

I have signed up to Hugging Face: https://huggingface.co/albertvillanova

## Share your model

These are the instructions I have been given to share a model.

You can now create a model repo directly from the website, [here](https://huggingface.co/new).

You can also upload/share your models from the [/transformers](https://github.com/huggingface/transformers) library, using our CLI.

See more info in the [docs](https://huggingface.co/transformers/model_sharing.html), or read the instructions below:

- First, login on your machine, using the same credentials as huggingface.co/join:
  ```sh
  transformers-cli login
  ```

- Create a model repo from the CLI if needed
  ```sh
  transformers-cli repo create model_name
  ```

- Clone your model locally:
  ```sh
  git clone https://huggingface.co/username/model_name
  git lfs install
  ```

- Then add, commit and push weights/tokenizer/config:
  - Recall: save files via `.save_pretrained()`
  ```sh
  git add .
  git commit -m "commit from $USER"
  git push
  ```

- Your model will then be accessible through its identifier: `"username/model_name"`

- Anyone can load it from code:
  ```python
  tokenizer = AutoTokenizer.from_pretrained("username/model_name")
  model = AutoModel.from_pretrained("username/model_name")
  ```
  