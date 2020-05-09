---
toc: true
comments: true
author: Wale
image: /images/latest-in-ai/convlayer_overview_demo.gif
categories: [Trending Research papers]
permalink: /papers/:year/:month/:day/:title
---

# Latest in AI Research - Week 19

![R for Research](https://media.giphy.com/media/26FPC5oAdfeFPkQQE/giphy.gif)

Hey there! It's another Tuesday, and here is a collation of what's new in AI research.

* > Title:  CNN Explainer - Learning Convolutional Neural Networks with Interactive Visualization

![cnn-explainer](/images/latest-in-ai/convlayer_overview_demo.gif)

> Abstract: Deep learning's great success motivates many practitioners and students to learn about this exciting technology. However, it is often challenging for beginners to take their first step due to the complexity of understanding and applying deep learning. We present CNN Explainer, an interactive visualization tool designed for non-experts to learn and examine convolutional neural networks (CNNs), a foundational deep learning model architecture. Our tool addresses key challenges that novices face while learning about CNNs, which we identify from interviews with instructors and a survey with past students. Users can interactively visualize and inspect the data transformation and flow of intermediate results in a CNN. CNN Explainer tightly integrates a model overview that summarizes a CNN's structure, and on-demand, dynamic visual explanation views that help users understand the underlying components of CNNs. Through smooth transitions across levels of abstraction, our tool enables users to inspect the interplay between low-level operations (e.g., mathematical computations) and high-level outcomes (e.g., class predictions). To better understand our tool's benefits, we conducted a qualitative user study, which shows that CNN Explainer can help users more easily understand the inner workings of CNNs, and is engaging and enjoyable to use. We also derive design lessons from our study. Developed using modern web technologies, CNN Explainer runs locally in users' web browsers without the need for installation or specialized hardware, broadening the public's education access to modern deep learning techniques.

> Task:| Explainability

> Implementation:| [code](https://github.com/poloclub/cnn-explainer) - Tensorflow

> Authors:| Zijie J | Wang | Robert Turko | Omar Shaikh | Haekyu Park | Nilaksh Das | Fred Hohman | Minsuk Kahng | Duen Horng Chau

> Read the paper [here](https://arxiv.org/pdf/2004.15004v2.pdf)

> Other Resources:| [CNN Explainer article](https://poloclub.github.io/cnn-explainer/) | [youtube](https://www.youtube.com/watch?v=HnWIHWFbuUQ&feature=youtu.be)

---

* > Title:  Jukebox: A Generative Model for Music

![jukebox](/images/latest-in-ai/jukebox.jpg)

> Abstract:We introduce Jukebox, a model that generates music with singing in the raw audio domain. We tackle the long context of raw audio using a multiscale VQ-VAE to compress it to discrete codes, and modeling those using autoregressive Transformers. We show that the combined model at scale can generate high-fidelity and diverse songs with coherence up to multiple minutes. We can condition on artist and genre to steer the musical and vocal style, and on unaligned lyrics to make the singing more controllable. We are releasing thousands of non cherry-picked samples, along with model weights and code.

> Task:| Music Generation

> Implementation:| [code](https://github.com/openai/jukebox/)

> Authors:| Prafulla Dhariwal | Heewoo Jun | Christine Payne | Jong Wook Kim | Alec Radford | Ilya Sutskever

> Read the paper [here](https://cdn.openai.com/papers/jukebox.pdf)

> Other Resources:| [OpenAI Blog](https://openai.com/blog/jukebox/)

---

* > Title:  Alleviating the Inconsistency Problem of Applying Graph Neural Network to Fraud Detection 

![gnn](/images/latest-in-ai/inconsistency.png)

> Abstract: The graph-based model can help to detect suspicious fraud online. Owing to the development of Graph Neural Networks~(GNNs), prior research work has proposed many GNN-based fraud detection frameworks based on either homogeneous graphs or heterogeneous graphs. These work follow the existing GNN framework by aggregating the neighboring information to learn the node embedding, which lays on the assumption that the neighbors share similar context, features, and relations. However, the inconsistency problem is hardly investigated, i.e., the context inconsistency, feature inconsistency, and relation inconsistency. In this paper, we introduce these inconsistencies and design a new GNN framework, GraphConsis, to tackle the inconsistency problem: (1) for the context inconsistency, we propose to combine the context embeddings with node features, (2) for the feature inconsistency, we design a consistency score to filter the inconsistent neighbors and generate corresponding sampling probability, and (3) for the relation inconsistency, we learn a relation attention weights associated with the sampled nodes. Empirical analysis on four datasets indicates the inconsistency problem is crucial in a fraud detection task. The extensive experiments prove the effectiveness of GraphConsis. We also released a GNN-based fraud detection toolbox with implementations of SOTA models.

> Task:| Fraud Detection

> Implementation:| [code](https://github.com/safe-graph/DGFraud)

> Authors:| Zhiwei Liu | Yingtong Dou | Philip S. Yu | Yutong Deng | Hao Peng

> Read the paper [here](https://arxiv.org/pdf/2005.00625v1.pdf)

---

* > Title:  TLDR - Extreme Summarization of Scientific Documents

> Abstract: We introduce TLDR generation for scientific papers, a new automatic summarization task with high source compression, requiring expert background knowledge and complex language understanding. To facilitate research on this task, we introduce SciTLDR, a dataset of 3.9K TLDRs. Furthermore, we introduce a novel annotation protocol for scalably curating additional gold summaries by rewriting peer review comments. We use this protocol to augment our test set, yielding multiple gold TLDRs for evaluation, which is unlike most recent summarization datasets that assume only one valid gold summary. We present a training strategy for adapting pretrained language models that exploits similarities between TLDR generation and the related task of title generation, which outperforms strong extractive and abstractive summarization baselines.

> Task:| Abstractive text summarization

> Implementation:| [code](https://github.com/allenai/scitldr)

> Authors:| Isabel Cachola | Kyle Lo | Arman Cohan | Daniel S. Weld

> Read the paper [here](https://arxiv.org/pdf/2004.15011v2.pdf)

> Other resources: [Demo](https://scitldr.apps.allenai.org/)

---

* > Title:  GIMP-ML - Python Plugins for using Computer Vision Models in GIMP

![gimp](/images/latest-in-ai/gimp.png)

> Abstract: This paper introduces GIMP-ML, a set of Python plugins for the widely popular GNU Image Manipulation Program (GIMP). It enables the use of recent advances in computer vision to the conventional image editing pipeline in an open-source setting. Applications from deep learning such as monocular depth estimation, semantic segmentation, mask generative adversarial networks, image super-resolution, de-noising and coloring have been incorporated with GIMP through Python-based plugins. Additionally, operations on images such as edge detection and color clustering have also been added. GIMP-ML relies on standard Python packages such as numpy, scikit-image, pillow, pytorch, open-cv, scipy. Apart from these, several image manipulation techniques using these plugins have been compiled and demonstrated in the YouTube [playlist](https://www.youtube.com/playlist?list=PLo9r5wFmpD5dLWTyo6NOiD6BJjhfEOM5t) with the objective of demonstrating the use-cases for machine learning based image modification. In addition, GIMP-ML also aims to bring the benefits of using deep learning networks used for computer vision tasks to routine image processing workflows.

> Task:| DEPTH ESTIMATION | EDGE DETECTION | IMAGE SUPER-RESOLUTION | MONOCULAR DEPTH ESTIMATION | SEMANTIC SEGMENTATION 

> Implementation:| [code](https://github.com/kritiksoman/GIMP-ML)

> Authors:| Kritik Soman

> Read the paper [here](https://arxiv.org/pdf/2004.13060v1.pdf)

---

* > Title:  TAPAS - Weakly Supervised Table Parsing via Pre-training

![tapas](/images/latest-in-ai/tapas.png)

> Abstract: Answering natural language questions over tables is usually seen as a semantic parsing task. To alleviate the collection cost of full logical forms, one popular approach focuses on weak supervision consisting of denotations instead of logical forms. However, training semantic parsers from weak supervision poses difficulties, and in addition, the generated logical forms are only used as an intermediate step prior to retrieving the denotation. In this paper, we present TAPAS, an approach to question answering over tables without generating logical forms. TAPAS trains from weak supervision, and predicts the denotation by selecting table cells and optionally applying a corresponding aggregation operator to such selection. TAPAS extends BERT's architecture to encode tables as input, initializes from an effective joint pre-training of text segments and tables crawled from Wikipedia, and is trained end-to-end. We experiment with three different semantic parsing datasets, and find that TAPAS outperforms or rivals semantic parsing models by improving state-of-the-art accuracy on SQA from 55.1 to 67.2 and performing on par with the state-of-the-art on WIKISQL and WIKITQ, but with a simpler model architecture. We additionally find that transfer learning, which is trivial in our setting, from WIKISQL to WIKITQ, yields 48.7 accuracy, 4.2 points above the state-of-the-art.

> Task:| QUESTION ANSWERING | SEMANTIC PARSING | TRANSFER LEARNING

> Implementation:| [code](https://github.com/google-research/tapas)

> Authors:| Jonathan Herzig | Paweł Krzysztof Nowak | Thomas Müller | Francesco Piccinno | Julian Martin Eisenschlos

> Read the paper [here](https://arxiv.org/pdf/2004.02349v2.pdf)

---

* > Title:  Reinforcement Learning with Augmented Data

![rlad](/images/latest-in-ai/RLAD.png)

> Abstract: Learning from visual observations is a fundamental yet challenging problem in reinforcement learning (RL). Although algorithmic advancements combined with convolutional neural networks have proved to be a recipe for success, current methods are still lacking on two fronts: (a) sample efficiency of learning and (b) generalization to new environments. To this end, we present RAD: Reinforcement Learning with Augmented Data, a simple plug-and-play module that can enhance any RL algorithm. We show that data augmentations such as random crop, color jitter, patch cutout, and random convolutions can enable simple RL algorithms to match and even outperform complex state-of-the-art methods across common benchmarks in terms of data-efficiency, generalization, and wall-clock speed. We find that data diversity alone can make agents focus on meaningful information from high-dimensional observations without any changes to the reinforcement learning method. On the DeepMind Control Suite, we show that RAD is state-of-the-art in terms of data-efficiency and performance across 15 environments. We further demonstrate that RAD can significantly improve the test-time generalization on several OpenAI ProcGen benchmarks. Finally, our customized data augmentation modules enable faster wall-clock speed compared to competing RL techniques.

> Task:| DATA AUGMENTATION

> Implementation:| [code](https://github.com/MishaLaskin/rad)

> Authors:| Michael Laskin | Kimin Lee | Adam Stooke | Lerrel Pinto | Pieter Abbeel | Aravind Srinivas

> Read the paper [here](https://arxiv.org/pdf/2004.14990v2.pdf)

---

* > Title:  TTNet - Real-time temporal and spatial video analysis of table tennis

![rlad](/images/latest-in-ai/RLAD.png)

> Abstract: Learning from visual observations is a fundamental yet challenging problem in reinforcement learning (RL). Although algorithmic advancements combined with convolutional neural networks have proved to be a recipe for success, current methods are still lacking on two fronts: (a) sample efficiency of learning and (b) generalization to new environments. To this end, we present RAD: Reinforcement Learning with Augmented Data, a simple plug-and-play module that can enhance any RL algorithm. We show that data augmentations such as random crop, color jitter, patch cutout, and random convolutions can enable simple RL algorithms to match and even outperform complex state-of-the-art methods across common benchmarks in terms of data-efficiency, generalization, and wall-clock speed. We find that data diversity alone can make agents focus on meaningful information from high-dimensional observations without any changes to the reinforcement learning method. On the DeepMind Control Suite, we show that RAD is state-of-the-art in terms of data-efficiency and performance across 15 environments. We further demonstrate that RAD can significantly improve the test-time generalization on several OpenAI ProcGen benchmarks. Finally, our customized data augmentation modules enable faster wall-clock speed compared to competing RL techniques.

> Task:| SEMANTIC SEGMENTATION | DECISION MAKING

> Implementation:| No code implementation yet

> Authors:| Roman Voeikov | Nikolay Falaleev | Ruslan Baikulov

> Read the paper [here](https://arxiv.org/pdf/2004.09927)

---

That's it folks. These arew what I've found most interesting in the past week.

Which paper interests you? Which would you like to see imlemented in an easily accessible colab notebook? Let me know in the comments below!

Until next time, stay safe!
