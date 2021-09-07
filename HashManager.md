# HashManager module


### class HashManager.HashManager()
Bases: `object`


#### AWSManager( = <AWSManager.AWSManager object>)

#### hash_sha256_string(string)
Function that will hash the given string using sha256 hashsing


* **Parameters**

    * **string** – A set of characters to hash



* **Returns**

    Returns a new hashed string



#### pii_hash_email(input_column, input_df, registry)
Hashes the teacher column


* **Parameters**
    
    * **input_column** – input_column will have the column which has to hashed and the hashed column name

    * **input_df** – input_column dataframe having all the data from input_column file

    * **registry** – The registry with all the job parameters



* **Returns**

    Returns the dataframe with hashed email column



#### pii_hash_student(input_column, input_df, registry)
Hashes the student column


* **Parameters**

    * **input_column** – input_column will have the column which has to hashed and the hashed column name

    * **input_df** – input_column dataframe having all the data from input_column file

    * **registry** – The registry with all the job parameters



* **Returns**

    Returns the dataframe with hashed student column



#### pii_hash_teacher(input_column, input_df, registry)
Hashes the teacher column


* **Parameters**

    * **input_column** – input_column will have the column which has to hashed and the hashed column name

    * **input_df** – input_column dataframe having all the data from input_column file

    * **registry** – The registry with all the job parameters



* **Returns**

    Returns the dataframe with hashed teacher column
