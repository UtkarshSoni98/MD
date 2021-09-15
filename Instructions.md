# Instructions module


### class Instructions.Instructions()
Bases: `object`


#### AWSManager( = <AWSManager.AWSManager object>)

#### FileManager( = <FileManager.FileManager object>)

#### HashManager( = <HashManager.HashManager object>)

#### JSONManager( = <JSONManager.JSONManager object>)

#### Transformation( = <Transformation.Transformation object>)

#### Utilities( = <Utilities.Utilities object>)

#### ValidationChecks( = <ValidationChecks.ValidationChecks object>)

#### Validations( = <Validations.Validations object>)

#### add_columns(registry)
This also doesn’t replaces dollar signs enclosed in curly braces,
to avoid nested math environments, such as

```
Example Instruction:
  rename_columns:
    old_column_name: new_column_name
    old_column_name_2: new_column_name_2
```


#### drop_columns(registry)
Drops the list of columns from the dataframe
Registry requirements: current_instruction, Dataframe

Example Instruction:

    drop_columns:


        * Column_1


        * Column_2


* **Parameters**

    **registry** – 
    * Registry that contains the current instructions, dataframes and all other job parameters




#### duplicate_columns(registry)
Duplicates the given input columns with a new name
Registry requirements: current_instruction, Dataframe

Example Instruction:

    duplicate_columns:

        existing_column_1: duplicate_column_1
        existing_column_2: duplicate_column_2


* **Parameters**

    **registry** – 
    * Registry that contains the current instructions, dataframes and all other job parameters




#### input_files(registry)
Reads the input files from the base into dataframes, checks for the required input columns, adds aliases to each dataframe and performs unions
Registry requirements: current_instruction

Example Instruction:

    input_files:

        File1.csv:

            base: intermediate
            required_input_columns:

            > 
            > * column1


            > * column2

            is_unioned: TRUE

        File2.csv:

            is_unioned: TRUE


* **Parameters**

    **registry** – 
    * Registry that contains the current instructions and all other job parameters




#### joins(registry)
Performs specific type of join operation on the provided dataframes and columns
Registry requirements: current_instruction, dataframe

Example Instruction:

    joins:
    -

    > from: table2.raw_ethnicity
    > to: table1.raw_ethnicity
    > type: left


    * from: table3.location
    to: table1.location
    type: left


* **Parameters**

    **registry** – 
    * Registry that contains the current_instruction, dataframe, along with all the other job parameters




#### output_files(registry)
Selects the output columns and stores the data to the output file in the base specified
Note: source_file generates a column with input file name in the output file

> If set to false, doesnt generate the column
> Default or if set to true, generates the column

Registry requirements: current_instruction, dataframe, overall result, bucket, environment,
customer_slug, current_date, job_spec_path

Example Instruction:

    output_files:

        output_file_1.csv:

            output_columns:


                * column_1


                * column_2


                * column_3

        output_file_2.csv:

            base: pii
            source_file: FALSE
            output_columns:

            > 
            > * column_1_uuid


            > * column_2_uuid


* **Parameters**

    **registry** – 
    * Registry that contains the current_instruction, dataframe, overall result, bucket, environment, customer_slug, current_date, job_spec_path, along with all the other job parameters




#### pii_hash_prefix(registry)
Uses this prefix while performing hash transformations
Registry requirements: current_instruction

Example Instruction:

    pii_hash_prefix: kyjf


* **Parameters**

    **registry** – 
    * Registry that contains the current_instruction, along with all the other job parameters




#### rename_columns(registry)
Renames the list of columns in the dataframe
Registry requirements: current_instruction, Dataframe

```
`Example Instruction:
        rename_columns:
                \- old_column_name: new_column_name
                \- old_column_name_2: new_column_name_2`
```


* **Parameters**

    **registry** – 
    * Registry that contains the current instructions, dataframes and all other job parameters




#### transformations(registry)
Performs the transformation instructions such as converting date to string, converting string to date, hashing, removing duplicates, anonymizing dates and when otherwise conditions
Note: If default value or datatype are not provided, adds a new column with null values
Registry requirements: current_instruction, Dataframe

Example Instruction:

    transformations:

        date_to_string:


            * entry_date:
            - entry_date_new: ddMMyyyy

        deduplicate: all


* **Parameters**

    **registry** – 
    * Registry that contains the current instructions, dataframes and all other job parameters




#### validations(registry)
Performs the validation instructions such as checking null values, checking if column is of datatype integer, generating reports with resultset of SQL queries
There are 3 types of validations:

> 
> 1. Alert - If this type of validation fails, then the count is displayed in the SNS


> 2. Fail - If this type of validation fails, then the overall status of the job is set to fail and displayed in the SNS


> 3. Report - Generates the resultset of various SQL queries and stores to separate files in s3

Registry requirements: current_instruction, Dataframe, Spark

Example Instruction:

    validations__pre:

        student_id:

            alert:


                * is_null

            fail:


                * is_not_unique

            report:

                count_of_student_id__pre: |

                    SELECT

                        COUNT(\*) as result

                    from

                        table1


* **Parameters**

    **registry** – 
    * Registry that contains the current instructions, dataframes and all other job parameters



```
```
