xiRT - Introduction
===================

xiRT is a deep learning tool to predict the retention times(s) of linear and crosslinked peptides
from multiple fractionation dimensions including RP (typically coupled to the mass spectrometer).
xiRT was developed with a combination of SCX / hSAX / RP chromatography. However, xiRT supports all
available chromatography methods.

Description
***********

xiRT is meant to be used to generate additional information about CSMs for machine learning-based
rescoring frameworks but the usage can be extended to spectral libraries, targeted acquisitions etc.

xiRT offers several training / prediction  modes that need to be configured
depending on the use case. At the moment training, prediction, crossvalidation are the supported
modes.
- *training*: trains xiRT on the input CSMs (using 10% for validation) and stores a trained model
- *prediction*: use a pretrained model and predict RTs for the input CSMs
- *crossvalidation*: load/train a model and predict RTs for all data points without using them
in the training process. Requires the training of several models during CV.

**Note**: all modes can be supplemented by using a pre-trained model ("transfer learning").