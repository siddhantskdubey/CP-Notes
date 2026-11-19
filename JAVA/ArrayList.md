from pathlib import Path
content = """# Java ArrayList Notes (1D & 2D)

## 1. Import
```java
import java.util.ArrayList;
```

## 2. 1D ArrayList

### Declaration
```java
ArrayList<Integer> list = new ArrayList<>();
```

### Add elements
```java
list.add(10);
list.add(20);
list.add(30);
```

### Access an element
```java
list.get(0); // element at index 0
```

### Update an element
```java
list.set(1, 50); // replace index 1 with 50
```

### Remove an element
```java
list.remove(0); // remove by index
list.remove(Integer.valueOf(20)); // remove by value
```

### Size
```java
list.size();
```

### Check if an element exists
```java
list.contains(10);
```

### Add another ArrayList
```java
ArrayList<Integer> list2 = new ArrayList<>();
list2.add(40);
list2.add(50);

list.addAll(list2);
```

### Print the list
```java
System.out.println(list);
```

### Traverse using a for loop
```java
for (int i = 0; i < list.size(); i++) {
    System.out.println(list.get(i));
}
```

### Traverse using an enhanced for loop
```java
for (int x : list) {
    System.out.println(x);
}
```

---

## 3. 2D ArrayList

### Declaration
```java
ArrayList<ArrayList<Integer>> matrix = new ArrayList<>();
```

### Add rows
```java
matrix.add(new ArrayList<>());
matrix.add(new ArrayList<>());
```

### Add elements to a row
```java
matrix.get(0).add(10);
matrix.get(0).add(20);

matrix.get(1).add(30);
matrix.get(1).add(40);
```

### Access an element
```java
matrix.get(0).get(1); // row 0, column 1
```

### Update an element
```java
matrix.get(0).set(1, 99); // row 0, column 1
```

### Remove an element
```java
matrix.get(0).remove(1); // remove from row 0, index 1
```

### Number of rows
```java
matrix.size();
```

### Number of elements in a row
```java
matrix.get(0).size();
```

### Traverse a 2D ArrayList
```java
for (int i = 0; i < matrix.size(); i++) {
    for (int j = 0; j < matrix.get(i).size(); j++) {
        System.out.print(matrix.get(i).get(j) + \" \");
    }
    System.out.println();
}
```

### Print the whole 2D ArrayList
```java
System.out.println(matrix);
```

---

## 4. Quick Reference

| Method / Syntax | Meaning |
|---|---|
| `add(x)` | Add element |
| `add(index, x)` | Insert at index |
| `get(index)` | Access element |
| `set(index, x)` | Update element |
| `remove(index)` | Remove by index |
| `remove(Integer.valueOf(x))` | Remove by value |
| `addAll(list2)` | Add all elements from another list |
| `size()` | Number of elements / rows |
| `contains(x)` | Check if element exists |
| `clear()` | Remove all elements |
| `isEmpty()` | Check whether empty |
"""
path = Path("/mnt/data/ArrayList_1D_2D_Basics.md")
path.write_text(content, encoding="utf-8")
print(f"Created: {path} | size: {path.stat().st_size} bytes")
