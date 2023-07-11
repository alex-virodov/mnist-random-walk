"Smooth"<sup>[1]</sup> random walk in MNIST image space. 
---

![](random_walk_n=5k_t=10.0_seed=1.gif)

This is my attempt to visualize the smoothness of the space of MNIST images. For each currently 
displayed image, I select the next image with probability proportional to the inverse distance 
(closer is more probable, distance is eucledian, aka RMS between corresponding pixels of the two images, precomputed).

This shows that the dataset has quite a lot of built-in smoothness just from its natural density in image space.

Next steps: figure out how to interpolate/extrapolate in this dataset without leaving the image space of digits.
Probably using GANs, though GANs have demonstrained<sup>[2]</sup> they are not confined to what I as human would qualify
as the image space of digits.

----------------

[1] preferring closest image using eucledian distance

[2] e.g.

![](https://machinelearningmastery.com/wp-content/uploads/2019/04/Plot-of-100-GAN-Generated-MNIST-Figures-After-100-Epochs.png)

(https://machinelearningmastery.com/how-to-develop-a-generative-adversarial-network-for-an-mnist-handwritten-digits-from-scratch-in-keras/)
