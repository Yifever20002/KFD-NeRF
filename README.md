# KFD-NeRF
### [Paper](https://arxiv.org/abs/2407.13185)

This is the repo for the ECCV2024 project

>KFD-NeRF: Rethinking Dynamic NeRF with Kalman Filter\
>[Yifan Zhan](https://yifever20002.github.io/), Zhuoxiao Li, [Muyao Niu](https://myniuuu.github.io/), [Zhihang Zhong](https://zzh-tech.github.io/),  Shohei Nobuhara, Ko Nishino, Yinqiang Zheng\
>European Conference on Computer Vision (ECCV), 2024

![image](https://github.com/Yifever20002/KFD-NeRF/blob/main/images/pipeline.PNG)

## About KFD-NeRF

We introduce KFD-NeRF, a novel dynamic neural radiance field integrated with an efficient and high-quality motion reconstruction framework based on Kalman filtering. Our key idea is to model the dynamic radiance field as a dynamic system whose temporally varying states are estimated based on two sources of knowledge: observations and predictions. We introduce a novel plug-in Kalman filter-guided deformation field that enables accurate deformation estimation from scene observations and predictions. We use a shallow Multi-Layer Perceptron (MLP) for observations and model the motion as locally linear to calculate predictions with motion equations. To further enhance the performance of the observation MLP, we introduce regularization in the canonical space to facilitate the network's ability to learn warping for different frames. Additionally, we employ an efficient tri-plane representation for encoding the canonical space, which has been experimentally demonstrated to converge quickly with high quality. This enables us to use a shallower observation MLP, consisting of just two layers in our implementation. We conduct experiments on synthetic and real data and compare with past dynamic NeRF methods. Our KFD-NeRF demonstrates similar or even superior rendering performance within comparable computational time and achieves state-of-the-art view synthesis performance with thorough training.
