# Transformation module


### class Transformation.Transformation()
Bases: `object`


#### add(column1, column2, column3, input_df)
Adds new columns to the dataframe


* **Parameters**

    
    * **column1** – The name of the new column


    * **column2** – The default value of the new column


    * **column3** – The datatype of the new column


    * **input_df** – The input dataframe with all the data from input file



* **Returns**

    Returns the dataframe with newly added columns



#### anonymize_date(input_sub_instruction, dataframe)
Anonymizes dates by resetting each date as a new date with the first of the dates’ month


* **Parameters**

    
    * **input_sub_instruction** – input_sub_instruction will have the column which has to anonymised and the new column name


    * **dataframe** – input_sub_instruction dataframe having all the data from input_sub_instruction file



* **Returns**

    Returns the dataframe with anonymised dates



#### date_to_string(input_sub_instruction, dataframe)
Converts Date datatype to specified format in String


* **Parameters**

    
    * **input_sub_instruction** – input_sub_instruction will have the date column, new column name and to format


    * **dataframe** – input_sub_instruction dataframe having all the data from input_sub_instruction file



* **Return dataframe**

    Returns the dataframe with a new formatted column



#### deduplicate(input_sub_instruction, dataframe)
Drops the duplicate rows


* **Parameters**

    
    * **input_sub_instruction** – If input_sub_instruction = all, then all the columns duplicate values are dropped. If input_sub_instruction = [columns], then only the list of columns duplicate values are dropped


    * **dataframe** – input_sub_instruction dataframe having all the data from input_sub_instruction file



* **Returns**

    Returns the dataframe without duplicate rows



#### drop_col(column1, input_df)
Drops the columns from the dataframe


* **Parameters**

    
    * **column1** – Name of the column to be dropped


    * **input_df** – The input dataframe with all the data from input file



* **Returns**

    Returns the dataframe with all the columns from input file other than the dropped columns



#### rename(column1, column2, input_df)
Renames the columns from the dataframe


* **Parameters**

    
    * **column1** – The old name of the column


    * **column2** – The new name of the column


    * **input_df** – The input dataframe with all the data from input file



* **Returns**

    Returns the dataframe with newly renamed columns



#### split_columns(input)
Split the name based on the regex condition


* **Parameters**

    **input** – Input string



* **Returns**

    Splitted string



#### string_to_date(input_sub_instruction, dataframe)
Converts String datatype to Date datatype


* **Parameters**

    
    * **input_sub_instruction** – input_sub_instruction will have the string column (which has to be converted to date), new column name and from format


    * **dataframe** – input_sub_instruction dataframe having all the data from input_sub_instruction file



* **Returns**

    Returns the dataframe with a new date column



#### strip_text(input)
Remove spaces at the beginning and at the end of the string


* **Parameters**

    **input** – Input string



* **Returns**

    A copy of the string by removing both the leading and the trailing characters



#### when_otherwise(input_sub_instruction, dataframe)
Applies when otherwise logic on the column and creates a new column


* **Parameters**

    
    * **input_sub_instruction** – input_sub_instruction will have case statements of SQL


    * **dataframe** – input_sub_instruction dataframe having all the data from input_sub_instruction file



* **Returns**

    Returns the dataframe with a new column having the when otherwise statement implemented
