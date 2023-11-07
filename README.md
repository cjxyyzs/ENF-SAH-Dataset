# About
This repository contains the ENF-STH short audio dataset, which was collected around Wuhan University. In addition, the repository provides  Matlab programs for extracting and estimating ENF, as well as a display of the corresponding visualization effects. These resources can help you better understand and utilize this audio dataset.

# Note about the Ground-Truth 
The ground-truth matched location (the lag that corresponding to the true timestamp) within the one day reference can be obtained by matching the noise-free ref files with the corresponding one day ref. For example, we can match "ref_005.wav" in "all_ref_2022" folder within "3-5,23,59-60,71-72,83-84.wav" in "ref_240_one_day" folder, and the matched lag index is the "ground truth" timestamp for recording "005.wav" in "all_2022" folder, meaning that "005.wav" should be matched at the same or a very close lag index in "3-5,23,59-60,71-72,83-84.wav". Both MSE and CC can be used for the matching criterion as long as the recording and ref are matched using the same criterion.It should be noted here that due to equipment reasons, some data have vertical deviations and require manual adjustment.The error caused by the device can be calculated by calculating the average vertical deviation between the extracted ENF signal and the reference signal.

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
* all_2022: "001~240.wav" 240 real-world recordings with captured ENF.
* all_ref_2022: "ref_001~240_ref.wav" the corresponding 240 reference ENF (noise-free, same duration) obtained from power main.
* ref_240_one_day: the corresponding one-day (24 hours) reference ENF for the 240 recordings. "3-5,23,59-60,71-72,83-84.wav" means "003.wav", "004.wav", "005.wav", "023.wav", "059.wav", "060.wav", "071.wav", "072.wav", "083.wav" and "084.wav" in all_2022 are recorded within the same day.
