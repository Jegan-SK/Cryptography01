# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:

```
#include <stdio.h>
#include <string.h>
int main() {
    int k;
    char pt[100], ct[100], dt[100];
    int i, n;
    printf("Enter the plain text : ");
    scanf("%99s", pt);
    printf("Enter the key value : ");
    scanf("%d", &k);
    n = strlen(pt);
    for (i = 0; i < n; i++) {
        if (k > 0)
            ct[i] = pt[i] + k;
        else
            ct[i] = pt[i] - (-k);
    }
    ct[n] = '\0';
    printf("Cipher text : %s\n", ct);
    for (i = 0; i < n; i++) {
        if (k > 0)
            dt[i] = ct[i] - k;
        else
            dt[i] = ct[i] + (-k);
    }
    dt[n] = '\0';
    printf("Decrypted text : %s\n", dt);
    return 0;
}
```

## OUTPUT:

<img width="982" height="307" alt="image" src="https://github.com/user-attachments/assets/652e06bd-96cc-4f09-9621-9059ee3427a4" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
