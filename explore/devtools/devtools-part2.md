1. **What was the bug?**
   - The bug was that the input values from HTML text fields are returned as strings, not numbers.
   - When the `+` operator is used with strings, it concatenates them instead of performing mathematical addition.
   - For example, adding `"5"` and `"10"` gave `"510"` instead of `15`.

2. **How would you fix it?**
   - Convert the string values to numbers before adding them using `Number()` or `parseInt()`:

   let result = Number(num1) + Number(num2);
