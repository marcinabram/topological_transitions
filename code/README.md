# Code Demonstrations

## Spinodal Decomposition Model

### Spinodal Decomposition (Part I)

See the notebook:
<a href="./spinodal_decomposition_part1.ipynb">spinodal_decomposition_part1.ipynb</a>.

In this notebook, we analyze the spinodal decomposition model. We visualize the simulation data.
We describe a class of output of particular interest, consisting of microscopic spanning clusters (SC).
We show, that the appearance of the SC instances can be characterized by a change in the characteristic length of the system and a dramatic increase in the spatial autocorrelation - both of which are displays of universality behavior of the system.
Next, we map the simulation frames to the latent (feature) space.
We analyze if there exist any well-defined clusters in the feature space.
In the last section, we apply the learning-by-confusion scheme, to determine the threshold values of parameters for which we can observe the transition between the two main morphology classes.

### Spinodal Decomposition (Part II)

See the notebook:
<a href="./spinodal_decomposition_part2.ipynb">spinodal_decomposition_part2.ipynb</a>.

Here, we presented how to train classifiers capable of detecting the SC instances without explicit access to the true labels.
We use a form of a teacher-student framework and the idea of the label propagation.
We map the input to the latent space using the pre-trained ResNet-V2 model.
Next, we use the k-Means to cluster the data in the latent space.
We train a classifier on auxiliary labels and we show, that in the process, it acquires the capability of detecting the SC instances.
We perform the experiment using several different neural network architectures, and we show that all of them overperform the baseline approach.

### Spinodal Decomposition (Part III)

See the notebook:
<a href="./spinodal_decomposition_part3.ipynb">spinodal_decomposition_part3.ipynb</a>.

In this notebook, we focus on training predictive models. We train a regression model, to predict the initial parameters from the final simulation output. We can use it to study transitions between different classes of microstructural patterns.

## Physical Vapor Deposition

See the notebook:
<a href="./pvd_criticality.ipynb">pvd_criticality.ipynb</a>.

In this notebook, we show whether our method can be generalized to more complex scenarios, namely to physical vapor deposition (PVD) of thin films.

## Bonus: Unsupervised Symmetry-Preserving Feature Learning

See the notebook:
<a href="https://gist.github.com/marcinabram/47e02a0cff1461c256b6e84bc021e515">unsupervised_feature_learning.ipynb</a>.

We demonstrate an unsupervised method of learning feature vector representation that preserves physical symmetries. To achieve this goal, we adopted the approach presented in A. Dosovitskiy et al. "Discriminative Unsupervised Feature Learning with Exemplar Convolutional Neural Networks" (2014), https://arxiv.org/abs/1406.6909. We test this approach on input representing a numerical simulation of the Spinodal Decomposition model.

