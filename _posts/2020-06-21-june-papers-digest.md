---
toc: true
comments: true
author: Wale
image: /images/2020-06-13-lpiair-wk21/oneshotSegmentation.gif
categories: [Trending Research papers]
permalink: /papers/:year/:month/:day/:title
---

# Latest in AI Research - June 2020

![R for Research](https://media.giphy.com/media/26FPC5oAdfeFPkQQE/giphy.gif)

## Author's Notes

Hey there! Here is a collation of what's new in AI research. I am doing things a bit different this time. I thought it would be more readable if I categorized them based on their context. This would also help you browse to the categories using the Table of Contents.

You might also notice that there haven't been posts over the couple of weeks. This is because I plan to transition to monthly posts instead. I am experimenting on this form of delivery to be able to firect more time at delivering on the other sections of this blog such as "how-to's and data hacks.

Now that that's out of the way, here is June's digest of papers.

---
---

## Vision

* > Title:  DetectoRS - Detecting Objects with Recursive Feature Pyramid and Switchable Atrous Convolution

![detectorRS](/images/2020-06-21-june-papers/detectorRS.jpg)

> Abstract: Many modern object detectors demonstrate outstanding performances by using the mechanism of looking and thinking twice. In this paper, we explore this mechanism in the backbone design for object detection. At the macro level, we propose Recursive Feature Pyramid, which incorporates extra feedback connections from Feature Pyramid Networks into the bottom-up backbone layers. At the micro level, we propose Switchable Atrous Convolution, which convolves the features with different atrous rates and gathers the results using switch functions. Combining them results in DetectoRS, which significantly improves the performances of object detection. On COCO test-dev, DetectoRS achieves state-of-the-art 54.7% box AP for object detection, 47.1% mask AP for instance segmentation, and 49.6% PQ for panoptic segmentation. The code is made publicly available.

> Task:|  INSTANCE SEGMENTATION | OBJECT DETECTION | PANOPTIC SEGMENTATION | SEMANTIC SEGMENTATION

> Implementation:| [Qiao, Siyuan and Chen, Liang-Chieh and Yuille, Alan](https://github.com/joe-siyuan-qiao/DetectoRS){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2006.02334v1.pdf){:target="_blank"}

> Currently SOTA for Object Detection on [COCO test-dev](https://paperswithcode.com/sota/object-detection-on-coco){:target="_blank"}

---
---

* > Title: Foreground-aware Semantic Representations for Image Harmonization

![harminization](/images/2020-06-21-june-papers/ih_teaser.jpg)

> Abstract: Image harmonization is an important step in photo editing to achieve visual consistency in composite images by adjusting the appearances of foreground to make it compatible with background. Previous approaches to harmonize composites are based on training of encoder-decoder networks from scratch, which makes it challenging for a neural network to learn a high-level representation of objects. We propose a novel architecture to utilize the space of high-level features learned by a pre-trained classification network. We create our models as a combination of existing encoder-decoder architectures and a pre-trained foreground-aware deep high-resolution network. We extensively evaluate the proposed method on existing image harmonization benchmark and set up a new state-of-the-art in terms of MSE and PSNR metrics.

> Task:|  INSTANCE SEGMENTATION | OBJECT DETECTION | PANOPTIC SEGMENTATION | SEMANTIC SEGMENTATION

> Implementation:| [Konstantin Sofiiuk, Polina Popenova, Anton Konushin](https://github.com/joe-siyuan-qiao/DetectoRS){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2006.00809v1.pdf){:target="_blank"}

---
---

* > Title:  Image Super-Resolution with Cross-Scale Non-Local Attention and Exhaustive Self-Exemplars Mining

![attention](/images/2020-06-21-june-papers/Attention.png)

> Abstract: Deep convolution-based single image super-resolution (SISR) networks embrace the benefits of learning from large-scale external image resources for local recovery, yet most existing works have ignored the long-range feature-wise similarities in natural images. Some recent works have successfully leveraged this intrinsic feature correlation by exploring non-local attention modules. However, none of the current deep models have studied another inherent property of images: cross-scale feature correlation. In this paper, we propose the first Cross-Scale Non-Local (CS-NL) attention module with integration into a recurrent neural network. By combining the new CS-NL prior with local and in-scale non-local priors in a powerful recurrent fusion cell, we can find more cross-scale feature correlations within a single low-resolution (LR) image. The performance of SISR is significantly improved by exhaustively integrating all possible priors. Extensive experiments demonstrate the effectiveness of the proposed CS-NL module by setting new state-of-the-arts on multiple SISR benchmarks.

> Task:|  IMAGE SUPER-RESOLUTION | SUPER-RESOLUTION

> Implementation:| [Lim, Bee and Son, Sanghyun and Kim, Heewon and Nah, Seungjun and Lee, Kyoung Mu](https://github.com/SHI-Labs/Cross-Scale-Non-Local-Attention){:target="_blank"}

---
---

* > Title:  Neural Pose Transfer by Spatially Adaptive Instance Normalization

![npt](/images/2020-06-21-june-papers/npt.jpg)

> Abstract: Pose transfer has been studied for decades, in which the pose of a source mesh is applied to a target mesh. Particularly in this paper, we are interested in transferring the pose of source human mesh to deform the target human mesh, while the source and target meshes may have different identity information. Traditional studies assume that the paired source and target meshes are existed with the point-wise correspondences of user annotated landmarks/mesh points, which requires heavy labelling efforts. On the other hand, the generalization ability of deep models is limited, when the source and target meshes have different identities. To break this limitation, we proposes the first neural pose transfer model that solves the pose transfer via the latest technique for image style transfer, leveraging the newly proposed component -- spatially adaptive instance normalization. Our model does not require any correspondences between the source and target meshes. Extensive experiments show that the proposed model can effectively transfer deformation from source to target meshes, and has good generalization ability to deal with unseen identities or poses of meshes. Code is available at [](https://github.com/jiashunwang/Neural-Pose-Transfer){:target="_blank"}.

> Demo:

{% include youtube.html content="https://youtu.be/1aQAc-bax9U" %}

> Task:|  POSE TRANSFER | STYLE TRANSFER

> Implementation:| [Jiashun Wang](https://github.com/SHI-Labs/Cross-Scale-Non-Local-Attention){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2003.07254v2.pdf){:target="_blank"}

---
---

* > Title:  SEAN - Image Synthesis with Semantic Region-Adaptive Normalization

![sean](/images/2020-06-21-june-papers/sean.png)

> Abstract: We propose semantic region-adaptive normalization (SEAN), a simple but effective building block for Generative Adversarial Networks conditioned on segmentation masks that describe the semantic regions in the desired output image. Using SEAN normalization, we can build a network architecture that can control the style of each semantic region individually, e.g., we can specify one style reference image per region. SEAN is better suited to encode, transfer, and synthesize style than the best previous method in terms of reconstruction quality, variability, and visual quality. We evaluate SEAN on multiple datasets and report better quantitative metrics (e.g. FID, PSNR) than the current state of the art. SEAN also pushes the frontier of interactive image editing. We can interactively edit images by changing segmentation masks or the style for any given region. We can also interpolate styles from two reference images per region.

> Task:|  IMAGE GENERATION

> Implementation:| [Peihao Zhu and Rameen Abdal and Yipeng Qin and Peter Wonka](https://github.com/ZPdesu/SEAN){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/1911.12861v2.pdf){:target="_blank"}

> How to use the UI:

{% include youtube.html content="https://youtu.be/0Vbj9xFgoUw" %}

---
---

* > Title:  End-to-End Object Detection with Transformers

![DETR](/images/2020-06-21-june-papers/DETR.png)

> Abstract: We present a new method that views object detection as a direct set prediction problem. Our approach streamlines the detection pipeline, effectively removing the need for many hand-designed components like a non-maximum suppression procedure or anchor generation that explicitly encode our prior knowledge about the task. The main ingredients of the new framework, called DEtection TRansformer or DETR, are a set-based global loss that forces unique predictions via bipartite matching, and a transformer encoder-decoder architecture. Given a fixed small set of learned object queries, DETR reasons about the relations of the objects and the global image context to directly output the final set of predictions in parallel. The new model is conceptually simple and does not require a specialized library, unlike many other modern detectors. DETR demonstrates accuracy and run-time performance on par with the well-established and highly-optimized Faster RCNN baseline on the challenging COCO object detection dataset. Moreover, DETR can be easily generalized to produce panoptic segmentation in a unified manner. We show that it significantly outperforms competitive baselines.

> Task:| OBJECT DETECTION | PANOPTIC SEGMENTATION

> Implementation:| [Nicolas Carion, Francisco Massa, Gabriel Synnaeve, Nicolas Usunier, Alexander Kirillov, Sergey Zagoruyko](https://github.com/facebookresearch/detr){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2005.12872v3.pdf){:target="_blank"}

> Try it out on [Colab](https://colab.research.google.com/github/facebookresearch/detr/blob/colab/notebooks/detr_demo.ipynb)

---
---

* > Title:   Supervised Contrastive Learning - Tensorflow 2

![DETR](/images/2020-06-21-june-papers/DETR.png)

> Abstract: Cross entropy is the most widely used loss function for supervised training of image classification models. In this paper, we propose a novel training methodology that consistently outperforms cross entropy on supervised learning tasks across different architectures and data augmentations. We modify the batch contrastive loss, which has recently been shown to be very effective at learning powerful representations in the self-supervised setting. We are thus able to leverage label information more effectively than cross entropy. Clusters of points belonging to the same class are pulled together in embedding space, while simultaneously pushing apart clusters of samples from different classes. In addition to this, we leverage key ingredients such as large batch sizes and normalized embeddings, which have been shown to benefit self-supervised learning. On both ResNet-50 and ResNet-200, we outperform cross entropy by over 1%, setting a new state of the art number of 78.8% among methods that use AutoAugment data augmentation. The loss also shows clear benefits for robustness to natural corruptions on standard benchmarks on both calibration and accuracy. Compared to cross entropy, our supervised contrastive loss is more stable to hyperparameter settings such as optimizers or data augmentations.

> Detailed report on the paper: [Wandb](https://app.wandb.ai/authors/scl/reports/Improving-Image-Classification-with-Supervised-Contrastive-Learning--VmlldzoxMzQwNzE){:target="_blank"}

> Task:| CALIBRATION | CALIBRATION | DATA AUGMENTATION | IMAGE CLASSIFICATION | SELF-SUPERVISED LEARNING |

> Implementation:| [Shweta Shaw and Sayak Paul](https://github.com/sayakpaul/Supervised-Contrastive-Learning-in-TensorFlow-2){:target="_blank"}{:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2004.11362v1.pdf){:target="_blank"}

> Try it out on [Colab](https://colab.research.google.com/github/facebookresearch/detr/blob/colab/notebooks/detr_demo.ipynb){:target="_blank"}

---
---

## Natural Language Processing

* > Title:  Cascaded Text Generation with Markov Transformers


![cascaded-generation-fastest](/images/2020-06-21-june-papers/cascaded-generation-fastest.gif)

> Abstract: The two dominant approaches to neural text generation are fully autoregressive models, using serial beam search decoding, and non-autoregressive models, using parallel decoding with no output dependencies. This work proposes an autoregressive model with sub-linear parallel time generation. Noting that conditional random fields with bounded context can be decoded in parallel, we propose an efficient cascaded decoding approach for generating high-quality output. To parameterize this cascade, we introduce a Markov transformer, a variant of the popular fully autoregressive model that allows us to simultaneously decode with specific autoregressive context cutoffs. This approach requires only a small modification from standard autoregressive training, while showing competitive accuracy/speed tradeoff compared to existing methods on five machine translation datasets.

> Task:|  MACHINE TRANSLATION | TEXT GENERATION

> Implementation:| [Yuntian Deng and Alexander M. Rush](https://github.com/harvardnlp/cascaded-generation){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2006.01112v1.pdf){:target="_blank"}

---
---

* > Title:  Language Models are Few-Shot Learners

> Abstract: Recent work has demonstrated substantial gains on many NLP tasks and benchmarks by pre-training on a large corpus of text followed by fine-tuning on a specific task. While typically task-agnostic in architecture, this method still requires task-specific fine-tuning datasets of thousands or tens of thousands of examples. By contrast, humans can generally perform a new language task from only a few examples or from simple instructions - something which current NLP systems still largely struggle to do. Here we show that scaling up language models greatly improves task-agnostic, few-shot performance, sometimes even reaching competitiveness with prior state-of-the-art fine-tuning approaches. Specifically, we train GPT-3, an autoregressive language model with 175 billion parameters, 10x more than any previous non-sparse language model, and test its performance in the few-shot setting. For all tasks, GPT-3 is applied without any gradient updates or fine-tuning, with tasks and few-shot demonstrations specified purely via text interaction with the model. GPT-3 achieves strong performance on many NLP datasets, including translation, question-answering, and cloze tasks, as well as several tasks that require on-the-fly reasoning or domain adaptation, such as unscrambling words, using a novel word in a sentence, or performing 3-digit arithmetic. At the same time, we also identify some datasets where GPT-3's few-shot learning still struggles, as well as some datasets where GPT-3 faces methodological issues related to training on large web corpora. Finally, we find that GPT-3 can generate samples of news articles which human evaluators have difficulty distinguishing from articles written by humans. We discuss broader societal impacts of this finding and of GPT-3 in general.

> Task:| COMMON SENSE REASONING | COREFERENCE RESOLUTION | DOMAIN ADAPTATION | FEW-SHOT LEARNING | LANGUAGE MODELLING | NATURAL LANGUAGE INFERENCE | QUESTION ANSWERING | SENTENCE COMPLETION | UNSUPERVISED MACHINE TRANSLATION | WORD SENSE DISAMBIGUATION

> Implementation:| [OpenAI](https://github.com/openai/gpt-3){:target="_blank"}

{% include alert.html text="This repository has been archived by the owner at this time. It is now read-only." %}
 
> Read the paper [here](https://arxiv.org/pdf/2005.14165v3.pdf){:target="_blank"}

> Currently  SOTA for [Language Modelling on Penn Treebank](https://paperswithcode.com/sota/language-modelling-on-penn-treebank-word){:target="_blank"} (Word Level) (using extra training data).

---
---

* > Title:  FastSpeech 2 - Fast and High-Quality End-to-End Text to Speech

![DETR](/images/2020-06-21-june-papers/DETR.png)

> Abstract: Advanced text to speech (TTS) models such as FastSpeech can synthesize speech significantly faster than previous autoregressive models with comparable quality. The training of FastSpeech model relies on an autoregressive teacher model for duration prediction (to provide more information as input) and knowledge distillation (to simplify the data distribution in output), which can ease the one-to-many mapping problem (i.e., multiple speech variations correspond to the same text) in TTS. However, FastSpeech has several disadvantages: 1) the teacher-student distillation pipeline is complicated, 2) the duration extracted from the teacher model is not accurate enough, and the target mel-spectrograms distilled from teacher model suffer from information loss due to data simplification, both of which limit the voice quality. In this paper, we propose FastSpeech 2, which addresses the issues in FastSpeech and better solves the one-to-many mapping problem in TTS by 1) directly training the model with ground-truth target instead of the simplified output from teacher, and 2) introducing more variation information of speech (e.g., pitch, energy and more accurate duration) as conditional inputs. Specifically, we extract duration, pitch and energy from speech waveform and directly take them as conditional inputs during training and use predicted values during inference. We further design FastSpeech 2s, which is the first attempt to directly generate speech waveform from text in parallel, enjoying the benefit of full end-to-end training and even faster inference than FastSpeech. Experimental results show that 1) FastSpeech 2 and 2s outperform FastSpeech in voice quality with much simplified training pipeline and reduced training time; 2) FastSpeech 2 and 2s can match the voice quality of autoregressive models while enjoying much faster inference speed.

> Task:| SPEECH SYNTHESIS |

> Implementation:| [Dathudeptrai](https://github.com/dathudeptrai/TensorflowTTS){:target="_blank"}
 
> Read the paper [here](https://arxiv.org/pdf/2006.04558v2.pdf){:target="_blank"}

> Currently  SOTA for [Speech Synthesis on North American English](https://paperswithcode.com/sota/speech-synthesis-on-north-american-english){:target="_blank"}.

---
---

## Environments and Frameworks

* > Title:  Acme - A Research Framework for Distributed Reinforcement Learning

![acme]/images/2020-06-21-june-papers/acme.png)

> Abstract: Deep reinforcement learning has led to many recent-and groundbreaking-advancements. However, these advances have often come at the cost of both the scale and complexity of the underlying RL algorithms. Increases in complexity have in turn made it more difficult for researchers to reproduce published RL algorithms or rapidly prototype ideas. To address this, we introduce Acme, a tool to simplify the development of novel RL algorithms that is specifically designed to enable simple agent implementations that can be run at various scales of execution. Our aim is also to make the results of various RL algorithms developed in academia and industrial labs easier to reproduce and extend. To this end we are releasing baseline implementations of various algorithms, created using our framework. In this work we introduce the major design decisions behind Acme and show how these are used to construct these baselines. We also experiment with these agents at different scales of both complexity and computation-including distributed versions. Ultimately, we show that the design decisions behind Acme lead to agents that can be scaled both up and down and that, for the most part, greater levels of parallelization result in agents with equivalent performance, just faster.

> More Information:|  [Deepmind Blogpost](https://deepmind.com/research/publications/Acme){:target="_blank"}

> Examples:| [DeepMind GitHub](https://github.com/deepmind/acme/tree/master/examples){:target="_blank"}

> Implementation:| [DeepMind](https://github.com/deepmind/acme){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/2006.00979v1.pdf){:target="_blank"}

---
---

## Reinforcement Learning

* > Title:  Adversarial Colorization Of Icons Based On Structure And Color Conditions

![colorization_of_icons](/images/2020-06-13-lpiair-wk21/colorization-of-icons.png)

> Abstract: We present a system to help designers create icons that are widely used in banners, signboards, billboards, homepages, and mobile apps. Designers are tasked with drawing contours, whereas our system colorizes contours in different styles. This goal is achieved by training a dual conditional generative adversarial network (GAN) on our collected icon dataset. One condition requires the generated image and the drawn contour to possess a similar contour, while the other anticipates the image and the referenced icon to be similar in color style. Accordingly, the generator takes a contour image and a man-made icon image to colorize the contour, and then the discriminators determine whether the result fulfills the two conditions. The trained network is able to colorize icons demanded by designers and greatly reduces their workload. For the evaluation, we compared our dual conditional GAN to several state-of-the-art techniques. Experiment results demonstrate that our network is over the previous networks. Finally, we will provide the source code, icon dataset, and trained network for public use.

> Task:|  COLORIZATION

> Implementation:| [Pytorch](https://github.com/jxcodetw/Adversarial-Colorization-Of-Icons-Based-On-Structure-And-Color-Conditions){:target="_blank"}

> Read the paper [here](https://arxiv.org/pdf/1910.05253v1.pdf){:target="_blank"}

---
---
