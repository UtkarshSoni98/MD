# MetaProcess module


### class MetaProcess.MetaProcess()
Bases: `object`


#### AWSManager( = <AWSManager.AWSManager object>)

#### FileManager( = <FileManager.FileManager object>)

#### JSONManager( = <JSONManager.JSONManager object>)

#### Utilities( = <Utilities.Utilities object>)

#### post_process(registry)
Post-processes the metadata files i.e. writing the result data to the files,preparing and writing json data and sending notification of meta job process via aws or local

> Registry requirements: metadata_input_csv_file, metadata_file, output_folder_path, glueContext, bucket, current_timestamp, input_file_name, input_folder_path, spark


* **Parameters**

   *  **registry** – The registry with all the job parameters



#### pre_process(registry)
Pre-processes the input files of metadata i.e create spaces in registry,read the file, clean the file and load the file in the registry.

> Registry requirements: bucket, input_folder_path, input_file_name, metadata_file_path, sparkcontext,


* **Parameters**

   *  **registry** – The registry with all the job parameters
