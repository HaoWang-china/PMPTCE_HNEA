The system extracts features by constructing a heterogeneous network.First obtain the relationship data between compound and compound, compound and enzyme, enzyme and enzyme,construct their matrices separately.Then merge the matrix into a heterogeneous network through a heterogeneous method,The specific operation is shown in the figure below.Next, feature extraction is performed, and then based on the obtained metabolic path data,label each enzyme and compound, and then use a multi-label classification algorithm for analysis and processingThe system extracts features by constructing a heterogeneous network.First obtain the relationship data between compound and compound, compound and enzyme, enzyme and enzyme,construct their matrices separately.Then merge the matrix into a heterogeneous network through a heterogeneous method,The specific operation is shown in the figure below.Next, feature extraction is performed, and then based on the obtained metabolic path data,label each enzyme and compound, and then use a multi-label classification algorithm for analysis and processing.


![Image text](https://github.com/HaoWang-china/PMPTCE_HNEA/blob/master/flowChart.png)


To run this program, you need to install the MATLAB environment, and the MATLAB version needs to support the c language editor.Install the c language editor on your MATLAB, and then run it according to the instructions of the code.


After getting the tagged data, run it with meka,you can run the following command directly in the cmd window to get the result (under the C drive).


SMO order：
java -cp "./lib/*" meka.classifiers.multilabel.RAkEL -M 10 -k 10 -P 0 -N 0 -S 0 -verbosity 5 -t aVSDxiangliangdata_0.3_300.arff -x 10 -W weka.classifiers.functions.SMO -- -C 2.0 -L 0.001 -P 1.0E-12 -N 0 -V -1 -W 1 -K "weka.classifiers.functions.supportVector.PolyKernel -E 1.0 -C 250007" -calibrator "weka.classifiers.functions.Logistic -R 1.0E-8 -M -1 -num-decimal-places 4"> C:\SMO_result.txt


RF order：
java -cp "./lib/*" meka.classifiers.multilabel.RAkEL -M 10 -k 11 -P 0 -N 0 -S 0 -verbosity 5 -t aVSDxiangliangdata_0.3_300.arff  -x 10 -W weka.classifiers.trees.RandomForest -- -P 100 -I 80 -num-slots 1 -K 0 -M 1.0 -V 0.001 -S 1 > C:\RandomForest.txt
