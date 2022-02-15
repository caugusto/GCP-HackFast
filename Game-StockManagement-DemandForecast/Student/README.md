<b>Building and visualizing demand forecast predictions using Datastream, BigQuery ML and Looker</b>

This document shows you how to  replicate and process operational data from an Oracle database into Google Cloud in real time. The tutorial also demonstrates how to forecast future demand, and how to visualize this data as it arrives. 
This tutorial is intended for data engineers and analysts who want to utilize their operational data. It assumes that you’re familiar with writing SQL queries and UDF functions.

The tutorial uses a fictitious retail store, FastFresh, to help demonstrate the concepts it describes. This store specializes in selling fresh produce, and wants to minimize food waste and optimize their stock levels across all stores.  You use fictitious sales transactions from FastFresh as the operational data in the tutorial..



The preceding diagram showcases the flow of operational data through Google Cloud:
- Incoming data from an Oracle source is captured and replicated into Cloud Storage via Datastream. 
- This data is processed and enriched by Dataflow templates, and is then sent to BigQuery.
- BigQuery ML is used to forecast demand for your data, which is then visualized in Looker.

Third party disclaimer:  Customers are responsible for procuring licenses for the Oracle workloads they choose to run on Google Cloud, and customers are responsible for complying with those licenses. Google does not provide licenses for Oracle workloads.
------
Objectives 
Learn how to replicate and process data from Oracle into BigQuery in real time
Learn how to run demand forecasting against  data that has been replicated and processed from Oracle in BigQuery
Learn how to visualize forecasted demand and operational data in real time in Looker.
Costs
This tutorial uses the following billable components of Google Cloud:
Datastream
Cloud Storage
Pub/Sub
Dataflow 
BigQuery (Including BQML)
Looker
Compute Engine (if installing the sample Oracle XE Docker on compute)
Use the Pricing Calculator to generate a cost estimate based on your projected usage.
