Here are the C programs with the comments removed:

### Task 1: Complete the Program to Fill an Array with Random Numbers

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

void fill_array(int ar[], int size);
void display_array(int ar[], int size);

int main() {
    int values[10];
    fill_array(values, 10);
    display_array(values, 10);
    return 0;
}

void fill_array(int ar[], int size) {
    srand(time(NULL));
    for (int i = 0; i < size; i++) {
        ar[i] = rand() % 1000;
    }
}

void display_array(int ar[], int size) {
    for (int i = 0; i < size; i++) {
        printf("%d ", ar[i]);
    }
    printf("\n");
}
```

### Task 2: Output of the Given Program

```c
#include <stdio.h>

int main() {
    int *ptr;
    int x;
    ptr = &x;
    *ptr = 0;
    printf("x = %d\n", x);
    printf("*ptr = %d\n", *ptr);
    *ptr += 5;
    printf("x = %d\n", x);
    printf("*ptr = %d\n", *ptr);
    (*ptr)++;
    printf("x = %d\n", x);
    printf("*ptr = %d\n", *ptr);
    return 0;
}
```

### Task 3: Add Two Numbers Using Pointers

```c
#include <stdio.h>

int main() {
    int a, b, sum;
    int *ptrA = &a, *ptrB = &b, *ptrSum = &sum;

    printf("Enter the first number: ");
    scanf("%d", ptrA);

    printf("Enter the second number: ");
    scanf("%d", ptrB);

    *ptrSum = *ptrA + *ptrB;

    printf("Sum = %d\n", *ptrSum);

    return 0;
}
```

### Task 4: Function to Double the Values Using Pointers

```c
#include <stdio.h>

void doubled(int *a, int *b, int *c);

int main() {
    int x = 5, y = 10, z = 15;
    doubled(&x, &y, &z);
    printf("Doubled values: x = %d, y = %d, z = %d\n", x, y, z);
    return 0;
}

void doubled(int *a, int *b, int *c) {
    *a *= 2;
    *b *= 2;
    *c *= 2;
}
```

### Task 5: Input and Print a String

```c
#include <stdio.h>

int main() {
    char str[100];

    printf("Input the string: ");
    fgets(str, sizeof(str), stdin);

    printf("The string you entered is: %s", str);

    return 0;
}
```

### Task 6: Find the Length of a String Using Library Functions

```c
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];

    printf("Input the string: ");
    fgets(str, sizeof(str), stdin);

    str[strcspn(str, "\n")] = '\0';

    printf("Length of the string is: %lu\n", strlen(str));

    return 0;
}
```

### Task 7: Compare Two Strings Using Library Functions

```c
#include <stdio.h>
#include <string.h>

int main() {
    char str1[100], str2[100];

    printf("Input the first string: ");
    fgets(str1, sizeof(str1), stdin);
    str1[strcspn(str1, "\n")] = '\0';

    printf("Input the second string: ");
    fgets(str2, sizeof(str2), stdin);
    str2[strcspn(str2, "\n")] = '\0';

    if (strcmp(str1, str2) == 0) {
        printf("Strings are equal.\n");
    } else {
        printf("Strings are not equal.\n");
    }

    return 0;
}
```

### Task 8: Concatenate Two Strings Using `strcat`

```c
#include <stdio.h>
#include <string.h>

int main() {
    char str1[100], str2[100];

    printf("Input the first string: ");
    fgets(str1, sizeof(str1), stdin);
    str1[strcspn(str1, "\n")] = '\0';

    printf("Input the second string: ");
    fgets(str2, sizeof(str2), stdin);
    str2[strcspn(str2, "\n")] = '\0';

    strcat(str1, str2);

    printf("After concatenation the string is: %s\n", str1);

    return 0;
}
```

These versions of the programs contain no comments and are ready for execution. Let me know if you need further assistance!
