# OpenAGI: When LLM Meets Domain Experts



> "May the Force be with LLM and Domain Experts." -- Generated by ChatGPT

[Paper on arXiv](https://arxiv.org/pdf/2304.04370.pdf)

![Teaser](image/pipeline.png)

## Introduction
Human intelligence has the remarkable ability to assemble basic skills into complex ones so as to solve complex tasks. This ability is equally important for Artificial Intelligence (AI), and thus, we assert that in addition to the development of large, comprehensive intelligent models, it is equally crucial to equip such models with the capability to harness various domain-specific expert models for complex task-solving in the pursuit of Artificial General Intelligence (AGI). Recent developments in Large Language Models (LLMs) have demonstrated remarkable learning and reasoning abilities, making them promising as a controller to select, synthesize, and execute external models to solve complex tasks. 

This project presents OpenAGI, an open-source AGI research platform, specifically designed to offer complex, multi-step tasks and accompanied by task-specific datasets, evaluation metrics, and a diverse range of extensible models. OpenAGI formulates complex tasks as natural language queries, serving as input to the LLM. The LLM subsequently selects, synthesizes, and executes models provided by OpenAGI to address the task. Furthermore, the project presents the Reinforcement Learning from Task Feedback (RLTF) mechanism, which uses the task-solving result as feedback to improve the LLM's task-solving ability. Thus, the LLM is responsible for synthesizing various external models for solving complex tasks, while RLTF provides feedback to improve its task-solving ability, enabling a feedback loop for self-improving AI. We believe that the paradigm of LLMs operating various expert models for complex task-solving is a promising approach towards AGI. 

To facilitate the community's long-term improvement and evaluation of AGI's ability, we open-source the code, benchmark, and evaluation methods of the OpenAGI project, and we appreciate any discussions, comments, suggestions or contributions from the community.

## Requirements:
- Python 3.9.16
- PyTorch 1.12.1

```
pip install -r requirements.txt
```



## Usage

0. Clone this repo

    ```
    git clone https://github.com/agiresearch/OpenAGI.git
    ```

1. Download the preprocessed data from this [Google Drive link](https://drive.google.com/drive/folders/1AjT6y7qLIMxcmHhUBG5IE1_5SnCPR57e?usp=share_link), put it into the *root/* folder, then unzip it. If you would like to preprocess your own data, please run data_augmentation.py in the *data* folder. Raw data will be automatically downloaded using HuggingFace datasets library; for COCO, please download from [COCO](https://cocodataset.org/#download).

```
wget http://images.cocodataset.org/zips/val2017.zip
```


![Teaser](image/data_sample.png)

2. To evaluate Zero-shot and Few-shot LLMs, use jupyter notebook in *zero_shot/* folder or *few_shot/* folder. 
   
3. To evaluate finetuned Flan-T5-Large, please first download the pretrained checkpoints from this [Google Drive link](https://drive.google.com/drive/folders/1AjT6y7qLIMxcmHhUBG5IE1_5SnCPR57e?usp=share_link) into *finetune/* folder, then run the notebook in that folder. Or pretrain with scripts in *finetune/* folder to get your own checkpoint, such as

    ```
    python finetune/flan_t5_finetune.py
    ```
 
 Under construction.
<!--
4. Evaluate with example jupyter notebooks in the *notebooks* folder. Before testing, create a soft link of *data* folder to the *notebooks* folder by
   
   ```
   cd notebooks
   ln -s ../data .
   ```
-->


## Citation

```
@article{openagi,
  title={OpenAGI: When LLM Meets Domain Experts},
  author={Ge, Yingqiang and Hua, Wenyue and Ji, Jianchao and Tan, Juntao and Xu, Shuyuan and Zhang, Yongfeng},
  journal={arXiv},
  year={2023}
}
```

