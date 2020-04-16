---
toc: true
comments: true
author: Wale
image: /images/latest-in-ai/3D-Photography-latest-in-ai.png
categories: [Trending Research papers]
permalink: /papers/:year/:month/:day/:title
---

Hey there folks! 
Here is a list of the latest in deep learning research, along with abstract extracts!

![Research is hard work](https://media.giphy.com/media/3oxHQr6r2x0GqGnois/giphy.gif)


1. Title:  3D Photography using Context-aware Layered Depth Inpainting

> Abstract: We propose a method for converting a single RGB-D input image into a 3D photo - a multi-layer representation for novel view synthesis that contains hallucinated color and depth structures in regions occluded in the original view. We use a Layered Depth Image with explicit pixel connectivity as underlying representation, and present a learning-based inpainting model that synthesizes new local color-and-depth content into the occluded region in a spatial context-aware manner. The resulting 3D photos can be efficiently rendered with motion parallax using standard graphics engines. We validate the effectiveness of our method on a wide range of challenging everyday scenes and show fewer artifacts compared with the state of the arts.

> Task: Novel View Synthesis

> Implementation: [code](https://github.com/vt-vl-lab/3d-photo-inpainting) | colab coming soon.

> Read the paper [here](https://arxiv.org/pdf/2004.04727v2.pdf)


2. > Title: EfficientDet: Scalable and Efficient Object Detection

> Abstract: Model efficiency has become increasingly important in computer vision. In this paper, we systematically study neural network architecture design choices for object detection and propose several key optimizations to improve efficiency. First, we propose a weighted bi-directional feature pyramid network (BiFPN), which allows easy and fast multi-scale feature fusion; Second, we propose a compound scaling method that uniformly scales the resolution, depth, and width for all backbone, feature network, and box/class prediction networks at the same time. Based on these optimizations and EfficientNet backbones, we have developed a new family of object detectors, called EfficientDet, which consistently achieve much better efficiency than prior art across a wide spectrum of resource constraints. In particular, with single-model and single-scale, our EfficientDet-D7 achieves state-of-the-art 52.2 AP on COCO test-dev with 52M parameters and 325B FLOPs, being 4x - 9x smaller and using 13x - 42x fewer FLOPs than previous detectors.

> Task: AutoML | Object Detection

> Implementation: [code](https://github.com/zylo117/Yet-Another-EfficientDet-Pytorch) | Colab coming soon

> Read the paper [here](https://arxiv.org/pdf/1911.09070v4.pdf)


3. > Title: Longformer: The Long-Document Transformer

> Abstract: Transformer-based models are unable to process long sequences due to their self-attention operation, which scales quadratically with the sequence length. To address this limitation, we introduce the Longformer with an attention mechanism that scales linearly with sequence length, making it easy to process documents of thousands of tokens or longer. Longformer's attention mechanism is a drop-in replacement for the standard self-attention and combines a local windowed attention with a task motivated global attention. Following prior work on long-sequence transformers, we evaluate Longformer on character-level language modeling and achieve state-of-the-art results on text8 and enwik8. In contrast to most prior work, we also pretrain Longformer and finetune it on a variety of downstream tasks. Our pretrained Longformer consistently outperforms RoBERTa on long document tasks and sets new state-of-the-art results on WikiHop and TriviaQA.

> Task: Language Modeling

> Implementation: [code](https://github.com/allenai/longformer)

> Read the paper [here](https://arxiv.org/pdf/2004.05150v1.pdf)


4. > Title: A Simple Baseline for Multi-Object Tracking

> Abstract: There has been remarkable progress on object detection and re-identification in recent years which are the core components for multi-object tracking. However, little attention has been focused on accomplishing the two tasks in a single network to improve the inference speed. The initial attempts along this path ended up with degraded results mainly because the re-identification branch is not appropriately learned. In this work, we study the essential reasons behind the failure, and accordingly present a simple baseline to addresses the problems. It remarkably outperforms the state-of-the-arts on the public datasets at 30 fps. We hope this baseline could inspire and help evaluate new ideas in this field.

>Task: Multi-object tracking | Object detection | Object tracking

> Implementation: [code](https://github.com/ifzhang/FairMOT)

> Read the paper [here](https://arxiv.org/pdf/2004.01888v2.pdf)


5. > Title: Learning to Explore using Active Neural SLAM

> Abstract: This work presents a modular and hierarchical approach to learn policies for exploring 3D environments, called `Active Neural SLAM'. Our approach leverages the strengths of both classical and learning-based methods, by using analytical path planners with learned SLAM module, and global and local policies. The use of learning provides flexibility with respect to input modalities (in the SLAM module), leverages structural regularities of the world (in global policies), and provides robustness to errors in state estimation (in local policies). Such use of learning within each module retains its benefits, while at the same time, hierarchical decomposition and modular training allow us to sidestep the high sample complexities associated with training end-to-end policies. Our experiments in visually and physically realistic simulated 3D environments demonstrate the effectiveness of our approach over past learning and geometry-based approaches. The proposed model can also be easily transferred to the PointGoal task and was the winning entry of the CVPR 2019 Habitat PointGoal Navigation Challenge.

> Task: Point goal Navigation

> Implementation: [code](https://github.com/devendrachaplot/Neural-SLAM)

> Read the paper [here](https://arxiv.org/pdf/2004.05155v1.pdf)


6. > Title: Top-1 Solution of Multi-Moments in Time Challenge 2019

> Abstract: In this technical report, we briefly introduce the solutions of our team 'Efficient' for the Multi-Moments in Time challenge in ICCV 2019. We first conduct several experiments with popular Image-Based action recognition methods TRN, TSN, and TSM. Then a novel temporal interlacing network is proposed towards fast and accurate recognition. Besides, the SlowFast network and its variants are explored. Finally, we ensemble all the above models and achieve 67.22\% on the validation set and 60.77\% on the test set, which ranks 1st on the final leaderboard. In addition, we release a new code repository for video understanding which unifies state-of-the-art 2D and 3D methods based on PyTorch.

> Task: Video understanding

> Implementation: [code](https://github.com/Sense-X/X-Temporal)

> Read the paper [here](https://arxiv.org/pdf/2003.05837v2.pdf)


7. > Title: Temporal Interlacing Network

> Abstract: For a long time, the vision community tries to learn the spatio-temporal representation by combining convolutional neural network together with various temporal models, such as the families of Markov chain, optical flow, RNN and temporal convolution. However, these pipelines consume enormous computing resources due to the alternately learning process for spatial and temporal information. One natural question is whether we can embed the temporal information into the spatial one so the information in the two domains can be jointly learned once-only. In this work, we answer this question by presenting a simple yet powerful operator -- temporal interlacing network (TIN). Instead of learning the temporal features, TIN fuses the two kinds of information by interlacing spatial representations from the past to the future, and vice versa. A differentiable interlacing target can be learned to control the interlacing process. In this way, a heavy temporal model is replaced by a simple interlacing operator. We theoretically prove that with a learnable interlacing target, TIN performs equivalently to the regularized temporal convolution network (r-TCN), but gains 4% more accuracy with 6x less latency on 6 challenging benchmarks.

> Task: Optical flow estimation | Video Understanding

> Implementation: [code1](https://github.com/Sense-X/X-Temporal) | [code2](https://github.com/deepcs233/TIN)

> Read the paper [here](https://arxiv.org/pdf/2001.06499v1.pdf)


8. > Title: XTREME: A Massively Multilingual Multi-task Benchmark for Evaluating Cross-lingual Generalization

> Abstract: Much recent progress in applications of machine learning models to NLP has been driven by benchmarks that evaluate models across a wide variety of tasks. However, these broad-coverage benchmarks have been mostly limited to English, and despite an increasing interest in multilingual models, a benchmark that enables the comprehensive evaluation of such methods on a diverse range of languages and tasks is still missing. To this end, we introduce the Cross-lingual TRansfer Evaluation of Multilingual Encoders XTREME benchmark, a multi-task benchmark for evaluating the cross-lingual generalization capabilities of multilingual representations across 40 languages and 9 tasks. We demonstrate that while models tested on English reach human performance on many tasks, there is still a sizable gap in the performance of cross-lingually transferred models, particularly on syntactic and sentence retrieval tasks. There is also a wide spread of results across languages. We release the benchmark to encourage research on cross-lingual learning methods that transfer linguistic knowledge across a diverse and representative set of languages and tasks.

> Task: Cross-lingual Transfer

> Implementation: [code](https://github.com/google-research/xtreme)

> Read the paper [here](https://arxiv.org/pdf/2003.11080v3.pdf)




**Disclaimer**: All papers and their related information is scraped from [Paperswithcode](https://paperswithcode.com/), a super awesome site!


So, tell me. Which of these catch your eye? Which would you like for me to discuss and implement next?
Let me know in the comment section!

Right now, my money is on 3D Photography. It sounds really interesting, doesn't it? Moreso, it involves GANs!