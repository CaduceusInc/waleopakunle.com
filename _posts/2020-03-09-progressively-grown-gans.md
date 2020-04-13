---
toc: true
comments: true
author: Wale
categories: [GANs, Research paper, Pro-GAN]
permalink: /papers/:year/:month/:day/:title
---

## [A Summary of Progressive Growing of GANs for improved quality, stability and variation (Pro-GANs) ](https://arxiv.org/pdf/1710.10196v3.pdf)



Before we begin, I thought it would be more insightful (and interesting) if you could first see for yourself what the algorithm produced in this paper is capable of. If you’re interested, please check [this youtube video out.](https://youtu.be/G06dEcZ-QTg)

## Original Abstract

We describe a new training methodology for generative adversarial networks. The key idea is to grow both the generator and discriminator progressively: starting from a low resolution, we add new layers that model increasingly fine details as training progresses. This both speeds the training up and greatly stabilizes it, allowing us to produce images of unprecedented quality, e.g., CELEBA images at 1024x1024. We also propose a simple way to increase the variation in generated images, and achieve a record inception score of 8:80 in unsupervised CIFAR10.

Additionally, we describe several implementation details that are important for discouraging unhealthy competition between the generator and discriminator. Finally, we suggest a new metric for evaluating GAN results, both in terms of image quality and variation. As an additional contribution, we construct a higher-quality version of the CELEBA dataset.

## My Summary

**What did they contribute?**

The NVIDIA team improved the stability, resolution (image quality) and variation of generated images. They also propose a new metric for evaluating generated images.

**What older methods were they improving on?**

  - **Resolution (Image quality)**

Durugkar et al. (2016) who use one generator and multiple discriminators concurrently.

Ghosh et al. (2017) who use multiple generators and one discriminator.

Wang et al. (2017), who use multiple discriminators that operate on different spatial resolutions.

Denton et al., 2015; Huang et al., 2016; Zhang et al., 2017 define a generator and discriminator for each level of an image pyramid (Hierarchical GANs).

  - **Variation**

Metz et al., 2016 who unroll the discriminator to regularize its updates.

Zhao et al., 2017 who use a “repelling regularizer” that adds a new loss term to the generator, trying to encourage it to orthogonalize the feature vectors in a minibatch.

Ghosh et al. (2017) who use multiple generators.

  - **Stability**

Ioffe & Szegedy, 2015; Salimans & Kingma, 2016; Ba et al., 2016 and many others tend to use a variant of batch normalization in the generator and discriminator to discourage the escalation of unhealthy competition between the networks.

**Issues with existing methods that necessitate this improvement**

[Autoregressive models](https://www.statisticshowto.datasciencecentral.com/autoregressive-model/) have limited applicability because they are slow to evaluate and do not have latent representation although they produce sharp images. Variational autoencoders (VAEs) are easy to train but tend to produce blurry results despite recent advances and this is due to restrictions in the model architecture. GANs produce sharp images, but they do so in fairly small **resolutions** and somewhat limited variation. Also, training GANs remains notoriously unstable despite recent advances.

**Which of the issues were they improving/solving?**

Their primary contribution was to develop a training methodology for the training of GANs in which the resolution of the resulting output images could be progressively increased from an initial low-resolution images. They achieved this by progressively adding layers to the networks.

**What did they propose to do differently and why?**

  - **<span class="underline">Change:</span>** Use a single generator and discriminator network that are mirror images of each other and always grow in synchrony. All existing layers in both networks remain trainable throughout the training process.
    
    **<span class="underline">Reason:</span>** In previous approaches to training, the networks had to learn both the large-scale structure and fine scale detail of image distributions and this understandably took a long period of time.
    
    **<span class="underline">Result: </span>**

<!-- end list -->

  1.  Stabilized training sufficiently to enable the reliable synthesis of high resolution images.

  2.  Reduced training time (2 - 6 times faster depending on the output resolution).

<!-- end list -->

  - **<span class="underline">Change</span>**: Dynamically setting the weights and scale it at runtime rather than careful initialization
    
    **<span class="underline">Reason</span>:** Previous methods normalize a gradient update by its estimated standard deviation, thus making the update independent of the scale of the parameter. As a result, if some parameters have a larger dynamic range than others, they will take longer to adjust.
    
    **<span class="underline">Result</span>:** Dynamically setting the weights ensures that learning speed is the equal for all weights.

  - **<span class="underline">Change:</span>** Normalize the feature vector in each pixel to unit length in the generator after each convolutional layer.
    
    **<span class="underline">Reason:</span>** To disallow the scenario where the magnitudes in the generator and discriminator spiral out of control as a result of competition.
    
    **<span class="underline">Result:</span>** prevents the escalation of signal magnitudes very effectively when needed.

  - **<span class="underline">Change:</span>** Considering the multiscale statistical similarity between distributions of local image patches drawn from Laplacian pyramid representations of generated and target images, starting at a low-pass resolution of 16 x 16 pixels.
    
    **<span class="underline">Reason:</span>** Previous methods of evaluating generative performance work reliably in finding large scale mode collapse, but fail to react well to smaller effects such as loss of variation in colors and textures. They also do not directly assess image quality in terms of similarity to the training set.
    
    **<span class="underline">Result:</span>** A new approach for evaluating generated images based on a combination of older methods, including sampling from a Laplacian pyramid and sliced Wasserstein distance (SWD) for estimating statistical similarities. A smaller SWD at a given Laplacian layer indicates that training and generated image samples appear similar in both appearance and variation at the pyramids spatial resolution.

  - **<span class="underline">Change:</span>** Use minibatch standard variation to increase variation.
    
    **<span class="underline">Reason:</span>** GANs tend to capture only a subset of variations present in training data and other approaches to tackle this problem are rather cumbersome.
    
    **<span class="underline">Result:</span>** In their experiment, including mini batch standard variation improved the sliced Wasserstein loss.

**Did their experiments show an improvement?**

![](/images/2020-03-09-progressively-grown-gans/media/image1.jpg)
source: [*Prograssive growing of GANs for Improved quality, stability and variation.*](https://arxiv.org/pdf/1710.10196v3.pdf)


As can be seen from their results that compare how different training configurations compare in terms of their SWD losses and structural similarities (MS-SIM) of generated images from different datasets (CELEBA and LSUN), progressive GANs have a significantly improved performance. Removing any of the teams new contributions makes the network perform in a handicapped manner as can be seen with and without minibatch standard deviation in (e) and (e\*) respectively.

![](/images/2020-03-09-progressively-grown-gans/media/Effect of progressive growing on training speed and convergence.jpg)
source: [*Prograssive growing of GANs for Improved quality, stability and variation.*](https://arxiv.org/pdf/1710.10196v3.pdf)


## Core Ideas

  - Older methods had notable weaknesses which were improved on in the paper, including training speed, stability in training and resolution of output images.

  - This paper introduced a new methodology for generating high resolution images by progressively increasing the layers in the network. They also tackled mode collapse by using pixel-wise feature normalization and equalized learning rates for all weights. Finally, they increased variation by introducing minibatch standard deviation and proposed a new way for evaluating generated images.

  - Advantages of the new method introduced:

  1. Decreased training time. With progressively growing GANs most of the iterations are done at lower resolutions, and comparable result quality is often obtained up to 2–6 times faster, depending on the final output resolution.

  1. More stable GAN training.

  1. Images are one step closer to photorealism.

  <!-- end list -->

## What the community says about the paper?

  - [\#2 Best Image Generation model](https://paperswithcode.com/sota/image-generation-on-cifar-10) for CIFAR10 dataset

## Future research areas

  - Conditional Pro-GANs.

  - Increasing resolution threshold.

  - Increasing training stability (i.e decreasing the chances of mode collapse)
    Notably, some work seems to have been done on that [here](https://ieeexplore.ieee.org/document/8683262)

## Possible business and other applications

  - Applications of Pro-GAN to critical domains, such as [this one](https://arxiv.org/pdf/1902.09856.pdf). Where a Pro-GAN architecture was used to generate high resolution synthesized training data for computer-assisted diagnosis, or this one used to generate [Gastritis data](https://eprints.lib.hokudai.ac.jp/dspace/bitstream/2115/75023/1/01SyntheticGastritisImageGenerationViaLossFunction-basedConditionalPGGAN.pdf).

  - Generating high resolution example datasets for computer vision tasks.

  - Generate high resolution logo (or of anything, really) images for creatives.

  P.S: If you think of any I may have omitted, please reach out to me. *wink*

## Implementations

You can find the original implementation by Tero Karras [here](https://github.com/tkarras/progressive_growing_of_gans). Alternatively, you can follow [this link](https://colab.research.google.com/drive/1_FLJPZGU30spY7fn0sduXdUH0gcWmFKZ) for a quick start to the colab notebook I set up using his implementation and pretrained network, so you can run it interactively. Create a copy for yourself and hack away.

## New Concepts / Terminology

**The Inception Score**, or IS for short, is an objective metric for evaluating the quality of generated images, specifically synthetic images output by generative adversarial network models. You can read more about how it is calculated and its application [here](https://machinelearningmastery.com/how-to-implement-the-inception-score-from-scratch-for-evaluating-generated-images/).

Average pooling: Pooling refers to techniques used to downscale / reduce the size of an image gotten from a preceding convolutional layer, in such a way that the information in the image is retained without distortion. Hence, average pooling is just one of the versions of pooling available. You can read all about pooling in [this post here](https://www.machinecurve.com/index.php/2020/01/30/what-are-max-pooling-average-pooling-global-max-pooling-and-global-average-pooling/#average-pooling).

**He’s initializer:** A weight initialization method that takes into account the size of the previous layer. The weights are still random, but differ in range depending on the size of the [previous layer.](https://medium.com/@prateekvishnu/xavier-and-he-normal-he-et-al-initialization-8e3d7a087528)

**Laplacian pyramid**: Used to reconstruct an upsampled image from an image lower in the pyramid (with less resolution). Please checkout [this post by Kang and Atul](https://theailearner.com/tag/laplacian-pyramid-opencv/) for a very nice explanation and description of the implementation in OpenCV.

**Sliced Wasserstein distance (SWD)**: A modification of the Wasserstein loss function used for increasing the stability of training GANs. You can read the rather involved paper that introduced it [here](https://www.zpascal.net/cvpr2018/Deshpande_Generative_Modeling_Using_CVPR_2018_paper.pdf). It leverages on the rather attractive feature of Wasserstein distance while making interesting modifications.

[**Least Squares Generative Adversarial Network (LSGAN)**](https://arxiv.org/abs/1611.04076): it's an extension to the GAN architecture that addresses the problem of vanishing gradients and loss saturation. If you would like to read more aboout it, including how to go about implementing it, check out [this blog post.](https://machinelearningmastery.com/least-squares-generative-adversarial-network/)

**WGAN-GP or Wasserstein GAN Gradient penalty**: It is a modification of the cost function used in WGANs. You can read [this article](https://medium.com/@jonathan_hui/gan-wasserstein-gan-wgan-gp-6a1a2aa1b490) to learn about the limitations of weight clipping in WGANs and the slight modification that makes WGAN-GP approach more desirable. 

## Training resources used


  - Network Architecture
    ![](/images/2020-03-09-progressively-grown-gans/media/network structure and training configuration.jpg)
    source: [*Prograssive growing of GANs for Improved quality, stability and variation.*](https://arxiv.org/pdf/1710.10196v3.pdf)

  - Hardware / Compute
  1. 8 Tesla V100 GPUs, trained for 4 days to achieve convergence.

  - Datasets
  1. CELEBA-HQ - A dataset containing HD images of celebrities. 30,000 images were used in total.
  1. LSUN - It contains around one million labeled images for each of 10 scene categories and 20 object categories.
  1. CIFAR10 - It  consists of 60000 32x32 colour images in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images.
  1. MNIST -  A database of handwritten digits, has a training set of 60,000 examples, and a test set of 10,000 examples. It is a subset of a larger set available from NIST. The digits have been size-normalized and centered in a fixed-size image. It is a good database for people who want to try learning techniques and pattern recognition methods on real-world data while spending minimal efforts on preprocessing and formatting.

  - Hyperparameters
  1. Optimizer: Adam

  1. Activation function: leaky ReLU, leakiness of 0.2

  1. No learning rate decay or rampdown.

  1. *n*<sub>critic</sub> = 1

  1. Small weight added to discriminator output.

  1. Adaptive minibatch size depending on the current output resolution.

     

  **Authors of the original paper**: [Tero Karras](https://research.nvidia.com/person/tero-karras) (NVIDIA), [Timo Aila](https://research.nvidia.com/person/timo-aila) (NVIDIA), [Samuli Laine](https://research.nvidia.com/person/samuli-laine) (NVIDIA), [Jaakko Lehtinen](https://research.nvidia.com/person/jaakko-lehtinen) (NVIDIA and Aalto University)



That's it for this post. Thank you for your time!

Please let me know in the comments:

1. Any new AI research papers you would like me to review.

2. Suggestions regarding the content that might need more explanation.

3. Anything you want really.

   





