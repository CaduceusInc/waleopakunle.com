---
toc: true
comments: true
author: Wale
image: /images/2020-03-09-matting/media/segmentation-and-matting-difference.png
categories: [Research paper digest, GANs]
permalink: /papers/:year/:month/:day/:title
---

## **Background Matting --- Making the world your green screen**


![appearing-blue-spirit](https://media.giphy.com/media/mDSTfBsVus2o1ZA4YB/giphy.gif)

​														*Source: giphy.com*

Link to my colab notebook: [Background matting Implementation](https://colab.research.google.com/drive/1JRfpi7mTHSIs5CGdDVCVAaT8yAfWDq2D)

Have you ever wished to replace the background of a picture you took and just did not want to go through the hassle of using a professional studio? Are you a graphics designer or movie director and are just sick of having to use green screens for your video recordings? Well, if that happens to be you for some reason, I have great news for you! You can now easily replace the background of your images and videos with ease, depending on you or your team’s level of technical experience. You can now do this from the comfort of your home using a fixed or handheld camera, thanks to the work of a computer vision research team at the University of Washington. In their paper released on the 1st of April, they describe a novel architecture they came up with which lets you do just that! Now, all you need to make this a reality is a couple of GPUs, a picture(or video) of the background you want (without you in it) as well as a picture(or video) of you in the same background, all taken from your handheld mobile device. Their method is state of the art, and in my opinion, provides images that are comparable to professional images.



In this post, I am going to be giving you the key ideas from their paper without getting too technical. I will walk you through the core ideas of their paper, possible lucrative applications of the technology, as well as other resources to help you dive further in. I will also be providing a notebook set up for you to try your hands on this novel architecture, and make new mattes of yourself and your friends. 





## **Paper Summary**

#### **Which issue/problem are they improving/solving?**

The problem they attempt to solve is the problem of matting a foreground to a different background, while maintaining the integrity and quality of the image. In order to achieve this, they modeled the problem using this equation:

**C = F \*** **α + B \*(1-α)**          															. . .	 **i.**

This is called the **matting equation.**



Before I proceed, let me break down the equation so you fully understand what is going on.



*First of all, what is matting?*

Matting is the process of separating an image into foreground (F) and background (B) so you can composite the foreground onto a new background. This is the key technique behind the green screen effect that is widely used in video production, graphics, and consumer apps.



*Now, what are foreground, alpha and background in the matting equation?*

> “Foreground” refers to the content of the image, that is, the human in the image, who is to be transferred to a different background for example.

> “Background” here refers to the part of a picture, scene, or design that forms a setting for the main figures or objects, or appears furthest from the viewer.

> “Alpha” refers to the mixing coefficient. It can also be thought of as the transparency of the subject being captured in the image or scene.

Now let’s look at that matting equation again:

**C = F \*** **α + B \*(1-α)**      						    . . .   **i.**

Precisely, they attempt to solve for the Foreground (F), Background (B) and transparency (**α**) for each pixel in a given image. 

If you are familiar with computer vision, you may know that an image consists of three channels (R, G and B). The presence of these channels imply that the number of unknowns increases significantly. In this case, there are now 7 unknowns, from only 3 observations per pixel. My understanding of this is the following:

Colored Foreground (with the channels): 3 unknowns

Colored Background (has 3 channels): 3 unknowns

Mixture factor/ transparency (**α):** 1 unknown.



#### **What do they improve?**

Most existing matting methods of creating mattes require a green screen background or a manually created trimap to produce a good matte. Other methods rely on segmentation. Automatic, trimap-free methods are beginning to appear, but are not of comparable quality. Instead, the group from the University of Washington propose taking an additional photo of the (static) background just before or after the subject is in frame, and using this photo to perform background matting. Essentially, they reduce the 



##### **What older methods are they improving on?**

- Context Aware Matting (CAM) which simultaneously predicts the alpha and the foreground, thus solving the complete matting problem, but is not robust to faulty trimaps.
- Sampling based methods which use sampling to build the color statistics of the known foreground and background, and then solve for the matte in the ‘unknown’ region.
- Propagation-based approaches aim to propagate the alpha matte from the foreground and the background region into the ‘unknown’ region to solve the matting equation. Both sampling and propagation approaches are traditional approaches.
- Matting with known natural background: Some older methods solved matting with a natural background by simple background subtraction and thresholding but the results were very sensitive to the threshold and produced binary mattes.

![img](/images/2020-03-09-matting/media/segmentation-and-matting-difference.png)

*Difference between segmentation and the background matting procedure.*

*Source: Vivek Jarayam’s blog post on Towards Data Science*



**Issues with existing methods that necessitate this improvement**

- Previous methods took too long
- Were not robust enough (e.g, to faulty trimaps)
- Binary mattes were produced in some cases.
- Background subtraction methods consider shadows and so do not produce alpha mattes. The problem with this is that a background image with and without a shadow are inherently different and could produce undesirable results.



**What do they propose to do differently?**

- Use casually taken images of the background with and without the subject.


![image-capture-process](/images/2020-03-09-matting/media/image-capture-process.png)

*The image capture process*.    *Source: Soumyadip Sengupta et al.* 

- Use a context switching block to switch between scenarios.
- Use a GAN architecture to refine the matting output.



**Limitations of their method?**

- Well, first of all, the procedure requires two images.
- Second, they require a static background and minute camera motion; their method would not perform well on backgrounds with people walking through (photo-bombers) or with a camera that moves far from the background capture position.
- Their approach specializes exclusively on human subjects.
- This approach will fail for transparent objects, waterfalls, or backgrounds containing moving humans (in the case of image inputs).



## **Core ideas of the paper**

#### **Contributions introduced by the paper**

- The first trimap-free automatic matting algorithm that utilizes a casually captured background. 
- A novel matting architecture (Context Switching Block) to select among input cues. 
- A self-supervised adversarial training to improve mattes on real images. 
- Experimental comparisons to a variety of competing methods on a wide range of inputs (handheld, fixed camera, indoor, outdoor), demonstrating the relative success of our approach. 

![img](/images/2020-03-09-matting/media/architecture-overview.png)

*An overview of the background matting architecture.*

 *Source: Soumyadip Sengupta et al.* 



##### **The network architecture**

- Inputs and outputs

There are actually 4 input images to the network, two of which are supplied by the user and the other two are generated off of the user supplied images. The user’s input to the system is expected to be:

1. A 512×512 image or video **“I”** of a person in front of a static, natural background
2. An image of just the background **“B”**. 

Basically, all the user has to do is to take a picture using a smartphone camera and then step away from the frame to capture the background, like in the images below. 

![img](/images/2020-03-09-matting/media/example-of-inputs.png)

*Source: Vivek Jarayam’s blog post on Towards Data Science* 

The augmentation script then generates a soft segmentation (**S**) of the provided image, **I**, that contains the subject. **“S”** is derived by using Person Segmentation. 



In addition, in the event that an image is passed rather than a video, the 4th input to be generated by the script is 4 concatenations “**M**” of the single frame **I** , converted to grayscale. However, if a video is passed instead of an image, the 4th input generated will consist of 4 concatenations of two frames before and two frames after the input video **I.** This is done to account for the motion cues.

This concatenated object then have their features selectively combined and passed on to Residual Blocks which then feed into the decoders that decode the Foreground and α-matte.

- Training procedure

The training of the network consists of two parts: 

1. ##### **Supervised training** 

This is done using 4 encoders managed by a Context Switching block of selectors and 3 Residual Blocks and Decoders, trained on the Adobe dataset.



![img](/images/2020-03-09-matting/media/supervised-portion-of-architecture.png)

*Supervised portion of the architecture.* *Source: Vivek Jarayam’s blog post on Towards Data Science* 



The purpose of the Context Switching block in the supervised training is to manage the interaction between the 4 groups of input cues [Image, Background, Segmentation and Motion] from the image and prior encoders and combine the features efficiently. They observed that the Context Switching Block architecture helped to generalize to real data.

The output of the supervised training are the foreground image **“F”** as well as alpha matte **α.**

Remember the matting equation we talked about? These are the unknowns they are trying to decipher. F and **α** are then laid over various backgrounds from the Adobe dataset. However the outputs at this stage were discovered to not be refined enough. That's where the other part of the system comes in.


2. ##### An unsupervised training using a Generative Adversarial Network.

![img](/images/2020-03-09-matting/media/unsupervised-portion-of-architecture.png)

*Self-Supervised portion of the architecture.* *Source: Vivek Jarayam’s blog post on Towards Data Science*



In order to produce refined images, the output of the supervised training is fed into the unsupervised architecture, consisting of a discriminator which has been trained to identify what real images look like, and a generator which tries to come up with new images using the outputs of the supervised network. The discriminator, which knows what real images look like, then scores the images produced by the generator in a teacher-student kind of scenario; a min-max game. The least square error approach used in LS-GAN framework is adopted and the generator tries to minimize the error, to fool the generator into assigning an image a “Real” value, while the discriminator, which is essentially a classifier, tries to spot the errors in the image produced and assign it a “Real” or “Fake” label. 

The result of this is that the generator learns to produce increasingly better images. The errors of copied background, and lack of quality of the images produced in the supervised arm of the architecture are gradually overcome and the matte which now has a new background cannot be categorized as a fake image.

To get a feel of the adversarial training losses and more details about the architecture used, please consult the paper, or better still the source code showing their implementations.



#### **Advantages of the new method introduced**

- Speed of producing new matting with varying backgrounds.
- Gets rid of the need to use a trimap altogether. A casual image in a natural background is sufficient.



## **Key achievements of the paper**

It is my understanding that because this is a novel architecture and approach, there was no numerical benchmark available for this research. Hence, they conducted user studies for their real data testing. What they did was use previously available methods that make use of trimaps to generate mattes, and then take a survey of users to find out which they thought was best.



![img](/images/2020-03-09-matting/media/result-on-real-data.png)

*Summary of survey results*. *Source: Soumyadip Sengupta et al.*



## **Future research areas**

1. Making the method work for subjects other than human.
2. Addressing the problem that subject has to remain static.
3. Working on transparent subject, such as glass and waterfalls.
4. Eradicate the need for taking more than one photograph.

## **Possible business applications**

- The movie industry for scene generation. They may no longer have to use green screens for recording videos. Now, they could use any background, and simply matte the characters into a background of their choice.
- Professional photography, to generate images of people in diverse locations/backgrounds.

## **Conclusion**

In this post, I have gone over a proposed background matting technique that enables casual capture of high quality foreground+alpha mattes in natural settings, presented by researchers from Washington University. Their method requires the photographer to take a shot with a (human) subject and without, not moving much between shots. This approach avoids using a green screen or painstakingly constructing a detailed trimap as typically needed for high matting quality. They have developed a deep learning framework trained on synthetic-composite data and then adapted to real data using an adversarial network.

For even more details such as the nitty gritty of the network architecture, training dataset, hyperparameters and such, I suggest you read their official paper.





## **Resources**

1. Link to their [paper](https://arxiv.org/pdf/2004.00626.pdf)

1. Link to their inference [code base](https://github.com/senguptaumd/Background-Matting)

1. Link to their blog post and project page:
- [blog](https://towardsdatascience.com/background-matting-the-world-is-your-green-screen-83a3c4f0f635)
- [project page](https://towardsdatascience.com/background-matting-the-world-is-your-green-screen-83a3c4f0f635)

1. Link to my colab notebook: [Background matting Implementation](https://colab.research.google.com/drive/1JRfpi7mTHSIs5CGdDVCVAaT8yAfWDq2D)

### **New Concepts**

- **Trimap**

> As the name suggests, a *trimap* of an image **I** is a partition containing three sets of regions - **F**, **B** and **M**. The set **F** contains foreground pixel information, set **B** contains background pixel information and **M** is an intermediate region separating **F** from **B**. You could think of trimap as a mask that contains a white region that defines **F**, a black region that defines **B** and a gray region that defines **M**, which is often a region of uncertainty (some parameters are undefined too, depending on the application)



- Random affine transformations

> [Affine transformation](https://www.mathworks.com/help/images/ref/affine2d.html) is a linear mapping method that preserves points, straight lines, and planes. Sets of parallel lines remain parallel after an affine transformation.
>
> The affine transformation technique is typically used to correct for geometric distortions or deformations that occur with non-ideal camera angles. For example, satellite imagery uses affine transformations to correct for wide angle lens distortion, panorama stitching, and image registration. Transforming and fusing the images to a large, flat coordinate system is desirable to eliminate distortion. This enables easier interactions and calculations that don’t require accounting for image distortion. - Mathworks.com
