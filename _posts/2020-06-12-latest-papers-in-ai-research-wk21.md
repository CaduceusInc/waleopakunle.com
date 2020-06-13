---
toc: true
comments: true
author: Wale
image: /images/2020-06-13-lpiair-wk21/oneshotSegmentation.gif
categories: [Trending Research papers]
permalink: /papers/:year/:month/:day/:title
---

# Latest in AI Research - Week 21

![R for Research](https://media.giphy.com/media/26FPC5oAdfeFPkQQE/giphy.gif)

Hey there! Here is a collation of what's new in AI research.

* > Title:  Adversarial Colorization Of Icons Based On Structure And Color Conditions

![colorization_of_icons](/images/2020-06-13-lpiair-wk21/colorization-of-icons.png)

> Abstract: We present a system to help designers create icons that are widely used in banners, signboards, billboards, homepages, and mobile apps. Designers are tasked with drawing contours, whereas our system colorizes contours in different styles. This goal is achieved by training a dual conditional generative adversarial network (GAN) on our collected icon dataset. One condition requires the generated image and the drawn contour to possess a similar contour, while the other anticipates the image and the referenced icon to be similar in color style. Accordingly, the generator takes a contour image and a man-made icon image to colorize the contour, and then the discriminators determine whether the result fulfills the two conditions. The trained network is able to colorize icons demanded by designers and greatly reduces their workload. For the evaluation, we compared our dual conditional GAN to several state-of-the-art techniques. Experiment results demonstrate that our network is over the previous networks. Finally, we will provide the source code, icon dataset, and trained network for public use.

> Task:|  COLORIZATION

> Implementation:| [Pytorch](https://github.com/jxcodetw/Adversarial-Colorization-Of-Icons-Based-On-Structure-And-Color-Conditions){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/1910.05253v1.pdf){:target="_blank"}

---
---

* > Title:  DeepFaceFlow - In-the-wild Dense 3D Facial Motion Estimation

![deepFaceFlow](/images/2020-06-13-lpiair-wk21/deepFaceFlow.png)

> Abstract: Dense 3D facial motion capture from only monocular in-the-wild pairs of RGB images is a highly challenging problem with numerous applications, ranging from facial expression recognition to facial reenactment. In this work, we propose DeepFaceFlow, a robust, fast, and highly-accurate framework for the dense estimation of 3D non-rigid facial flow between pairs of monocular images. Our DeepFaceFlow framework was trained and tested on two very large-scale facial video datasets, one of them of our own collection and annotation, with the aid of occlusion-aware and 3D-based loss function. We conduct comprehensive experiments probing different aspects of our approach and demonstrating its improved performance against state-of-the-art flow and 3D reconstruction methods. Furthermore, we incorporate our framework in a full-head state-of-the-art facial video synthesis method and demonstrate the ability of our method in better representing and capturing the facial dynamics, resulting in a highly-realistic facial video synthesis. Given registered pairs of images, our framework generates 3D flow maps at ~60 fps.

> Task:| 3D RECONSTRUCTION | FACIAL EXPRESSION RECOGNITION | MOTION CAPTURE | MOTION ESTIMATION

> Implementation:

{% include alert.html text="The group has only released a peper as at the time of writing this post. The dataset used and code implementations are still in the works and you can [stay updated here.](https://github.com/mrkoujan/DeepFaceFlow)" %}

> Read the paper [here](https://arxiv.org/pdf/2005.07298v1.pdf){:target="_blank"}

---
---

* > Title: EfficientPS - Efficient Panoptic Segmentation

Demo:

{% include youtube.html content="https://youtu.be/mvcNEQcxo3w" %}

> Abstract: Understanding the scene in which an autonomous robot operates is critical for its competent functioning. Such scene comprehension necessitates recognizing instances of traffic participants along with general scene semantics which can be effectively addressed by the panoptic segmentation task. In this paper, we introduce the Efficient Panoptic Segmentation (EfficientPS) architecture that consists of a shared backbone which efficiently encodes and fuses semantically rich multi-scale features. We incorporate a new semantic head that aggregates fine and contextual features coherently and a new variant of Mask R-CNN as the instance head. We also propose a novel panoptic fusion module that congruously integrates the output logits from both the heads of our EfficientPS architecture to yield the final panoptic segmentation output. Additionally, we introduce the KITTI panoptic segmentation dataset that contains panoptic annotations for the popularly challenging KITTI benchmark. Extensive evaluations on Cityscapes, KITTI, Mapillary Vistas and Indian Driving Dataset demonstrate that our proposed architecture consistently sets the new state-of-the-art on all these four benchmarks while being the most efficient and fast panoptic segmentation architecture to date.

Below is a short video that summarises this awesome piece of work. You will get a visual understanding of what image segmentation is about, the architecture used to achieve this, as well as see it in action:

{% include youtube.html content="https://youtu.be/j11mvFqFmfA" %}

> Task:| INSTANCE SEGMENTATION | PANOPTIC SEGMENTATION | SEMANTIC SEGMENTATION

> Implementation:

{% include alert.html text=" This piece is licenced under the GPL-3 License. It is currently the state of the art (SOTA) for Panoptic Segmentation based on the _Mapillary val_ dataset. Due to the inherent nature of the GPL-3 License, you need to contact the authors to get the source code. However, you can read a short article on its usage, architecture  as well as see several demos [here](http://panoptic.cs.uni-freiburg.de/) and see the License [here](https://github.com/DeepSceneSeg/EfficientPS)." %}


{% include alert.html text="Links in alert boxes do not open into a new window... yet. Work in progress." %}


> Read the paper [here](https://arxiv.org/pdf/2004.02307v2.pdf){:target="_blank"}

> Current SOTA for [Panoptic Segmentation on Mapillary val](https://paperswithcode.com/sota/panoptic-segmentation-on-mapillary-val){:target="_blank"}

---
---

* > Title:  Order-Aware Generative Modeling Using the 3D-Craft Dataset

![voxelcnn](/images/2020-06-13-lpiair-wk21/voxelcnn.png)

> Abstract: In this paper, we study the problem of sequentially building houses in the game of Minecraft, and demonstrate that learning the ordering can make for more effective autoregressive models. Given a partially built house made by a human player, our system tries to place additional blocks in a human-like manner to complete the house. We introduce a new dataset, HouseCraft, for this new task. HouseCraft contains the sequential order in which 2,500 Minecraft houses were built from scratch by humans. The human action sequences enable us to learn an order-aware generative model called Voxel-CNN. In contrast to many generative models where the sequential generation ordering either does not matter (e.g. holistic generation with GANs), or is manually/arbitrarily set by simple rules (e.g. raster-scan order), our focus is on an ordered generation that imitates humans. To evaluate if a generative model can accurately predict human-like actions, we propose several novel quantitative metrics. We demonstrate that our Voxel-CNN model is simple and effective at this creative task, and can serve as a strong baseline for future research in this direction. The HouseCraft dataset and code with baseline models will be made publicly available. 

> Task:| HOUSE GENERATION

> Implementation:| [Facebook Research's Pytorch Code](https://github.com/facebookresearch/VoxelCNN){:target="_blank"}

> Read the paper [here](http://openaccess.thecvf.com/content_ICCV_2019/papers/Chen_Order-Aware_Generative_Modeling_Using_the_3D-Craft_Dataset_ICCV_2019_paper.pdf){:target="_blank"}

---
---

* > Title:  U<sup>2</sup>-Net - Going Deeper with Nested U-Structure for Salient Object Detection 

![U2Net](/images/2020-06-13-lpiair-wk21/U2Net.png)

> Abstract: In this paper, we design a simple yet powerful deep network architecture, U<sup>2</sup>-Net, for salient object detection (SOD). The architecture of our U<sup>2</sup>-Net is a two-level nested U-structure. The design has the following advantages: (1) it is able to capture more contextual information from different scales thanks to the mixture of receptive fields of different sizes in our proposed ReSidual U-blocks (RSU), (2) it increases the depth of the whole architecture without significantly increasing the computational cost because of the pooling operations used in these RSU blocks. This architecture enables us to train a deep network from scratch without using backbones from image classification tasks. We instantiate two models of the proposed architecture, U2-Net (176.3 MB, 30 FPS on GTX 1080Ti GPU) and U2-Net† (4.7 MB, 40 FPS), to facilitate the usage in different environments. Both models achieve competitive performance on six SOD datasets. The code is available: [here](https://github.com/NathanUA/U-2-Net.){:target="_blank"}

> Task:| IMAGE CLASSIFICATION | OBJECT DETECTION | SALIENT OBJECT DETECTION

> Implementation:| [code](https://github.com/NathanUA/U-2-Net){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2005.09007v1.pdf){:target="_blank"}

This code has been used in [this AR Project by Cyril](https://github.com/cyrildiagne/ar-cutpaste){:target="_blank"}


---
---

* > Title: Surfboard: Audio Feature Extraction for Modern Machine Learning

![surfboard](/images/2020-06-13-lpiair-wk21/surfboard.png)

> Abstract: We introduce Surfboard, an open-source Python library for extracting audio features with application to the medical domain. Surfboard is written with the aim of addressing pain points of existing libraries and facilitating joint use with modern machine learning frameworks. The package can be accessed both programmatically in Python and via its command line interface, allowing it to be easily integrated within machine learning workflows. It builds on state-of-the-art audio analysis packages and offers multiprocessing support for processing large workloads. We review similar frameworks and describe Surfboard's architecture, including the clinical motivation for its features. Using the mPower dataset, we illustrate Surfboard's application to a Parkinson's disease classification task, highlighting common pitfalls in existing research. The source code is opened up to the research community to facilitate future audio research in the clinical domain.

> Task:| AUDIO FEATURE EXTRACTION

> Implementation:| [code](https://github.com/novoic/surfboard){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2005.08848v1.pdf){:target="_blank"}

---
---

* > Title: Single-Stage Semantic Segmentation from Image Labels

![oneshotSegmentation](/images/2020-06-13-lpiair-wk21/oneshotSegmentation.gif)

> Abstract: Recent years have seen a rapid growth in new approaches improving the accuracy of semantic segmentation in a weakly supervised setting, i.e. with only image-level labels available for training. However, this has come at the cost of increased model complexity and sophisticated multi-stage training procedures. This is in contrast to earlier work that used only a single stage − training one segmentation network on image labels − which was abandoned due to inferior segmentation accuracy. In this work, we first define three desirable properties of a weakly supervised method: local consistency, semantic fidelity, and completeness. Using these properties as guidelines, we then develop a segmentation-based network model and a self-supervised training scheme to train for semantic masks from image-level annotations in a single stage. We show that despite its simplicity, our method achieves results that are competitive with significantly more complex pipelines, substantially outperforming earlier single-stage methods.

> Task:| SEMANTIC SEGMENTATION

> Implementation:| [code](https://github.com/visinf/1-stage-wseg){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2005.08104v1.pdf){:target="_blank"}

---
---

* > Title: Flowtron - an Autoregressive Flow-based Generative Network for Text-to-Speech Synthesis

![Flowtron](https://nv-adlr.github.io/images/flowtron_logo.png)

> Abstract: In this paper we propose Flowtron: an autoregressive flow-based generative network for text-to-speech synthesis with control over speech variation and style transfer. Flowtron borrows insights from IAF and revamps Tacotron in order to provide high-quality and expressive mel-spectrogram synthesis. Flowtron is optimized by maximizing the likelihood of the training data, which makes training simple and stable. Flowtron learns an invertible mapping of data to a latent space that can be manipulated to control many aspects of speech synthesis (pitch, tone, speech rate, cadence, accent). Our mean opinion scores (MOS) show that Flowtron matches state-of-the-art TTS models in terms of speech quality. In addition, we provide results on control of speech variation, interpolation between samples and style transfer between speakers seen and unseen during training. Code and pre-trained models will be made publicly available at [Github]](https://github.com/NVIDIA/flowtron)

> Task:| TEXT-TO-SPEECH SYNTHESIS | STYLE TRANSFER | SPEECH SYNTHESIS

> Implementation:| [NVIDIA Pytorch code](https://github.com/NVIDIA/flowtron){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2005.05957v2.pdf){:target="_blank"}

---
---

* > Title: Variational quantum Gibbs state preparation with a truncated Taylor series

> Abstract: The preparation of quantum Gibbs state is an essential part of quantum computation and has wide-ranging applications in various areas, including quantum simulation, quantum optimization, and quantum machine learning. In this paper, we propose variational hybrid quantum-classical algorithms for quantum Gibbs state preparation. We first utilize a truncated Taylor series to evaluate the free energy and choose the truncated free energy as the loss function. Our protocol then trains the parameterized quantum circuits to learn the desired quantum Gibbs state. Notably, this algorithm can be implemented on near-term quantum computers equipped with parameterized quantum circuits. By performing numerical experiments, we show that shallow parameterized circuits with only one additional qubit can be trained to prepare the Ising chain and spin chain Gibbs states with a fidelity higher than 95%. In particular, for the Ising chain model, we find that a simplified circuit ansatz with only one parameter and one additional qubit can be trained to realize a 99% fidelity in Gibbs state preparation at inverse temperatures larger than 2.

> Task:| QUANTUM MACHINE LEARNING

> Implementation:| [Github, Chinese](https://github.com/PaddlePaddle/Quantum){:target="_blank"} | [Github, English Translated](http://translate.google.com/translate?hl=en&sl=auto&tl=en&u=https%3A%2F%2Fgithub.com%2FPaddlePaddle%2FQuantum){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2005.08797v1.pdf){:target="_blank"}

---
---

* > Title: Neural Controlled Differential Equations for Irregular Time Series

{% include youtube.html content="https://youtu.be/sbcIKugElZ4" %}

> Abstract: Neural ordinary differential equations are an attractive option for modelling temporal dynamics. However, a fundamental issue is that the solution to an ordinary differential equation is determined by its initial condition, and there is no mechanism for adjusting the trajectory based on subsequent observations. Here, we demonstrate how this may be resolved through the well-understood mathematics of \emph{controlled differential equations}. The resulting \emph{neural controlled differential equation} model is directly applicable to the general setting of partially-observed irregularly-sampled multivariate time series, and (unlike previous work on this problem) it may utilise memory-efficient adjoint-based backpropagation even across observations. We demonstrate that our model achieves state-of-the-art performance against similar (ODE or RNN based) models in empirical studies on a range of datasets. Finally we provide theoretical results demonstrating universal approximation, and that our model subsumes alternative ODE models.

> Task:| IRREGULAR TIME SERIES | TIME SERIES

> Implementation:| [code](https://github.com/patrick-kidger/NeuralCDE){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2005.08926v1.pdf){:target="_blank"}

---
---

## Other ways to catch up on research

### Henry AI Labs

Truth be told, I thought to create this section because Henry does what he does exceedingly well. In fact, I look forward to his posts every week. Here's the one he released for the corresponding 21<sup>st<sup> week of the year 2020:

{% include youtube.html content="https://youtu.be/BA2Ft6YlG4g" %}

Here he describes what could potentially help me automate my "paper summary" adventures:

{% include youtube.html content="https://youtu.be/5WJZgSwRUSQ" %}

### Two minute papers

If you don't know about Dr Károly Zsolnai-Fehér, let me introduce you to a master storyteller. He (and his team) do an outstanding job on all their videos. He makes catching up on AI developments a breeze, and very enjoyable. For example, have a look at how he talks about OpenAI’s Jukebox AI.

{% include youtube.html content="https://youtu.be/6oQ0Obi14rM" %}

---
---

That's it folks. These are were the trendy papers for the 21<sup>st</sup> week of 2020.

I am particularly happy that I had found a lot more demos to append to the papers than all my previous posts.

These researchers are the absolute best, and you all have been an excellent audience. You all have my heartfelt appreciation.

Which paper interests you? Which would you like to see imlemented in an easily accessible colab notebook? Let me know in the comments below!

Until next time, stay safe!
