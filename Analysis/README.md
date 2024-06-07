# Contextualizing Data

<p align="center">
<strong>PROPOSAL FOR A HYBRID RADIO-OPTICAL COMMUNICATION TECHNOLOGY TO IMPROVE INDOOR TELECOMMUNICATION SYSTEMS</strong>
</p>

<p align="center">
<strong>Juan David Navarro Restrepo</strong>
</p>

<p align="center">
<strong>Institución Universitaria ITM, Cl. 54A #30-01, Medellín, Colombia.</strong>
</p>

<p align="center">
<strong>e-mail:</strong> Juannavarro139070@correo.itm.edu.co
</p>

-----
Wireless communications face significant challenges in urban areas **[1]** due to signal degradation when radio waves travel through the air and encounter various obstacles in the wireless channel. Several propagation mechanisms negatively impact RF signals **[1]**, such as shadowing, deep fading, scattering, and atmospheric absorption, among others. Currently, since ubiquity is a necessary feature in telecommunications, connectivity with external antennas from indoor spaces and vice versa is the worst scenario when we want to stay connected while maintaining high quality of service. The problem will be even greater if there are many skyscrapers or large buildings in the surroundings. However, we have different technologies that can be very useful for guiding radio waves through the walls of buildings and then using some network infrastructure devices to distribute the signals to all interior spaces, even to the most inconceivable corner of the building, maintaining wireless connectivity.

Based on a thorough review of the state of the art, we identified the potential convergence **[2]**, **[3]**, **[4]** of RF and VLC (Visible Light Communication) systems as a promising solution capable of transmitting signals in the visible range of the spectrum, which does not require licenses for operation. On the other hand, the use of VLC allows covering two needs at the same time, such as indoor lighting and, of course, communication **[5]**, **[6]**. Another aspect that makes VLC technology attractive is that it allows a higher level of security in IT systems, as light does not penetrate walls or ceilings, and this same behavior of light solves a latent problem in horizontal property buildings, as these are saturated with WiFi signals. It is common to find not only the local wireless network but also the neighbors' networks at home. With VLC, wireless connectivity would be restricted to the spaces occupied by the respective user, thus avoiding interference in neighboring wireless networks. This hybrid approach also aims to improve the signal-to-noise ratio (SNR) in indoor environments.

In our study, we propose the technological integration of RF-VLC to improve indoor connectivity quality. Based on our measurements of a conventional RF signal across various levels and spaces of the University, we evidenced signal degradation as the conditions of the environment surrounding the signal capture system change, observing that the best SNR is obtained when the antenna is in a free environment (in this case), where it is exposed to electromagnetic waves radiated by different communication media. It is then through the integration of VLC systems for indoor signal distribution that we expect the SNR to be relatively uniform across the different spaces of the building.

This proposal opens the possibility of suggesting some recommendations for the installation of communication infrastructure in buildings to enable communication systems with higher SNR, implying connectivity with high-quality standards in any indoor space, ranging from places like homes to the most challenging scenarios such as underwater stations or underground mines.

***Keywords:*** *Atmospheric Absorption; Deep Fading; Scattering; RF; Shadowing, SNR; VLC.*

# **Laboratory Description**
For the SNR Laboratory, 9 samples of a conventional broadcast signal were taken in different spaces of the university, from the terrace to the basement 2; at a frequency tuned to 103.5 MHz using a USRP device connected to a laptop.

Technically, after data collection, this laboratory consists of a series of Python tool applications to handle, process, and visualize data, especially focused on the signal-to-noise ratio (SNR). Using libraries such as Pandas, Matplotlib, and Seaborn to perform data analysis tasks and generate graphics.

# **Consolidated Data**

| Place                             | Q1 {dB} | Mean {dB} | Q3 {dB} | IQR {dB} | Lower Outlier {dB} | Upper Outlier {dB} | Std Dev {dB} | Median {dB} | Mode {dB} | Variance {dB} |
|-----------------------------------|---------|-----------|---------|----------|--------------------|--------------------|--------------|-------------|-----------|----------------|
| Piso 1           | 24.0575 | 25.06790  | 26.0500 | 1.9925   | 22.07915           | 28.05665           | 1.560855     | 24.980      | 25.45     | 2.436269       |
| Piso 2           | 19.6975 | 20.33655  | 21.0025 | 1.3050   | 18.37905           | 22.29405           | 0.926371     | 20.280      | 20.17     | 0.858163       |
| Piso 3         | 19.1375 | 20.20470  | 21.6775 | 2.5400   | 16.39470           | 24.01470           | 1.845682     | 19.565      | 19.21     | 3.406542       |
| Piso 4          | 21.0275 | 21.92640  | 22.6325 | 1.6050   | 19.51890           | 24.33390           | 1.534590     | 21.920      | 21.15     | 2.354966       |
| Piso 5        | 24.5550 | 25.75220  | 26.6800 | 2.1250   | 22.56470           | 28.93970           | 1.758153     | 25.725      | 25.17     | 3.091103       |
| Piso 6       | 23.2450 | 24.14060  | 25.0225 | 1.7775   | 21.47435           | 26.80685           | 1.211611     | 24.170      | 22.10     | 1.468002       |
| Piso 6 Outdoor  | 24.0650 | 24.74790  | 25.5400 | 1.4750   | 22.53540           | 26.96040           | 1.255151     | 24.805      | 25.80     | 1.575404       |
| Sotano 1B        | 7.8750  | 11.50050  | 11.8150 | 3.9400   | 5.59050            | 17.41050           | 5.896987     | 8.565       | 8.26      | 34.774451      |
| Sotano 2E        | 4.6100  | 4.92600   | 5.1800  | 0.5700   | 4.07100            | 5.78100            | 0.342081     | 4.935       | 4.57      | 0.117019       |



# **References**
<div align="left">
<ul>
  <li>[1] A. G. Longley and J. M. Kreps, “OT Report 78-144: Radio Propagation in Urban Areas,” 1978.</li>
  <li>[2] Kungl. Tekniska högskolan and Institute of Electrical and Electronics Engineers, 2018 10th
International Conference on Advanced Infocomm Technology (ICAIT) : 12-15 August, 2018,
Stockholm, Sweden.</li>
  <li>[3] F. Defrance et al., “Structured Surface Design to Generate Any Beam Pattern at THz Frequencies.” [Online]. Available: https://www.researchgate.net/publication/335292622</li>
 <li>[4] L. Bravo Alvarez, S. Montejo-Sánchez, L. Rodríguez-López, C. Azurdia-Meza, and G. Saavedra, “A Review of Hybrid VLC/RF Networks: Features, Applications, and Future Directions,” Sensors, vol. 23, no. 17. Multidisciplinary Digital Publishing Institute (MDPI), Sep. 01, 2023. doi: 10.3390/s23177545.</li>
 <li>[5] ] M Pravin, “VLC BASED INDOOR BLIND NAVIGATION SYSTEM.”</li>
 <li>[6] T. Koonen, “Indoor Optical Wireless Systems: Technology, Trends, and Applications,” Journal of Lightwave Technology, vol. 36, no. 8, pp. 1459–1467, Apr. 2018, doi: 10.1109/JLT.2017.2787614.</li>
  <li>[7] E. Kreyszig, H. Kreyszig, and E. J. Norminton, “Advanced Engineering Mathematics,” 2011. [Online]. Available: www.ieee.org.</li>
</ul>
</div>


