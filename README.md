# STCFS
Code: Incremental Feature selection for dynamic incomplete data using sub-tolerance relations

# Data Preparation:
(1) The data needs to be discretized, preferably using the MDLP method (for high classification accuracy). Save the data in the following format: test\dataset\lung.csv, with "xxx.csv" as the file name.
(2) Divide the entire dataset equally into 10 parts. Save the division information only in a file named "lung_randomDivide.csv", with "xxx_randomDivide.csv" as the file name. The first column indicates the nth division, and the second column indicates the mth part of the division (you only need to perform one division).
(3) Place the processed data file and the division file in a folder with the following naming convention: the name of the dataset, i.e., "xxx". It is recommended to create a folder named "test" on the desktop, then create a "dataset" folder inside it, and place the "xxx" folder in the "dataset" folder (because the result files will be outputted in the "test" folder).
Path (excluding the aforementioned folders):
For example, "C:\Users\A\Desktop\test\dataset\xxx" (remove "xxx" here, but keep the "\" separator).

Run the program in cmd: java -jar INEC_Experiment.jar parameters
The parameters are as follows:

The first parameter is set to the default "15%". You don't need to change or pay attention to it; it is just a file name.
The second parameter is the dataset name, "xxx".
The third parameter is the path. Example: java -jar INEC_Experiment.jar 15% xxx "C:\Users\A\Desktop\test\dataset\"
The resulting reduction output will appear in the "allDataReduce" folder under "xxx". The first row represents the column names, which includes all the features obtained from the reduction, as well as the last column for the label. This result can be directly used for classification.
