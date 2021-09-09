# HashManager module


### class HashManager.HashManager()
Bases: `object`


#### AWSManager( = <AWSManager.AWSManager object>)

#### hash_sha256_string(string)
Hashes the given string using sha256 hashing


* **Parameters**

   * **string** – A set of characters to hash



* **Returns**

    A new hashed string



#### pii_hash_email(input_dictionary, dataframe, registry)
Hashes the email column
> Registry requirements: bucket, pii_hash_prefix


* **Parameters**

    * **input_dictionary** – A dictionary with the column name which has to hashed and the new hashed column name

    * **dataframe** – Dataframe which contains all the data in a tabular format

    * **registry** – Registry that contains the bucket, pii_hash_prefix, along with all other job parameters



* **Returns**

    Dataframe with the hashed email column



#### pii_hash_student(input_dictionary, dataframe, registry)
Hashes the student column
> Registry requirements: bucket, pii_hash_prefix


* **Parameters**
    
    * **input_dictionary** – A dictionary with the column name which has to hashed and the new hashed column name

    * **dataframe** – Dataframe which contains all the data in a tabular format

    * **registry** – Registry that contains the bucket, pii_hash_prefix, along with all other job parameters



* **Returns**

    Dataframe with the hashed student column



#### pii_hash_teacher(input_dictionary, dataframe, registry)
Hashes the teacher column
> Registry requirements: bucket, pii_hash_prefix


* **Parameters**

    * **input_dictionary** – A dictionary with the column name which has to hashed and the new hashed column name

    * **dataframe** – Dataframe which contains all the data in a tabular format

    * **registry** – Registry that contains the bucket, pii_hash_prefix, along with all other job parameters



* **Returns**

    Dataframe with the hashed teacher column
