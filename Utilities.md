# Utilities module


### class Utilities.Utilities()
Bases: `object`


#### clean_file_name(input_file)
Replaces special characters with underscores in the file name


* **Parameters**

    * **input_file** – The name of the input file



* **Returns**

    Returns the input file name with underscores



#### clean_null_dict(dictionary)
Cleans the null values in the dictionary


* **Parameters**

    * **dictionary** – Input dictionary



* **Returns**

    Cleaned dictionary



#### convert_df_to_dydf(dataframe, glueContext, DynamicFrame)
Converts dataframe to aws glue dynamic dataframe


* **Parameters**
    
    * **dataframe** – Input dataframe

    * **glueContext** –  Used for writing DynamicFrame

    * **DynamicFrame** – Dataframe used in Glue



* **Returns**

    Dynamic dataframe



#### csv_file_delimiter(input_file_location, registry)
Identifies the delimiter of the csv file
> Registry requirements: sparkcontext


* **Parameters**
    
    * **input_file_location** – The location of the input file

    * **registry** – The registry with all job parameters



* **Returns**

    Returns the delimiter of the input file



#### extract_day(date)
Extracts day from the date


* **Returns**

    Returns the day from the date



#### extract_month(date)
Extracts month from the date


* **Returns**

    Returns the month from the date



#### extract_year(date)
Extracts year from the date


* **Returns**

    Returns the year from the date



#### file_exists(path, registry)
Checks if file exists in the provided s3 path


* **Parameters**

    * **path** – The path of the input file to check if it exists or not

    * **registry** – The registry with all the job parameters



* **Returns**

    Returns True if file is found in the path, False if file is not found in the path



#### get_file_name(input_file)
Fetches the file name without the extension


* **Parameters**

   *  **input_file** – The name of the input file



* **Returns**

    Returns the input file name without the extension of the file



#### get_file_name_with_extension_without_path(input_file)
Fetches the file name with the extension


* **Parameters**

    * **input_file** – The name of the input file



* **Returns**

    Returns the input file name along with the extension of the file



#### get_file_name_without_extension_without_path(input_file)
Fetches the file name with the extension


* **Parameters**

    * **input_file** – The name of the input file



* **Returns**

    Returns the input file name along with the extension of the file



#### get_file_path(filename, input_directory, registry, file_exist_date=None)
Gets the complete file path of the file even if it is present back in time

> Registry requirements: bucket, environment, customer_slug, current_date, limit


* **Parameters**

    * **filename** – Name of the file

    * **input_directory** – Source directory where we need to search for the file

    * **registry** – The registry with all the job parameters

    * **file_exist_date** – Date in which file is need to be lookup



* **Returns**

    Path of the file if exist otherwise None



#### get_index_of_dict(dataframe, key)
Identifies the index of the dataframe based on the name or alias of the dataframe


* **Parameters**
  
    * **dataframe** – Dataframe object

    * **key** – Key whose index we need to find



* **Returns**

    Index of the key that is passed



#### get_proper_column_names(input_string)
Converts the provided string to lowercase, accepts only a-z0-9 and underscores


* **Parameters**

    * **input_string** – A set of characters



* **Returns**

    Returns the string with lowercase, a-z0-9 and underscores



#### is_dev_env(registry)
Checks whether the environment is local or aws

> Registry requirements: environment


* **Parameters**

    * **registry** – The registry with all the job parameters



* **Returns**

    True if environment is dev else False



#### now()
Fetches the current timestamp


* **Returns**

    Returns the current timestamp



#### output_columns(list_of_columns, dataframe, input_file_name, source_file_column, result)
Selects the output columns based on the instructions to process the output file


* **Parameters**
 
    * **list_of_columns** – list of columns for the output file

    * **dataframe** – Dataframe object

    * **input_file_name** – Name of the input file

    * **source_file_column** – Name of the output file that you want to generate

    * **result** – Overall results of job



* **Returns**

    Dataframe object only with selected columns



#### output_columns_order(dataframe)
Gets the order of the columns in the dataframe


* **Parameters**

    * **dataframe** – Dataframe object



* **Returns**

    Order of the columns in dataframe



#### source_file(dataframe, input_file_name)
Creates a new source file column in the dataframe with values as filename


* **Parameters**

    * **dataframe** – Dataframe object

    * **input_file_name** – File name that is to be added as value on the source column



* **Returns**

    Dataframe object with new column i.e source_file



#### tabulate_validation_result(result, output_file)
Function to display the validations results in a tabulated  format


* **Parameters**
   
    * **result** – Overall results after processing jobspec

    * **output_file** – Location of output file



* **Returns**

    Tabulated visuals of result space



#### today()
Fetches the current date


* **Returns**

    Returns the current date



#### union_dfs(dataframes)
Unions those dataframes which has the property of union


* **Parameters**

    * **dataframes** – Input list of dataframes



* **Returns**

    List of dataframes with unioned dataframe on first index
