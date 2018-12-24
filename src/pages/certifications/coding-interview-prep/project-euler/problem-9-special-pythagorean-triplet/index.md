---
title: Special Pythagorean triplet
---
## Problem 9: Special Pythagorean triplet

### Explaination:
- Since we have a condition: `a+b+c = n` where n being the number passed, we can simplify the equation to `c = (n-a-b)`.
- Now, for every iteration check the pythagorian equation `a^2 + b^2 = c^2` to be true if so then we we got our product `a*b*c`.

### Solution:

```
  function specialPythagoreanTriplet(n) {
     var prodOfTriplet
     for (let i = 1; i < n; i++) {
        for (let j = 1; j < n; j++) {
          if (Math.pow(i, 2) + Math.pow(j, 2) == Math.pow(n - i - j, 2)) {
            prodOfTriplet = i * j * (n - i - j);
          }
        }
      }

      return prodOfTriplet;

  }
  specialPythagoreanTriplet(1000);
```

### Try with [Repl.it](https://repl.it/@GemjuSherpa/Special-Pythagorean-triplet)
