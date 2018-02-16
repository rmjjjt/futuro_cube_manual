# LoadVariable 

Load data of named variable to given array

Syntax: `LoadVariable(name[], arr[], size = sizeof arr)`

* `name` name of the registered variable
* `arr[]` array af data to be stored
* `size` size of the array, maximum is 501 cells

Returns: returns 1 if variable has been loaded or 0 if there is a problem or variable does not yet exist

Example: `LoadVariable(’’my variable name’’, data)`, load named variable to data

See also: [RegisterVariable](/api-native-functions/registervariable.md), [StoreVariable](/api-native-functions/storevariable.md)