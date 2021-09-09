# Transformation module


### class Transformation.Transformation()
Bases: `object`


#### add(new_column_name, default_value, datatype, dataframe)
Adds new columns to the dataframe


* **Parameters**

    * **new_column_name** – The name of the new column

    * **default_value** – The default value of the new column

    * **datatype** – The datatype of the new column

    * **dataframe** – Dataframe in which we need to add the new column.



* **Returns**

    Dataframe with newly added columns



#### anonymize_date(input_sub_instruction, dataframe)
Anonymizes dates by resetting each date as a new date with the first of the dates’ month


* **Parameters**

    * **input_sub_instruction** – input_sub_instruction will have the column which has to anonymized and the new column name

    * **dataframe** – Dataframe Dataframe in which we need to apply the transformation



* **Returns**

    Dataframe with anonymized dates



#### date_to_string(input_sub_instruction, dataframe)
Converts Date datatype to specified format that is given in the sub instruction


* **Parameters**
  
    * **input_sub_instruction** – input_sub_instruction will have the date column, new column name and format to which we need to convert the data

    * **dataframe** – Dataframe in which we need to perform the transformation



* **Returns**

    Dataframe with a new formatted column



#### deduplicate(input_sub_instruction, dataframe)
Drops the duplicate rows


* **Parameters**
   
    * **input_sub_instruction** – If input_sub_instruction = all, then all the columns duplicate values are dropped. If input_sub_instruction = [columns], then only the list of columns duplicate values are dropped

    * **dataframe** – Dataframe in which we need to apply the transformation.



* **Returns**

    Dataframe without duplicate rows



#### drop_col(column_name, dataframe)
Drops the columns from the dataframe


* **Parameters**

    * **column_name** – Name of the column to be dropped

    * **dataframe** – Dataframe that contains the column which is about to be dropped



* **Returns**

    Dataframe with all the columns except the dropped columns



#### rename(old_column_name, new_column_name, dataframe)
Renames the columns from the dataframe


* **Parameters**
  
    * **old_column_name** – The old name of the column

    * **new_column_name** – The new name of the column

    * **dataframe** – Dataframe that contains the column which is about to be renamed



* **Returns**

    Dataframe with updated column names.



#### split_columns(input_string)
Split the name based on the regex condition


* **Parameters**

    * **input_string** – A set of characters



* **Returns**

    Splitted string



#### string_to_date(input_sub_instruction, dataframe)
Converts String date to Date datatype


* **Parameters**
    
    * **input_sub_instruction** – input_sub_instruction will have the date column, new column name and format to which we need to convert the data

    * **dataframe** – Dataframe in which we need to perform the transformation



* **Returns**

    Dataframe with a new formatted column



#### strip_text(input_string)
Remove spaces at the beginning and at the end of the string


* **Parameters**

    * **input_string** – A set of characters



* **Returns**

    A copy of the string by removing both the leading and the trailing characters



#### when_otherwise(input_sub_instruction, dataframe)
Similars to a if-else condition. Based on the given condition it will create a new column and add a new value
to the column.


* **Parameters**
 
    * **input_sub_instruction** – input_sub_instruction will have the condition based on that new values are added to the new column..

    * **dataframe** – Dataframe in which we need to perform the transformation



* **Returns**

    Dataframe with a new column having the when otherwise statement implemented
