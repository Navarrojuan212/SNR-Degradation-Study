# SNR Degradation Study

This repository contains a detailed study on the degradation of RF signal (Signal-to-Noise Ratio - SNR) at different levels within a university building. The study analyzes how conventional radio signals behave in indoor environments and proposes alternatives for the uniform distribution of RF signals in high-density urban environments.

## Repository Contents

```bash
tree SNR-Degradation-Study -I .git
```

```bash                                      
SNR-Degradation-Study
├── Analysis
│   └── README.md
├── Data
│   ├── Piso1_103_5MHz_SNR.xlsx
│   ├── Piso2_103_5MHz_SNR.xlsx
│   ├── Piso3_103_5MHz_SNR.xlsx
│   ├── Piso4_103_5MHz_SNR.xlsx
│   ├── Piso5_103_5MHz_SNR.xlsx
│   ├── Piso6_103_5MHz_SNR.xlsx
│   ├── Piso6_Outdoor_103_5MHz_SNR.xlsx
│   ├── README.md
│   ├── Sotano1_103_5MHz_SNR_B.csv
│   └── Sotano2_103_5MHz_SNR_E.csv
├── Images
│   ├── An_Urban_Broadcast_RadioTower.png
│   ├── histogram.png
│   ├── Histogram.png
│   ├── ITM.png
│   ├── scatterplot.png
│   ├── ScatterPlot.png
│   ├── violin_plot.png
│   └── ViolinPlot.png
├── main.py
├── pu.sh
├── README.md
├── requirements.txt
└── scripts
    ├── histogram.py
    ├── __pycache__
    │   ├── data_analysis1.cpython-312.pyc
    │   ├── data_analysis.cpython-312.pyc
    │   ├── histogram1.cpython-312.pyc
    │   ├── histogram.cpython-312.pyc
    │   ├── scatterplot.cpython-312.pyc
    │   ├── statistics.cpython-312.pyc
    │   └── violinplot.cpython-312.pyc
    ├── scatterplot.py
    ├── statistics.py
    └── violinplot.py

6 directories, 34 files

```

## Prerequisites
> [!Warning]
> Make sure you have Python 3 or higher installed on your system. Also, install the required dependencies by running the following command:


## How to Run the Project
### Clone the repository 
```bash
git clone https://github.com/Navarrojuan212/SNR-Degradation-Study
```
```bash
cd SNR-Degradation-Study
```
### Install the dependencies
```bash
pip install -r requirements.txt
```

### Run the analysis
This will process the data in the Data folder and generate the corresponding images in the Images folder. 
```bash
python3 main.py
```

## Study Proposal
The aim of this study is to:

- Analyze the degradation of RF signals at different levels within a university building, from the sixth-floor terrace to the second basement.
- Propose alternatives for the uniform distribution of RF signals in high-density urban environments.
- Visualize the collected data through histograms, scatter plots, and violin plots to gain a detailed understanding of signal behavior in indoor environments.

## Project Structure
- `Data`: Includes .xlsx and .csv files containing SNR data collected from different floors and basements of the building.
- `Images`: Contains generated visualizations such as histograms, scatter plots, and violin plots.
- `scripts`: Includes specific scripts for each type of visualization and statistical analysis:
  - `histogram.py`: Generates histograms.
  - `scatterplot.py`: Generates scatter plots.
  - `statistics.py`: Performs statistical analyses.
  - `violinplot.py`: Generates violin plots.

>[!NOTE]
>For more details on specific analyses and the interpretation of results, refer to the `README.md` file in the Analysis folder.

## Contributions
Contributions are welcome. Please open an issue or a pull request to discuss any changes you would like to make.

