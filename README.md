# About
This repository comprises the ENF-SAH audio dataset, encompassing considerably contaminated short ENF signals, along with their corresponding reference and one-day reference datasets, collected on the campus of Wuhan University. In addition, the repository provides  Matlab programs for extracting and estimating ENF, as well as a display of the corresponding visualization results. These resources can help you better understand and utilize this audio dataset.
# ENF-SAH Dataset
* Recording location: restaurants, playground, gymnasium, parking lot, square, library and lawn.
* Environment diversity: day/night, interior/exterior.
* Recording device: Redmi K40, Aigo R6633, iPad Air4, Tascam DR-07x, Philips VTR7100, and iPhone 13.
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
The ground-truth matched location (the lag that corresponds to the true timestamp) can be determined by aligning noise-free reference files with their respective one-day references. For instance, matching "ref_05.wav" in "ref_audio" folder with "3-5,23.wav" in "ref_one_day" folder yields the lag index, serving as the ground truth timestamp for "05.wav" in "enf_audio" folder. This implies that "05.wav" should align with the same or very close lag index in "3-5,23.wav". Both MSE and CC can be used for the matching criterion as long as the recording and ref are matched using the same criterion.
 
* Related works
 >\[1] G. Hua and H. Zhang, "ENF Signal Enhancement in Audio Recordings," in IEEE Transactions on Information Forensics and Security, vol. 15, pp. 1868-1878, 2020.
  >\[2] G. Hua, H. Liao, H. Zhang, D. Ye and J. Ma, "Robust ENF Estimation Based on Harmonic Enhancement and Maximum Weight Clique," in IEEE Transactions on Information Forensics and Security, vol. 16, pp. 3874-3887, 2021.
  > \[3] G. Hua, "Error analysis of forensic ENF matching," in Proc. 2018 IEEE International Workshop on Information Forensics and Security (WIFS), pp. 1-7, Hong Kong, Dec. 2018. [link](https://ieeexplore.ieee.org/document/8630786)<br>
  > \[4] G. Hua, G. Bi, and V. L. L. Thing, "On practical issues of electric network frequency based audio forensics," IEEE Access, vol. 5, pp. 20640-20651, Oct. 2017. [link](https://ieeexplore.ieee.org/document/7807225)<br>
  > \[5] G. Hua, Y. Zhang, J. Goh, and V. L. L. Thing, "Audio authentication by exploring the absolute error map of the ENF signals," IEEE Trans. Inf. Forensics Security, vol. 11, no. 5, pp. 1003-1016, May 2016. [link](https://ieeexplore.ieee.org/document/7378470)<br>
  > \[6] G. Hua, J. Goh, and V. L. L. Thing, “A dynamic matching algorithm for audio timestamp identification using the ENF criterion,” IEEE Trans. Inf. Forensics Security, vol. 9, no. 7, pp. 1045-1055, Jul. 2014. [link](https://ieeexplore.ieee.org/document/6808537)<br>
  > \[7]H. Liao, G. Hua and H. Zhang, "ENF Detection in Audio Recordings via Multi-Harmonic Combining," IEEE Signal Processing Letters, vol. 28, pp. 1808-1812, 2021. [link](https://ieeexplore.ieee.org/document/9528023)


  
