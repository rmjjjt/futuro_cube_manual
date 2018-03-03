## DrawArray

Draw array to virtual canvas

Syntax: DrawArray(arr\[\],size=sizeof arr)

* `arr[]` source array
* `size` size of the array. Must be 54, otherwise exception is raised

Returns: Function always returns 0

Notes: This function draws user array to the virtual canvas. That means it uses all drawing procedures and preset drawing styles.

Example: `DrawArray(temp)`, draw array temp to canvas

See also: [SetDrawDefaults](/api-native-functions/setdrawdefaults.md), [SetDrawStyle](/api-native-functions/setdrawstyle.md)

