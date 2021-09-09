# AWSManager module


### class AWSManager.AWSManager()
Bases: `object`


#### Utilities( = <Utilities.Utilities object>)

#### get_pii_secret_salt(registry)
Gets the secret salt from AWS Secrets Manager using the ARN provided
> Registry requirements: pii_secret_salt


* **Parameters**

   * **registry** – Registry that contains the ARN for pii_secret_salt, along with all other job parameters



* **Returns**

    The secret salt



#### s3_resource(registry)
Generates the s3 boto3 resource
> Registry requirements: bucket


* **Parameters**

   * **registry** – Registry that contains the bucket, along with all other job parameters



* **Returns**

    The s3 boto3 resource object



#### send_validation_result(body, output_path, registry, overall_fail_result='', overall_alert_result='')
Sends the overall result of the jobspec using SNS
> Registry requirements: customer_slug, job_spec_path, sns_topic_arn, bucket


* **Parameters**

    * **body** – Result of jobspec in json format

    * **output_path** – The location of result JSON file

    * **registry** – Registry that contains the customer_slug, job_spec_path, sns_topic_arn, bucket, along with all other job parameters

    * **overall_fail_result** – Overall status of “Fail” in result of fail type of validations

    * **overall_alert_result** – Overall count of “Fail” in result of alert type of validations



* **Returns**

    True or False, used for unit testing



#### send_validation_result_metadata(body, registry)
Sends the overall result of the metadata using SNS

> Registry requirements: sns_topic_arn


* **Parameters**

    * **body** – Result of metadata job in json format

    * **registry** – Registry that contains the sns_topic_arn, along with all other job parameters
