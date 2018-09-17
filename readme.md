
# Coin Calculator Code Test

## Summary

Write a simple PHP web application that, given an input figure in pounds and/or pence, will calculate the minimum number of standard UK denomination coins needed to equal that amount.

Eg.

170 (or 1.70) = 1 x £1, 1 x 50p, 1 x 20p

The test should take 1-2 hours.

## Requirements

 * Account for the UK coins: £2, £1, 50p, 20p, 2p and 1p coins
 * The app should be wriiten using only PHP, JS, CSS and HTML
 * libraries and frameworks are allowed but not mandatory
 * The user interface should consist of an HTML page with an input field that accepts an 'amount' string (Eg. "92p", "£2.12")
 * The response should display the number of each coin denomination needed when the user hits enter
 * Include a README with any instructions, libraries, build files in order for us to run & view your code 
 * The README should include notes on any enhancements, ideas, etc for future improvement if there are any
 * Submission should be in the form of a link to a github repo (or similar publically available code base)

## What we are looking for

 * High quality, secure, maintainable code
 * Test cases for your code
 * Appropriately documented and/or readable code and instructions
 * Consistent coding standards
 * Accessible, semantic, valid HTML
 * Extensible user input parsing and validation
 * Logical separation of functionality (Eg, input, controllers, models, utils, views) following standard patterns
 
## Tests

 * Valid inputs are: 

 	integers (123)  
 	floats of arbitrary length (1.234)  
 	numbers prefaced with `£` and/or suffixed with `p` (£12, £2.34, 123p, £3.45p)

 * Invalid inputs are anything other than valid inputs (e.g. `1x` is invalid)
 * Invalid inputs should raise an error (or be ignored) and return zero coins required

## Acceptance tests:

The following inputs are valid and should return coin amounts:

| input         | pence (canonical) | description                             |
|---------------|-------------------|-----------------------------------------|
| 4             |    4              | single digit                            |
| 85            |   85              | double digit                            |
| 197p          |  197              | pence symbol                            |
| 2p            |    2              | pence symbol single digit               |
| 1.87          |  187              | pounds decimal                          |
| £1.23         |  123              | pound symbol                            |
| £2            |  200              | single digit pound symbol               |
| £10           | 1000              | double digit pound symbol               |
| £1.87p        |  187              | pound and pence symbol                  |
| £1p           |  100              | missing pence                           |
| £1.p          |  100              | missing pence but present decimal point |
| 001.41p       |  141              | buffered zeros                          |
| 4.235p        |  424              | rounding three decimal places to two    |
| £1.257422457p |  126              | rounding with symbols                   |

The following inputs are **NOT** valid

| input  | pence (canonical) | description              |
|--------|-------------------|--------------------------|
|        | 0                 | empty string             |
| 1x     | 0                 | non-numeric character    |
| £1x.0p | 0                 | non-numeric character    |
| £p     | 0                 | missing digits           | 


For convenience the tests above are included in [test cases](tests.csv)
