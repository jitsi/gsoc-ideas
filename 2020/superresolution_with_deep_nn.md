# Super-resolution with Deep Neural Networks to save bandwidth

## Prerequisites

Prior knowledge in these areas will be an advantage for this project, but none of them
are strictly necessary:

* Git
* Java
* Python
* Javascript
* Matlab
* Video encoding
* Tensorflow/PyTorch
* Deep Learning/convolutional networks
* React
* RTP (real-time transport protocol)
* super-resolution techniques
* WebRTC

## Goal

Provide a proof-of-concept which explores the feasibility of using super-resolution algorithms to provide HD video in a 
video conference while the server only sends SD video to users. 

## The project:

Recently, deep neural networks have been used to perform the task of super-resolution: Mapping a low-resolution image into
its high resolution equivalent [1]. Moreover, a framework called FAST [2] has been developed which exploits video compression 
in such a way that not every frame needs to be processed by the deep neural network. 
These promising advances made us wonder whether these technologies are mature enough to be used for Jitsi Meet.
The main bottleneck in video conferencing is the bandwidth requirement. Therefore, allowing the server to send SD video to users 
instead of HD video could allow for meetings with more users while still delivering HD quality meetings!

This project is very difficult: we do not expect a fully-working solution at the end of the summer.
We're mostly interested in exploring and answering these research questions:

1. Can we make use of the FAST [2] framework with the video compression provided by WebRTC?
2. At what frame-rate can the algorithm perform, with and without fast?
3. Is it realistic to serve the model weights of the network to each client?
4. Is the quality of the super-resolution high-definition video frames acceptable?
5. What is the resolution of the images we need to send from the server? 180p? 360p? 480p?
6. What is the resolution of the super-resolution high-definition video frames? 720p? 1080p? 4k????
7. Can we generate our own dataset to increase the performance?

In order to answer these questions, a working prototype should be implemented during the summer. 

[1] = https://arxiv.org/abs/1501.00092  
[2] = http://www.mit.edu/~sze/fast.html

## Pro tips for your application

Can you already find the answers to some of the research questions? What are your deliverables each week? Are there 
open-source implementation of SRCNN? What about pre-trained weights? 
If so, can you already try to run the network and explore its capabilities? 

If you have any questions, feel free to [create an issue](https://github.com/jitsi/gsoc-ideas/issues/new)!

## Mentors

@nikvaessen  
@bgrozev
