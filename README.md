<div align="center">

<h1> 24Fall-CV Project: FlashVLM </h1>

</div>

## Team Member
Yuan Zhang, Hao Wang, Yueru Jia, Yi Huang, Yaoxu Lv

## 👨‍💻 Preparation

1. Clone this repository and navigate to SparseVLMs folder
```bash
git clone https://github.com/Gumpest/SparseVLMs.git
cd SparseVLMs
```

2. Install necessary package
```Shell
conda create -n SparseVLMs python=3.10 -y
conda activate SparseVLMs
pip install -e .
```

3. Download Multimodal Benchmark

Please follow the detailed instruction in [LLaVA-Evaluation](https://github.com/haotian-liu/LLaVA/blob/main/docs/Evaluation.md).

## 🎯 Usage
Specifically, `--sparse` in script indicates whether to perform sparseness, while `--scale` and `--bias` control the degree of token sparsity.

1. Example for evaluating MME results (192 tokens, scale = 13.5, bias = 0.0):
```Shell
CUDA_VISIBLE_DEVICES=0 bash scripts/v1_5/eval/mme.sh
```

2. Example for evaluating POPE results (128 tokens, scale = 9, bias = 6):
```Shell
CUDA_VISIBLE_DEVICES=0 bash scripts/v1_5/eval/pope.sh
```

3. Example for evaluating TextVQA results (64 tokens, scale = 0.8, bias = 0.0):
```Shell
CUDA_VISIBLE_DEVICES=0 bash scripts/v1_5/eval/textvqa.sh
```

## License

This project is released under the [Apache 2.0 license](LICENSE).


## Acknowledgment

We extend our gratitude to the open-source efforts of [TCFormer](https://github.com/zengwang430521/TCFormer), [LLaVA](https://github.com/haotian-liu/LLaVA), [MiniGemini](https://github.com/dvlab-research/MGM) and [VideoLLaVA](https://github.com/PKU-YuanGroup/Video-LLaVA).
