# CollisionTest 

Test two arrays for collisions

Syntax: `CollisionTest(source1[],source2[],dest[],val=1;sizes1=sizeof source1,sizes2=sizeof source2,sized=sizeof dest)`

* `source1` first source array for collision test
* `source2` second source array for collision test
* `dest` destination array to store result from collision test
* `val` value indicating collision to be stored into destination array
* `sizes` sizes of all arrays that must be same

Notes: Destination array is cleared prior the operation. Collision is performed by easy condition `if (source1[index] && source2[index]) {dest[index]=val}`

Returns: returns number of collision points

Example: 

* `if (CollisionTest(a, b)) {....}` test number of collision points without using dest
* `if (CollisionTest(a, b, dest, WHITE)) {....}`, test number of collision points and stores WHITE into dest