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



#### prepare_result_for_json(result, output_file_path, manifest_file, input_file, registry)
Generates json dictionary for the jobspec results

> Registry requirements: environment, customer_slug, current_timestamp, job_spec_path


* **Parameters**
    
    * **result** – Complete results of validations

    * **output_file_path** – File path of generated file.

    * **manifest_file** – Json generated manifest

    * **input_file** – input file path

    * **registry** – The registry with all the job parameters



* **Returns**

    Json data with all the results.



#### prepare_result_for_json_metadata(action, status, current_timestamp, metadata_location, error_message)
Generates json dictionary for the metadata results


* **Parameters**

    * **action** – Complete status of metadata

    * **status** – Status of metadata job i.e passed or fail

    * **current_timestamp** – Time of execution

    * **metadata_location** – Filepath of metadata job results

    * **error_message** – Error message if metajob fails



* **Returns**

    Json data with all the results.
