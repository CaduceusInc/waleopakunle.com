---
toc: true
comments: true
author: Wale
image: /images/2020-04-21-latest-in-ai/ours_1.gif
categories: [Trending Research papers]
permalink: /papers/:year/:month/:day/:title
---

# Latest in AI Research - Week 17

![R for Research](https://media.giphy.com/media/26FPC5oAdfeFPkQQE/giphy.gif)

Hey there! It's another Tuesday, and here is a collation of what's new in AI research.

* > Title:  Learning to see in the dark

> Abstract:Imaging in low light is challenging due to low photon count and low SNR. Short-exposure images suffer from noise, while long exposure can induce blur and is often impractical. A variety of denoising, deblurring, and enhancement techniques have been proposed, but their effectiveness is limited in extreme conditions, such as video-rate imaging at night. To support the development of learning-based pipelines for low-light image processing, we introduce a dataset of raw short-exposure low-light images, with corresponding long-exposure reference images. Using the presented dataset, we develop a pipeline for processing low-light images, based on end-to-end training of a fully-convolutional network. The network operates directly on raw sensor data and replaces much of the traditional image processing pipeline, which tends to perform poorly on such data. We report promising results on the new dataset, analyze factors that affect performance, and highlight opportunities for future work. The results are shown in the supplementary video at https://youtu.be/qWKUFK7MWvg

> Task:| Deblurring | Denoising

> Implementation:| [code1](https://github.com/cchen156/Learning-to-See-in-the-Dark) - Python 2.7, Tensorflow | [code2](https://github.com/cydonia999/Learning_to_See_in_the_Dark_PyTorch) - Pytorch

> Read the paper [here](https://arxiv.org/pdf/1805.01934v1.pdf)

---

* > Title:  DeepFactors: Real-Time Probabilistic Dense Monocular SLAM

> Abstract: The ability to estimate rich geometry and camera motion from monocular imagery is fundamental to future interactive robotics and augmented reality applications. Different approaches have been proposed that vary in scene geometry representation (sparse landmarks, dense maps), the consistency metric used for optimising the multi-view problem, and the use of learned priors. We present a SLAM system that unifies these methods in a probabilistic framework while still maintaining real-time performance. This is achieved through the use of a learned compact depth map representation and reformulating three different types of errors: photometric, reprojection and geometric, which we make use of within standard factor graph software. We evaluate our system on trajectory estimation and depth reconstruction on real-world sequences and present various examples of estimated dense geometry.

> Task:| 

> Implementation:| [code](https://github.com/jczarnowski/DeepFactors) - C++

> Read the paper [here](https://github.com/jczarnowski/DeepFactors)

---

* > Title:  Weight Poisoning Attacks on Pre-trained Models

> Abstract:Recently, NLP has seen a surge in the usage of large pre-trained models. Users download weights of models pre-trained on large datasets, then fine-tune the weights on a task of their choice. This raises the question of whether downloading untrusted pre-trained weights can pose a security threat. In this paper, we show that it is possible to construct weight poisoning'' attacks where pre-trained weights are injected with vulnerabilities that expose backdoors'' after fine-tuning, enabling the attacker to manipulate the model prediction simply by injecting an arbitrary keyword. We show that by applying a regularization method, which we call RIPPLe, and an initialization procedure, which we call Embedding Surgery, such attacks are possible even with limited knowledge of the dataset and fine-tuning procedure. Our experiments on sentiment classification, toxicity detection, and spam detection show that this attack is widely applicable and poses a serious threat. Finally, we outline practical defenses against such attacks.

> Task:| Sentiment Analysis

> Implementation:| [code](https://github.com/neulab/RIPPLe)

> Read the paper [here](https://arxiv.org/pdf/2004.06660v1.pdf)

---

* > Title:  Revisiting the Arcade Learning Environment: Evaluation Protocols and Open Problems for General Agents

> Abstract: The Arcade Learning Environment (ALE) is an evaluation platform that poses the challenge of building AI agents with general competency across dozens of Atari 2600 games. It supports a variety of different problem settings and it has been receiving increasing attention from the scientific community, leading to some high-profile success stories such as the much publicized Deep Q-Networks (DQN). In this article we take a big picture look at how the ALE is being used by the research community. We show how diverse the evaluation methodologies in the ALE have become with time, and highlight some key concerns when evaluating agents in the ALE. We use this discussion to present some methodological best practices and provide new benchmark results using these best practices. To further the progress in the field, we introduce a new version of the ALE that supports multiple game modes and provides a form of stochasticity we call sticky actions. We conclude this big picture look by revisiting challenges posed when the ALE was introduced, summarizing the state-of-the-art in various problems and highlighting problems that remain open.

> Task:| Atari Games

> Implementation:| [code](https://github.com/google-research/batch_rl)

> Read the paper [here](https://arxiv.org/pdf/1709.06009v2.pdf)

---

* > Title:  Footprints and Free Space from a Single Color Image

> Abstract: Understanding the shape of a scene from a single color image is a formidable computer vision task. However, most methods aim to predict the geometry of surfaces that are visible to the camera, which is of limited use when planning paths for robots or augmented reality agents. Such agents can only move when grounded on a traversable surface, which we define as the set of classes which humans can also walk over, such as grass, footpaths and pavement. Models which predict beyond the line of sight often parameterize the scene with voxels or meshes, which can be expensive to use in machine learning frameworks. We introduce a model to predict the geometry of both visible and occluded traversable surfaces, given a single RGB image as input. We learn from stereo video sequences, using camera poses, per-frame depth and semantic segmentation to form training data, which is used to supervise an image-to-image network. We train models from the KITTI driving dataset, the indoor Matterport dataset, and from our own casually captured stereo footage. We find that a surprisingly low bar for spatial coverage of training scenes is required. We validate our algorithm against a range of strong baselines, and include an assessment of our predictions for a path-planning task.

> Task:| Semantic Segmentation

> Implementation:| [code](https://github.com/nianticlabs/footprints)

> Read the paper [here]()

---

* > Title:  An Optimistic Perspective on Offline Reinforcement Learning 

> Abstract: Off-policy reinforcement learning (RL) using a fixed offline dataset of logged interactions is an important consideration in real world applications. This paper studies offline RL using the DQN replay dataset comprising the entire replay experience of a DQN agent on 60 Atari 2600 games. We demonstrate that recent off-policy deep RL algorithms, even when trained solely on this replay dataset, outperform the fully trained DQN agent. To enhance generalization in the offline setting, we present Random Ensemble Mixture (REM), a robust Q-learning algorithm that enforces optimal Bellman consistency on random convex combinations of multiple Q-value estimates. Offline REM trained on the DQN replay dataset surpasses strong RL baselines. The results here present an optimistic view that robust RL algorithms trained on sufficiently large and diverse offline datasets can lead to high quality policies. The DQN replay dataset can serve as an offline RL benchmark and is open-sourced.

> Task:| Atari games | Q-Learning

> Implementation:| [code](https://github.com/google-research/batch_rl)

> Read the paper [here](https://arxiv.org/pdf/1907.04543v3.pdf)

---

* > Title:  AI Feynman: a Physics-Inspired Method for Symbolic Regression 

> Abstract: A core challenge for both physics and artificial intellicence (AI) is symbolic regression: finding a symbolic expression that matches data from an unknown function. Although this problem is likely to be NP-hard in principle, functions of practical interest often exhibit symmetries, separability, compositionality and other simplifying properties. In this spirit, we develop a recursive multidimensional symbolic regression algorithm that combines neural network fitting with a suite of physics-inspired techniques. We apply it to 100 equations from the Feynman Lectures on Physics, and it discovers all of them, while previous publicly available software cracks only 71; for a more difficult test set, we improve the state of the art success rate from 15% to 90%.

> Task:|

> Implementation:| [code](https://github.com/SJ001/AI-Feynman)

> Read the paper [here](https://arxiv.org/pdf/1905.11481v2.pdf)

---

* > Title:  Few-Shot NLG with Pre-Trained Language Model

> Abstract: Neural-based end-to-end approaches to natural language generation (NLG) from structured data or knowledge are data-hungry, making their adoption for real-world applications difficult with limited data. In this work, we propose the new task of \textit{few-shot natural language generation}. Motivated by how humans tend to summarize tabular data, we propose a simple yet effective approach and show that it not only demonstrates strong performance but also provides good generalization across domains. The design of the model architecture is based on two aspects: content selection from input data and language modeling to compose coherent sentences, which can be acquired from prior knowledge. With just 200 training examples, across multiple domains, we show that our approach achieves very reasonable performances and outperforms the strongest baseline by an average of over 8.0 BLEU points improvement.

> Task:| Few Shot learning | Language Modelling | Text Generation

> Implementation:| [code](https://github.com/czyssrs/Few-Shot-NLG)

> Read the paper [here](https://arxiv.org/pdf/1904.09521v3.pdf)

---

**Disclaimer**: All papers and their related information are scraped from [Paperswithcode](https://paperswithcode.com/), a super awesome site!

---

Which paper interests you? Which would you like to see imlemented in an easily accessible colab notebook? Let me know in the comments below!

Until next time, stay safe!
