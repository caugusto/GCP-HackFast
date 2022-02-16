

# Challenge 1: Prepare your environment 

home – previous challenge – next challenge 


## Introduction

Now that you have created and installed the necessary technologies, you are now tasked with preparing the environment. In this challenge, you will create all necessary resources within your Google Cloud project so that  


##  \
Steps



1. Gain access to sample data in cloud shell 
    1. In Cloud Shell, clone the GitHub tutorial repository located [here](https://github.com/caugusto/datastream-bqml-looker-tutorial.git), which contains the scripts and utilities that you use in this hack 
    2. Extract the comma delimited file containing sample transactions to be loaded into oracle:

        ```
        bunzip2 datastream-bqml-looker-tutorial/sample_data/oracle_data.csv.bz2
        ```


2. Create a sample Oracle XE 11 g docker instance on Compute Engine 
    3. While connected to the shell, change the directory to `build_docker`
    4. Execute `build_orcl.sh `using the following command: 

        ```
        ./build_orcl.sh
        ```



        This script does the following: 

        *   Creates a new Google Cloud Compute instance
        *   Configures an Oracle 11 g XE docker container 
        *   Pre-loads the fastfresh schema and the Datastream prerequisites 
3. In Cloud Shell define the following environment variables: 
    5. PROJECT\_NAME = 
    6. PROJECT\_ID = 
    7. PROJECT\_NUMBER = 
    8. BUCKET\_NAME = 

    This will set variables for the entire project and make it easier to run commands throughout the hack 

4. Create Cloud Storage bucket to store your replicated data named `$BUCKET_NAME `


```
		Hack Now! 

```



5. Configure your bucket to send notifications about object changes to a Pub/Sub topic. 
    9. Create a new Pub/Sub topic called <code>oracle_retail<em>. </em></code>This will send notifications about object changes in your bucket to the following Pub/Sub.

        <em>Hack now! You can find information to hack this task here: https://cloud.google.com/storage/docs/reporting-changes#enabling</em>

    10. Create a new Pub/Sub subscription that receives messages which are sent to the  `oracle_retail` topic. 

        _Hack now!_

    11. Documentation for creating and subscribing to Pub/Sub topics can be found here
6. Create a BigQuery dataset named `retail` and assign the BigQuery Admin role to your Compute Engine service account. 


## You can move on if: 

1.

2.


## Resources for this challenge:

A little stuck? Not sure how to proceed or complete a step? Here are some helpful resources and documentation 
