A novel computational method, namely PMPTCE-HNEA, was proposed to predict metabolic pathway types of compounds and enzymes. To obtain informative features of compounds and enzymes, three heterogeneous networks containing above two objects were constructed and we generalized an existing network embedding algorithm, Mashup, to its heterogeneous network version. Such algorithm was termed as MashupH and applied on above three heterogeneous networks. The extracted compound and enzyme features were fed into RAndom k-labELsets (RAKEL) to construct the method. SVM or RF was employed as the base classification algorithm. Such method provided good performance and was superior to the previous method that adopted compound and enzyme features obtained by directly applying Mashup to the heterogeneous network. 


![Image text](https://github.com/HaoWang-china/PMPTCE_HNEA/blob/master/flowChart.png)


To run this program, you need to install the MATLAB environment, and the MATLAB version needs to support the c language editor. Install the c language editor on your MATLAB, and then run it according to the instructions of the code.


After getting the tagged data, run it with Meka, you can run the following command directly in the cmd window to obtain the result (under the C drive).

SMO order：

java -cp "./lib/*" meka.classifiers.multilabel.RAkEL -M 10 -k 10 -P 0 -N 0 -S 0 -verbosity 5 -t aVSDxiangliangdata_0.3_300.arff -x 10 -W weka.classifiers.functions.SMO -- -C 2.0 -L 0.001 -P 1.0E-12 -N 0 -V -1 -W 1 -K "weka.classifiers.functions.supportVector.PolyKernel -E 1.0 -C 250007" -calibrator "weka.classifiers.functions.Logistic -R 1.0E-8 -M -1 -num-decimal-places 4"> C:\SMO_result.txt


RF order：

java -cp "./lib/*" meka.classifiers.multilabel.RAkEL -M 10 -k 11 -P 0 -N 0 -S 0 -verbosity 5 -t aVSDxiangliangdata_0.3_300.arff  -x 10 -W weka.classifiers.trees.RandomForest -- -P 100 -I 80 -num-slots 1 -K 0 -M 1.0 -V 0.001 -S 1 > C:\RandomForest.txt
