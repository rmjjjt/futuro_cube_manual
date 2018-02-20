# StoreVariable 

Stores given array as named variable

Syntax: `StoreVariable(name[], arr[], size = sizeof arr)`

* `name` name of the registered variable
* `arr[]` array af data to be stored
* `size` size of the array, maximum is 501 cells

Notes: Variable is stored into non-volatile memory over buffer in RAM. As long as
the script is using the same one variable, it can store it as many times as needed.
Write into non-volatile memory is performed when a different variable is used
or if the cube is switched off. One script should not use more than one
variable. If it does, the number of writing to non-volatile memory is limited
to 5 per 5secs and a total limit of 20 per script.

Example: `StoreVariable(’’my variable name’’, data)` stores data as named variable

See also: [RegisterVariable](/api-native-functions/registervariable.md), [LoadVariable](/api-native-functions/loadvariable.md)