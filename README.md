# Personality Perception in Human Videos Altered by Motion Transfer Networks

The software provides functionality for an extensive analysis of Thin-Plate Spline Motion Model (TPS) performance in portraying personality through utilizing different samples as the source and driving inputs.

The repository contains the implementation of the framework, including functionality for the analysis of two user studies, data, and user study results for further studies. 

Original Thin-Plate Spline Motion Model Repository: https://github.com/yoyo-nb/Thin-Plate-Spline-Motion-Model
Original Notebook: https://colab.research.google.com/drive/1DREfdpnaBhqISg0fuQlAAIwyGVn1loH_?usp=sharing

## Running Instructions
- [TED-Samples-50](TED-Samples-50) directory contains the 50 samples rated for their personalities in our user study.
- [Selected Samples](Selected%20Samples) directory contains the low, neutral, and high samples chosen per personality factor.
- [Thin_Plate_Spline_Motion_Model.ipynb](Thin_Plate_Spline_Motion_Model.ipynb) contains the code to generate the altered video samples. This Notebook file can run on Google Colab and includes any necessary downloads for functioning, including:
  -  Downloading [TPS](https://github.com/yoyo-nb/Thin-Plate-Spline-Motion-Model.git) Model for pose transfer
  -  Installing [mediapipe](https://pypi.org/project/mediapipe/) for pose estimation
  -  Importing [TED-Talks](https://paperswithcode.com/dataset/ted-talks) dataset
  -  Dependencies:
    - `GoogleAuth, GoogleDrive, GoogleCredentials, drive, torch, mediapipe, imageio, numpy, scipy, skimage, pandas, gspread` 
- [Generated Samples](Generated%20Samples) directory contains altered samples used in our second user study.
- The code in [Analysis/Analysis.ipynb](Analysis/Analysis.ipynb) produces the analysis in Tables 2, 3, 5, 6, and 7 of the article and the charts in Figures 1 and 4.
  - This code uses our study results included in [Analysis/FirstStudy.csv](Analysis/FirstStudy.csv) and [Analysis/SecondStudy.csv](Analysis/SecondStudy.csv)
  - The code runs ANOVA and TukeyHSD analysis on the data
  -  Dependencies:
    - `numpy, matplotlib, seaborn, scipy, statsmodels, factor_analyzer, sklearn, `
