# CellLM: A generative pre-trained cell language model for Single-Cell RNA-Seq Analysis

This decoder-only architecture is trained through self-supervised learning on large-scale unannotated single-cell data, enabling it to capture intrinsic patterns of cellular states. As a universal cellular state generator, its core capabilities encompass multiple downstream tasks including cell type annotation, perturbation prediction, and in silico cell generation.

## Downstream Task
- Cell Type Annotation: Leveraging pre-trained representations for accurate cell type identification. 

## Model Training
The decoder-only model was pretrained on 156,726 single cells * 33159 genes of the human embryonic meninges at 5-13 weeks post conception. The training scripts is wrapped up in ![pretrained model](./S1_decoder_only_pretrained_model.ipynb)

## Performance Highlights
### Cell type annotation:
- given 1% or 5% training dataset, the pretrained model+MLP is outperform over MLP in precision and recall.
![cell type annotation](./evaluation/boxplot.jpg)
