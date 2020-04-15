---
toc: true
comments: true
author: Wale
image: images/2020-04-14-openai-microscope/resnetV2_50_deep_dream.png
categories: [AI News]
permalink: /ai-news/:year/:month/:day/:title
---

## OpenAI Releases Microscope

![clock-viual-feature](/images/2020-04-14-openai-microscope/resnetV2_50_clock_visual_feature_visualizations.png)

Have you ever wondered how you could interprete how the neurons in a deep learning network comes about its classifications? Are you a researcher focused on shining the light on the black box of deep learning neurons? Are you an avid deep learning enthusiast like myself who would like to understand what makes your model draw a conclusion that the picture you passed to it was actualy a cup? Or do you just want to make fancy deep-dream styled artwork?

Well, OpenAI has just released the first version of an awesome toolkit that makes you do just that and more! The tool comes in a bid to understand (and study) the behavior of the thousands of neurons that make up deep learning models.

According to their [blogpost](https://openai.com/blog/microscope/), 

> Microscope makes it easier to analyze the features that form inside these neural networks, and we hope it will help the research community as we move towards understanding these complicated systems.

## How do you use the Microscope?
Quoting the "About" section here,

> The OpenAI Microscope is based on two concepts, a location in a model and a technique. Metaphorically, the location is where you point the microscope, the technique is what lens you affix to it.
 
> Our models are composed of a graph of “nodes” (the neural network layers), which are connected to each other through “edges.” Each op contains hundreds of “units”, which are roughly analogous to neurons. Most of the techniques we use are useful only at a specific resolution. For instance, feature visualization can only be pointed at a “unit”, not its parent “node”. 

The "lenses" refer to the Vis/channel and Vis/neuron settings applied to the layers in the settings section.

Here is one such visualization, using the resnet V2 50 architecture... err, "model organism". Here, I selected neurons of the clock visual logits of the architecture:

![resnetV2_50_clock_visual_logits](/images/2020-04-14-openai-microscope/resnetV2_50_clock_visual_logits.png)

The shapes displayed by each neuron has some similarities with the dataset being explored. The visualizations included in the Microscope include feature visualizations, DeepDream, dataset examples (images that cause neurons to fire strongly), and synthetic tuning curves (neuroscience-inspired plots of how units respond to synthetic image families). Each technique is explained when selected. More features will be added over time of course.

In this initial release, they made a collection of visualizations of every every significant layer and neuron of eight vision model architectures, which they term "model organisms".

Microscope offers a way for research to collaborate in a way that was previously notoriously difficult. With this tool, collaborators can make reference to a particular neurons, investigate neural intreractions in detail and share findings easily, with really eye-catching visuals. 

![openai-microscope](/images/2020-04-14-openai-microscope/openai-microscope.png)

The underlying models employed in Microscope (did I mention that there are 8 of them?) are already open source on [lucid](https://github.com/tensorflow/lucid), but Microscope makes all them (the models) and the neurons linkable. Since researchers can make references to particular neurons, researchers all over the world can immediately scrutinize another researcher's claims, and make personal explorartions as well. 

There are a few drawbacks to the Microscope though, although I believe these are only transient inconveniences.
1. They have only implemented 8 models. While these are likely among the more popular models, the diversity is a bit lacking. Again, this is only temporary and is due to the sheer complexity of setting these up in distributed systems. I expect that there will be a huge spike in the amount of model organisms available in coming months as the community soaks this in.
1. Can't use your custom model... yet. This was a big blow to me. When I read the introduction to the launch, I had already started anticipating configuring the Microscope to visualize how GANs come about their outputs. It seems that's a pipe-dream for now. The community is stuck using relatively older models till the tool is upgraded. The reason for this is that the tooling for developing these distributed jobs isn't available to everyone just yet.


Asides from these draw backs, it does look like a particularly promising and powerful tool. And it produces some really slick visuals! This tool is a major improvement in the field of model interpretability. Conceptualizing features and neuron interactions is fundamental to evolve our understanding of increasingly complex deep learning models.

Y'all should check it out! let me know what you think about this tool in the comments! 
Don't forget to tag me if you find really cool visuals!

Until next time, stay safe!