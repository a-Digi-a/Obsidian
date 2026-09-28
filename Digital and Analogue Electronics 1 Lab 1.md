#electronics 

# 2 Input AND Gate

| A   | B   | F   | V (Actual Voltage) |
| --- | --- | --- |:------------------:|
| 0   | 0   | 0   |         0          |
| 0   | 1   | 0   |         0          |
| 1   | 0   | 0   |         0          |
| 1   | 1   | 1   |       4.09V        |
Behaved as expected
# 4 Input AND Gate

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
# 2 Input OR Gate


| A   | B   | F   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 1   |

Behaved as expected
# 2 Input NOR Gate

| A   | B   | F   |
| --- | --- | --- |
| 0   | 0   | 1   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 0   |

Behaved as expected
# 1 Input NOT Gate

| A   | F   |
| --- | --- |
| 0   | 1   |
| 1   | 0   |

Behaved as expected

# NAND Gate turned into AND
| A   | B   | F   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 1   |

Behaved as expected

# NAND Gate turned into AND (disconnecting this time)

0 means disconnected, not going to ground*

| A   | B   | F   |
| --- | --- | --- |
| 0   | 0   | 1   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 1   |

- With both disconnected, th