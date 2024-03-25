# About
Welcome to the Electric Network Frequency short audio harmonic (ENF-SAH) dataset repository. This unique dataset, curated at **Wuhan University**, encompasses a series of short Electric Network Frequency (ENF) recordings, significantly influenced by environmental disturbances. It presents a realistic challenge for audio processing, particularly in urban outdoor environments teeming with noise.
# ENF-SAH Dataset
- **Recording location**: restaurants, playground, gymnasium, parking lot, square, library and lawn.
- **Environment diversity**: day/night, interior/exterior.
- **Recording device**: Redmi K40, Aigo R6633, iPad Air4, Tascam DR-07x, Philips VTR7100, and iPhone 13.
- **Duration**: 2~10 minutes
- **Format**: PCM WAVE
- **Quantization depth**: 16-bit
- **Channel**: mono
- **Sampling frequency**: 8000 Hz (400 Hz for reference data)
- **Category**:
  - **'enf_audio'**: "01~40.wav" 40 real-world recordings with captured ENF.
  - **'ref_audio'**: "ref_01~ref_40.wav" the corresponding 40 reference ENF (noise-free, same duration) obtained from power main.
  - **'ref_one_day'**: the corresponding one-day (24 hours) reference ENF for the 40 recordings. "3-5,23.wav" means "03.wav", "04.wav", "05.wav" and "23.wav" in enf_audio folder are recorded within the same day.
# Note about the Ground-Truth 
The ground-truth matched location (the lag that corresponds to the true timestamp) can be determined by aligning noise-free reference files with their respective one-day references. For instance, matching "ref_05.wav" in "ref_audio" folder with "3-5,23.wav" in "ref_one_day" folder yields the lag index, serving as the ground truth timestamp for "05.wav" in "enf_audio" folder. This implies that "05.wav" should align with the same or very close lag index in "3-5,23.wav". Both MSE and CC can be used for the matching criterion as long as the recording and ref are matched using the same criterion.

# Comparation with existing ENF datasets
- **[Carioca 1 database](http://lps.lncc.br/index.php/demonstracoes/wifs15)**：The Carioca 1 dataset contains 100 audio recordings ranging from 19 to 35 seconds, all recorded at a sampling rate of 44.1kHz and a bit depth of 16 bits, with the primary voice energy concentrated between 100Hz and 4000Hz, avoiding interference from 60Hz electrical network frequencies. These audios are divided into 50 original male and female voices and their respective edited versions through cutting or insertion, with detailed records of editing details such as time points and ranges. Primarily intended for tampering detection, its application is limited due to the short duration of audios and the uniform recording conditions, particularly in unrestricted environments for ENF audio forensics research.
- **[UFL dataset](http://www.sal.ufl.edu/download.html)**:The UFL dataset, also known as the Two-Recording dataset, consists of two synchronously recorded tracks named "Data1" and "Data2," showing the same ENF fluctuations. Data1 was captured through a connection between a power outlet and a computer sound card, resulting in a high signal-to-noise ratio (SNR); in contrast, Data2 consists of actual voice recordings captured by an internal microphone in a laptop, which has a relatively lower SNR for the ENF signal. Both recordings were initially sampled at 44.1kHz, 16-bit, and were later resampled to 441Hz, preserving only the fundamental frequency and two higher harmonics of ENF. Despite its limited number of samples, the UFL dataset holds historical significance for ENF forensics research a decade ago, though its current reference value is limited due to the small sample size.
- **[ENF-WHU dataset](https://github.com/ghua-ac/ENF-WHU-Dataset)**：The ENF-WHU Dataset is currently one of the largest open-source ENF audio datasets, containing 130 real-world recordings with ENF signals and corresponding reference signals. The recording devices include voice recorders and smartphones, covering mainly quiet indoor scenes such as classrooms, laboratories, and libraries. Despite considering various scenarios and providing ENF reference signals, most recording environments have strong electrical network frequency signals and high signal-to-noise ratios, with a relatively uniform type of recording device. The lengths of the recordings are primarily between 5 to 16 minutes, with a lower degree of noise pollution. This limits its applicability in forensic research of short-duration ENF audio in environments with strong noise.

<table align="center">
  <tr>
    <th align="center">Dataset</th>
    <th align="center">File Size</th>
    <th align="center">Time Duration</th>
    <th align="center">Reference Signal</th>
    <th align="center">Recording Scene</th>
    <th align="center">Number of Devices</th>
    <th align="center">Application Scope</th>
  </tr>
  <tr>
    <td align="center">Carioca 1</td>
    <td align="center">100</td>
    <td align="center">19～35 s</td>
    <td align="center">✗</td>
    <td align="center">1</td>
    <td align="center">1</td>
    <td align="center">Temper detection only</td>
  </tr>
  <tr>
    <td align="center">UFL </td>
    <td align="center">2</td>
   <td align="center">30 min</td>
    <td align="center">✓</td>
    <td align="center">1</td>
    <td align="center">1</td>
    <td align="center">General testing</td>
  </tr>
  <tr>
    <td align="center">ENF-WHU</td>
    <td align="center">130</td>
    <td align="center">5～20 min</td>
    <td align="center">✓</td>
    <td align="center">6</td>
    <td align="center">4</td>
    <td align="center">General testing</td>
  </tr>
 <tr>
    <td align="center">Our ENF-SAH</td>
    <td align="center">40</td>
    <td align="center">2～10 min</td>
    <td align="center">✓ </td>
    <td align="center">7</td>
    <td align="center">6</td>
    <td align="center">General testing</td>
  </tr>
</table>

# Related works
- **ENF Detection**:
  >\[1] G. Hua, H. Liao, Q. Wang, H. Zhang and D. Ye, "Detection of Electric Network Frequency in Audio Recordings–From Theory to Practical Detectors," in IEEE Transactions on Information Forensics and Security, vol. 16, pp. 236-248, 2021.[link](https://ieeexplore.ieee.org/document/9143185)<br>
  >\[2] H. Liao, G. Hua and H. Zhang, "ENF Detection in Audio Recordings via Multi-Harmonic Combining," in IEEE Signal Processing Letters, vol. 28, pp. 1808-1812, 2021.[link](https://ieeexplore.ieee.org/document/9528023)<br>
- **ENF Enhancement**:
  >\[3] G. Hua and H. Zhang, "ENF Signal Enhancement in Audio Recordings," in IEEE Transactions on Information Forensics and Security, vol. 15, pp. 1868-1878, 2020.[link](https://ieeexplore.ieee.org/abstract/document/8894138)<br>
  >\[4] G. Hua, H. Liao, H. Zhang, D. Ye and J. Ma, "Robust ENF Estimation Based on Harmonic Enhancement and Maximum Weight Clique," in IEEE Transactions on Information Forensics and Security, vol. 16, pp. 3874-3887, 2021.[link](https://ieeexplore.ieee.org/abstract/document/9494518)<br>
- **ENF Matching**:  
  > \[5] G. Hua, "Error analysis of forensic ENF matching," in Proc. 2018 IEEE International Workshop on Information Forensics and Security (WIFS), pp. 1-7, Hong Kong, Dec. 2018. [link](https://ieeexplore.ieee.org/document/8630786)<br>
   > \[6] G. Hua, J. Goh, and V. L. L. Thing, “A dynamic matching algorithm for audio timestamp identification using the ENF criterion,” IEEE Trans. Inf. Forensics Security, vol. 9, no. 7, pp. 1045-1055, Jul. 2014. [link](https://ieeexplore.ieee.org/document/6808537)<br>


  
