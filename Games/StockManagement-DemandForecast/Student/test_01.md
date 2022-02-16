

# Challenge 1: Prepare your environment 

home – previous challenge – next challenge 


## Introduction

Now that you have created and installed the necessary technologies, you are now tasked with preparing the environment.


##  \
Steps



1. Gain access to sample data in cloud shell 
    1. In Cloud Shell, clone the GitHub tutorial repository located [here](https://github.com/caugusto/datastream-bqml-looker-tutorial.git), which contains the scripts and utilities that you use in this hack 
    2. Extract the comma delimited file containing sample transactions to be loaded into oracle:

        _bunzip2 datastream-bqml-looker-tutorial/sample\_data/oracle\_data.csv.bz2_

2. Create a sample Oracle XE 11 g docker instance on Compute Engine \*\*_Note: if you are using an existing Oracle Database as the change data capture source, skip this step _
    3. While connected to the shell, change the directory to `build_docker:`
    4. 

             
