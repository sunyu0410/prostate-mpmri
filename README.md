# prostate-mpmri
This repo holds some models internally developed by the BiRT project.

## Tumour location with ADC
This model takes the mpMRI data and outputs the likelihood of the tumour.
* Input
  * T2w: bias-field corrected, normalised
  * Prostate contour: a binary mask outlining the prostate region
  * ADC map
  * High-b DWI: 1200 was used in the training. It should match as much as possible. Normalised
* Run
  * Load the model using `keras.models.load_model()`;
  * Prepare the intput data as described;
  * Run the model using `model.predict()`.
