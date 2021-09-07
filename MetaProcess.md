# MetaProcess module


### class MetaProcess.MetaProcess()
Bases: `object`


#### AWSManager( = <AWSManager.AWSManager object>)

#### FileManager( = <FileManager.FileManager object>)

#### JSONManager( = <JSONManager.JSONManager object>)

#### Utilities( = <Utilities.Utilities object>)

#### postProcess(registry)
Postprocess the metadata files i.e. writing the result data to the files,preparing and writing json data and sending notification of meta job process via aws or local


* **Parameters**

    **registry** – The registry with all the job parameters



#### preProcess(registry)
Preprocess the input files of metadata i.e create spaces in registry,read the file, clean the file


* **Parameters**

    **registry** – The registry with all the job parameters
