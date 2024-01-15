# LAB2: swedish_fine_tune_whisper

## Fine tuning Whisper model for Swedish audio transcription.
The Common Voice 11.0 dataset was used to fine tune the small open AI whisper model for 2000 steps using google colab GPU. 

For the feature pipeline, a feature extraction function was used to extract the features from the audio data, while the pre-trained model's tokenizer was used to divide the label into tokens. This data was then saved to google drive. 

For the training pipeline, the model was fine-tuned and the evaluation metric was the Word Error Rate (WER).

## Improve model performance

There are two main different approaches to improving the model performance:

- Model centric
- Data centric

Model-centric entails doing modifications to the model architecture, hyperparameters, and training method to improve model performance. In our case, we could have used the bigger whisper model, changed the hyperparameters such as the learning rate or batch size. We could also employ regularization techniques such as dropout, early-stopping or L1/L2-norm to prevent overfitting. 

Data-centric approach on the other hand focuses on improving the quality of the data. This could mean increasing data size by aggregating multiple data sources for example by using the Swedish ASR database (https://www.nb.no/sprakbanken/en/resource-catalogue/oai-nb-no-sbr-56/), or improving the quality of the data by doing a feature selection such as by dimensionality reduction technique like PCA. Another method could also be doing a data augmentation technique and an appropriate technique I found was Spec Augmentation which augments data by way of time and frequency masking, and has shown to be an effective technique to improve performance of ASR models.
