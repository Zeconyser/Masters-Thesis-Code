# Masters-Thesis-Code

This code implements a comparative analysis of a Spiking Neural Network, and Artificial Neural Network trained on MNIST and FashionMNIST. Both networks are based on PyTorch, where the SNN uses Norse (https://open-neuromorphic.org/neuromorphic-computing/software/snn-frameworks/norse/) for its spiking components. In fact, Norse offers a nice tutorial on how to set up a MNIST-classifier SNN here https://norse.github.io/notebooks/mnist_classifiers.html.

To run it as it is, simply execute all cells in a google colab environment. Results dictionaries (intra_epoch_metrics, epoch_metrics) get saved into a a google drive folder as pickle files, so the 'save_path' needs to be adjusted before running it. 

The code does the following: 

1. Download  MNIST and FashionMNIST and create data loaders for. 
2. Set up two neural networks, with an equal number of layers and hidden layer neurons
3. Train the networks and perform analyses, both within the first epoch, as well as between full epochs.
4. Plot the results
5. Coorrelate the Cluster Distances between the network types trained on the same dataset

To run the training and analysis on a particular network and dataset, simply chose the appropriate train/test loaders in the corresponding tracker class (snn_tracker or ann_tracker) at the bottom.

The SNN with FashionMNIST is particularly slow in the first epoch. Training the first epoch until 50% accuracy took around six hours. To complete to ramaining epochs however, should take around 15 minutes.
