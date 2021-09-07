# ValidationChecks module


### class ValidationChecks.ValidationChecks()
Bases: `object`


#### DD_is_greater_than(alert_result, df, column, value)

* **Parameters**

    
    * **alert_result** – 


    * **df** – 


    * **column** – 


    * **value** – 



* **Returns**

    


#### MM_is_greater_than(alert_result, df, column, value)

* **Parameters**

    
    * **alert_result** – 


    * **df** – 


    * **column** – 


    * **value** – 



* **Returns**

    


#### check_if_column_exists(dataframe, column)
Checks if column is present in the dataframe or not


* **Parameters**

    
    * **dataframe** – The input dataframe with all the data from input file


    * **column** – The column to be checked for its presence in the dataframe



* **Return True or False**

    Returns True if column exists, False if column doesnt exist



#### check_overall_fail_result(result)
Checks whether overall result is fail or pass


* **Parameters**

    **result** – Overall result i.e result after validation__pre and validation__post



* **Returns**

    Fail or Pass based on count of “Fail”



#### check_previous_dates(file_exists_path, filename, input_directory, registry)
Checks whether the given file is present back in time or not based on the limit


* **Parameters**

    
    * **file_exists_path** – Current file path


    * **filename** – Name of the file


    * **input_directory** – Source folder of the file


    * **registry** – The registry with all the job parameters



* **Returns**

    Path of the file if exist otherwise None



#### compare(\*args)

* **Parameters**

    **args** – 



* **Returns**

    


#### date_dd(alert_result, df, column, operator, value)
Compares the dd of the date with the value


* **Parameters**

    
    * **alert_result** – Result of each function


    * **df** – Dataframe containing the column on which the comparison should happen


    * **column** – Column on which the comparison should happen


    * **operator** – Different types of relational operators


    * **value** – Numeric value



* **Returns**

    Validation Status (Pass/ Fail)



#### date_difference(\*args)

* **Parameters**

    **args** – 



* **Returns**

    


#### date_mm(alert_result, df, column, operator, value)
Compares the mm of the date with the value


* **Parameters**

    
    * **alert_result** – result of each function


    * **df** – dataframe containing the column on which the comparison should happen


    * **column** – column on which the comparison should happen


    * **operator** – different types of relational operators


    * **value** – numeric value



* **Returns**

    Validation Status (Pass/ Fail)



#### if_result(alert_result, dataframe, column, value)

* **Parameters**

    
    * **alert_result** – 


    * **dataframe** – 


    * **column** – 


    * **value** – 



* **Returns**

    


#### is_boolean(df, column)
Checks if the datatype of the column is boolean


* **Parameters**

    
    * **df** – Dataframe containing the column


    * **column** – Column to be checked if the datatype is boolean



* **Returns**

    Returns Fail if column is of datatype boolean, Pass if column is not of datatype boolean



#### is_in_values(alert_result, df, column, values)
Checks if the values provided are present in the input column


* **Parameters**

    
    * **alert_result** – Result of each function


    * **df** – The input dataframe with all the data from input file


    * **column** – The column to check for in values



* **Returns**

    Returns Fail if column doesnt have provided values, Pass if column has provided values



#### is_integer(df, column)
Checks if the datatype of the column is integer


* **Parameters**

    
    * **df** – Dataframe containing the column


    * **column** – Column to be checked if the datatype is integer



* **Returns**

    Returns Fail if column is of datatype integer, Pass if column is not of datatype integer



#### is_not_boolean(df, column)
Checks if the datatype of the column is not boolean


* **Parameters**

    
    * **df** – Dataframe containing the column


    * **column** – Column to be checked if the datatype is not boolean



* **Returns**

    Returns Fail if column is not of datatype boolean, Pass if column is of datatype boolean



#### is_not_in_values(alert_result, df, column, values)
Checks if the values provided are not present in the input column


* **Parameters**

    
    * **alert_result** – Result of each function


    * **df** – The input dataframe with all the data from input file


    * **column** – The column to check for not in values



* **Returns**

    Returns Fail if column has provided values, Pass if column doesnt have provided values



#### is_not_integer(df, column)
Checks if the datatype of the column is not integer


* **Parameters**

    
    * **df** – Dataframe containing the column


    * **column** – Column to be checked if the datatype is not integer



* **Returns**

    Returns Fail if column is not of datatype integer, Pass if column is of datatype integer



#### is_not_null(df, column)
Checks if column has not null values in the data


* **Parameters**

    
    * **df** – The input dataframe with all the data from input file


    * **column** – The column to be checked for not null values



* **Returns**

    Returns Fail if column has not null values, Pass if column doesnt have not null values



#### is_not_unique(df, column)
Checks for unique values in the column


* **Parameters**

    
    * **df** – The input dataframe with all the data from input file


    * **column** – The column to be checked for unique values



* **Returns**

    Returns Fail if column has duplicate values, Pass if column has unique values



#### is_null(df, column)
Checks if column has null values in the data


* **Parameters**

    
    * **df** – The input dataframe with all the data from input file


    * **column** – The column to be checked for null values



* **Returns**

    Returns Fail if column has null values, Pass if column doesnt have null values



#### is_null_percentage(alert_result, df, column, value)
Checks for the percentage null values in comparison to the specified percentage


* **Parameters**

    
    * **alert_result** – Result of each function


    * **df** – The input dataframe with all the data from input file


    * **column** – The column to be checked for percentage of null values



* **Returns**

    Returns Fail if column does not satisfy the condition, Pass if column satisfies the condition



#### is_null_percentage_where(alert_result, df, column, value)

* **Parameters**

    
    * **alert_result** – 


    * **df** – 


    * **column** – 


    * **value** – 



* **Returns**

    


#### is_null_where_percentage(alert_result, df, column, value)

* **Parameters**

    
    * **alert_result** – 


    * **df** – 


    * **column** – 


    * **value** – 



* **Returns**

    


#### only_null_where(alert_result, df, column, value)

* **Parameters**

    
    * **alert_result** – 


    * **df** – 


    * **column** – 


    * **value** – 



* **Returns**

    


#### overall_alert_result_count(result)
Counts the total number of fails in alert of validation


* **Parameters**

    **result** – Overall result i.e result after validation__pre and validation__post



* **Returns**

    Total count of “Fail” in alert



#### required_input_columns(input, dataframe)
Checks whether the required_input_columns from jobspec are present in the input file dataframe or not


* **Parameters**

    **input** – List of the columns



* **Returns**

    Returns the dataframe with all the columns from input file
