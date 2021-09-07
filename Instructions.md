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
Gets the list of add column instruction from the current instruction and based on the given default value and datatype it
will add new column to the dataframe filled with default value and if the instruction don’t have any default value or datatype for the
new column it will fill the new column with null values in dataframe.

    Example Instruction:
    
    [ “new_column_1” : {}, “new_column_2”: { default : Some_Value, datatype : string } ]


* **Parameters**

    **registry** – Registry that contains the current instructions, dataframes and all other job parameter’s.



#### drop_columns(registry)
Gets list of all the column from the given instruction and drops them from the dataframe .

    Example Instruction:
    
    [ Column_1, Column_2 ]
    

* **Parameters**

    **registry** – Registry that contains the current instructions, dataframes and all other job parameter’s.



#### input_files(registry)
Reads the input files based on the given locations in instruction and stores them in registry in a seperate
space. It also perfoms unions between the files which has an attribute of union. Space where these input
files are stored contains list of dataframes in which the first dataframe is unioned with others in case of
Union property and resultant dataframe updated with first dataframe. It will also maintain a varibales space
in registry which contains all the necessary required variables.

    Example Instruction:
     
     { “File1.csv” : {
    “base” : “intermediate”, ”required_input_columns” : None, ”is_unioned” : True } , “File2.csv” : { “base” :
    “intermediate” , ” is_unioned ”: True }}

>
* **Parameters**

    **registry** -  Registry that contains the current instructions and all other job parameter’s.



#### joins(registry)
Function that perfom the specific type of join operations between the dataframes based on the given instructions.

    Example Instruction:
    
    {
    "from" : "table2.raw_ethnicity",
    "to" : "table1.raw_ethnicity",
    "type" : "left"
    }


* **Parameters**

    **registry** - Registry that contains the current instructions, dataframes and all other job parameter’s.



#### output_file(registry)
Reads the instructions i.e output file name, output columns, directory etc from the current instructions and
generate an output file of the same type which is given in the instructions. If output directory is specified
in the instructions then it will generate the file in the given directory otherwise default directory is
used. It will also process the the overall results of validations and all other instructions and prepare’s a
json for the results which contains all the informations regarding the current jobspec along with results.
These results and json are also conveyed to the user through the email, for emails environment should not be
dev.

    Example Instructions:
    
    {
    “student_enrollments_ut.csv” : { “base” : “pii” , “output_columns” : [ “school_id”, “student_id”, “table3.grades” ]
    }

> 
* **Parameters**

    **registry** -   Registry that contains the current instructions, dataframes, results and all other job parameter’s.



#### pii_hash_prefix(registry)
Function that will add the hashing key in the registry from the instructions.

    Example Instruction:

    * kyjf - Hashing key


* **Parameters**

    **registry** - Registry that contains the current instructions and all other job parameter’s.



#### rename_columns(registry)
Gets the rename column instruction from the current instruction i.e old column name and new column name and changes the name of old olumn to to the new name in the given dataframe.

    Example Instruction:
    { “old_column_name” : “new_column_name”, “old_column_name_2” : “new_column_name_2” }


* **Parameters**

    **registry** – Registry that contains the current instructions, dataframes and all other job parameter’s.



#### transformations(registry)
Gets all the transformations instructions such as date_to_string, hashing, removing duplicate etc. from the current
instruction and based on the given transformation it will transform the given dataframe

    Example Instruction:
    
    {“date_to_string”: {“entry_date”: { “entry_date_new”: “ddMMyyyy” }}, “deduplicate” : “all”}
    

* **Parameters**

    **registry** – Registry that contains the current instructions, dataframes and all other job parameter’s.



#### validations(registry)
Gets the Validations instructions such as column name and type of validation to perform on column like null
values, datatype checks, generating reports i.e count of some columns etc. from the current instruction. It
will validate the column based on the conditions and update the results in the respective validations such as
alerts, fails and reports. Complete results are maintained in the registry in the space with name same as
instruction name.

    Example Instruction:
    
    {
    student_id : { alert : [ is_null, is_not_unique ] } ,
    primary_enrollment : { fail : [ is_not_boolean] },
    school_id : { report: { count_of_school_id : SELECT COUNT(\*) as result from table1 } }
    }


* **Parameters**

    **registry** -  Registry that contains the current instructions, results space and all other job parameter’s.
