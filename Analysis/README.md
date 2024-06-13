<p align="center">
<strong>HYBRID OPTICAL-RADIO COMMUNICATION TECHNOLOGIES TO IMPROVE INDOOR TELECOMMUNICATIONS SYSTEMS</strong>
</p>

<p align="center">
<strong>MSc(C) Juan David Navarro Restrepo</strong>
</p>

<p align="center">
<strong>Institución Universitaria ITM, Cl. 54A #30-01, Medellín, Colombia.</strong>
</p>

<p align="center">
<strong>e-mail:</strong> Juannavarro139070@correo.itm.edu.co
</p>

### Abstract
This work experimentally demonstrates, through statistical studies, the degradation of the SNR of a conventional broadcasting signal in urban environments. Additionally, it proposes a hybrid system that combines Radio Frequency and Visible Light Communication technologies to mitigate the non-uniformity of signals in indoor environments. The combination of these two technologies proves to be a promising solution for multiple application scenarios, such as the Internet of Things, Smart Cities, Sustainable Mining, Indoor Positioning, and others.

<p align="left">
<i><strong>Keywords:</strong> Atmospheric Absorption, RF, VLC, SNR, Scattering, Shadowing.</i>
</p>

## Introduction
The deployment of telecommunications networks faces significant challenges due to bandwidth management in wireless channels. Although the electromagnetic spectrum is theoretically infinite, only a portion of the radio spectrum is utilized, limiting its use to a few tens of GHz (See Table 1). Some bands must remain free for special uses, further restricting the spectrum available for commercial services [Hattab2019]. Additionally, the wireless channel is more limited compared to optical fiber and conductor cables due to physical phenomena such as cosmic noise [Bala2002], atmospheric noise [Reuveni2010], atmospheric absorption [Rashmeet2018], multipath interference [Lucas2017], partial reflection of electromagnetic waves in matter [Gaonkar2016], and diffraction [Tinin2020].

<div align="center">
    <img src="https://github.com/Navarrojuan212/SNR-Degradation-Study/blob/master/Images/An_Urban_Broadcast_RadioTower.png" alt="An Urban Broadcast RadioTower" width="600">
</div>

These phenomena force communication systems to preprocess signals to ensure bandwidth efficiency and maintain desired speeds under adverse conditions. However, meeting quality standards in an indoor wireless communication system is extremely complex in cities due to the shadowing of electromagnetic waves by buildings of varying heights. This makes it difficult for indoor receivers to have an equitable SNR among different users.

### Frequency Bands
| Band | Acronym | Frequency | Wavelength ($\lambda$) |
|------|---------|-----------|-----------------------|
| 4    | VLF     | 3 to 30 KHz      | 100 to 10 Km  |
| 5    | LF      | 30 to 300 KHz    | 10 to 1 Km    |
| 6    | MF      | 300 to 3000 KHz  | 1 Km to 100 m |
| 7    | HF      | 3 to 30 MHz      | 100 to 10 m   |
| 8    | VHF     | 30 to 300 MHz    | 10 to 1 m     |
| 9    | UHF     | 300 to 3000 MHz  | 1 m to 100 mm |
| 10   | SHF     | 3 to 30 GHz      | 100 to 10 mm  |
| 11   | EHF     | 30 to 300 GHz    | 10 to 1 mm    |
| 12   | THF     | 300 to 3000 GHz  | $<$ 1 mm      |

Data taken from the National Spectrum Agency - ANE.

----

To handle these challenges, Visible Light Communication - VLC is considered, a promising technology for indoor environments that can complement the deficiencies of RF systems [Mohsan2023]. In the following section, experimental results and statistical studies demonstrating signal degradation in urban environments will be presented, and a hybrid RF-VLC system will be proposed as a potential solution.

## Experimental Laboratory and Proposal of the RF-VLC Hybrid System
### Degradation of a Broadcasting Signal
For our study, we chose the free commercial frequency tuned to 103.5 MHz in the city of Medellín. We used a USRP (Universal Software Radio Peripheral) device along with AIRSPY software to perform the measurements. The selected locations for the measurements included the 1st to 5th floors of the university building, the terrace on the sixth floor, and the basements 1 and 2 of the Fraternidad campus at the ITM University Institution.

<div align="center">
    <img src="https://github.com/Navarrojuan212/SNR-Degradation-Study/blob/master/Images/ITM.png" alt="ITM" width="600">
</div>

### Statistic Analysis
Our object of study resulted in the consolidated data shown in Table 2, where a lower average can be observed on the lower levels compared to the upper levels. A more graphical view can be seen in the histogram in Figure 2.

The worst SNR values are observed in basements 1 and 2, indicating greater signal degradation in underground environments. In contrast, the terrace shows the best SNR values, reflecting better transmission conditions compared to the lower levels.

<div align="center">
    <img src="https://github.com/Navarrojuan212/SNR-Degradation-Study/blob/master/Images/Histogram.png" alt="Histogram" width="600">
</div>

In Figure 3, the scatter measurements show a clear downward trend in the basements, indicating significant signal degradation compared to the upper levels. While the upper floors present more stable SNR values, the basements suffer from greater interference and signal absorption, reflecting worse transmission conditions.

<div align="center">
    <img src="https://github.com/Navarrojuan212/SNR-Degradation-Study/blob/master/Images/ScatterPlot.png" alt="Scatter Plot" width="600">
</div>

We applied the Kruskal-Wallis test, a non-parametric test used to determine if there are significant differences between the medians of two or more independent groups. We obtained the following results:
- **Test statistic (H):** 1403.1096315801597
- **p-value:** $1.2036681993227117e-297$

Such a high H value indicates that at least one of the groups has a different median from the others. The extremely low p-value (practically zero) suggests that we reject the null hypothesis that the medians of all groups are equal.

**The Kruskal-Wallis Test** indicates that there are significant differences between the medians of the different groups, since the p-value is extremely low (practically zero), which leads us to reject the null hypothesis; indicating that at least one of the groups has a different median from the others.

The SNR statistical data presented in Table 3 support these findings. Basements 1 and 2 show the lowest means and medians (11.5 dB and 8.565 dB for Basement 1, 4.926 dB and 4.935 dB for Basement 2), as well as the highest variability (standard deviations of 5.896 and 0.342 respectively), indicating significant RF signal degradation in subway indoor environments. In contrast, the terrace has a higher mean and median (24.747 dB and 24.805 dB respectively) and lower variability, reflecting better transmission conditions in an outdoor environment.

### Consolidated SNR Statistical Data
| Place       | Q1      | Mean    | Q3      | IQR   | $\downarrow$ Outlier | $\uparrow$ Outlier | Std Dev | Median | Mode  | Variance |
|-------------|---------|---------|---------|-------|--------------|------------|---------|--------|-------|----------|
| Floor 1     | 24.057 | 25.06  | 26.050  | 1.992 | 22.079       | 28.056     | 1.560   | 24.98  | 25.45 | 2.436   |
| Floor 2     | 19.697 | 20.33  | 21.002  | 1.305 | 18.379       | 22.294     | 0.926   | 20.28  | 20.17 | 0.858    |
| Floor 3     | 19.137 | 20.20  | 21.677  | 2.540 | 16.394       | 24.014     | 1.845   | 19.56  | 19.21 | 3.406    |
| Floor 4     | 21.027 | 21.92   | 22.632  | 1.605 | 19.518       | 24.333     | 1.534   | 21.92  | 21.15 | 2.354    |
| Floor 5     | 24.555 | 25.75   | 26.680  | 2.125 | 22.564       | 28.939     | 1.758   | 25.72  | 25.17 | 3.091    |
| Floor 6     | 23.245 | 24.14   | 25.022  | 1.777 | 21.474       | 26.806     | 1.211   | 24.17  | 22.10 | 1.468    |
| Terrace 6   | 24.065  | 24.74  | 25.540  | 1.475 | 22.535       | 26.960     | 1.255   | 24.80 | 25.80 | 1.575 |
| Basement 1  | 7.875  | 11.50  | 11.815  | 3.940 | 5.590        | 17.410     | 5.896   | 8.56  | 8.26  | 34.774   |
| Basement 2  | 4.610   | 4.92  | 5.180   | 0.570 | 4.0710       | 5.781      | 0.342   | 4.93  | 4.57  | 0.117    |

---

Analysis of the SNR violin plot by source reveals significant differences in radio signal quality across the different levels of the university. The lower floors show narrower distributions and more consistent SNR values, indicating more stable transmission conditions. In contrast, the upper floors and terrace show greater variability,
probably due to external environmental factors. Basements, although with intermediate variability, tend to have lower SNR values, reflecting more unfavorable transmission conditions in these subway environments. These findings highlight how location and environment influence RF signal degradation, underscoring the need for specific strategies to improve uniform signal distribution in areas with diverse characteristics.

<div align="center">
    <img src="https://github.com/Navarrojuan212/SNR-Degradation-Study/blob/master/Images/ViolinPlot.png" alt="Violin Plot" width="600">
</div>

### Hybrid RF-VLC System

Broadcasting in densely populated urban environments faces critical challenges, as RF signals, although critical, are susceptible to interference, attenuation by physical obstacles and bandwidth saturation. These difficulties are compounded in indoor environments, where the presence of various structures and materials can cause shadow zones and significant SNR variations. 

To handle these challenges, the integration of Visible Light Communication (VLC) systems presents itself as a complementary and promising solution. VLC systems use LEDs as transmitters and photodetectors as receivers, operating in the visible spectrum, from 400 THz to 790 THz \cite{Talha2019}.

This technology is particularly suitable for indoor environments due to its ability to provide high bandwidth and lower interference compared to RF signals. In addition, research on VLC shows various applications and advantages, such as low power consumption and the use of free spectrum bands \cite{Khan2017} \cite{Matheus2019} \cite{Pathak2015}.

The convergence of RF and VLC systems has the potential to combine the strengths of both technologies, mitigating their individual limitations. RF signals offer wide coverage and penetration capability, essential for traversing obstacles and reaching more remote areas within buildings. VLC systems, on the other hand, can provide superior transmission speeds and efficient use of bandwidth, leveraging existing lighting infrastructure \cite{Almadani2020}.

The design of a hybrid RF-VLC system involves the integration of specific components that enable efficient and reliable communication. Using the heterodyning process \cite{Avdeyenko2023}, intermediate frequency radio signals can be matched to the frequency response of the LEDs, creating a system that combines the best of both worlds. This hybrid system would not only improve SNR in indoor environments, but also optimize the distribution of broadcast signals in densely populated urban areas.


### Conclusion

The convergence of RF and VLC technologies offers an innovative solution to overcome current barriers in indoor data transmission. This integration not only handles the challenges inherent in indoor communications, but also establishes a new paradigm in data transmission, providing more reliable and efficient communication in densely populated urban environments. This proposal promises to significantly improve the quality of telecommunications service, meeting the growing demands for speed and reliability in data transmission.

The SNR study demonstrated signal degradation in indoor environments and, based on the state of the art and our experience in VLC, we propose convergence as a promising solution to mitigate these problems and improve the quality of communications. Also, this technology is not only applicable to urban scenarios, but also to potential applications in IoT, smart cities, sustainable mining and subway communications, among others.

## References

<div align="left">
<ul>
  <li>[1] G. Hattab and D. Cabric, “Unlicensed spectrum sharing for massive
internet-of-things communications,” 2019.</li>
  <li>[2] Kungl. Tekniska högskolan and Institute of Electrical and Electronics Engineers, 2018 10th
International Conference on Advanced Infocomm Technology (ICAIT) : 12-15 August, 2018,
Stockholm, Sweden.</li>
  <li>[3] F. Defrance et al., “Structured Surface Design to Generate Any Beam Pattern at THz Frequencies.” [Online]. Available: https://www.researchgate.net/publication/335292622</li>
 <li>[4] L. Bravo Alvarez, S. Montejo-Sánchez, L. Rodríguez-López, C. Azurdia-Meza, and G. Saavedra, “A Review of Hybrid VLC/RF Networks: Features, Applications, and Future Directions,” Sensors, vol. 23, no. 17. Multidisciplinary Digital Publishing Institute (MDPI), Sep. 01, 2023. doi: 10.3390/s23177545.</li>
 <li>[5] ] M Pravin, “VLC BASED INDOOR BLIND NAVIGATION SYSTEM.”</li>
 <li>[6] T. Koonen, “Indoor Optical Wireless Systems: Technology, Trends, and Applications,” Journal of Lightwave Technology, vol. 36, no. 8, pp. 1459–1467, Apr. 2018, doi: 10.1109/JLT.2017.2787614.</li>
  <li>[7] E. Kreyszig, H. Kreyszig, and E. J. Norminton, “Advanced Engineering Mathematics,” 2011. [Online]. Available: www.ieee.org.</li>
  <li>[7] M. V. Tinin, “Role of diffraction effects in the formation
of a radio signal reflected from a randomly inhomogeneous
ionospheric layer,” https://doi.org/10.1117/12.2575532, vol.
11560, pp. 387–391, 11 2020. [Online]. Available: https:
//www.spiedigitallibrary.org/conference-proceedings-of-spie/11560/
115601Q/Role-of-diffraction-effects-in-the-formation-of-a-radio/10.
1117/12.2575532.short?tab=ArticleLink</li>
<li>[8] S. A. H. Mohsan, M. Sadiq, Y. Li, A. V. Shvetsov, S. V. Shvetsova,
and M. Shafiq, “Noma-based vlc systems: A comprehensive review,” 3
2023.</li>
<li>[9] T. Khani, H. Mangrio, and F. Umrani, “Performance analysis of vlc
system using commercially available components,” 2019.</li>
<li>[10] L. U. Khan, “Visible light communication: Applications, architecture,
standardization and research challenges,” pp. 78–88, 5 2017.</li>
<li>[11] L. E. M. Matheus, A. B. Vieira, L. F. Vieira, M. A. Vieira, and
O. Gnawali, “Visible light communication: Concepts, applications and challenges,” IEEE Communications Surveys and Tutorials, vol. 21, pp. 3204–3237, 10 2019.</li>
<li>[12] P. H. Pathak, X. Feng, P. Hu, and P. Mohapatra, “Visible light communication, networking, and sensing: A survey, potential and challenges,” pp. 2047–2077, 10 2015.</li>
<li>[13] Y. Almadani, D. Plets, S. Bastiaens, W. Joseph, M. Ijaz, Z. Ghassemlooy, and S. Rajbhandari, “Visible light communications for industrial applications—challenges and potentials,” pp. 1–38, 12 2020.</li>
<li>[14] G. Avdeyenko and I. Butko, “Impulse ultrawideband wireless communication system of the terahertz frequency band.” Institute of Electrical and Electronics Engineers Inc., 2023.</li>
</ul>
</div>










