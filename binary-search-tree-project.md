# Project 4

**[7, 5, 1, 8, 3, 6, 0, 9, 4, 2]**

ilk gelen root olduguna gore root: 7 dir 

- 5 < 7 olduğu için
    - 7’nin soluna 5 eklenir.

- 1 < 7 ve 1 < 5 olduğu için
    - 5’in soluna 1 eklenir.

- 8 > 7 olduğu için
    - 7’nin sağına 8 eklenir.

- 3 < 7, 3 < 5, 3 > 1 olduğu için
    - 1’in sağına 3 eklenir.

- 6 < 7 ve 6 > 5 olduğu için
    - 5’in sağına 6 eklenir.

- 0 < 7, 0 < 5, 0 < 1 olduğu için
    - 1’in soluna 0 eklenir.

- 9 > 7 ve 9 > 8 olduğu için
    - 8’in sağına 9 eklenir.

- 4 < 7, 4 < 5, 4 > 1, 4 > 3 olduğu için
    - 3’ün sağına 4 eklenir.

- 2 < 7, 2 < 5, 2 > 1, 2 < 3 olduğu için
    - 3’ün soluna 2 eklenir.

```
        7
       / \
      5   8
     / \   \
    1   6   9
   / \
  0   3
     / \
    2   4
```
