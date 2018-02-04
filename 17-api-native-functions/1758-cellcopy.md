# 17.58 cellcopy 

Copying one array to another with using memmove 

Syntax: `cellcopy(dest[],source[],index=0,numcells=sizeof source,maxlength=sizeof dest)` 

* `dest` destination array 
* `source` source array 
* `index` index of cell in source from where to start copy 
* `numcells` number of cells to copy 
* `maxlength` size of the destination 

Notes: This function copies cells from one array to another. If the last 3 parameters are left as default, it performs a safe array to array copy. This function internally uses memmove, so arrays can overlap. 

Example: 

* `cellcopy(dest,source)` tries to copy the whole source to the max size of dest 
* `cellcopy(dest,source,2,10,_)` tries to copy the whole 10 cells from source at index 2, but up to a maximum of the size of dest. However, the size of source might be violated 
* `cellcopy(dest,source,_,10)` same as above, but from index 0 

See also: [cellset](/17-api-native-functions/1757-cellset.md)

