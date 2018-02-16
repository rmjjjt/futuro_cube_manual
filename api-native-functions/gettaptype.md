# GetTapType 

Decision between side, top and bottom tap 

Syntax: `res=GetTapType(topside_wi)` 

* `topside_wi` walker or index which is used for information: tells which side points towards top 

Returns: One of the following results is returned: 

* 0: no decision can be made, perhaps no side tap has been detected 
* 1: tap to gravity side has been detected 
* 2: tap to gravity top has been detected 
* 3: tap to gravity bottom has been detected 

Notes: This function same as [GetTapSide](/api-native-functions/gettapside.md) reads [Motion\(\)](/api-native-functions/motion.md) to retrieve pattern info. Then, it combines this motion pattern info with user input to decide which side is pointing up and returns type of gravity tap. 

Example: `res=GetTapType(GetCursor())`

