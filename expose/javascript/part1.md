### Part 1: Variable Scoping in JavaScript

**1. What is printed by line 9 (using `var`)?**  
values added:  20 is printed because result is updated inside the if block and var is function-scoped.

**2. What is printed by line 13 (using `var`)?**  
final result:  20 is printed. Even though result was declared in the if block, var makes it accessible throughout the function.

**3. Why should you not use var?**  
var is function-scoped, not block-scoped. This can lead to unexpected behavior and bugs. Use let or const instead for safer, more predictable scoping.

**4. What is printed by line 9 (using `let`)?**  
values added:  20 is printed. let result is block-scoped and used within the if block.

**5. What is printed by line 13 (using `let`)?**  
A ReferenceError is thrown because result is block-scoped and not accessible outside the if block.

**6. What is printed by line 9 (using `const`)?**  
A TypeError is thrown at line 7: Assignment to constant variable. This happens because const result = 0 cannot be reassigned.

**7. What is printed by line 13 (using `const`)?**  
Nothing is printed. Line 13 is never reached because the function throws an error before it can get there.
