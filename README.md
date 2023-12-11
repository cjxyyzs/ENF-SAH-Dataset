# About
This repository contains the ENF-STH audio dataset containing short-contaminated ENF signals, the corresponding reference and one-day reference, which was collected around Wuhan University. In addition, the repository provides  Matlab programs for extracting and estimating ENF, as well as a display of the corresponding visualization effects. These resources can help you better understand and utilize this audio dataset.
# ENF-STH Dataset
* Recording location: Restaurants, playground, gymnasium, parking lot, square, library and lawn.
* Environment diversity: day/night, interior/exterior.
* Recording device: recording pens, smartphones, tablets, laptops, a total of ten types of devices.
* Duration: 2~10 minutes
* Format: PCM WAVE
* Quantization depth: 16-bit
* Channel: mono
* Sampling frequency: 8000 Hz (400 Hz for reference data)
* Category:
* enf_audio: "01~40.wav" 40 real-world recordings with captured ENF.
* ref_audio: "ref_01~ref_40.wav" the corresponding 40 reference ENF (noise-free, same duration) obtained from power main.
* ref_one_day: the corresponding one-day (24 hours) reference ENF for the 40 recordings. "3-5,23.wav" means "03.wav", "04.wav", "05.wav" and "23.wav" in enf_audio folder are recorded within the same day.
# Note about the Ground-Truth 
The ground-truth matched location (the lag that corresponds to the true timestamp) within the one-day reference can be obtained by matching the noise-free ref files with the corresponding one-day ref. For example, we can match "ref_05.wav" in "ref_audio" folder within "3-5,23.wav" in "ref_one_day" folder, and the matched lag index is the "ground truth" timestamp for recording "05.wav" in "enf_audio" folder, meaning that "05.wav" should be matched at the same or a very close lag index in "3-5,23.wav". Both MSE and CC can be used for the matching criterion as long as the recording and ref are matched using the same criterion.
# Matlab Programs
It contains our adaptive-window-based harmonic recombination (AWHR) method, which is effective in short-contaminated audio. Here we provide the steps on how to use AWHR to process ENF signals.

#Step 1: Data Preparation
Firstly, it is necessary to prepare audio files with ENF signals. In addition, to further verify the processing effect of the signal, it is necessary to prepare corresponding reference signals and a reference database for a period of time. Taking the data in ENF-STH as an example, we can use '02.wav' in the 'enf_audio' folder, 'ref_02.wav' in the 'ref_audio' folder, and '2,19, 21, 24.wav' in the 'ref_one_day' folder.

#Step 2: Data Preprocessing


an example of the process of using AWHR to process signal in ENF-STH. 

in comparison with the following existing work
* Robust filtering algorithm (RFA) [1],
* Harmonic robust filtering algorithm (HRFA) and graph-based harmonic selection algorithm (GHSA) [2],
* Robust media time-stamping method by [S. Vatansever et al. 2022 IEEE SPL](https://ieeexplore.ieee.org/document/9882322/references#references),

evaluated using real-world recordings from short-contaminated ENF-STH dataset. The following figure shows the comparison between our method and [1], [2], [3] methods.

xxfigurexx


# Citation Information
* ENF Enhancement
  >\[1] G. Hua and H. Zhang, "ENF Signal Enhancement in Audio Recordings," in IEEE Transactions on Information Forensics and Security, vol. 15, pp. 1868-1878, 2020, doi: 10.1109/TIFS.2019.2952264.
  
  >\[2] G. Hua, H. Liao, H. Zhang, D. Ye and J. Ma, "Robust ENF Estimation Based on Harmonic Enhancement and Maximum Weight Clique," in IEEE Transactions on Information Forensics and Security, vol. 16, pp. 3874-3887, 2021, doi: 10.1109/TIFS.2021.3099697.
* Related work
  
  

  
