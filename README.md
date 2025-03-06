# Model Tuning with Lamini

This repository contains code for tuning a language model using the Lamini library. The code reads training data from a JSONL file, initializes the model, and trains it with the provided data.

## Requirements

- Python 3.7+
- `lamini`
- `dotenv`
- `datasets`
- `jsonlines`

## Setup

1. Clone the repository:
    ```sh
    git clone [https://github.com/yourusername/model_tuning.git](https://github.com/AyoBankole/LLM_FineTuning_Using_LAMINI.git)
    cd model_tuning
    ```

2. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

3. Create a [.env](http://_vscodecontentref_/0) file in the root directory and add your Lamini API key:
    ```env
    LAMINI_API_KEY=your_api_key_here
    ```

## Usage

1. Place your training data in a JSONL file. Update the [file_path](http://_vscodecontentref_/1) variable in [model_tuning.py](http://_vscodecontentref_/2) to point to your JSONL file.

2. Run the script to start the training process:
    ```sh
    python model_tuning.py
    ```

3. The script will initialize the model, read the training data, and start the training process. Once the training is complete, it will generate text based on the tuned model.

## Example

```python
# For text generation after tuning the llm
llm = Lamini(model_name="<Enter your LAMINI API KEY here>")
print(llm.generate("""<|begin_of_text|><|start_header_id|>user<|end_header_id|>

What is PCOS?<|eot_id|>
<|start_header_id|>assistant<|end_header_id|>

"""))
