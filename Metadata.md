# Metadata module


### class Metadata.Metadata()
Bases: `object`


#### registry( = <Registry.Registry object>)

#### run()
Executes the complete metadata job via managing multiple functions calls


* **Returns**

    True if the meta job executes successfully else exits the process with error message



#### setup(space, value=None, security=False)
Initial setup that will create a space in registry with some values and security if passed as arguments otherwise it will create a blank space with no security.


* **Parameters**

    * **space** – Name of the space

    * **value** – Value of the space

    * **security** – Security for the space
