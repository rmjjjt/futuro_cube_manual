## GetCursor

Retrieving of gravity cursor

Syntax: `cursor=GetCursor(past=4)`

* `past` tells how far back in data from accelerometer to go for cursor computation

Returns: This function returns walker on the spot that relates to gravity cursor with default orientation

Example:

* `cursor=GetCursor()`, standard cursor
* `cursor=GetCursor(0)`, cursor from newest data

See also: [ReadAcc](/api-native-functions/readacc.md)

