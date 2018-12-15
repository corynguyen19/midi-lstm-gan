# MIDI File LSTM & GAN
Using LSTMs and GANs to Generate Music from MIDI Files (APM Fall 2018)
Check out our blog post [here](https://medium.com/@abrahamkhan/generating-pokemon-inspired-music-from-neural-networks-bc240014132)! 

## Requirements:
* Python 3.x
* GPU compatible with the CuDNN Keras sequential model layers
* Installation of the following packages:
    * Music21
    * Keras
    * Tensorflow

## LSTM
For creating an LSTM to generate music, run lstm.py. This will parse all of the files in the Pokemon MIDI folder and train an LSTM model on them. The model will then be used to predict on a random sequence of notes from within the input data and a .mid file will be created.

## GAN
For creating a GAN to generate music, run mlp_gan.py. This will parse all of the files in the Pokemon MIDI folder and train a GAN model on them, with an LSTM-based discriminator and an MLP-based generator. After training, the generator will be fed random noise to make an output that will be converted into a .mid file using Music21. A plot of the discriminator and generator loss will also be saved.
