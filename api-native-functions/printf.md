# printf

Debug function for text output

Syntax: `printf(const format[], Fixed, _:...`)

* `const` format\[\] array with formatting text
* `...` variable arguments used to feed into formatting text

Notes: This function works similar as standard printf function, only there is just a subset of format specifiers:

* `%s` inserts a string that can be either packed or unpacked
* `%d` signed integer number
* `%x` hexadecimal number
* `%X` hexadecimal number
* `%c` character

Example:

* `printf("%s\r\n",data)`
* `printf("%s\r\n",data)`
* `printf("this is %d, this is text %s\r\n",number, data)`
* `printf("0x%08x\r\n",hexnumber)`

See also: [snprintf](/api-native-functions/snprintf.md)

