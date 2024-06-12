# half-Hourglass-Star-Pattern
The provided code generates a pattern that first creates a right-aligned decreasing triangle and then a left-aligned increasing triangle. The combined pattern creates an hourglass-like shape. Here is the code along with the explanation:

### Complete Code

```c
#include <stdio.h>

int main() {
    int i, j, n;
    printf("enter num= ");
    scanf("%d", &n);

    // Upper part of the hourglass (right-aligned decreasing triangle)
    for (i = 0; i < n - 1; i++) {
        for (j = 0; j < i; j++) {
            printf(" ");
        }
        for (; j < n; j++) {
            printf("*");
        }
        printf("\n");
    }

    // Lower part of the hourglass (left-aligned increasing triangle)
    for (i = 0; i < n; i++) {
        for (j = 0; j < n - i - 1; j++) {
            printf(" ");
        }
        for (; j < n; j++) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}
```

### Explanation:

1. **Input Handling:**
   - The user inputs the value `n`, which represents the number of rows in each part of the pattern.

2. **Upper Part (Right-Aligned Decreasing Triangle):**
   - The first `for` loop handles the upper part of the hourglass.
   - The inner loop for spaces `for (j = 0; j < i; j++)` prints increasing spaces for each row.
   - The inner loop for stars `for (; j < n; j++)` prints decreasing stars as the number of spaces increases.

3. **Lower Part (Left-Aligned Increasing Triangle):**
   - The second `for` loop handles the lower part of the hourglass.
   - The inner loop for spaces `for (j = 0; j < n - i - 1; j++)` prints decreasing spaces for each row.
   - The inner loop for stars `for (; j < n; j++)` prints increasing stars as the number of spaces decreases.

### Result:

If the user inputs `5`, the output will be:

```
*****
 ****
  ***
   **
    *
   **
  ***
 ****
*****
```

### Pattern Name

This pattern can be named the **"Hourglass Star Pattern"**. This name reflects the shape of the pattern, resembling an hourglass.
