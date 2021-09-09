# Executor module


### class Executor.Executor()
Bases: `object`


#### jobspec_executor(registry)
Executes the instructions of jobspec one after the other
> Registry requirements: jobspec_instructions


* **Parameters**

   * **registry** – Registry that the contains jobspec_instructions, along with all other job parameters



#### metadata_executor(registry)
Generates the metadata for each column based on the metadata instructions provided
> Registry requirements: metadata_csv_file, metadata_file, current_timestamp


* **Parameters**

   * **registry** – Registry that the contains metadata_csv_file, metadata_file, current_timestamp, along with all other job parameters
