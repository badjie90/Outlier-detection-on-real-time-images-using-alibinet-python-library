# IMAGE-OUTLIER-DETECTION-WITH-THE-ALIBINET-DETECT-PYTHON-LIBRARY


[Alibi-Detect](https://docs.seldon.io/projects/alibi-detect/en/stable/), a Python library that is available as open source, is specifically designed to detect outliers, adversarial perturbations, and drift in various types of datasets. This comprehensive package is aimed at providing users with both online and offline detectors that can be applied to tabular data, text, images, and time series. The outlier detection methods that are included within the library have been meticulously developed and refined to enable users to accurately and effectively identify global, contextual, and collective outliers, thereby enabling a greater degree of granularity and precision in their analyses. By leveraging the sophisticated algorithms and techniques embedded within this cutting-edge tool, users can improve their detection capabilities and gain a deeper understanding of complex datasets, ultimately leading to more informed and insightful decision-making.
However, this project involves the use of only an image dataset.

The dataset can be found at https://www.mvtec.com/company/research/datasets/mvtec-ad

To use this our, you must install the alibi-detect library by running:

#### pip install alibi-detect           

            or                 

#### conda install alibi-detect (if you are using a conda environment)





Also you have install the tensorflow 2.0 and above. You can do that by running:

pip install tensorflow ==version_number 

               or 

conda install tensorflow ==version_number if you are using a conda environment.

For a better understand, the link below provides a detail summary of this library.

https://docs.seldon.io/_/downloads/alibi-detect/en/v0.5.1/pdf/



If you are interested in an introduction to auto-encoders, head over to this [article](https://hackernoon.com/latent-space-visualization-deep-learning-bits-2-bd09a46920df). If a more technical breakdown is what you are looking for, check out this [blog post](https://lilianweng.github.io/posts/2018-08-12-vae/), from which the below image is sourced. It shows how an auto-encoder for MNIST images works, but the idea is still the same. 

<img width="1035" alt="denoising-autoencoder-architecture" src="https://user-images.githubusercontent.com/73148658/219651610-c0357396-a057-4102-a585-361a99d1906d.png">



The idea is quite straightforward:

1. Due to the bottleneck architecture of the neural network, it is forced to learn a condensed representation from which to reproduce the original input.

2. You just need to feed it only normal data, which it will learn to reproduce with high fidelity.

3. As a consequence, if any abnormal data is sufficiently distinct from normal data, the auto-encoder will have trouble reproducing it with its learned weights, and the subsequent reconstruction loss will be high.

4. Anything above a specific loss (treshold) will be flagged as anomalous and thus labeled as abnormal and will be recontruct.


 






 

