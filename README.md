# Related Knowledge Perturbation Matters

This repository includes the data and python implementation for the paper "Related Knowledge Perturbation Matters: Rethinking Multiple Pieces of Knowledge Editing in Same-Subject." (Accepted by NAACL 2025 Main Conference).

[![arXiv](https://img.shields.io/badge/arXiv-paper-b31b1b.svg)](https://arxiv.org/abs/2502.06868)

<div align="center">
    <img src="./pic/demo.png" alt="Pipeline Diagram" width=50%; height=50%;">
</div>

## DataSet

Our dataset is located in `S2RKE.json`. Compared to the dataset COUTERFACT, the knowledge density surrounding the same topic is higher.
| Item | S2RKE| COUNTERFACT |
|------|---------|---------|
| Records | 22064 | 21919 |
| Subjects | 4503 | 20391 |
| Relations | 43 | 32 |
| Maximum records per subject | 13 | 4 |
| Minimum records per subject | 3 | 1 |
| Average records per subject | 4.9 | 1.1 |
### Example
```json
{
    "subjectID": 0,"class": "xxx",
        "subject": {
            "name": "Double Xposure","URL": "/resource/schema:Movie",
            "original_name": "<Double_Xposure>","description": "2012 film directed by Li Yu"
        },
        "Star_Topology": [
            {
                "requested_rewrite": {
                    "prompt": "{}, which is located in","relation": "<isLocatedIn>",
                    "target_true": "China", "target_new": "Głogów County"
                },
                "paraphrase_prompts": [
                    "Double Xposure, a 2012 film by Li Yu, is set in"
                ],
                "neighborhood_prompts": [
                    "Ping Zhang is a citizen of", "Ricky Lee has citizenship in"
                ]
            },"..." ]}
```

## Experiment
### Model preparation
| Model name                                     | Link                                                         |
| ---------------------------------------------- | ------------------------------------------------------------ |
| GPT2-XL                      | [[Huggingface link]](https://huggingface.co/openai-community/gpt2-xl) |
| GPT-J-6B                           | [[Huggingface link]](https://huggingface.co/EleutherAI/gpt-j-6b) |
| Llama2-7B                      | [[Huggingface link]](https://huggingface.co/meta-llama/Llama-2-7b) |
### Results of Same-Editing
<div align="center">
    <img src="./pic/fig7.png";">
</div>
