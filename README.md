# Personality Perception in Human Videos Altered by Motion Transfer Networks

The software provides functionality for an extensive analysis of Thin-Plate Spline Motion Model (TPS) performance in portraying personality through utilizing different samples as the source and driving inputs.

The repository contains the implementation of the framework, including functionality for the analysis of two user studies, data, and user study results for further studies. 

Original Thin-Plate Spline Motion Model Repository: https://github.com/yoyo-nb/Thin-Plate-Spline-Motion-Model
Original Notebook: https://colab.research.google.com/drive/1DREfdpnaBhqISg0fuQlAAIwyGVn1loH_?usp=sharing

## Running Instructions
- [TED-Samples-50](TED-Samples-50) directory contains the 50 samples rated for their personalities in our user study.
- [Selected Samples](Selected%20Samples) directory contains the low, neutral, and high samples chosen per personality factor.
- [Thin_Plate_Spline_Motion_Model.ipynb](Thin_Plate_Spline_Motion_Model.ipynb) contains the code to generate the altered video samples. This Notebook file can run on [Google Colab](https://colab.research.google.com/) and includes any necessary downloads for functioning, including:
  -  Downloading [TPS](https://github.com/yoyo-nb/Thin-Plate-Spline-Motion-Model.git) Model for pose transfer
  -  Installing [mediapipe](https://pypi.org/project/mediapipe/) for pose estimation
  -  Importing [TED-Talks](https://paperswithcode.com/dataset/ted-talks) dataset
  -  Dependencies:
      - `GoogleAuth, GoogleDrive, GoogleCredentials, drive, torch, mediapipe, imageio, numpy, scipy, skimage, pandas, gspread`
  - Note that this code requires a default pose image to choose representatives for the video samples. Any image that contains an idle upper body can be used; we provide the one used in our study as [default_pose.png](default_pose.png).
  - The samples in [TED-Samples-50](TED-Samples-50) directory should be copied to the MotionTransfer folder to be used by TPS.
- [Generated Samples](Generated%20Samples) directory contains altered samples used in our second user study.
- The code in [Analysis/Analysis.ipynb](Analysis/Analysis.ipynb) produces the analysis in **Tables 2, 3, 5, 6, and 7** of the article and the charts in **Figures 1 and 4**. The cells containing the related code are marked within the Notebook file.
  - This code uses our study results included in [Analysis/FirstStudy.csv](Analysis/FirstStudy.csv) and [Analysis/SecondStudy.csv](Analysis/SecondStudy.csv)
  - The code runs ANOVA and TukeyHSD analysis on the data and produces box charts to summarize the results
  - Dependencies:
    - `numpy, matplotlib, seaborn, scipy, statsmodels, factor_analyzer, sklearn, `
- Included codes are tested on [Google Colab](https://colab.research.google.com/) with Python 3.10.12


If you find this work useful, please cite 

Ayda Yurtoğlu, Sinan Sonlu, Yalım Doğan, and Uğur Güdükbay. Personality Perception in Human Videos Altered by Motion Transfer Networks. Computers & Graphics, 119:Article No. 103886, 11 pages, April 2024.

```
@Article{YurtogluSDG2024,
	author	=	{Ayda Yurto{\^g}lu and Sinan Sonlu and Yal{\i}m Do{\^g}an and U{\^g}ur G{\"u}d{\"u}kbay},
	title = {Personality Perception in Human Videos Altered by Motion Transfer Networks},
	journal = {Computers \& Graphics},
	volume = {119},
	pages = {Article No. 103886, 11 pages},
	year = {2024},
	month	= {April},
	issn = {0097-8493},
	doi = {https://doi.org/10.1016/j.cag.2024.01.013},
	url = {https://www.sciencedirect.com/science/article/pii/S009784932400013X},
	keywords = {Pedestrian detection and tracking, Data-driven simulation, Three-dimensional reconstruction, Crowd simulation, Augmented reality, Deep learning},
	abstract = {Crowd simulations imitate the group dynamics of individuals in different environments. Applications in entertainment, security, and education require augmenting simulated crowds into videos of real people. In such cases, virtual agents should realistically interact with the environment and the people in the video. One component of this augmentation task is determining the navigable regions in the video. In this work, we utilize semantic segmentation and pedestrian detection to automatically locate and reconstruct the navigable regions of surveillance-like videos. We place the resulting flat mesh into our 3D crowd simulation environment to integrate virtual agents that navigate inside the video avoiding collision with real pedestrians and other virtual agents. We report the performance of our open-source system using real-life surveillance videos, based on the accuracy of the automatically determined navigable regions and camera configuration. We show that our system generates accurate navigable regions for realistic augmented crowd simulations.}
}
```
