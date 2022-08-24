# C - Best Practices

## Pointers
* The `*` goes with the variable, not the type - `char *s, *t, *u`.
* The `malloc` command (`calloc` can be used as well) is used to allocate space on the heap for a variable, so that the reference is not destroyed when scope is left  - `char* var1 = malloc(sizeof(char) * numChars)`.
* Allocating space for a double pointer - `char** var1 = malloc(sizeof(char*) * numRows)`
  * `for (size_t i = 0; i < numRows; ++i) { var1[i] = malloc(sizeof(var1[0] * numColumns)) }`
* The `free` command deallocates space provided for a pointer.
* Passing by reference - (Initialize variable) `Struct var1`
  * (Declare function) `getFunction(Struct *var)`
  * (Use function, passing by reference) `getFunction(&var1)`
* Always keep a reference to the length of arrays.
