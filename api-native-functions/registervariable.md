## RegisterVariable

Register named variable array to notify system to keep the variable active

Syntax: `RegisterVariable(var[])`

* `var` array that contains `VAR_MAGIC1`, `VAR_MAGIC2` and variable name - must be longer than 6 characters and shorter than 24 characters

Notes: Variable array must have the specified format in order to be correctly registered.
If the variable is not registered, it will be erased from the system and not used.
NOTE THAT ARRAY `var` MUST BE DEFINED IN THE GLOBAL NAME SPACE!!!
Otherwise the variable might be wrongly recognized in bytecode.

Example:

```
var[]=[VAR_MAGIC1,VAR_MAGIC2,’’my_variable_name’’]
RegisterVariable(var)
```

See also: [StoreVariable](/api-native-functions/storevariable.md), [LoadVariable](/api-native-functions/loadvariable.md)