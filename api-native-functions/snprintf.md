## snprintf

Formatting output into unpacked string

Syntax: `snprintf(dest[],size=sizeof dest,const format[], {Fixed, }:...)`

* `dest[]` string array where to store formatted output
* `size` size of output array
* `const format[]` string array with formatting text
* `...` variable arguments used to feed into formatting text

Notes: This function works  in the same was as [printf](/api-native-functions/printf.md) with the exception that it stores the output into the destination. The size of the destination must be specified and usually is retrieved during runtime by leaving a standard value.

Example: `snprintf(dest,"My name is %s\r\n", ,name)`, stands for sizeof dest and it is filled automatically in runtime

See also: [printf](/api-native-functions/printf.md)

