# CSS Guidelines

- use BEM

1. Do not use important! - the project will self-destroy :) - if you follow the specificity rules and write your styles from mobile all the way to larger screens, the use of important is unnecessary and harmful.
2. Use rem (relative units) instead of px. [62.5% trick](https://www.aleksandrhovhannisyan.com/blog/62-5-percent-font-size-trick/)
3. Use proper indentation (2 spaces) and keep the consistency throughout the file
4. Avoid inline styles
5. Use short-hand properties when possible **padding: 0 0 2rem 10rem;** instead of..***padding-bottom: 2rem; and padding-left: 10rem;***
6. Value 0 doesn't need the value type (0 instead of 0px / 0rem)
7. Add comments for better readability or for complex rules
8. Do not use color names ( color: black ), specify your color values with hex and color functions instead
9. When grouping selectors, keep individual selectors each on one line
