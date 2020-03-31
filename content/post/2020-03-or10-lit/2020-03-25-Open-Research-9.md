---
author: Rene Bidart
date: "2020-03-00T00:00:00Z"
title: 'Open Research 10: Literature Review'
---

## VAE intuition:

BETA VAE!
[https://ermongroup.github.io/blog/a-tutorial-on-mmd-variational-autoencoders/](https://ermongroup.github.io/blog/a-tutorial-on-mmd-variational-autoencoders/)
[https://arxiv.org/pdf/1706.02262.pdf](https://arxiv.org/pdf/1706.02262.pdf)
Tutorial:
[https://www.tandfonline.com/doi/full/10.1080/01621459.2017.1285773?casa_token=ikcvwnjzvHQAAAAA%3A0KzUTSM4saUASpVBTfK0nVJxhlh41o5FKFhQkmMAd2uIOxollNkbQEgznDrpZkwEPsVVgDEcPMII](https://www.tandfonline.com/doi/full/10.1080/01621459.2017.1285773?casa_token=ikcvwnjzvHQAAAAA%3A0KzUTSM4saUASpVBTfK0nVJxhlh41o5FKFhQkmMAd2uIOxollNkbQEgznDrpZkwEPsVVgDEcPMII)
Less important:
[https://arxiv.org/abs/1509.00519](https://arxiv.org/abs/1509.00519)

## Disentangled (in general)
Previous work has shown in general [https://arxiv.org/pdf/1811.12359.pdf](https://arxiv.org/pdf/1811.12359.pdf) the unsupervised learning of disentangled representations requires inductive bias on the model and the data. For this work we will focus on a particular .


Following the results in this paper, we are focusing on a specific case of learning a disentangled representation, with a specific goal. In this work we will focus on the aim of disentangling object orientation and shape, with the goal of allowing lower capacity models to generalize better.

There is no formal definition of what it means to be a disentangled representation, but intuitively … In this work we will focus on disentangling the shape of an object and its orientation.

The idea is the model has to "learn" what the object is at each orientation, rather than representing it as a single object with an orientation.


## Supervised:
[http://openaccess.thecvf.com/content\_ICCV\_2017/papers/Worrall\_Interpretable\_Transformations\_With\_ICCV\_2017\_paper.pdf](http://openaccess.thecvf.com/content_ICCV_2017/papers/Worrall_Interpretable_Transformations_With_ICCV_2017_paper.pdf)
Given the relative rotation between a set of 2d faces, they use an autoencoder style network to learn a laten representation of the face that can be transformed by the 3d rotation.  This enforces that the latent representation accurately reflects 3d structure of the face, because it is transformed in 3d space. 

#### Weakly supervised
[https://openreview.net/pdf?id=H1e1XeXlP4](https://openreview.net/pdf?id=H1e1XeXlP4)
Using groups of observations:
[https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/viewPaper/16521](https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/viewPaper/16521)


## INVERSE GRAPHICS Style 
pre-specified decoders:

- review these again
[http://papers.nips.cc/paper/7297-visual-object-networks-image-generation-with-disentangled-3d-representations.pdf](http://papers.nips.cc/paper/7297-visual-object-networks-image-generation-with-disentangled-3d-representations.pdf)
They separate image generation into shape, viewpoint and texture by rendering a 3d shape, then rendering a 2.5D (silhouette and depth map), and finally adds texture. 

Learn a disentangled generative model for images by explicitly specifying the generation in terms of shape, viewpoint, and texture. Use a 3D shape generation network, which is then fed into a renderer to show this in 2D, including viewpoint and texture. 
Does not disentangle the 3D pose of the object, ((this would be a good extension of our work, using this to extend it to generating 2d with viewpoint and texture.)) -reread this more closely

[http://papers.nips.cc/paper/7459-3d-aware-scene-manipulation-via-inverse-graphics.pdf](http://papers.nips.cc/paper/7459-3d-aware-scene-manipulation-via-inverse-graphics.pdf)
Here they use a multiple encoder networks to generate semantic segmentation, object pose and orientation, and texture parameters from an image. The image is then reconstructed by ...

[https://arxiv.org/pdf/1906.03281.pdf](https://arxiv.org/pdf/1906.03281.pdf)





### Half- INVERSE GRAPHICS Style 

[http://openaccess.thecvf.com/content\_CVPR\_2019/papers/Xing\_Unsupervised\_Disentangling\_of\_Appearance\_and\_Geometry\_by\_Deformable\_Generator\_Network\_CVPR\_2019_paper.pdf](http://openaccess.thecvf.com/content_CVPR_2019/papers/Xing_Unsupervised_Disentangling_of_Appearance_and_Geometry_by_Deformable_Generator_Network_CVPR_2019_paper.pdf)
They disentangle appearance and geometry by using different generator for each and combining the results using a warping function to create an image. They also extend this to a VAE, where they use two networks to infer the latent vectors describing appearance and geometry.

[http://papers.nips.cc/paper/8387-explicit-disentanglement-of-appearance-and-perspective-in-generative-models.pdf](http://papers.nips.cc/paper/8387-explicit-disentanglement-of-appearance-and-perspective-in-generative-models.pdf)
They extent a VAE to consider two separate latent spaces, a perspective and appearance latent space, 
((((Read this for inspiration on paper writing))) Good refs on what counts as disentangled, and good lit review. 


[https://arxiv.org/pdf/1903.06946.pdf](https://arxiv.org/pdf/1903.06946.pdf)
[https://arxiv.org/pdf/1806.06298.pdf](https://arxiv.org/pdf/1806.06298.pdf)

### very weak priors over latent space, model structure:
[http://papers.nips.cc/paper/7174-learning-disentangled-representations-with-semi-supervised-deep-generative-models.pdf](http://papers.nips.cc/paper/7174-learning-disentangled-representations-with-semi-supervised-deep-generative-models.pdf)

###   Some metrics and methods: (important)
[https://arxiv.org/pdf/1711.00848.pdf](https://arxiv.org/pdf/1711.00848.pdf)
[http://papers.nips.cc/paper/7527-isolating-sources-of-disentanglement-in-variational-autoencoders.pdf](http://papers.nips.cc/paper/7527-isolating-sources-of-disentanglement-in-variational-autoencoders.pdf)


### ???
[https://arxiv.org/abs/1906.11732](https://arxiv.org/abs/1906.11732)


## Equivariance 
[https://dspace.mit.edu/handle/1721.1/113001](https://dspace.mit.edu/handle/1721.1/113001)

## Important 3d models
[http://papers.nips.cc/paper/6600-unsupervised-learning-of-3d-structure-from-images.pdf](http://papers.nips.cc/paper/6600-unsupervised-learning-of-3d-structure-from-images.pdf)
[https://ieeexplore.ieee.org/abstract/document/7469347](https://ieeexplore.ieee.org/abstract/document/7469347)












### Optimizing Affine Transforms in VAEs
Our goal is to create a VAE which will only encode a subset of affine transforms, but generalize to all. This is shown below:
![avae_3d.png](../avae_3d.png)

[Previously](https://renebidart.com/post/or5/2020-03-02-open-research-5/) we showed takes a higher capacity VAE to encode all possible orientations of an object, compared to encoding a single orientation. Our goal is to create a smaller model by only encoding a subset of all orientations, but still generalize to all orientations at inference. But how can we do this, given a dataset at random orientations?

Because the VAE is a generative model, we can the optimize an affine transform to find the orinetation at which the VAE best encodes the data, or has lowest loss. Our approach is to use an inner optimization loop during training to optimize this affine transform. The goal is that this will force the model to encode only a subset of the distribution. Then at inference time, this affine optimization can be used to allow the model to generalize to all orientations.

Normally stochastic gradient descent is used to update the parameters of the network to reduce the loss of the VAE. Here we will take another approach, where the forward pass of the VAE will include an optimization over a set of parameters, where the parameters are optimized to reduce the VAE's loss, maximizing the ELBO. These are the parameters of an affine transform, so the process corresponds to finding the optimal orientation to encode an object at. This optimization objective is shown as:

$\underset{\alpha}{\text{argmin}}\\{ L_{VAE}[\tau_{\alpha}^{-1}(p_\rho(q_\phi(\tau_{\alpha}(x))))]\\}$

To train a network of this form is very expensive, because the above optimization must be solved once for each forward pass. As I discussed [before](https://renebidart.com/post/or7/2020-03-17-open-research-7/), optimizing $\alpha$ is differentiable, but is likely to get caught in a local optima. To overcome this, we evaluate the performance at a number of different random initializations of $\alpha$, and then select the top k of these initializations to do gradient descent on. Here we used 32 random initializations, and did gradient descent on the top 8 of these.

These tests take a while to run, so we'll look at results later, and give a rigorous interpretation of the above in terms of variational inference.