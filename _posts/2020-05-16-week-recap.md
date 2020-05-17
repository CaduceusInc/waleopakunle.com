---
toc: true
comments: true
author: Wale
image: https://media.giphy.com/media/DcSE3dQGqAzE4/giphy.gif
categories: [Weekly Recap]
permalink: /news/:year/:month/:day/:title
---

# Previously in the AI field...

Hey folks! Here are some of the things I've come across this past week in the AI field. Hope this can be informative/interesting in some way to the geeks who read to the end. *wink*

## New Open Source Tools

- The coolest I came across this week, by far, was [deon](https://deon.drivendata.org/); a cli tool for adding an ethics checklist to your data science project. It's cool because it shows that the community is really taking the issue of ethics and bias in machine learning algorithms into cognizance.

- Detectron2: A PyTorch based modular object detection library. They made it available as a library so it can just be imported into your project. This is a really cool way to make an opensource contribution!
Detectron2 has new features such as panoptic segmentation, densepose, Cascade R-CNN, rotated bounding boxes, etc. You can read more about it on their [blog](https://ai.facebook.com/blog/-detectron2-a-pytorch-based-modular-object-detection-library-/) or check out the [code base](https://github.com/facebookresearch/detectron2).

- Codespaces: GitHub just added a new feature folks! You can now write code on Github just like you would on a VS Code editor! With this cool feature, you can code, build, test, debug, and deploy with a complete development environment in your browser. There's also a plugin for codespaces in VS Code. Seriously, you should check it out and request for early access. You see, it's still in beta stage. You can do so [here](https://github.com/features/codespaces/).

- Qualcom has opensourced their AI Model Efficiency Toolkit! This is in their bid to provide a simple library plugin for AI developers to utilize for state-of-the-art model efficiency performance and to make artificial intelligence ubiquitous across devices, machines, vehicles, and things. Check out their [blog post](https://www.qualcomm.com/news/onq/2020/05/04/open-sourcing-ai-model-efficiency-toolkit?cmpid=oofyus194234&linkId=87923665) and the [code base](https://github.com/quic/aimet) for the installation guide, user guide and API documentation.

- Japanese Company, Preferred Networks, releases their [First PyTorch Library](https://github.com/pfnet/pytorch-pfn-extras). This library will help in Distributed snapshots (reducing the costs of implementing distributed deep learning with automated backup, loading, and generation management of snapshots). Other features include automatic inference of parameter sizes (easier network definitions by automatically inferring the sizes of linear or convolution layer parameters via input sizes) and implementations of convenient extensions and reporters. Let's hope they successfully merge  these features into the PyTorch base build.

- Check out the [ML-Agents Unity Package v1.0](https://github.com/Unity-Technologies/ml-agents)

{% include youtube.html content="https://youtu.be/yIChlf9hcRE" %}

---

## Cool Projects

- Here's an OpenCV digit recognition model by [jagadishb1409](https://github.com/jagadishb1409/Digit-recognition). It's really neat and would be better still if it were modularized. He uses opencv to create a window on the screen and wait to recognize your input from the screen which are captured by pre-designated keys assigned to mouse actions. An image is created when you draw a "4" on the screen for example and sent to a pre-trained MNIST digit recognizer tensorflow model generated from one of the scripts. A great way to extend this would be to modularize it and maybe make it into a flask application as is done  in this [MNIST-flask_app]((https://github.com/veb-101/mnist-flask_app)) by [Vaihab](https://github.com/veb-101).

- [MedSeg.ai](https://www.medseg.ai/) uses a segmentation model to analyze CT scans. It's free to use, but not openSource, unfortunately.

- [A Multi-Language Sentiment Analysis tool using flask API](https://github.com/amrha/MLSA) using using a catboost model trained on the sentement140 kaggel dataset.

- [Basketball analysis API](https://github.com/chonyy/AI-basketball-analysis) built with flask, tensorflow and opencv. Try it out for yourselves [here](https://ai-basketball-analysis.herokuapp.com/)

- [Online Tool Animates Your Actions in Real Time](https://github.com/yemount/pose-animator/). Pose Animator takes a 2D vector illustration and animates its containing curves in real-time based on the recognition result from PoseNet and FaceMesh. Pose Animator basically animates users’ poses and movements from either a camera feed or a static image, and can run on browsers in real time using TensorFlow.js.

---

## New Events

- Competition:
  - [The Facebook/Data-Driven "Hateful Memes" Competition](https://www.drivendata.org/competitions/64/hateful-memes/). The goal is to create an algorithm that identifies multimodal hate speech in internet memes.

- Conferences:
  - [Virtual Microsoft build](https://mybuild.microsoft.com/).

---

## New Datasets

- [World largest  real-world masked face dataset](https://www.catalyzex.com/paper/arxiv:2003.09093).
The dataset includes 5,000 pictures of 525 people wearing masks and 90,000 images of the same 525 subjects without masks. This can be used in grocery stores and other public places to check if people are wearing masks or not. Conventional facial recognition technology is ineffective in many cases, such as community access control, face access control, facial attendance, facial security checks at train stations, etc. I'd be mighty interested in building something in this direction with (or without) someone.

---

## Resources

- Springer has made 65 machine-learning related books available for free... for now. Check out the full list [here](https://towardsdatascience.com/springer-has-released-65-machine-learning-and-data-books-for-free-961f8181f189)

- Papers I read this week:

  - [Learning concepts with enery functions](https://openai.com/blog/learning-concepts-with-energy-functions/) :

    > Energy-functions are typically a mere afterthought in current machine learning. A core function of the Energy - its smoothness - is usually not exploited at inference time. This paper takes a stab at it. Inferring concepts, world states, and attention masks via gradient descent on a learned energy function leads to an interesting framework with many possibilities.

  - paper: [arxiv](https://arxiv.org/abs/1811.02486)
  - blog:  [openai](https://openai.com/blog/learning-concepts-with-energy-functions/)
  - video: [Watch explanatory video on youtube](https://youtu.be/Cs_j-oNwGgg), or right here:

{% include youtube.html content="https://youtu.be/Cs_j-oNwGgg" %}

- Cooperation Instead of Competition: Harvard & Microsoft Research Optimizes AI-Human Teamwork:

  - The paper identifies a possible area for future research on human-machine cooperation as an optimization of team performance when interactions extend beyond the current level of querying humans for answers. This could include settings with more complex, interleaved interactions and those with different levels of human initiative and machine autonomy.

  - paper: [arxiv](https://arxiv.org/pdf/2005.00582.pdf)
  - blog: [Quick read](https://medium.com/syncedreview/cooperation-instead-of-competition-harvard-microsoft-research-optimizes-ai-human-teamwork-4f7f89bbbf6f)

- Books: This past week, I've been joggling reading two books:
  - Learning OpenCV 4 Computer Vision with Python 3 Joseph Howse and Joe Minichino. You can subscribe to read it on [Packt](https://www.packtpub.com/data/learning-opencv-4-computer-vision-with-python-3-third-edition), or simply go through the code for the book [here](https://github.com/PacktPublishing/Learning-OpenCV-4-Computer-Vision-with-Python-Third-Edition) if you have a good background in Python. I settled on this book after a lot of consideration and exploring other books on OpenCV. What makes it stand out is the detailed explanations and the fact that it is in Python, rather than C++. No regrets so far.

 {% include alert.html text="I had tremendous dificulty installing Python opencv-contrib on my windows computer using anaconda. If you experience this issue,  you may have to settle for OpenCV3. All examples in the book run as per normal so far. You can use the code below to install it in a conda environment." %}

```shell
# You need to install the contrib version of opencv, otherwise you wont have access to some
# features such as video editing/manipulation.
# This was what worked for me after several hours of hair pulling.
# you can use any python version you want actually. I prefer to be one step behind the latest release.
# Why, you ask? BUGSSSS!! Bugs, thats why!
C:\Users\xyz> conda create -n flask-env flask python=3.7
# activate the environment
C:\Users\xyz> conda activate flask-env
# install opencv-contrib
C:\Users\xyz> conda install -c michael_wild opencv-contrib
```

- Flask Web Development - Miguel Grinberg.

Heard of [Flask Mega Tutorial](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)?

No?

Heard of [Flask-Migrate](https://flask-migrate.readthedocs.io/en/latest/)?

No?

Seriously?

Well, you probably don't use Flask very often if that's the case. Let's change that. I would highly recommend this book if you're looking to get started, or solidify your foundation, like I am. If you can't afford to buy it, you can simply follow on his site [here](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world). It's almost the same as the book. Alternatively, check out the [code base](https://github.com/miguelgrinberg/flasky). You can get the code for each chapter of the book by 'git check'-ing the branch tags for each chapter. It's all very efficiently managed by Miguel.

Trust me, this guy has the most educative resources by far, when it comes to flask (to the best of my very limited knowledge, of course). But seriously, his book is really awesome. Highly, highly recommend.

Thanks Miguel!

- Tutorials
  - I also went through this cool tutorial on converting old footage to 4K + 60fps + colorized with AI. You may have guessed it. They threw Jason's (@citnaj on twitter) DeOldify algorithm into the mix. Really cool.

  {% include youtube.html content="https://youtu.be/h-zNjxY-m90" %}
  
---

## AI developments

- Facebook AI built and deployed a [real-time neural text-to-speech system that can process 1 sec of audio in 500 ms, using only CPUs.](https://ai.facebook.com/blog/a-highly-efficient-real-time-text-to-speech-system-deployed-on-cpus/)

- [Watson's Creator Wants to Teach AI a New Trick: Common Sense](https://www.wired.com/story/watsons-creator-teach-ai-new-trick-common-sense/)

- Read about a budding use case of artificial intelligence that could very well be a new age Alzheimer's diagnosis tool [here](https://www.wired.com/story/watsons-creator-teach-ai-new-trick-common-sense/).

- Find out how Intel and University of Pennsylvania are using federated learning to detect brain tumors [here](https://newsroom.intel.com/news/intel-works-university-pennsylvania-using-privacy-preserving-ai-identify-brain-tumors/#gs.5rq2yc), while protecting privacy of course.

- [This AI can simulate an economy millions of times to create fairer tax policy](https://www.technologyreview.com/2020/05/05/1001142/ai-reinforcement-learning-simulate-economy-fairer-tax-policy-income-inequality-recession-pandemic/).

---

That's it folks. That's a recap of all AI related content I came across this week. What did I miss? What else is new in the AI field? Let me know in the comments!

Happy exploration.
