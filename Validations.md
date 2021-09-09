# Validations module


### class Validations.Validations()
Bases: `object`


#### ValidationChecks( = <ValidationChecks.ValidationChecks object>)

#### alert(registry, input_df, column, validation)
Process all the alerts instructions in the validations. Generates a result dictionary which contain all the alerts instructions with their result of validations


* **Parameters**

    * **registry** – The registry with all the job parameters

    * **input_df** – input dataframe

    * **column** – Name of column in which alerts are need to be processed.

    * **validation** – Alert instructions of validation



* **Returns**

    Dictionary which contain all the alerts instructions with their result of validations.



#### fail(registry, input_df, column, validation)
Process all the fail instructions in the validations. Generates a result dictionary which contain all the fail instructions with their result of validations


* **Parameters**

    * **registry** – The registry with all the job parameters

    * **input_df** – Input dataframe

    * **column** – Name of column in which fail are need to be processed.

    * **validation** – Fail instructions of validation



* **Returns**

    Dictionary which contain all the fail instructions with their result of validations.



#### report(registry, input_df, column, validation)
Process all the report instructions in the validations. Generates a report and write it to a file with its respective file name which contain all the information of report instruction of validations

> Registry requirements: spark, bucket, environment, customer_slug, current_date,dataframe


* **Parameters**
    
    * **registry** – The registry with all the job parameters

    * **input_df** – Input dataframe

    * **column** – Name of column in which report are need to be processed.

    * **validation** – Report instructions of validation



* **Returns**

    Complete data of report of column which is used to process the report




