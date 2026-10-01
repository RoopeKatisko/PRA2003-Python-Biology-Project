# PRA2003-Bacterial-Kinematics-Project
### Student Info
### Name: Kristofer Katisko
### StudentID: 6433876

# 1.Question(s) to answer:

### 1.1 Does the bacteria and its mutant variant behave in the same way
 Is there symmetry within the original population and its mutant variation, if not, how much do the two populations deviate from eachother
### 1.2 Can we calculate and simulate the bacteria's momentum in a 3 dimensional plane using graphing tools

### 1.3 What are the standard deviations and uncertainties of each bacterial variant
  How many standard deviations of difference does the wild variant have compared to its mutant counterpart

# 2.Implementation
 Create a program that reads data from 10 downloaded files each running 500,000 experiments and show its movement within a 3 dimensional plane using functions containing 3 dimensional arrays displayed through plugins of python such as Numpy, Matplotlib. After this use the program to calculate the uncertainties within the different bacterial types (Mainly the bacteria's wild variant and its mutated variant. After this, analyse the data and calculate the standard deviations between the two types of bacteria for each bacteria. The code works by the user inputting the file they wish to use by copy-pasting its file path within the computers internal file storage and from that analysing the code itself and providing the user with the values required.

Sub sampling, Each data file AND particle id is used as its own sub sampling category to create a more precise uncertainty and mean. Using the 10 different files provided, each file was used in conjunction with the particle id selector within the code to create multiple sets of data which were then analysed
 Statistical uncertainty, Standard deviation divided by the square root of the entries in the sub sample
 Gaussian distribution curve used to measure how far (in terms of standard deviation) the values of the Mutant variant is from the Wild variant 




# 3. Dependencies and plugins
### Numpy (For calculations that would take long to code, and to use Numpy arrays)
### Pandas (To create dataframes which are easier to work with)
### Matplotlib (To plot the momenta of bacteria (week 5&6))
### Scipy.statistics (For calculations of uncertainty and standard deviation)
### Os (For navigating and working with the files and folder used)

# 4. User guide
## 4.1 Installation requirements
| Category | Requirement |
| -------- | ----------- |
| Operating System | Windows 10/11, macOS, or Linux |
| Python Version | Python 3.13+ |
| RAM | Minimum 8 GB |
| Storage Space | 7–10 GB available disk space |
| Internet Connection | Required for installation and updates |
| Dependencies | Install via `pip install -r "Numpy/Pandas/Matplotlib/Scipy" |
### 4.2 Provided files
The files are split into 2. The first one, "File_Analyser_PRA2003_Project" is the first installation, and it runs 1 file at a time and gives the values of the bacterium within that file. It is however a bit rudimentary and does not provide assymetries or z scores.
The second file "Folder_Analyser_PRA2003_Project" is the final complete version of the project and it analyses an entire folder with all the wanted files within the folder
The last file provided is the readme file which contains all the information about the code, project and results.
### 4.3 Usage
 To begin, the user must download the above mentioned requirements and begin by entering the "Main code" section. After this the user will start the program and the program will request the user to input a file path from their computers directory. Following this the code will ask for the particle id from the user and will respond with the appropriate information based on the file provided
 For the folder analyser the user must input the Folder containing all the files that wish to be analysed. 

# 5.Results
### Abbreviations
MT = Mutant, WD = Wild, CD = Capsule deficient, DR = Drug resistant
| ID    | Name              | Mean  | Uncertainty | Standard Deviation  |
| ------| ----------------- | ----- | ----------- | ------------------- |
| 211   | E-Coli WD         | 3.646 | 0.003       | 5.377               |
| -211  | E-Coli MT         | 3.640 | 0.003       | 5.339               |
| 321   | Bacillius WD      | 4.940 | 0.013       | 7.092               |
| -321  | Bacillius MT      | 4.902 | 0.012       | 6.957               |
| 2212  | Pseudomonas WD    | 6.086 | 0.021       | 8.157               |
| -2212 | Pseudomonas MT    | 6.038 | 0.021       | 7.967               |
| 3122  | Streptoccus WD    | 6.773 | 0.051       | 9.104               |
| -3122 | Streptoccus CD    | 6.710 | 0.050       | 8.942               |
| 3312  | Tuberculosis WD   | 7.614 | 0.152       | 10.21               |
| -3312 | Tuberculosis DR | 7.543 | 0.152       | 10.17               |
| 3334  | Salmonella WD     | 8.696 | 0.970       | 11.338              |
| -3334 | Salmonella MT     | 8.851 | 1.023       | 11.763              |
### Comparison of the organism pairs
| Bacterial Pair                          | Distribution             | 
| -------------------------------------- | ------------------------ |
| E-Coli WD and E-Coli MT                | 1.12σ     |
| Bacillius WD and Bacillius MT          | 2.03σ     |
| Pseudomonas WD and Pseudomonas MT      | 1.42σ     |
| Streptoccus WD and Streptoccus CD      | 0.999σ  |
| Tuberculosis WD and DR Tuberculosis    | 0.868σ    |
| Salmonella WD and Salmonella MT        | 1.012σ    |
### Asymmetry for each bacterial pair
| Organism | WD Mean | MT/CD/DR Mean | Asymmetry (A) | Asymmetry (%) |
| -------- | ------- | ---------- | ------------- | ------------- |
| E-Coli   | 3.646 | 3.640 | 0.0007 | 0.07% |
| Bacillius | 4.940 | 4.902 | 0.0017 | 0.17% |
| Pseudomonas |6.086 | 6.038 | 0.0098 |0.98% |
| Streptococcus | 6.773 | 6.710 | 0.0075 | 0.75% |
| Tuberculosis | 7.614 | 7.543 | 0.008 | 0.8% |
| Salmonella | 8.696 | 8.851 | 0.011 | 1.1% |


# 6.Discussion and limitations
 From the uncertainties we see that E coli and its mutant variant have the lowest uncertainty  and Salmonella and its mutant have the highest as seen from the their uncertainties. This may be however to the significantly lower amount of data entries for salmonella compared to E-coli which had nearly 9 times more entries.
In each strain of bacteria we see that the Wild type is more common than the mutated type even if just slightly so. This however may change with time as a mutation becomes optimal for conditions causing an evolutionary step of the mutation becoming the normal wild type
For the standard deviations we see that most wild and mutant pairs fall well within 3 standard deviations of each other which Bacillius having the highest standard deviation from its mutant counterpart at 2.03 standard deviations.
Concerning the symmetry of bacterial strain, we find that Pseudomonas and Salmonella (and their respective mutant variants) are the most asymmetrical of bacterial pairs boasting a 1.1% and 0.98% difference.
To conclude we see that within the data provided, the wild strain of bacteria is more prevalent having a slightly higher mean than the mutated type but the difference is quite small.

### 6.1 Limitations
The statistical uncertainties are taken into account in the programs calculations above but the systematic uncertainty is ignored as we are given no information on the measuring devices / practices used to obtain the values present in the datafiles
Another limitation is simply the time it took to analyse most of the files multiple times as for each bacterial ID (partly may be due to inefficiency in my code) the program had to scan through the entire document usually taking 3-5 minutes per run due to the sheer size of the file and low amount of RAM and processing power within my laptop
