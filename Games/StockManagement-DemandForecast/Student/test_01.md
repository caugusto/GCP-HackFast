
# Challenge 1: Prepare your environment 

home – previous challenge – next challenge 


## Introduction

Now that you have created and installed the necessary technologies, you are now tasked with preparing the environment. In this challenge, you will create all necessary resources within your Google Cloud project so that  


## Steps



1. Gain access to sample data in cloud shell 
    1. In Cloud Shell, clone the GitHub tutorial repository located [here](https://github.com/caugusto/datastream-bqml-looker-tutorial.git), which contains the scripts and utilities that you use in this hack 
    2. Extract the comma delimited file containing sample transactions to be loaded into oracle:

        ```
        bunzip2 datastream-bqml-looker-tutorial/sample_data/oracle_data.csv.bz2
        ```


2. Create a sample Oracle XE 11 g docker instance on Compute Engine 

    _Note: if you are using an existing Oracle Database as the change data capture source, skip this step _

    3. While connected to the shell, change the directory to `build_docker`
    4. Execute `build_orcl.sh `
        1. This script does the following: 
            1. Creates a new Google Cloud Compute instance
            2. Configures an Oracle 11 g XE docker container 
            3. Pre-loads the fastfresh schema and the Datastream prerequisites 
3. Configure your own Oracle Database source settings

    _Note: If you completed step 2 and are not using an existing oracle database, skip this step_

    5. Create the fastfresh schema and database objects. Script datastream-bqml-looker-tutorial/oracle\_ddl/fastfresh.sql can be used to help you automate this task.   
    6. Load the fastfresh.orders table. You can use file datastream-bqml-looker-tutorial/sample\_data/oracle\_data.csv to load the sample data and the SQL\*Loader template scripts from datastream-bqml-looker-tutorial/sqlloader.  
    7. Configure the source Oracle Database to satisfy the prerequisites required for Datastream. To learn more, see [Configure a self-hosted Oracle database] (https://cloud.google.com/datastream/docs/configure-your-source-oracle-database#[selfhostedoracle](https://cloud.google.com/datastream/docs/configure-your-source-oracle-database#selfhostedoracle)). "
4. In Cloud Shell define the following environment variables: 
    8. PROJECT\_NAME = 
    9. PROJECT\_ID = 
    10. PROJECT\_NUMBER = 
    11. BUCKET\_NAME = 

    This will set variables for the entire project and make it easier to run commands throughout the hack 

5. Create Cloud Storage bucket to store your replicated data named `$BUCKET_NAME `
6. Configure your bucket to send notifications about object changes to a Pub/Sub topic. 
    12. Create a new Pub/Sub topic called <code>oracle_retail<em>. </em></code>This will send notifications about object changes in your bucket to the following Pub/Sub<em> </em> 
    13. Create a new Pub/Sub subscription that receives messages which are sent to the  <code>oracle_retail</code> topic. 
7. Create a BigQuery dataset named <code>retail</code> and assign the BigQuery Admin role to your Compute Engine service account. 


## You can move on if: 

1.

2.


## Resources for this challenge:

A little stuck? Not sure how to proceed or complete a step? Here are some helpful resources and documentation 
