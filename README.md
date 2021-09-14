<p align="center">
  <a href="https://www.perceptilabs.com">
  <img src="./pl_logo.png">
  </a>
</p>

# Voice classification to recognize Yes-No instructions

This dataset<sup>1</sup> contains sounds and spectrogram images of the words "yes" and "no".

The spectrogram images can be used to build and train an ML model that can classify a yes/no sound converted to spectrogram with high accuracy.

# Structure

This repo contains the following structure:

- **sound_2_spectrograms.ipynb** Jupyter notebook for generating spectrogram image files from sound files.
- **train**: original sounds (in .wav format), converted to mono.
- **train_images**: spectrogram images (in .jpg format) corresponding to each sound. These were generated using sound_2_spectrograms.ipynb.
- **dataset.csv**: CSV file that maps spectrogram files to **yes**/**no** classification labels.

<p align="center">
  <img src="./sample.png">
</p>

The following shows a partial example of the data stored in **dataset.csv**:

| **labels**  | **images**                    |
|-------------|-------------------------------|
| yes       | train_images/yes0.jpg       |
| yes       | train_images/yes1.jpg       |
| no        | train_images/no0.jpg |
| no        | train_images/no1.jpg |


The **yes**/**no** labels in the CSV map the image files to the yes or no classifications respectively. 

After the model has been trained it can be used for inference. For this, you could use sound_2_spectrograms.ipynb to generate a spectrogram from a given .wav file and then pass that spectrogram image file to the trained model for classification. 

# Community

Got questions, feedback, or want to join a community of machine learning practitioners working with exciting tools and projects? Check out our [Community](https://forum.perceptilabs.com/)!

<sup>1</sup> Dataset Credits: https://github.com/vi/codegolf-jein

