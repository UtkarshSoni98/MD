# JSONManager module


### class JSONManager.JSONManager()
Bases: `object`


#### create_manifest(key, value, manifest_dict)
Add key and value in the json object


* **Parameters**
   
    * **key** – Key of dictionary

    * **value** – Value of key

    * **manifest_dict** – Json object



* **Returns**

    Json object with some key value pairs



#### prepare_result_for_json(result, output_file, manifest_file, input_file, registry)
Generates json dictionary for the jobspec results


* **Parameters**
 
    * **result** – Complete results of validations

    * **output_file** – File path of generated file.

    * **manifest_file** – Json generated manifest

    * **input_file** – Input file path

    * **registry** – The registry with all the job parameters



* **Returns**

    Json dictionary with complete status of jobspec.



#### prepare_result_for_json_metadata(action, status, current_timestamp, metadata_location, error_message)
Generates json dictionary for the metadata results


* **Parameters**

    * **action** – Complete status of metadata

    * **status** – Status of metadata job i.e passed or fail

    * **current_timestamp** – Time of execution

    * **metadata_location** – Filepath of metadata job results

    * **error_message** – Error message if metajob fails



* **Returns**

    Json dictionary with complete status of jobspec
