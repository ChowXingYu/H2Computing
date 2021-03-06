# Tutorial 1B

- [Tutorial 1B](#tutorial-1b)
  - [Q1. Factory program](#q1-factory-program)
    - [(i) Decision table](#i-decision-table)
    - [(ii) Simplified decision table](#ii-simplified-decision-table)
    - [(iii) Pseudocode](#iii-pseudocode)
    - [Notations](#notations)
  - [Q2. Insurance program](#q2-insurance-program)
    - [(i) Decision table](#i-decision-table-1)
    - [(ii) Simplified decision table](#ii-simplified-decision-table-1)
    - [Notations](#notations-1)

## Q1. Factory program

### (i) Decision table

| DIM | STR | PAI | PASS | REP | REJ |
| --- | --- | --- | ---- | --- | --- |
| N   | N   | N   |      |     | X   |
| N   | N   | Y   |      |     | X   |
| N   | Y   | N   |      |     | X   |
| N   | Y   | Y   |      |     | X   |
| Y   | N   | N   |      |     | X   |
| Y   | N   | Y   |      | X   |     |
| Y   | Y   | N   |      | X   |     |
| Y   | Y   | Y   | X    |     |     |


### (ii) Simplified decision table

| DIM | STR | PAI | PASS | REP | REJ |
| --- | --- | --- | ---- | --- | --- |
| Y   | Y   | Y   | X    |     |     |
| Y   | N   | Y   |      | X   |     |
| Y   | Y   | N   |      | X   |     |
| N   | -   | -   |      |     | X   |
| Y   | N   | N   |      |     | X   |

### (iii) Pseudocode

```
BEGIN
    READ Dimensions
    READ Strength
    READ Paint
    IF Dimensions = FALSE
        PRINT "part is rejected"
    ELSE IF Strength = FALSE AND Paint = FALSE 
        PRINT "part is rejected"
    ELSE 
        PRINT "part is not rejected"
    ENDIF
END
```

### Notations

| Abbreviation | Meaning                    |
| ------------ | -------------------------- |
| DIM          | All dimensions are correct |
| STR          | Strength tests are passed  |
| PAI          | Paint tests are passed     |
| PASS         | Fit for use                |
| REP          | Sent for repair            |
| REJ          | Rejected                   |

## Q2. Insurance program

### (i) Decision table

| ANO | AGE > 10 | CLA ??? 3 | REF | NO-DIS | DIS |
| --- | -------- | ------- | --- | ------ | --- |
| N   | N        | N       |     |        |     |
| N   | N        | Y       |     |        | X   |
| N   | Y        | N       |     | X      |     |
| N   | Y        | Y       |     | X      |     |
| Y   | N        | N       |     | X      |     |
| Y   | N        | Y       |     | X      |     |
| Y   | Y        | N       | X   |        |     |
| Y   | Y        | Y       | X   |        |     |

### (ii) Simplified decision table

| ANO | AGE > 10 | CLAIMS ??? 3 | REF | NO-DIS | DIS |
| --- | -------- | ---------- | --- | ------ | --- |
| N   | N        | N          |     |        |     |
| N   | N        | Y          |     |        | X   |
| N   | Y        | -          |     | X      |     |
| Y   | N        | -          |     | X      |     |
| Y   | Y        | -          | X   |        |     |

### Notations

| Abbreviation | Meaning                                         |
| ------------ | ----------------------------------------------- |
| ANO          | Has been refused insurance by another company   |
| AGE > 10     | Car is over 10 years old                        |
| CLAIMS ??? 3   | Have made not more than three claims previously |
| REF          | Insurance is refused                            |
| NO-DIS       | Insurance without any discount is available     |
| DIS          | Insurance with a discount is available          |
