# **UTIL2000**
---

![Photo of Output](assets/codeRunning.png)

## Programmers
<!-- Using &nbsp to add white space so Github links are aligned -->
* *Bret Dunker         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;          [GitHub](https://github.com/KirbyD-YEAH)*

## Version
1.0

## Purpose
This program performs calculations to check the value of a yearly-compounding interest over a set amount of years. It then doubles that initial investment and does the interest calculations. This repeats one more time resulting in the interest values for your investment, double your investment, and quadruple your investment. It then displays all of this in a compact output file. The JCL to run this code is included in the project.

## Paragraphs
```000-CALCULATE-FUTURE-VALUES```
* The driver code for the program. Delegates the work to other paragraphs and doubles ```INVESTMENT-AMOUNT``` after each iteration
* First it performs ```100-CALCULATE-FUTURE-VALUE``` then it performs ```140-DISPLAY-VALUES``` and finally it doubles ```INVESTMENT-AMOUNT```

```100-CALCULATE-FUTURE-VALUE```
* Handles the loop for calculating future values by performing ```120-CALCULATE-NEXT-FV``` once for every year in ```NUMBER-OF-YEARS```
* Uses ```YEAR-COUNTER``` to keep track of when it needs to stop

```120-CALCULATE-NEXT-FV```
* Calculates the next ```FUTURE-VALUE``` and increments ```YEAR-COUNTER``` which is the exit-condition defined in ```100-CALCULATE-FUTURE-VALUE```

```140-DISPLAY-VALUES```
* Displays the values of ```INVESTMENT-AMOUNT```, ```NUMBER-OF-YEARS```, ```YEARLY-INTEREST-RATE```, and ```FUTURE-VALUE``` in a compact list

## Data Items
* ```INPUT-VALUES``` - Groups the different program inputs together
  *   ```INVESTMENT-AMOUNT``` - The initial investment amount to be compounded (principle)
  *   ```NUMBER-OF-YEARS``` - Number of years to compound the interest for
  *   ```YEARLY-INTEREST-RATE``` - The interest rate for your investment, compounded annually
* ```WORK-FIELDS``` - Groups the different fields used in the logic of the program
  *   ```FUTURE-VALUE``` - The value after compounding
  *   ```YEAR-COUNTER``` - Tracks the iterations it has compounded the interest for
  *   ```EDITED-WHOLE-VALUE``` - A formatted data item for outputting values, **whole number** items are moved here before displayed
  *   ```EDITED-DECIMAL-VALUE``` - A formatted data item for outputting values, **decimal number** items are moved here before displayed


---
