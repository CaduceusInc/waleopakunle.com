---
toc: true
comments: true
author: Wale
image: https://media.giphy.com/media/lrQ2T4iMddQhG/giphy.gif
categories: [Weekly Recap]
permalink: /news/:year/:month/:day/:title
---

# Previously in the AI field...

Hey folks, I am back with a recap of last week in AI! This week, I decided to add on a new section, based on feedback from a fellow data scientist. Be sure to check out the "Job" section for a highlight of some opportunities that are open for machine learning practitioners.

Working on feedback from last week, all links now open in new tabs. I will be implementing that for all links going forward. Thanks for the feedback, and I hope you enjoy a better reading experience.

---
T.O.C

1. [New Open Source Tools](#new-open-source-tools)

1. [Cool Projects](#cool-projects)

1. [New Events](#new-events)

1. [New Datasets](#new-datasets)

1. [Resources](#resources)

1. [AI Developments](#ai-developments)

1. [Jobs](#jobs)

---

## New Open Source Tools

{% include giphy.html content="https://media.giphy.com/media/26BRzozg4TCBXv6QU/giphy.gif" %}

---
---

- Tensorflow announced the release of BigTransfer (BiT); a compilation of pre-trained models for easy and effective transfer learning for vision with TF-Hub! For a detailed walkthrough on how to utilize these models and customize it to your computer vision needs, checkout the [official tensorflow blog post](https://blog.tensorflow.org/2020/05/bigtransfer-bit-state-of-art-transfer-learning-computer-vision.html){:target="_blank"} or try it out for yourselves in [colab](https://colab.research.google.com/github/google-research/big_transfer/blob/master/colabs/big_transfer_tf2.ipynb){:target="_blank"}. If you're so inclined, checkout their paper on [Graphical Visual Representation Learning](https://arxiv.org/pdf/1912.11370){:target="_blank"}.

- [Flowtron](https://github.com/NVIDIA/flowtron){:target="_blank"}: an autoregressive flow-based generative network for text-to-speech synthesis with control over speech variation and style transfer.

- [Transformers](https://github.com/huggingface/transformers/blob/master/README.md){:target="_blank"} (formerly known as pytorch-transformers and pytorch-pretrained-bert) provides state-of-the-art general-purpose architectures (BERT, GPT-2, RoBERTa, XLM, DistilBert, XLNet, T5, CTRL...) for Natural Language Understanding (NLU) and Natural Language Generation (NLG) with over thousands of pretrained models in 100+ languages and deep interoperability between PyTorch & TensorFlow 2.0.
  - Features:
    - High performance on NLU and NLG task
    - State-of-the-art NLP for everyone

- [OpenTPOD](https://github.com/cmusatyalab/OpenTPOD){:target="_blank"}
OpenTPOD is an all-in-one open-source tool for nonexperts to create custom deep neural network object detectors. It is designed to lower the barrier of entry and facilitates the end-to-end authoring workflow of custom object detection using state-of-art deep learning methods. It provides several features via an easy-to-use web interface, including; training data management, data annotation through seamless integration, one-click training / fine-tuning of object detection deep neural networks, one-click model export for interface with Tensorflow Serving, and extensible architecture for easy addition of new deep neural network architectures...

{% include youtube.html content="https://youtu.be/UHnNLrD6jTo" %}

---

## Cool Projects

{% include giphy.html content="https://media.giphy.com/media/RyLtUMBdogHvO/giphy.gif" %}

---
---

- Open Source:

  - [Olivia](https://olivia-ai.org/){:target="_blank"}: an open-source chatbot built in Golang using Machine Learning technologies. Its goal is to provide a free and open-source alternative to big services like DialogFlow. You can chat with her by speaking (STT) or writing, she replies with a text message but you can enable her voice (TTS). It currently supports 7 languages and you can try it out [here](https://olivia-ai.org/){:target="_blank"}
  Olivia is organized in modules to facilitate the addition of new capabilities. These modules can be written in Go to execute multiple tasks. The project is entirely open-source from the website to the backend. This gives you the ability to build your own chatbot and contribute to Olivia. Don't you just love open source?

  - [Groknet](https://ai.facebook.com/research/publications/groknet-unified-computer-vision-model-trunk-and-embeddings-for-commerce){:target="_blank"}: Earlier this week, Facebook announced their deployment of a universal [computer vision system designed for shopping](https://ai.facebook.com/blog/powered-by-ai-advancing-product-understanding-and-building-new-shopping-experiences/){:target="_blank"}. It can identify fine-grained product attributes across billions of photos — in different categories, such as fashion, auto, and home decor.

  - [Using reinforcement learning algorithms to play the game 2048](https://github.com/FelipeMarcelino/2048-Gym){:target="_blank"}
  This repository is a project about using DQN(Q-Learning) to play the Game 2048 and accelarate and accelerate the environment using Numba). The algorithm used is from Stable Baselines, and the environment is a custom Open AI env.

---

## New Events

{% include giphy.html content="https://media.giphy.com/media/40KXzKllSl6ve/giphy.gif" %}

---
---

- [ETL and Advanced Machine Learning - Open Source, No Code Required](https://www.knime.com/knime-analytics-platform-for-data-scientists-webinar-kd-americas?utm_source=kdnuggets&utm_medium=banner&utm_campaign=knime-intro-webinar){:target="_blank"}

- [The Stanford Institute for Human-Centered Artificial Intelligence's COVID + AI: The Road Ahead](https://hai.stanford.edu/events/covid-ai-road-ahead){:target="_blank"}:
Two months into the COVID-19 pandemic, we see curves flattening and cities lifting shelter restrictions. By no means is this pandemic over; and yet, policymakers, researchers, medical practitioners, and industry are starting to grapple with how we operate in a post-COVID world. What is the path forward, economically, medically, and culturally?
Scholars from across disciplines will discuss their research using AI, data science and/or informatics to help us understand how we emerge from this crisis.

***Live Virtual Event Details***

Date: June 01, 2020 - 09:15am–12:30pm

Register [here](https://www.eventbrite.com/e/covid-ai-the-road-ahead-tickets-105468430916){:target="_blank"}.

- [CVPR 2020](http://cvpr2020.thecvf.com/){:target="_blank"}

CVPR is the premier annual computer vision event comprising the main conference and several co-located workshops and short courses. With its high quality and low cost, it provides an exceptional value for students, academics and industry researchers.
CVPR 2020 will take place virtually from June 14 to June 19th.

- [Apple WWDC 2020](https://developer.apple.com/wwdc20/){:target="_blank"}

On June 22, WWDC20 takes off. Get ready for the first global, all-online WWDC by downloading the Apple Developer app to stay notified on all the latest news, with updates for events and sessions. And there’s a lot more to come — starting with the first-ever Swift Student Challenge.

---

## New Datasets

{% include giphy.html content="https://media.giphy.com/media/7rSqa74vJW0Te/giphy.gif" %}

---
---

- [Flickr 30k Dataset](https://www.kaggle.com/hsankesara/flickr-image-dataset){:target="_blank"}: The Flickr 30k dataset has over 30,000 images, and each image is labeled with different captions. This dataset is used to build an image caption generator. And this dataset is an upgraded version of Flickr 8k used to build more accurate models.

**Possible project idea**:  You can train a deep learning model that is capable of analysing and extracting features from the image and generate as English sentence that describes the image. Next time when your friend send you an image and goes, "Caption this", you can ask your model what it thinks and get back to your friend with the machine caption.

- [Chatbot Intents Dataset](https://github.com/katanaml/katana-assistant/blob/master/mlbackend/intents.json){:target="_blank"}
The dataset for a chatbot is a JSON file that has disparate tags like goodbye, greetings, pharmacy_search, hospital_search, etc. Every tag has a list of patterns that a user can ask, and the chatbot will respond according to that pattern. The dataset is perfect for understanding how chatbot data works.

**Possible Project Idea**: You can build a chatbot or understand the working of a chatbot by modifying and expanding the data with your observations. To build a Chatbot of your own, you need to have a good knowledge of Natural language processing concepts.
[This article](https://dzone.com/articles/python-chatbot-project-build-your-first-python-pro){:target="_blank"} from DZone could help you get started with that.

- [Mall Customers Dataset](https://www.kaggle.com/shwetabh123/mall-customers){:target="_blank"}
The Mall customers dataset holds the details about people visiting the mall. The dataset has an age, customer id, gender, annual income, and spending score. It gains insights from the data and divides the customers into different groups based on their behaviors.

**Possible Project Idea**: Segment the customers based on their gender, age, interest. It is useful in customized marketing. Customer segmentation is an important practice of dividing customers based on individual groups that are similar.

[This article](https://data-flair.training/blogs/r-data-science-project-customer-segmentation/){:target="_blank"} could help you get started with customer segmentation with R or [this one](https://towardsdatascience.com/customer-segmentation-analysis-with-python-6afa16a38d9e){:target="_blank"}, if you speak the language of the gods.

- [Youtube 8M Dataset](https://research.google.com/youtube8m/){:target="_blank"}
The youtube 8M dataset is a large scale labeled video dataset that has 6.1 million Youtube video ids, 350,000 hours of video, 2.6 billion audio/visual features, 3862 classes, and 3 avg labels per video. It is used for video classification purposes.

**Project Idea**: Video classification can be done by using the dataset, and the model can describe what video is about. A video takes a series of inputs to classify in which category the video belongs. This would be a rather involved project, but if you are interested, [this paper](https://arxiv.org/pdf/1609.08675v1.pdf){:target="_blank"} could help get you started, along with the following implementations:

  1. [google/youtube-8m](https://github.com/google/youtube-8m){:target="_blank"}

  1. [AKASH2907/Content-based-Video-Recommendation](https://github.com/AKASH2907/Content-based-Video-Recommendation){:target="_blank"}

---

## Resources

{% include giphy.html content="https://media.giphy.com/media/X1LTQuH3i8fza/giphy.gif" %}

---
---

- Papers I read
  - [Grounding Language in Play: A scalable approach for controlling robots with natural language](https://language-play.github.io/){:target="_blank"}
  - [Instance-aware Image Colorization](https://arxiv.org/pdf/2005.10825v1.pdf){:target="_blank"}

- Articles:

  - [AI Ethics in China](https://www.nesta.org.uk/report/chinas-approach-to-ai-ethics/){:target="_blank"}
  > "... It is therefore surprising that the western misconception that China lacks debate around AI ethics seems to prevail, when in fact: i) existing Chinese AI principles largely align with global ones; ii) Chinese discussions enjoy unprecedented government support; and iii) the country is already investigating the technical and social implementation of these principles by exploring how they interact with its distinct cultural heritage.
  > In this essay I explore AI ethics in China through the lens of some of the key topics discussed in depth in the other essays on this collection – education, healthcare, smart cities and social credit systems – to consider which, if any, ethical issues are unique to China and which should be seen as global concerns." - Danit Gal, *Technology advisor to the UN Secretary General’s High-level Panel on Digital Cooperation and associate fellow at the Leverhulme Centre for the Future of Intelligence at the University*

  - [Microsoft responsible machine learning capabilities build trust in AI systems, developers say](https://blogs.microsoft.com/ai/azure-responsible-machine-learning/?utm_source=msr-social). Read this article by John Roach to find out what the industry, particularly Micrsosft, is doing regarding ethical AI and model interpretability. Going further in the rabbit hole, I discovered they now have modules that cater for interpretability which I didn't notice when I was using the service last year. You can check that out in the official [Azure Machine Learning docs](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-machine-learning-interpretability-aml){:target="_blank"}.
  For an example of how to use this, checkout [this repo](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/explain-model?ocid=AID2463683&wt.mc_id=ai-c9-sejuare){:target="_blank"}.

  - [Three Risks in Building Machine Learning Systems](https://insights.sei.cmu.edu/sei_blog/2020/05/three-risks-in-building-machine-learning-systems.html){:target="_blank"} , Benjamin Cohen

  - Read how Waymo is using GANs in modules of their self-driving software, to simulate autonomous vehicle camera and sensor data in this article by [Kyle Wiggers on Venturebeat](https://venturebeat.com/2020/05/20/waymo-is-using-ai-to-simulate-autonomous-vehicle-camera-data/){:target="_blank"}.

  > " In the simulation, when a trajectory of a self-driving car and other agents (e.g. other cars, cyclists, and pedestrians) changes, the system generates realistic visual sensor data that helps us model the scene in the updated environment … "   - A Waymo spokesperson.

  - [Is AI democratization a real thing?](https://medium.com/sciforce/is-ai-democratization-a-real-thing-12957ca18534){:target="_blank"}

  - [This Will Change the Way You Look at GANs](https://towardsdatascience.com/this-will-change-the-way-you-look-at-gans-9992af250454){:target="_blank"}

  - [Entity linking: A primary NLP task for Information Extraction](https://medium.com/@msundarv/entity-linking-a-primary-nlp-task-for-information-extraction-22f9d4b90aa8){:target="_blank"}

  - [Top 10 Nice-To-Have Data Science Libraries](https://medium.com/analytics-vidhya/top-10-nice-to-have-data-science-libraries-d155196710ef){:target="_blank"}

  - [Building a Business From a Bedroom, $98,130 and 11-Months In](https://medium.com/the-post-grad-survival-guide/building-a-business-from-a-bedroom-98-130-and-11-months-in-7a55774b2a0){:target="_blank"}

- Free Books:
  - [The Elements of Statistical Learning](https://link.springer.com/content/pdf/10.1007%2F978-0-387-84858-7.pdf){:target="_blank"}, by Trevor Hastie, Robert Tibshirani, and Jerome Friedman
  - [Dive Into Deep Learning](https://d2l.ai/d2l-en.pdf){:target="_blank"}
  You can also download the entire book in [notebook format](https://d2l.ai/chapter_installation/index.html){:target="_blank"}, so you can run it locally or on [AWS Sagemaker](https://d2l.ai/chapter_appendix-tools-for-deep-learning/sagemaker.html){:target="_blank"}.

- Paid Books:

  - [High Performance Python, 2nd Edition by Micha Gorelick & Ian Ozsvald](http://shop.oreilly.com/product/0636920268505.do){:target="_blank"}.

- Notes:
  - [Notes from an Introductory course on probablistic graphical models](https://ermongroup.github.io/cs228-notes/){:target:"_blank"}. They are based on the Stanforf course, CS228.

  - [My colab notebook](https://colab.research.google.com/drive/1DuzClGB5T79yPk-VmETpOVeginpO8gbx?usp=sharing){:target:"_blank"} exploring the ["Adversarial-Colorization-Of-Icons-Based-On-Structure-And-Color-Conditions"](https://github.com/jxcodetw/Adversarial-Colorization-Of-Icons-Based-On-Structure-And-Color-Conditions){:target="_blank"} project. I merely provide comments on the code and an intuition of how to minimally customize the set up. This group of researchers present a system to help designers create icons that are widely used in banners, signboards, billboards, homepages, and mobile apps. Designers are tasked with drawing contours and then, the system colourizes contours in different styles. This goal is achieved by training a dual conditional generative adversarial network (GAN) on the collected icon dataset. If you are familiar with Python wx, you can get the user interface which was built with Python Wx [here](https://drive.google.com/file/d/1ckhFl6Pmx6ltnYd9-geeFQU1z5F3uW-L/view?usp=sharing){:target="_blank"}. You can either get the [preprocessed data](https://drive.google.com/file/d/1B8GjpBPpIxpAEy7cf8xpmA_ESy3CQXLh/view?usp=sharing){:target="_blank"}, or the [unprocessed data](https://drive.google.com/open?id=1qtfA_fOCVzU8bigJut1LYKOOlTI20f9d){:target="_blank"} if you would like to train the model yourself. I'm at the phase of understanding and customizing the UI. Perhaps I will be able to add a new feature. *fingers-crossed*

  - [My colab notebook](https://colab.research.google.com/drive/15YgjvL85GJpPfYOTXz9iURkLXqBvKn41?usp=sharing){:target="_blank"} on building a food classifier with Keras. The model is suffering from acute overfitting as you can see from the loss logs. This was initially meant to be a video tutorial series on how to deploy deep learning models in production, but I wont be completing the video shoot until I get the accuracy up a lot higher than it currently is. This week, I will be tuning hyperparameters and retraining the model. Problem is, it takes too friggin long! Just training on 4 classes took an hour per epoch. I'll have to look into options to reduce training time as well. Once that headache is done, I'll be sharing how you can put the model into a flask application, deploy its docker image and manage it with kubernetes.

- Cool Tutorials
  - [CMU Neural Nets for NLP 2020 (24 Video Playlist)](https://www.youtube.com/playlist?list=PL8PYTP1V4I8CJ7nMxMC8aXv8WqKYwj-aJ){:target="_blank"}

  - [AI Saturday Lagos - ML Track, Week 10 : Nonlinear Modeling, Cross Validation and Regularization](https://youtu.be/CyHMukDEllg){:target="_blank"} by the amazing Tejumade Afonja.

    {% include youtube.html content="https://youtu.be/CyHMukDEllg" %}

  - [AI Saturday Lagos - DL Track, Week 10 : Natural Language Processing & RNNs](https://youtu.be/V1GVx4mQ9gQ){:target="_blank"} by the awesome Oreva Ahia.

    {% include youtube.html content="https://youtu.be/V1GVx4mQ9gQ" %}

  - [Data Engineering 101 by Damilola Ojo, with Data Science Nigeria](https://youtu.be/UqPE_OejWsQ){:target="_blank"}

    {% include youtube.html content="https://youtu.be/UqPE_OejWsQ" %}

  - [Docker & Kubernetes Demo in 15 mins: Package & Deploy Your First App](https://youtu.be/-wr_lNd6y84){:target="_blank"}

    {% include youtube.html content="https://youtu.be/-wr_lNd6y84" %}

- Nuggets:
  - [Deploying a Go application with Docker images on Kubernetes](https://www.youtube.com/watch?v=-wr_lNd6y84&feature=youtu.be){:target="_blank"}.

  - [The Only Step-by-Step Guide You’ll Need to Build a Web Scraper With Python](https://medium.com/better-programming/the-only-step-by-step-guide-youll-need-to-build-a-web-scraper-with-python-e79066bd895a)

  - [A Visual Survey of Data Augmentation in NLP](https://amitness.com/2020/05/data-augmentation-for-nlp/){:target="_blank"}
  > "...I was curious if there were attempts at developing augmentation techniques for NLP and explored the existing literature. In this post, I will give an overview of the current approaches being used for text data augmentation based on my findings.." - Amit Chaudhary, *Machine Learning Engineer at Fusemachines*

  - [Everything you need to know about Auto-Deeplab: Google’s latest on Segmentation](https://towardsdatascience.com/everything-you-need-to-know-about-auto-deeplab-googles-latest-on-segmentation-181425d17cd5){:target="_blank"}

  - [Five Cool Python Libraries for Data Science](https://medium.com/towards-artificial-intelligence/five-cool-python-libraries-for-data-science-7f1fce402b90){:target="_blank"}

  - [Federated Learning for Medical AI](https://medium.com/deeptek/federated-learning-for-medical-ai-65d0daeafe8b){:target="_blank"}

  - [Python List Comprehension](https://towardsdatascience.com/all-about-python-list-comprehension-14dd979ec0d1){:target="_blank"}
  
---

## AI Developments

{% include giphy.html content="https://media.giphy.com/media/2f41Z7bhKGvbG/giphy.gif" %}

---
---

- Watch how OpenAI and Microsoft apply OpenAI's language model to achieve code generation.

{% include youtube.html content="https://youtu.be/y5-wzgIySb4" %}

- Air Force 'Skyborg' AI powered drones to take flight alongside warplanes by 2023, because apparently 'Skynet' was copyrighted.
  >The  U.S. Air Force is soliciting the aerospace industry to provide flyable “Skyborg” drones by 2023. The drones will be powered by artificial intelligence, capable of taking off, landing, and performing missions on their own.
  >Skyborg will not only free manned pilots from dangerous and dull missions but allow the Air Force to add legions of new, unpiloted, cheap planes...[Read more](https://www.popularmechanics.com/military/aviation/a32631612/skyborg-drones-2023/?source=nl&utm_source=nl_pop&utm_medium=email&date=052220&utm_campaign=nl20376989&src=nl&utm_source=reddit.com){:target="_blank"}.

- [AI vs. Cyberattacks](https://www.techradar.com/news/ai-vs-ai-the-next-battle-in-the-cyber-arms-race?utm_source=ONTRAPORT-email-broadcast&utm_medium=ONTRAPORT-email-broadcast&utm_term=&utm_content=Data+Science+Insider%3A+May+22nd%2C+2020&utm_campaign=23052020){:target="_blank"}
It's no news that hackers are now taking advantage of machine learning.
Cyberattacks have become part of the modern way of life, with companies investing billions of dollars to protect their data from hackers. As ways to secure systems have become more advanced and innovative, so too have the means of attack. Following the 2017 ‘worms’ attack by WannaCry and NotPetya, which bypassed firewalls and crippled thousands of organisations, companies have turned to AI in order to provide greater protection. Machine algorithms have the advantage of speed and are less labour intensive than traditional security models. However, hackers are now also leveraging ML in order to develop more sophisticated modes of attack. They are employing malicious algorithms that have the ability to evade detection by adapting, learning, and continuously improving. AI-led attacks look likely to feature in the future, with a recent study by Forrester revealing that 88% of security professionals expect AI-driven attacks to become mainstream.

**Why this is important?**:

> "...Only AI can fight AI."

With new threats on the horizon, the industry will have to adapt in order to defend itself. Companies are already shifting towards more ‘offensive AI’ systems and we are likely to see even more developments as people fight to protect their most valuable resource - data.

[Researchers Develop Method for Artificial Neuronal Networks to Communicate with Biological Ones](https://www.unite.ai/researchers-develop-method-for-artificial-neuronal-networks-to-communicate-with-biological-ones/){:target="_blank"}
A group of researchers has developed a way for artificial neuronal networks to communicate with biological neuronal networks. The new development is a big step forward for neuroprosthetic devices, which replace damaged neurons with artificial neuronal circuitry.

The new method relies on the conversion of artificial electrical spiking signals to a visual pattern. That is then used, via optogenetic stimulation, in order to entrain the biological neurons.

---

## Jobs

{% include giphy.html content="https://media.giphy.com/media/QxUiLkCQZEMzS/giphy.gif" %}

---
---

- [Machine Learninig Engineer](https://www.glassdoor.ca/Job/canada-machine-learning-engineer-jobs-SRCH_IL.0,6_IN3_KO7,32.htm?fromAge=7&jl=3552705517&ja=128504383&guid=0000017246b98e83b7d30fec6495cdd5&pos=101&srs=EMAIL_JOB_ALERT&s=224&ao=863973&utm_source=jobalert&utm_medium=email&utm_campaign=jobAlertAlert&utm_content=ja-jobtitle&utm_term=){:target="_blank"}; MavTek, Montreal.

- [Machine Learning Engineer](https://www.glassdoor.ca/Job/canada-machine-learning-engineer-jobs-SRCH_IL.0,6_IN3_KO7,32.htm?fromAge=7&jl=3552705517&ja=128504383&guid=0000017246b98e83b7d30fec6495cdd5&pos=101&srs=EMAIL_JOB_ALERT&s=224&ao=863973&utm_source=jobalert&utm_medium=email&utm_campaign=jobAlertAlert&utm_content=ja-jobtitle&utm_term=){:target="_blank"} Apple, Vancouver.

- [Machine Learning Engineer](https://www.glassdoor.ca/Job/canada-machine-learning-engineer-jobs-SRCH_IL.0,6_IN3_KO7,32.htm?fromAge=7&jl=3552705517&ja=128504383&guid=0000017246b98e83b7d30fec6495cdd5&pos=101&srs=EMAIL_JOB_ALERT&s=224&ao=863973&utm_source=jobalert&utm_medium=email&utm_campaign=jobAlertAlert&utm_content=ja-jobtitle&utm_term=){:target="_blank"} Paytm, Toronto.

- [Machine Learning/Data Infrastructure Engineer](https://www.glassdoor.ca/Job/canada-machine-learning-engineer-jobs-SRCH_IL.0,6_IN3_KO7,32.htm?fromAge=7&jl=3552705517&ja=128504383&guid=0000017246b98e83b7d30fec6495cdd5&pos=101&srs=EMAIL_JOB_ALERT&s=224&ao=863973&utm_source=jobalert&utm_medium=email&utm_campaign=jobAlertAlert&utm_content=ja-jobtitle&utm_term=){:target="_blank"} Wise Systems, Montreal.

- [Deep Learning R&D Engineer](https://www.glassdoor.ca/Job/canada-machine-learning-engineer-jobs-SRCH_IL.0,6_IN3_KO7,32.htm?fromAge=7&jl=3552705517&ja=128504383&guid=0000017246b98e83b7d30fec6495cdd5&pos=101&srs=EMAIL_JOB_ALERT&s=224&ao=863973&utm_source=jobalert&utm_medium=email&utm_campaign=jobAlertAlert&utm_content=ja-jobtitle&utm_term=){:target="_blank"}

- [Machine Learning Scientist](https://www.glassdoor.ca/Job/canada-machine-learning-engineer-jobs-SRCH_IL.0,6_IN3_KO7,32.htm?fromAge=7&jl=3552705517&ja=128504383&guid=0000017246b98e83b7d30fec6495cdd5&pos=101&srs=EMAIL_JOB_ALERT&s=224&ao=863973&utm_source=jobalert&utm_medium=email&utm_campaign=jobAlertAlert&utm_content=ja-jobtitle&utm_term=){:target="_blank"} Amazon, Montreal.

- [Senior Data Analyst](https://ai-jobs.net/job/1478-senior-data-analyst/){:target="_blank"}, Remote or Austin, TX

- [Software Developer, Machine Learning](https://careers.google.com/jobs/results/107074172166775494-software-developer-machine-learning/){:target="_blank"}, Google, Waterloo, ON, Canada

---

That's it folks! That's a review of my week.

If you would like to collaborate on an interesting AI project, please let me know.

Until next time, stay safe! Love and l[I](http://gen.lib.rus.ec/){:target="_blank"}ght, in the name of Professor Dumbledore.

{% include giphy.html content="https://media.giphy.com/media/IIJpyNVX37NAI/giphy.gif" %}
