# Azure-Databricks-Synapse-Spark-Pipeline
Data pipeline using Azure Data Factory, Lake gen2, Databricks, Spark and Synapse Analytics

 -- WHEN USING AZURE ENVIRONMENT REMEMBER TO HIT THE PUBLISH BUTTOM AFTER EVERY CHANGE YOU'D LIKE TO MAKE -- 


Raw data >> Data Ingestion (Azure data Factory) >> Data Lake (Azure Lake Gen 2) >> Transformation (AzureDataBricks, Spark) >> Analysis (Azure Synapse Analytics) ::

~ Assuming we've already successfully signed into Azure with an account

Step 1. #The Data Setup#  >>  Create a container inside a storage account in Azure portal:

![image](https://github.com/EduAFernandes/Azure-Databricks-Synapse-Spark-Pipeline/assets/78389579/91fbf664-330b-4eaf-a4ff-eb7bd172eaee)


Step 2. Create Data Factory instance and proceed to load each table into raw-data previously create:

![image](https://github.com/EduAFernandes/Azure-Databricks-Synapse-Spark-Pipeline/assets/78389579/c813b0f9-3352-49e9-b784-c2507548fe9b)

Step 3. Create Databricks instance, then create a new compute and boot up a new notebook link it with the new compute cluster and proceed to pull data from raw-data directory (make sure to give authorization for databricks to access containers) :

![image](https://github.com/EduAFernandes/Azure-Databricks-Synapse-Spark-Pipeline/assets/78389579/1efba0bf-3bc3-4efc-8579-4fa73af670ba)



Step 4. Run data transformation sequences and load them back to data lake transformed-data:

![image](https://github.com/EduAFernandes/Azure-Databricks-Synapse-Spark-Pipeline/assets/78389579/83e6c713-2fb5-447e-8a5a-1b027267dc21)

![image](https://github.com/EduAFernandes/Azure-Databricks-Synapse-Spark-Pipeline/assets/78389579/3d74be32-3c70-444b-80f3-90f718fedef7)



Step 5. Start up Synapse Analytics new instance and load all the tables from transformed-data container:

![image](https://github.com/EduAFernandes/Azure-Databricks-Synapse-Spark-Pipeline/assets/78389579/0c0e69c4-603e-473f-ae4a-7820a77c4fea)


Step 6. Query tables to make sure everything has been loaded, then proceed to create relationships and metrics:

![image](https://github.com/EduAFernandes/Azure-Databricks-Synapse-Spark-Pipeline/assets/78389579/5d654abf-0029-4a78-b570-70f2e1795b87)

![image](https://github.com/EduAFernandes/Azure-Databricks-Synapse-Spark-Pipeline/assets/78389579/73d3d1be-ffc7-43b6-a871-8900e05723c6)







