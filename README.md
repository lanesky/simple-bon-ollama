# Simple BoN Jailbreaking for Ollama

This project is based on the references linked below. Since the original source code from the paper is difficult to use, I created a simple Python program for local testing.

- https://x.com/AnthropicAI/status/1867608917595107443
- https://jplhughes.github.io/bon-jailbreaking/
- https://github.com/jplhughes/bon-jailbreaking

The main source file is `bon.py`, which borrows code from [bon-jailbreaking](https://github.com/jplhughes/bon-jailbreaking/blob/main/bon/attacks/run_text_bon.py), including functions such as `FALSE_POSITIVE_PHRASES`, `apply_word_scrambling`, `apply_random_capitalization`, and `apply_ascii_noising` for text augmentation.

To determine whether a response is harmful, this program uses the [OpenAI moderation API](https://platform.openai.com/docs/guides/moderation/overview).

In `bon.py`, the model `llama3.2` is hardcoded for testing purposes. You can replace it with any Ollama-supported model.

For an example of test result, see `candidate.txt`.

## How to run

1. **Install Ollama**  
   Download Ollama from the following link:

   - [https://ollama.com/download](https://ollama.com/download)

2. **Install an Ollama Model**  
   Use the following command to install the `llama3.2` model:

```
ollama run llama3.2
```

For more information, refer to https://ollama.com/library/llama3.2

3. **Install Ollama Python Library**
   Install the required Python library with:

```
pip install ollama
```

For details, see https://github.com/ollama/ollama-python

4. **Run this program**

Execute the program using:

```
python bon.py
```
