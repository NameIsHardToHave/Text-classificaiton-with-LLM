# Text-classificaiton-with-LLM
Use llama3-8B to achieve the text-classification task. The fine-tuning code and inference code are given here.

After the original text is applied with the template, it is converted into input_id and attention_mask through the tokenizer, and then combined with the real label to be sent to the model. Note that due to the different lengths of data, the same batch needs to be completed to the same length. There is a mature framework for the training part.

In our prompts, we provide three contextual examples for each use case. It is recommended to use vllm for model inference, which can achieve high-throughput batch processing.
