### Part 2: Function Scope and Output

**1. What happens at line 12 and why (with `var i`)?**  
It prints 3 because i is declared with var, which is function-scoped and accessible outside the loop.

**2. What happens at line 13 and why (logging `discounted`)?**  
It prints [50, 100, 150] because discounted is declared with var and is accessible throughout the function.

**3. What happens at line 14 and why (logging `finalPrice`)?**  
It prints 150 because finalPrice is declared with var, which is function-scoped. Its last assigned value (in the final loop iteration) remains accessible outside the loop.

**4. What will this function return? Give a brief explanation why.**  
It returns `[50, 100, 150]`. Each price in the array is multiplied by 0.5 (50% discount), then rounded to two decimal places and pushed to the `discounted` array, which is returned at the end.

**5. What happens at line 12 and why (with `let i`)?**  
Line 12 throws a ReferenceError because `i` is declared with `let` inside the for-loop block. `let` is block-scoped, so `i` is not accessible outside the loop.

**6. What happens at line 13 and why (with `let discountedPrice`)?**  
Line 13 throws a ReferenceError because `discountedPrice` is declared with `let` inside the for-loop block and is not accessible outside of it due to block scoping.

**7. What happens at line 14 and why (with `let finalPrice`)?**  
Line 14 works and prints 150. Even though `finalPrice` is declared with `let`, it is scoped to the entire function (not the loop), so it remains accessible and retains the last assigned value.

**8. What will this function return? Give a brief explanation why.**  
It will return `[50, 100, 150]`. The function uses `let` for all variables, ensuring proper block and function scoping. Each price is halved (because of 50% discount), rounded, and added to the `discounted` array, which is returned at the end.

**9. What happens at line 11 and why (with `let i`)?**  
Line 11 throws a ReferenceError because `i` is declared with `let` inside the for-loop and is not accessible outside of it. `let` is block-scoped, so `i` does not exist beyond the loop block.

**10. What happens at line 12 and why (logging `length`)?**  
Line 12 prints `3` because `length` is declared with `const` at the top of the function. `const` is block-scoped, and since this is at the function level, it is accessible anywhere inside the function.

**11. What will this function return? Give a brief explanation why.**  
It returns `[50, 100, 150]`. The function uses `const` for the array and length, and calculates a 50% discount on each price, pushing the result to the `discounted` array. `discounted` is returned correctly with no scoping issues.

### Object Property Notation (from Question 12)

**A. Accessing the value of the name property in the student object**  
`student.name`

**B. Accessing the value of the Grad Year property in the student object**  
`student['Grad Year']`

**C. Calling the function for the greeting property in the student object**  
`student.greeting()`

**D. Accessing the name property of the object in the Favorite Teacher property in student**  
`student['Favorite Teacher'].name`

**E. Access index zero in the array of the courseLoad property of the student object**  
`student.courseLoad[0]`

### Basic Operators & Type Conversion (Questions 13–15)

**13. Arithmetic**  
A. `'3' + 2` → `'32'` — String concatenation occurs because one operand is a string.  
B. `'3' - 2` → `1` — String is converted to number for subtraction.  
C. `3 + null` → `3` — `null` becomes `0`, so 3 + 0 = 3.  
D. `'3' + null` → `'3null'` — String concatenation.  
E. `true + 3` → `4` — `true` becomes `1`, so 1 + 3 = 4.  
F. `false + null` → `0` — `false` is 0, `null` is 0, total is 0.  
G. `'3' + undefined` → `'3undefined'` — String concatenation.  
H. `'3' - undefined` → `NaN` — `undefined` becomes NaN, math with NaN results in NaN.  

**14. Comparison**  
A. `'2' > 1` → `true` — `'2'` is coerced to number 2.  
B. `'2' < '12'` → `false` — Lexical string comparison, '2' > '1'.  
C. `2 == '2'` → `true` — Loose equality with type coercion.  
D. `2 === '2'` → `false` — Strict equality checks type and value.  
E. `true == 2` → `false` — `true` is 1, not equal to 2.  
F. `true === Boolean(2)` → `true` — Both are strictly true boolean values.  

**15. Explain the difference between the `==` and `===` operators.**  
`==` checks for equality with type coercion (e.g. `'2' == 2` is true), while `===` checks for both value **and** type equality (e.g. `'2' === 2` is false).  
"""

