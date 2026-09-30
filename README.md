# PRA2003-Bacterial-Kinematics-Project
### Student Info
### Name: Kristofer Katisko
### StudentID: 6433876

# 1.Question to answer:

## Does the bacteria and its mutant variant behave in the same way
 Is there symmetry within the original population and its mutant variation, if not, how much do the two populations deviate from eachother
## Can we calculate and simulate the bacteria's momentum in a 3 dimensional plane using graphing tools

## What are the standard deviations and uncertainties of each bacterial variant
  How do they measure on Gaussian probability curve

# 2.Implementation.
 Create a program that reads data from 10 downloaded files each running 500,000 experiments and show its movement within a 3 dimensional plane using functions containing 3 dimensional arrays displayed through plugins of python such as Numpy, Matplotlib. After this use the program to calculate the uncertainties within the different bacterial types (Mainly the bacteria's wild variant and its mutated variant. After this, analyse the data and calculate the standard deviations between the two types of bacteria for each bacteria. The code works by the user inputting the file they wish to use by copy-pasting its file path within the computers internal file storage

Sub sampling, Each data file AND particle id is used as its own sub sampling category to create a more precise uncertainty and mean. Using the 10 different files provided, each file was used in conjunction with the particle id selector within the code to create multiple sets of data which were then analysed
 Statistical uncertainty, Standard deviation divided by the square root of the entries in the sub sample
 Gaussian distribution curve used to measure how far (in terms of standard deviation) the values of the Mutant variant is from the Wild variant 




# 3. Dependencies and plugins
### Numpy (For calculations that would take long to code and to use Numpy arrays)
### Pandas (To creata dataframes which are easier to work with)
### Matplotlib (To plot the momenta of bacteria (week 5&6)

# 4. User guide
## 4.1 Installation requirements
| Category | Requirement |
| -------- | ----------- |
| Operating System | Windows 10/11, macOS, or Linux |
| Python Version | Python 3.13+ |
| RAM | Minimum 8 GB |
| Storage Space | 7–10 GB available disk space |
| Internet Connection | Required for installation and updates |
| Dependencies | Install via `pip install -r requirements.txt` |
### 4.2 Usage
 To begin, the user must download the above mentioned requirements and begin by entering the "Main code" section. After this the user will start the program and the program will request the user to input a file path from their computers directory. Following this the code will ask for the particle id from the user and will respond with the appropriate information based on the file provided

# 5.Results
### Abbreviations
MT = Mutant, WD = Wild, CD = Capsule deficient, DR = Drug resistant
| ID    | Name              | Mean  | Uncertainty | Standard Deviations |
| ------| ----------------- | ----- | ----------- | ------------------- |
| 211   | E-Coli WD         | 3.735 | 0.003       | 5.865               |
| -211  | E-Coli MT         | 3.743 | 0.003       | 5.854               |
| 321   | Bacillius WD      | 5.163 | 0.014       | 7.791               |
| -321  | Bacillius MT      | 5.143 | 0.014       | 7.618               |
| 2212  | Pseudomonas WD    | 6.399 | 0.024       | 8.955               |
| -2212 | Pseudomonas MT    | 6.401 | 0.023       | 8.792               |
| 3122  | Streptoccus WD    | 7.195 | 0.056       | 9.989               |
| -3122 | Streptoccus CD    | 7.075 | 0.055       | 9.965               |
| 3312  | Tuberculosis WD   | 8.335 | 0.177       | 9.753               |
| -3312 | DR Tuberculosis   | 7.716 | 0.169       | 9.757               |
| 3334  | Salmonella WD     | 9.923 | 1.00003     | 12.003              |
| -3334 | Salmonella MT     | 9.234 | 1.130       | 12.542              |
### Comparison of the organism pairs
| Organism Pair                          | Distribution             | 
| -------------------------------------- | ------------------------ |
| E-Coli WD and E-Coli MT                | 0.357σ below the mean    |
| Bacillius WD and Bacillius MT          | 0.456σ below the mean    |
| Pseudomonas WD and Pseudomonas MT      | 0.537σ above the mean    |
| Streptoccus WD and Streptoccus CD      | 0.55012σ above the mean  |
| Tuberculosis WD and DR Tuberculosis    | 0.622σ below the mean    |
| Salmonella WD and Salmonella MT        | 0.675σ above the mean    |
### Asymmetry for each bacterial pair
| Organism | WD Mean | MT/CD/DR Mean | Asymmetry (A) | Asymmetry (%) |
| -------- | ------- | ---------- | ------------- | ------------- |
| E-Coli | 3.735 | 3.743 | -0.00107 | -0.107% |
| Bacillus | 5.163 | 5.143 | 0.00194 | 0.194% |
| Pseudomonas | 6.399 | 6.401 | -0.00016 | -0.016% |
| Streptococcus | 7.195 | 7.075 | 0.00841 | 0.841% |
| Tuberculosis | 8.335 | 7.716 | 0.03856 | 3.856% |
| Salmonella | 9.923 | 9.234 | 0.03597 | 3.597% |


# 6.Discussion and limitations
 From the uncertainties we see that E coli and its mutant variant have the lowest uncertainty when compared to each-other and Salmonella and its mutant have the highest as seen from the their uncertainties and distributions on the Gaussian probability curve. This may be however to the significantly lower amount of data entries for salmonella compared to E-coli which had nearly 9 times more entries.
In each strain of bacteria we see that the Wild type is more common than the mutated type even if just slightly so. This however may change with time as a mutation becomes optimal for conditions causing an evolutionary step of the mutation becoming the normal wild type
To conclude we see that within the data provided, the wild strain of bacteria is more prevalent than the mutated type but the difference is quite small.
### 6.1 Limitations
The statistical uncertainties are taken into account in the programs calculations above but the systematic uncertainty is ignored as we are given no information on the measuring devices / practices used to obtain the values present in the datafiles
Another limitation is simply the time it took to analyse most of the files multiple times as for each bacterial ID (partly may be due to inefficiency in my code) the program had to scan through the entire document usually taking 3-5 minutes per run due to the sheer size of the file and low amount of RAM and processing power within my laptop
