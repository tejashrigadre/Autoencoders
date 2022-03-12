# Variational Autoencoder for Art Generation

I have forked [Variational Autoencoder](https://github.com/developershutt/Autoencoders/tree/main/4%20-%20Variational%20Autoencoder) project and explored using VAE for Abstract Art Generation. VAE can work as Generative Adversarial Network which can be used for generating new images using the latent space of the image dataset it is trained with. When a random noise from standard distribution is passed to the decoder of VAE, it generates a new image sampled from latent space.

## Dataset
Below image dataset from kaggle is used to train the model.
https://www.kaggle.com/greg115/abstract-art

## Hardware dependencies
Best to use a GPU to train the model as even with AWS ml.g4dn.xlarge GPU instance, it took about 45 minutes to train for 100 epochs.

## Results
The model was able to generate art images with similar patterns as training data, however the generated images were blurry and lacked sharpness.
One technique that I tried to increase image sharpness was to balance KL divergence loss in coparison to reconstruction loss by multiplying KL loss with a factor of 0.001, but that did not result in much improvement for this dataset.

The original dataset used in this project was trained on 60k anime images and I believe that given the images being used for art generation model are abstract. Either a larger dataset or augmented data can help to further improve the quality of generated images.

I wish to further explore this topic.





