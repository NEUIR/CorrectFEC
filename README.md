# Unsupervised Fact Error Correction Modeling by Using Span-Level Contrastive Learning
Source code for our paper : Unsupervised Fact Error Correction Modeling by Using Span-Level Contrastive Learning.

Click the links below to view our checkpoints

<a href='https://huggingface.co/yuqinglanok/CorrectFEC/tree/main'><img src='https://img.shields.io/badge/huggingface-CorrectFEC-blue'></a>

## Requirement
**1. Install the following packages using Pip or Conda under this environment**

```
Python==3.9
Pytorch
transformers
```
We provide the version file `requirements.txt` of all our used packages, if you have any problems configuring the environment, please refer to this document.

## Reproduce CorrectFEC
### Download Code & Dataset
* First, use `git clone` to download this project:
```bash
git clone https://github.com/NEUIR/CorrectFEC
cd CorrectFEC
```
* Download link for [data and model](https://drive.google.com/file/d/1Mys4xFUOHEk4ocDt6GPlCwwVVk5b6Lbi/view?usp=sharing)

### Train CorrectFEC
**I will show you how to reproduce the results in the CorrectFEC paper.**

* Go to the ``model`` folder and train the CorrectFEC model [checkpoint](https://huggingface.co/yuqinglanok/CorrectFEC/tree/main/mfec):
```
cd model
bash train.sh
```
### Inference CorrectFEC
* For the FEVER and SCIFACT dataset: Go to the ``inference`` folder and inference on the CorrectFEC model:
```
cd inference
bash inference_final.sh
```

## Evaluate Prediction Effectiveness
* These experimental results are shown in Table 1 of our paper.
* Go to the ``evals`` folder and evaluate model performance as follow:
```
cd evals
bash evals.sh
python chatgpt_gpteval.py
python sentencebert.py
```

## Contact
If you have questions, suggestions, and bug reports, please email:
```
lanyuqing@stumail.neu.edu.cn     
```
