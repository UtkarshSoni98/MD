# AWSManager module


### class AWSManager.AWSManager()
Bases: `object`


#### Utilities( = <Utilities.Utilities object>)

#### get_pii_secret_salt(registry)
Gets the secret salt from AWS Secrets Manager


* **Parameters**

    **registry** – The registry with all the job parameters



* **Returns**

    Returns the secret salt



#### s3_resource(registry)
Generates the s3 boto3 resource


* **Parameters**

    **registry** – The registry with all the job parameters



* **Returns**

    Returns the s3 boto3 resource



#### send_validation_result(body, output_path, registry, overall_fail_result='', overall_alert_result='')
Sends the result json using SNS


* **Parameters**

   **body** – Overall jobspec result

  **output_path** – The path where overall jobspec result are stored

  **registry** – The registry with all the job parameters

  **overall_fail_result** – Overall count of "Fail" in the fail resutlts.

   **overall_alert_result** – Overall count of "Fail" in alert results 



* **Returns**

    Returns the secret salt
