# Sum of Digits of a Number

## Problem Statement

Given an integer `n`, find the sum of all its digits.

## Example

Input:
```text
1234
```

Output:
```text
10
```

Explanation:

```text
1 + 2 + 3 + 4 = 10
```

## Approach

1. Initialize `sum` as 0.
2. Extract the last digit using `% 10`.
3. Add the digit to `sum`.
4. Remove the last digit using `/ 10`.
5. Repeat until the number becomes 0.
6. Print the sum.

## Java Solution

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int sum = 0;

        while (n > 0) {
            int digit = n % 10;
            sum += digit;
            n /= 10;
        }

        System.out.println(sum);
    }
}
```

## Example Walkthrough

For `n = 1234`:

```text
digit = 4, sum = 4
digit = 3, sum = 7
digit = 2, sum = 9
digit = 1, sum = 10
```

Final Output:

```text
10
```

## Complexity Analysis

- **Time Complexity:** O(d)
- **Space Complexity:** O(1)

Where `d` is the number of digits in the given number.

## Tags

`Math` `Number Manipulation` `Basic Programming`
