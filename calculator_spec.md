# Javascript Calculator
This is a specification for our javascript calculator. It describes everything the calculator should be able to do.

-------

Create a calculator using vanilla Javascript and Bootstrap. The calculator should have all the basic functionality of your average pocket calculator.

## Layout
Using Bootstrap's grid system, create a calculator with six rows in total.

The top row should be dedicated to the calculator display, which should be a text input.

Row two is four columns wide and contains the following four buttons: 7, 8, 9, and +.

Row three is four columns wide and contains the following four buttons: 4, 5, 6, and -.

Row four is four columns wide and contains the following four buttons: 1, 2, 3, and x.

Row five is four columns wide and contains the following three buttons: 0, ., ÷. The 0 button should take up the space of two columns.

Row six is four columns wide and contains the following two buttons: AC and =. Each button has a width of two columns.

## Logic

By and large, this app will function exactly as a pocket calculator would.

### Number buttons
Each numeric button (0 - 9), when clicked, will display that number on the screen. If the numbers `3` and `7` were clicked in succession, the number `37` would appear in the display.

### Action buttons
The action buttons include +, -, x, ÷, ., AC, and =.

#### `AC` button
The AC, or "all clear" button, will change the display value to `0`. Pressing this button clears the memory and aborts any in-progress calculations.

#### Decimal button
The decimal button allows the user to create floating point numbers for use in calculations. Pressing this button adds a decimal point to the right-hand side of the number in the display. Pressing additional numeric keys will insert numbers to the right of the decimal point.

#### Mathematical Operator Buttons
When any of the mathematical operator buttons (+, -, x, ÷) are clicked, it replaces the current content of the screen with the appropriate symbol. Both the number that was on the screen and the selected operation are saved to a queue for later processing.

#### Equals Button
The equals button performs all operations that have been saved for processing. Operations are performed in the order that they are entered into the queue. The result of the operations appears on the display.

## Calculation Algorithm

When the total is being calculated, the queue contains an alternating sequence of numeric values and mathematical operations to be performed.

When the calculation method begins, assign the value of the first element in your queue to a running total.

Initialize a loop, with the first index set to 1. The loop should terminate when it reaches the end of the queue. Each iteration should increase the index by two.

Each mathematical operation requires two numbers. The first number for each operation will always be the running total. The second number will be the next numeric value in the queue.

Ensure that the appropriate operation is performed as the queue is processed and the running total remains up to date.

When the loop finishes, return the running total from the function.
