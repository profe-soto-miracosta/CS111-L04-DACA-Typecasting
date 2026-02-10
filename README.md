# Lab 04 - DACA + Typecasting

## Learning Objective
- Demonstrate an understanding of typecasting + choosing data types and application to DACA article.

## Program Description
[Article on DACA Recipients and Taxes](https://www.nbcnews.com/news/latino/daca-recipients-12-states-pay-over-50-million-taxes-report-n1053041)
[Key Facts on Deferred Action for Childhood Arrivals (DACA)](https://www.kff.org/racial-equity-and-health-policy/key-facts-on-deferred-action-for-childhood-arrivals-daca/#:~:text=As%20of%20September%2030%2C%202024,through%20Medicaid%2C%20the%20Children's%20Health)
[A DACA fix could add $400 billion to the U.S. economy in the next 10 years](https://www.fwd.us/news/daca-fix/)

As you read in this week's article, DACA recipients contribute massively to our economy which includes paying taxes. There are humanistic, ethical, and social reasons for supporting DACA in addition to realistic pathways to citizenship. The article, however, focused on the economic reasons, so your team would like for you to calculate and output:

- Average DACA recipient tax contribution
- Average DACA recipient tax contribution, rounded down to the nearest whole dollar
- State with the most DACA recipients

## Specifications
There are some decisions that were made in the backend system that you have no control over. The database that this data will come from stores data in the following ways:

- State abbreviations (ex: _NY_) are stored as two separate characters, each lower-case (ex: _n_ and _y_)
- Number of DACA recipients is stored as a whole number
- Total federal tax contribution stored as a whole number

| State First | State Last | DACA Recipients | Federal Tax (2013 - 2022) |
|-------------|------------|-----------------|---------------------------|
| c           | a          | 150,640         | $6,918,000,000            |
| t           | x          | 91,460          | $2,804,000,000            |
| i           | l          | 269,000         | $1,198,000,000            |

You've been instructed to stick to the same data types. **Declare and initialize variables that match the database.**

They are expecting output similar to:
```
Average DACA-recipient Tax Contribution: $85714.28571428571
Rounded down to nearest whole dollar: $85714
State with most DACA recipients: CA
```
**Testing tip:**

- Each line ends with the value requested, in the above order
- The state must be capitalized (ex: NY, NV, etc.)
- No blank lines between outputs (see above)

**Java tip:**

- Having an issue with storing an integer outside of the `int` range? For example, the total federal tax contributions. Use a larger data type for integers, like `long`. Use `L` right after the number so that Java recognizes it as a larger integer type.
```java
double bigNumber = 123456789012345L;
```
- The difference between the ASCII value of any lowercase English alphabet character and its corresponding uppercase character is always 32. `'a'` has an ASCII value of 97. `'A'` has an ASCII value of 65.\(97-65=32\). By subtracting 32 from a lowercase character's integer value, you obtain the integer value of its uppercase equivalent.
```java
char lowercase = 'c';
// Subtract 32 from the ASCII value to get the uppercase equivalent
char uppercaseChar = (char) (lowercaseChar - 32); 
```

## HACKER CHALLENGE

Formatting on the average tax contribution looks bad right? So many values after the decimal! With what we've covered in the course so far, upgrade your code to only show 2 places after the decimal.

