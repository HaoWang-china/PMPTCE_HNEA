
#################################
          code introduce
#################################



To run the program, just run PMPTCE_HNEA_main.m。PMPTCE_HNEA_main.m is the entrance of the program，set the relevant parameters according to the notes and then run.


PMPTCE_HNEA.m is the data processing program，The input data will be constructed into a matrix to perform operations.


lbfgsb.m is to solve the optimization problem in the program。The method in lbfgsb_wrapper.c will be used in this program，But lbfgsb_wrapper.c is a C language program，When matlab runs the c language, you need to edit the c language file to a file format supported by the system，Therefore, we compile the c language file in advance to support the matlab operation of windows system, Mac system and linux system.


load_network_heterogeneous.m is used to isomerize the matrix.


rwr.m is used to calculate restart random walk.


vector_embedding.m is used to calculate the output vector.


num.csv in network is the number corresponding to enzyme and compound.


the data.txt in the network is the data used when matlab extracts features.

