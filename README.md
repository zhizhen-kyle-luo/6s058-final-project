# Post-Hoc DyT: LayerNorm Replacement in Pretrained Vision Encoders

Spring 2026 Final project for 6.S058 by Kyle Luo.

This project tests whether Dynamic Tanh (DyT) can replace LayerNorm inside a LayerNorm-pretrained vision encoder via post-hoc swap followed by fine-tuning. Two backbones are evaluated: ViT-B/16 fine-tuned on CIFAR-100, and SegFormer-B0 fine-tuned on a 2000-image ADE20K subset. We compare the paper-default DyT initialization against an affine-preserving variant that copies the pretrained LayerNorm γ, β into DyT.

Run experiments in Colab:
https://colab.research.google.com/github/zhizhen-kyle-luo/6s058-final-project/blob/main/colab_train.ipynb

## Repo structure

```
.
├── CV_Final.pdf         compiled paper PDF
├── main.tex             CVPR-style paper source
├── references.bib       bibliography
├── cvpr.sty             CVPR latex style
├── ieee_fullname.bst    CVPR bibliography style
├── colab_train.ipynb    training and plotting notebook
├── figures/             figure PDFs used by main.tex
└── runs/                per-run logs (config.json, log.jsonl, summary.json)
                         model checkpoints are gitignored
```
