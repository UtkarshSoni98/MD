# Registry module


### class Registry.Registry()
Bases: `object`


#### check_reserve(key)
Checks whether the key is reserved for registry or not


* **Parameters**

    **key** – Input Key for registry



* **Returns**

    True if the key is already reserved otherwise False



#### check_security_type(security)
Checks the datatype for security


* **Parameters**

    * **security** – Input value for setting the security.



* **Returns**

    True if the security value is of boolean datatype else False



#### clear(space)
Empty the given space


* **Parameters**

    * **space** – Name of the Space



#### create_space(space, value=None, security=False)
Creates the space in the registry


* **Parameters**

    * **space** – Name of the space to create in registry

    * **value** – Some value for the created space

    * **security** – Security of the space whether we need the space to be secure or not



#### delete(key, space=None)
Removes the key and value from the given space if it is not reserved


* **Parameters**

    * **key** – Name of the key

    * **space** – Name of the Space



#### get(key, space=None)
Gets the value of the key from the given space


* **Parameters**
  
    * **key** – Name of the key

    * **space** – Name of the Space



* **Returns**

    Value of the given key from given space



#### get_all(space=None)
Gets complete data from the given space


* **Parameters**

    * **space** – Name of the space



* **Returns**

    Dictionary of the complete data in the given space



#### get_reserved_keywords()
Get the reserved keywords from registry and returns a copy


* **Returns**

    Copy of the reserved keywords in the registry



#### is_secure(space)
Checks whether the given space is secured or not


* **Parameters**

    * **space** – Name of the space



* **Returns**

    True if the space is secured otherwise false



#### put(key, value, space=None)
Adds new data to the given space


* **Parameters**
  
    * **key** – Key of the data by which we can access later

    * **value** – Value of the data

    * **space** – Name of the space



* **Returns**

    True if the data is inserted in space otherwise error



#### set_security(space, security)
Sets the security of the space


* **Parameters**
  
    * **space** – Name of the space

    * **security** – Security of the space whether we need the space to be secure or not



#### set_space(space)
Sets the default space to the given space in registry


* **Parameters**

    * **space** – Name of the space
