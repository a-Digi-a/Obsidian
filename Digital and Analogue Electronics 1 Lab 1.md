#electronics 


# Logic Gate Circuits
## 2 Input AND Gate

| A   | B   | F   | V (Actual Voltage) |
| --- | --- | --- |:------------------:|
| 0   | 0   | 0   |         0          |
| 0   | 1   | 0   |         0          |
| 1   | 0   | 0   |         0          |
| 1   | 1   | 1   |       4.09V        |
Behaved as expected
## 4 Input AND Gate

| A   | B   | C   | D   | F   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | 0   |
| 0   | 0   | 0   | 1   | 0   |
| 0   | 0   | 1   | 0   | 0   |
| 0   | 0   | 1   | 1   | 0   |
| 0   | 1   | 0   | 0   | 0   |
| 0   | 1   | 0   | 1   | 0   |
| 0   | 1   | 1   | 0   | 0   |
| 0   | 1   | 1   | 1   | 0   |
| 1   | 0   | 0   | 0   | 0   |
| 1   | 0   | 0   | 1   | 0   |
| 1   | 0   | 1   | 0   | 0   |
| 1   | 0   | 1   | 1   | 0   |
| 1   | 1   | 0   | 0   | 0   |
| 1   | 1   | 0   | 1   | 0   |
| 1   | 1   | 1   | 0   | 0   |
| 1   | 1   | 1   | 1   | 1   |
Behaved as expected
## 2 Input OR Gate


| A   | B   | F   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 1   |

Behaved as expected
## 2 Input NOR Gate

| A   | B   | F   |
| --- | --- | --- |
| 0   | 0   | 1   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 0   |

Behaved as expected
## 1 Input NOT Gate

| A   | F   |
| --- | --- |
| 0   | 1   |
| 1   | 0   |

Behaved as expected

## NAND Gate turned into AND
| A   | B   | F   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 1   |

Behaved as expected

## 2 Input NAND Gate (disconnecting this time)

| A   | B   | F   |
| --- | --- | --- |
| x   | x   | 1   |
| x   | 1   | 1   |
| 1   | x   | 1   |
| 1   | 1   | 0   |

- The outputs behave as expected

# Boolean Algebra

## Testing the Associative Law


| A   | B   | C   | Predicted F | Predicted G | F   | G   |
| --- | --- | --- | ----------- | ----------- | --- | --- |
| 0   | 0   | 0   | 0           | 0           | 0   | 0   |
| 0   | 0   | 1   | 0           | 0           | 0   | 0   |
| 0   | 1   | 0   | 0           | 0           | 0   | 0   |
| 0   | 1   | 1   | 0           | 0           | 0   | 0   |
| 1   | 0   | 0   | 0           | 0           | 0   | 0   |
| 1   | 0   | 1   | 0           | 0           | 0   | 0   |
| 1   | 1   | 0   | 0           | 0           | 0   | 0   |
| 1   | 1   | 1   | 1           | 1           | 1   | 1   |
![[Pasted image 20260928155301.png]]

F = (BC)A = ABC
G = (AB)C = ABC

Both F and G are the same, they are 3 way AND gates

## Testing the Distributive Law

| A   | B   | C   | Predicted F | Predicted G | F   | G   |
| --- | --- | --- | ----------- | ----------- | --- | --- |
| 0   | 0   | 0   | 0           | 0           | 0   | 0   |
| 0   | 0   | 1   | 0           | 0           | 0   | 0   |
| 0   | 1   | 0   | 0           | 0           | 0   | 0   |
| 0   | 1   | 1   | 0           | 0           | 0   | 0   |
| 1   | 0   | 0   | 0           | 0           | 0   | 0   |
| 1   | 0   | 1   | 1           | 1           | 1   | 1   |
| 1   | 1   | 0   | 1           | 1           | 1   | 1   |
| 1   | 1   | 1   | 1           | 1           | 1   | 1   |
![[Pasted image 20260928161212.png]]

F = (AC)+(AB) = A(B+C)
G = A(B+C)

# Boolean Equations


