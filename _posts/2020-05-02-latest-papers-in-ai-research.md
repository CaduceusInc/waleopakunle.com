---
toc: true
comments: true
author: Wale
image: /images/2020-05-02-latest-in-ai/alae1.gif
categories: [Trending Research papers]
permalink: /papers/:year/:month/:day/:title
---

# Latest in AI Research - Week 18

![R for Research](https://media.giphy.com/media/OnJLRvXvAmvPW/giphy.gif)

Hey there! Here is a collation of what's new in AI research.

* > Title:  Adversarial Latent Autoencoders

![adversarial_latent_autoencoders](/images/2020-05-02-latest-in-ai/alae1.gif)
![adversarial_latent_autoencoders2](/images/2020-05-02-latest-in-ai/alae2.gif)

> Abstract: Autoencoder networks are unsupervised approaches aiming at combining generative and representational properties by learning simultaneously an encoder-generator map. Although studied extensively, the issues of whether they have the same generative power of GANs, or learn disentangled representations, have not been fully addressed. We introduce an autoencoder that tackles these issues jointly, which we call Adversarial Latent Autoencoder (ALAE). It is a general architecture that can leverage recent improvements on GAN training procedures. We designed two autoencoders: one based on a MLP encoder, and another based on a StyleGAN generator, which we call StyleALAE. We verify the disentanglement properties of both architectures. We show that StyleALAE can not only generate 1024x1024 face images with comparable quality of StyleGAN, but at the same resolution can also produce face reconstructions and manipulations based on real images. This makes ALAE the first autoencoder able to compare with, and go beyond the capabilities of a generator-only type of architecture.

> Task:| IMAGE GENERATION

> Implementation:| [code](https://github.com/podgorskiy/ALAE)

> Read the paper [here](https://arxiv.org/pdf/2004.04467v1.pdf)

---
---

* > Title:  YOLOv4 - Optimal Speed and Accuracy of Object Detection

![darknet](/images/2020-05-02-latest-in-ai/darknet.png)

> Abstract: There are a huge number of features which are said to improve Convolutional Neural Network (CNN) accuracy. Practical testing of combinations of such features on large datasets, and theoretical justification of the result, is required. Some features operate on certain models exclusively and for certain problems exclusively, or only for small-scale datasets; while some features, such as batch-normalization and residual-connections, are applicable to the majority of models, tasks, and datasets. We assume that such universal features include Weighted-Residual-Connections (WRC), Cross-Stage-Partial-connections (CSP), Cross mini-Batch Normalization (CmBN), Self-adversarial-training (SAT) and Mish-activation. We use new features: WRC, CSP, CmBN, SAT, Mish activation, Mosaic data augmentation, CmBN, DropBlock regularization, and CIoU loss, and combine some of them to achieve state-of-the-art results: 43.5% AP (65.7% AP50) for the MS COCO dataset at a realtime speed of ~65 FPS on Tesla V100.

> Task:| DATA AUGMENTATION | OBJECT DETECTION

> Implementation:| [Code with most stars - in C & Cuda](https://github.com/pjreddie/darknet) | [Tensorflow](https://github.com/AlexeyAB/darknet)

> Read the paper [here](https://arxiv.org/pdf/2004.10934v1.pdf)

---
---

* > Title:  NBDT - Neural-Backed Decision Trees

![neural_backed_decision_trees](/images/2020-05-02-latest-in-ai/neural_backed_decision_trees.png)

> Abstract: Deep learning is being adopted in settings where accurate and justifiable predictions are required, ranging from finance to medical imaging. While there has been recent work providing post-hoc explanations for model predictions, there has been relatively little work exploring more directly interpretable models that can match state-of-the-art accuracy. Historically, decision trees have been the gold standard in balancing interpretability and accuracy. However, recent attempts to combine decision trees with deep learning have resulted in models that (1) achieve accuracies far lower than that of modern neural networks (e.g. ResNet) even on small datasets (e.g. MNIST), and (2) require significantly different architectures, forcing practitioners pick between accuracy and interpretability. We forgo this dilemma by creating Neural-Backed Decision Trees (NBDTs) that (1) achieve neural network accuracy and (2) require no architectural changes to a neural network. NBDTs achieve accuracy within 1% of the base neural network on CIFAR10, CIFAR100, TinyImageNet, using recently state-of-the-art WideResNet; and within 2% of EfficientNet on ImageNet. This yields state-of-the-art explainable models on ImageNet, with NBDTs improving the baseline by ~14% to 75.30% top-1 accuracy. Furthermore, we show interpretability of our model's decisions both qualitatively and quantitatively via a semi-automatic process.

> Implementation:| [Pytorch code](https://github.com/alvinwan/neural-backed-decision-trees) | [Colab](https://colab.research.google.com/github/alvinwan/neural-backed-decision-trees/blob/master/examples/load_pretrained_nbdts.ipynb)

> Read the paper [here](https://arxiv.org/abs/2004.00221v1)

---
---

* > Title:  ResNeSt - Split-Attention Networks

![gluon](/images/2020-05-02-latest-in-ai/gluon_demo.gif)

> Abstract: While image classification models have recently continued to advance, most downstream applications such as object detection and semantic segmentation still employ ResNet variants as the backbone network due to their simple and modular structure. We present a simple and modular Split-Attention block that enables attention across feature-map groups. By stacking these Split-Attention blocks ResNet-style, we obtain a new ResNet variant which we call ResNeSt. Our network preserves the overall ResNet structure to be used in downstream tasks straightforwardly without introducing additional computational costs. ResNeSt models outperform other networks with similar model complexities. For example, ResNeSt-50 achieves 81.13% top-1 accuracy on ImageNet using a single crop-size of 224x224, outperforming previous best ResNet variant by more than 1% accuracy. This improvement also helps downstream tasks including object detection, instance segmentation and semantic segmentation. For example, by simply replace the ResNet-50 backbone with ResNeSt-50, we improve the mAP of Faster-RCNN on MS-COCO from 39.3% to 42.3% and the mIoU for DeeplabV3 on ADE20K from 42.1% to 45.1%.

> Task:| IMAGE CLASSIFICATION | INSTANCE SEGMENTATION | OBJECT DETECTION | SEMANTIC SEGMENTATION

> Implementation:| [Tensorflow code](https://github.com/dmlc/gluon-cv) | [Pytorch](https://github.com/zhanghang1989/PyTorch-Encoding)

> Read the paper [here](https://arxiv.org/pdf/2004.08955v1.pdf)

---
---


* > Title:  Lite Transformer with Long-Short Range Attention

![lite_transformer.png](/images/2020-05-02-latest-in-ai/lite_transformer.png)

> Abstract: Transformer has become ubiquitous in natural language processing (e.g., machine translation, question answering); however, it requires enormous amount of computations to achieve high performance, which makes it not suitable for mobile applications that are tightly constrained by the hardware resources and battery. In this paper, we present an efficient mobile NLP architecture, Lite Transformer to facilitate deploying mobile NLP applications on edge devices. The key primitive is the Long-Short Range Attention (LSRA), where one group of heads specializes in the local context modeling (by convolution) while another group specializes in the long-distance relationship modeling (by attention). Such specialization brings consistent improvement over the vanilla transformer on three well-established language tasks: machine translation, abstractive summarization, and language modeling. Under constrained resources (500M/100M MACs), Lite Transformer outperforms transformer on WMT'14 English-French by 1.2/1.7 BLEU, respectively. Lite Transformer reduces the computation of transformer base model by 2.5x with 0.3 BLEU score degradation. Combining with pruning and quantization, we further compressed the model size of Lite Transformer by 18.2x. For language modeling, Lite Transformer achieves 1.8 lower perplexity than the transformer at around 500M MACs. Notably, Lite Transformer outperforms the AutoML-based Evolved Transformer by 0.5 higher BLEU for the mobile NLP setting without the costly architecture search that requires more than 250 GPU years.

> Task:| ABSTRACTIVE TEXT SUMMARIZATION | AUTOML | LANGUAGE MODELLING | MACHINE TRANSLATION | QUANTIZATION | QUESTION ANSWERING

> Implementation:| [Pytorch code](https://github.com/mit-han-lab/lite-transformer)

> Read the paper [here](https://arxiv.org/pdf/2004.11886v1.pdf)

---
---

* > Title:  MASS - Masked Sequence to Sequence Pre-training for Language Generation
![mass.png](/images/2020-05-02-latest-in-ai/mass.png)

> Abstract: Pre-training and fine-tuning, e.g., BERT, have achieved great success in language understanding by transferring knowledge from rich-resource pre-training task to the low/zero-resource downstream tasks. Inspired by the success of BERT, we propose MAsked Sequence to Sequence pre-training (MASS) for the encoder-decoder based language generation tasks. MASS adopts the encoder-decoder framework to reconstruct a sentence fragment given the remaining part of the sentence: its encoder takes a sentence with randomly masked fragment (several consecutive tokens) as input, and its decoder tries to predict this masked fragment. In this way, MASS can jointly train the encoder and decoder to develop the capability of representation extraction and language modeling. By further fine-tuning on a variety of zero/low-resource language generation tasks, including neural machine translation, text summarization and conversational response generation (3 tasks and totally 8 datasets), MASS achieves significant improvements over the baselines without pre-training or with other pre-training methods. Specially, we achieve the state-of-the-art accuracy (37.5 in terms of BLEU score) on the unsupervised English-French translation, even beating the early attention-based supervised model.

> Task:| CONVERSATIONAL RESPONSE GENERATION |MACHINE TRANSLATION | TEXT GENERATION | TEXT SUMMARIZATION | UNSUPERVISED MACHINE TRANSLATION



> Implementation:| [Pytorch code (Microsoft)](https://github.com/microsoft/MASS) | [Pytorch code](https://github.com/microsoft/MPNet)

> Read the paper [here](https://arxiv.org/pdf/1905.02450v5.pdf)

---

That's it, that's what's trending in AI research these days. What do you think?
