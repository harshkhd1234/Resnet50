# Resnet50

# Overview :
Resnet short for Residual Networks is a classic neural network used as a backbone for many computer vision tasks and '50' refers to 50 layers of neurons. This model was the winner of ImageNet challenge in 2015. The fundamental breakthrough with ResNet was it allowed us to train extremely deep neural networks with 150+layers successfully. Prior to ResNet training very deep neural networks was difficult due to the problem of vanishing gradients.

# 1 - The problem of very deep neural networks
The main benefit of a very deep network is that it can represent very complex functions. It can also learn features at many different levels of abstraction, from edges (at the lower layers) to very complex features (at the deeper layers). However, using a deeper network doesn't always help. A huge barrier to training them is vanishing gradients: very deep networks often have a gradient signal that goes to zero quickly, thus making gradient descent unbearably slow. More specifically, during gradient descent, as you backprop from the final layer back to the first layer, you are multiplying by the weight matrix on each step, and thus the gradient can decrease exponentially quickly to zero (or, in rare cases, grow exponentially quickly and "explode" to take very large values).

During training, you might therefore see the magnitude (or norm) of the gradient for the earlier layers descrease to zero very rapidly as training proceeds:

https://www.google.com/url?sa=i&url=https%3A%2F%2Fkknews.cc%2Fcode%2Fpkk6538.html&psig=AOvVaw2oitnItVLW6Hv_38a2lh1b&ust=1598197782712000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCLDEseuUr-sCFQAAAAAdAAAAABAD

