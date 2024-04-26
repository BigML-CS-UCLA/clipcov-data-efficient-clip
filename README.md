# Data-Efficient Contrastive Language-Image Pretraining (AISTATS 2024)

## Abstract
Contrastive Language-Image Pre-training (CLIP) on large-scale image-caption datasets learns representations that can achieve remarkable zero-shot generalization. However, such models require a massive amount of pre-training data. Improving the quality of the pre-training data has been shown to be much more effective in improving CLIP's performance than increasing its volume. Nevertheless, finding small subsets of training data that provably generalize the best has remained an open question. In this work, we propose the first theoretically rigorous data selection method for CLIP. We show that subsets that closely preserve the cross-covariance of the images and captions of the full data provably achieve a superior generalization performance. Our extensive experiments on ConceptualCaptions3M and ConceptualCaptions12M demonstrate that subsets found by \method\ achieve over 2.7x and 1.4x the accuracy of the next best baseline on ImageNet and its shifted versions. Moreover, we show that our subsets obtain 1.5x the average accuracy across 11 downstream datasets, of the next best baseline.


[Project Page](https://sjoshi804.github.io/data-efficient-clip/)

[Paper](https://arxiv.org/abs/2403.12267)

## CLIPCov subsets and Baseline Subsets

Baseline Subsets are in baseline_subsets/. 

CLIPCov subsets are in clip_cov_subsets/. 

## Create Subset

The code for creating the subset is provided in clip_core.ipynb.

Due to size constraints we cannot upload the computed cosine similarity files etc. 

## Training Code

We train these subsets using the code provided by https://github.com/goel-shashank/CyCLIP.

The command we use to train the model is the following:

python -m src.main --name "<name_of_run>" --train_data <path_to_dataset_file> --image_key file --epochs 30 --batch_size 512 --distributed --device_ids <gpu_id_0> <gpu_id_1>

## BibTex

```bibtex
        @article{joshi2024data,
          title = {Data-Efficient Contrastive Multi-Modal Learning: Prioritizing Data Quality Over Quantity},
          author = {Joshi, Siddharth and Jain, Arnav and Payani, Ali and Mirzasoleiman, Baharan},
          journal = {International Conference on Artificial Intelligence and Statistics (AISTATS)},
          year = {2024}
        }
```
