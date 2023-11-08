# About
This repository contains the ENF-STH short audio dataset, which was collected around Wuhan University. In addition, the repository provides  Matlab programs for extracting and estimating ENF, as well as a display of the corresponding visualization effects. These resources can help you better understand and utilize this audio dataset. More information on:https://cjxyyzs.github.io/.
# ENF-STH Dataset
* Recording location: : Cafes, restaurants, KTV, shopping malls, cinemas, underground parking lots, squares, libraries, museums, and conference rooms.
* Environment diversity: day/night, interior/exterior.
* Recording device: recording pens, smartphones, tablets, laptops, a total of ten types of devices.
* Duration: 1~8 minutes
* Format: PCM WAVE
* Quantization depth: 16-bit
* Channel: mono
* Sampling frequencuy: 8000 Hz (400 Hz for reference data)
* Category:
* enf_audio: "01~40.wav" 40 real-world recordings with captured ENF.
* ref_audio: "ref_01~ref_40.wav" the corresponding 40 reference ENF (noise-free, same duration) obtained from power main.
* ref_one_day: the corresponding one-day (24 hours) reference ENF for the 40 recordings. "3-5,23.wav" means "03.wav", "04.wav", "05.wav" and "23.wav" in enf_audio folder are recorded within the same day.
# Note about the Ground-Truth 
The ground-truth matched location (the lag that corresponding to the true timestamp) within the one day reference can be obtained by matching the noise-free ref files with the corresponding one day ref. For example, we can match "ref_05.wav" in "ref_audio" folder within "3-5,23.wav" in "ref_one_day" folder, and the matched lag index is the "ground truth" timestamp for recording "05.wav" in "enf_audio" folder, meaning that "05.wav" should be matched at the same or a very close lag index in "3-5,23.wav". Both MSE and CC can be used for the matching criterion as long as the recording and ref are matched using the same criterion.It should be noted here that due to equipment reasons, some data have vertical deviations and require manual adjustment.The error caused by the device can be calculated by calculating the average vertical deviation between the extracted ENF signal and the reference signal.
# Matlab Programs
* ENF Detection
  
