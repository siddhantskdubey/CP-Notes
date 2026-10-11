# 1D Arrays in Java

## 1. What is an Array?

An array is a collection of elements of the same data type stored in a single variable.

Example:
```java
int[] arr = {10, 20, 30, 40, 50};
```

Here, `arr` stores 5 integer values.

## 2. Important Points

- An array stores multiple values of the same data type.
- Array indexing starts from `0`.
- The size of an array is fixed after creation.
- We use square brackets `[]` to declare and access arrays.
- We use `.length` to find the size of an array.

Example:

```java
int[] arr = {10, 20, 30};

System.out.println(arr[0]); // 10
System.out.println(arr[1]); // 20
System.out.println(arr[2]); // 30
System.out.println(arr.length); // 3
```

## 3. Declaration and Initialization

### Method 1: Direct Initialization

```java
int[] arr = {10, 20, 30, 40};
```

### Method 2: Creating an Array of Fixed Size

```java
int[] arr = new int[5];
```

This creates an integer array of size 5.

Default values for an `int` array are `0`.

### Method 3: Assigning Values Using Indexes

```java
int[] arr = new int[3];

arr[0] = 10;
arr[1] = 20;
arr[2] = 30;
```

## 4. Accessing and Updating Elements

We can access an element using its index.

```java
int[] arr = {10, 20, 30};

System.out.println(arr[1]); // 20

arr[1] = 99;

System.out.println(arr[1]); // 99
```

Remember: `arr[1]` refers to the second element.

## 5. Taking Array Input Using Scanner

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        for (int i = 0; i < n; i++) {
            System.out.println(arr[i]);
        }

        sc.close();
    }
}
```

Example Input:
```text
5
10 20 30 40 50
```

Output:
```text
10
20
30
40
50
```

## 6. Traversing an Array

Traversing means visiting each element of an array.

```java
int[] arr = {10, 20, 30, 40};

for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
```

**Important:** Use `i < arr.length`, not `i <= arr.length`.

The last valid index is `arr.length - 1`.

## 7. Sum of Array Elements

```java
int[] arr = {10, 20, 30, 40};

int sum = 0;

for (int i = 0; i < arr.length; i++) {
    sum = sum + arr[i];
}

System.out.println(sum); // 100
```

We initialize `sum = 0` and add every element to it.

## 8. Find the Maximum Element

```java
int[] arr = {10, 50, 20, 80, 30};

int max = arr[0];

for (int i = 1; i < arr.length; i++) {
    if (arr[i] > max) {
        max = arr[i];
    }
}

System.out.println(max); // 80
```

We initialize `max` with the first element and compare the remaining elements.

## 9. Find the Minimum Element

```java
int[] arr = {10, 50, 20, 5, 30};

int min = arr[0];

for (int i = 1; i < arr.length; i++) {
    if (arr[i] < min) {
        min = arr[i];
    }
}

System.out.println(min); // 5
```

## 10. Count Even Numbers

```java
int[] arr = {1, 2, 4, 7, 8};

int count = 0;

for (int i = 0; i < arr.length; i++) {
    if (arr[i] % 2 == 0) {
        count++;
    }
}

System.out.println(count); // 3
```

The `%` operator gives the remainder. An even number has remainder `0` when divided by `2`.

## 11. Linear Search

Linear search checks each element until the target is found.

```java
int[] arr = {10, 20, 30, 40};

int target = 30;
int index = -1;

for (int i = 0; i < arr.length; i++) {
    if (arr[i] == target) {
        index = i;
        break;
    }
}

System.out.println(index); // 2
```

Here:
- `target` is the value we want to find.
- `index` stores the position where the value is found.
- `-1` means the value was not found.
- `break` stops the loop once the target is found.

## 12. Reverse Order Printing

```java
int[] arr = {10, 20, 30, 40, 50};

for (int i = arr.length - 1; i >= 0; i--) {
    System.out.println(arr[i]);
}
```

Output:
```text
50
40
30
20
10
```

This prints the array in reverse order without changing the original array.

## 13. Enhanced For Loop

The enhanced `for` loop is useful when we only need the values, not their indexes.

```java
int[] arr = {10, 20, 30};

for (int value : arr) {
    System.out.println(value);
}
```

Here, `value` takes each element of the array one by one.

## 14. Common Mistakes

1. Accessing an invalid index, such as `arr[arr.length]`.
2. Using `i <= arr.length` instead of `i < arr.length`.
3. Forgetting to initialize variables such as `sum`.
4. Confusing an index with an element's value.
5. Accessing `arr[0]` when the array is empty.
6. Forgetting that array indexes start from `0`.

## 15. Time Complexity

| Operation | Time Complexity |
|---|---|
| Access an element by index | O(1) |
| Traverse the array | O(n) |
| Calculate sum | O(n) |
| Find maximum or minimum | O(n) |
| Linear search | O(n) |

Here, `n` represents the number of elements.

- **O(1):** Constant time.
- **O(n):** Time grows approximately with the number of elements.

## 16. Practice Questions

Try solving these questions yourself:

1. Take `n` elements as input and print them.
2. Find the sum of all array elements.
3. Find the largest element.
4. Find the smallest element.
5. Count even and odd numbers.
6. Print the array in reverse order.
7. Search for a given number.
8. Count positive, negative, and zero elements.
9. Calculate the average of all elements.
10. Check whether an array is sorted in ascending order.

## Quick Revision

- Declaration: `int[] arr;`
- Creation: `new int[5]`
- Initialization: `int[] arr = {10, 20, 30};`
- Access: `arr[0]`
- Array size: `arr.length`
- Last index: `arr.length - 1`
- Loop condition: `i < arr.length`
- Arrays use zero-based indexing.
- Array size is fixed after creation.