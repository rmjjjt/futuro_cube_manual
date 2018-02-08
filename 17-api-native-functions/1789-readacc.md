# 17.89 ReadAcc

Retrieves accelerometer game data

Syntax: `ReadAcc(data[3],past=5)`

* `data` 3 cell size vector for storing acc data 
* `past` how deep in acc buffer reach into history &lt;0...50&gt;

Notes: When there is any motion like tap etc., it is much better to take data before this even happened, because they reflect the situation when the user wanted to do an action. Recommended and standard value is 4 - that means data is 32 ms old.

Example:

* `ReadAcc(data)`, reads 32 ms old acceleration data 
* `ReadAcc(data,0)`, reads newest acceleration data 

See also: [GetCursor](/17-api-native-functions/1790-getcursor.md)

