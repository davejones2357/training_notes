#Array Name / index swapping

```
#include <stdio.h>

int main() {    
    char mystr[26] = "awopbabaloobopawopbamboom";
    mystr[5] = '!';
    printf("%c\n", mystr[5] );
    printf("%c\n", 5[mystr] );
    
    mystr[35] = '!';
    printf("%c\n", mystr[35] );
    printf("%c\n", 35[mystr] );    
}
```
Whilst the existence this quirk is no surprise to me, I did think C had bounds checking on arrays, I would expect 
```
mystr[35] = '!';
```
to generate a compile time error, wheras passing

```
nshow( mystr, 35);  
```

to
```
int nshow( const char* p, int i) {
    printf("%c\n", p[i] );
}
```
would not, as the array decays to a mere pointer. This has directed me down the rabbit hole of Annex K & address sanitisers. More to follow.

