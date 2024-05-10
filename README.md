# Apply Lighweight Fine-Tunning to a Foundation Model

## Project Overview
### Project Introduction

Lightweight fine-tuning is one of the most important techniques for adapting foundation models, because it allows you to modify foundation models for your needs without needing substantial computational resources.


In this project, we will apply **parameter-efficient fine-tuning** using the Hugging Face *peft* library.

## Project Summary
- We will be using PyTorch + Hugging Face training and inference process. Specifically:
- We will load a pre-trained model and evaluate its performance
- Perform parameter-efficient fine tuning using the pre-trained model
- Perform inference using the fine-tuned model and compare its performance to the original model

## Project Walkthrough

### 1 - Load a pre-trained model and evaluate its performance
- We will perform parameter-efficient fine-tuning using the pre-trained model (a foundation model)
- Perform inference using the fine-tuned model and compare its performance to the original model

    #### 1.1 - PEFT technique
    - Low Rank Adaptation, LoRA, is a PEFT Technique and the only PEFT technique that is compatible with all models at this time.

    #### 1.2 - Model
    - We chose a GPT2 model for classification.
    - Also, we constrained the **batch_size to 4** to train in our old 1650Ti Card.
    - This is a relatively small model that is compatible with several tasks and LoRA.

    #### 1.3 - Evaluation approach
    - The evaluation approach covered here was the evaluate method with a Hugging Face Trainer.
    - Finally, we compared the original foundation model with the evaluation model to see the performance.
    
    #### 1.4 - Dataset
    - Our PEFT process have a Hugging Face's dataset. Also selected one with a small data to handle.

### 2 - Loading and Evaluating a Foundation Model
- 
    #### 2.1 - Loading the model
    - We selected a foundation model (GPT-2), included the relevant imports, loads a pretrained Hugging Face model that can be used classification.

    #### 2.2 - Evaluating the model
    - Performed an initial evaluation of the model on your chosen classification task. Also applied some tokenization and transformation techniques to the dataset.

### 3 - Performing Parameter-Efficient Fine-Tuning
- 
    #### 3.1 - Creating a PEFT config   
    - Made the PEFT config with appropriate hyperparameters for a chosen model.

    #### 3.2 - Creating a PEFT model
    - Used the PEFT config and foundation model, create a PEFT model.

### 4 - Training the model
We used the PEFT model and dataset, run a training loop with at least one epoch.

### 5 - Saving the trained model
Our PEFT model may have already been saved to the folder issaiass/gpt2-lora.

### 6 - Performing Inference with a PEFT Model
- 
    ### 6.1 - Loading the model
    - Used the appropriate PEFT model class, load your trained model.

    ### 6.2 - Evaluating the model
    - We finally repeated the process to see the results of the foundation model side by side with the LoRA model.

<details open>
<summary> <b>Results<b></summary>

Below we provide results of the foundation model and the LoRA model.

|    metric name      | GPT2       | GPT2-LoRA |
|------------------------|------------|-----------|
| eval_loss              | 8.165428   | 0.391603  |
| eval_accuracy          | 0.492      | 0.862     |
| eval_f1                | 0.659517   | 0.864440  |
| eval_precision         | 0.492000   | 0.836502  |
| eval_recall            | 1.000000   | 0.894309  |
| eval_runtime           | 44.8370    | 140.7062  |
| eval_samples_per_second| 11.152     | 3.554     |
| eval_steps_per_second  | 2.788      | 0.888     |
| epoch                  | not applicable | 1.0 |


<p align="center"> </p>
</details>

<details open>
<summary> <b>Issues<b></summary>

- no issues found yet.

</details>

<details open>
<summary> <b>Future Work<b></summary>

- None

</details>

<details open>
<summary> <b>Contributing<b></summary>

Your contributions are always welcome! Please feel free to fork and modify the content but remember to finally do a pull request.

</details>

<details open>
<summary> :iphone: <b>Having Problems?<b></summary>

<p align = "center">

[<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" />](https://www.linkedin.com/in/riawa)
[<img src="https://img.shields.io/badge/telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/>](https://t.me/issaiass)
[<img src="https://img.shields.io/badge/instagram-%23E4405F.svg?&style=for-the-badge&logo=instagram&logoColor=white">](https://www.instagram.com/daqsyspty/)
[<img src="https://img.shields.io/badge/twitter-%231DA1F2.svg?&style=for-the-badge&logo=twitter&logoColor=white" />](https://twitter.com/daqsyspty) 
[<img src ="https://img.shields.io/badge/facebook-%233b5998.svg?&style=for-the-badge&logo=facebook&logoColor=white%22">](https://www.facebook.com/daqsyspty)
[<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" />](https://www.linkedin.com/in/riawe)
[<img src="https://img.shields.io/badge/tiktok-%23000000.svg?&style=for-the-badge&logo=tiktok&logoColor=white" />](https://www.linkedin.com/in/riawe)
[<img src="https://img.shields.io/badge/whatsapp-%23075e54.svg?&style=for-the-badge&logo=whatsapp&logoColor=white" />](https://wa.me/50766168542?text=Hello%20Rangel)
[<img src="https://img.shields.io/badge/hotmail-%23ffbb00.svg?&style=for-the-badge&logo=hotmail&logoColor=white" />](mailto:issaiass@hotmail.com)
[<img src="https://img.shields.io/badge/gmail-%23D14836.svg?&style=for-the-badge&logo=gmail&logoColor=white" />](mailto:riawalles@gmail.com)

</p>

</details>

<details open>
<summary> <b>License<b></summary>
<p align = "center">
<img src= "https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-sa.svg" />
</p>
</details>