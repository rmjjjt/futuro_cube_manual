# Operator sizeof 

Many functions are using `sizeof` operator as one of the default values. 

The nice thing is that, for example, as in function `AdjArray()` is the size of the array `arr` given at run time. And this value is usually used as boundary inside the function. So, if it is really not needed, always leave this param out of the function and it will be passed correctly for you.

