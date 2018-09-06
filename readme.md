
# Coin Calculator Code Test

## Summary

Write a simple PHP web application that, given a figure in pence, will calculate the minimum number of standard UK denomination coins needed to equal that amount.

Eg. 123p = 0 x £2, 1 x £1, 0 x 50p, 1 x 20p, 0 x 10p, 0 x 5p, 1 x 2p, 1 x 1p

The test should take 1-2 hours.

## Requirements

 * Account for only the main UK coins: £2, £1, 50p, 20p, 10p, 5p, 2p and 1p coins.
 * The app should be wriiten using only PHP, JS, CSS and HTML (libraries are allowed).
 * The user interface should consist of an HTML page with an input field that accepts an 'amount' string (Eg. 92p, £2.12) and displays the number of each coin denomination needed when the user hits 'enter'.
 * Include a README with any instructions, libraries, build files in order for us to run & view your code. 
 * The README should include notes on any enhancements, ideas, etc for future improvement if there are any
 * Submission should be in the form of a link to a github repo (or similar public )

## What we are looking for

 * High quality, secure, maintainable code.
 * Test cases for your code.
 * Well documented and commented code.
 * Consistent coding standards.
 * Accessible, semantic, valid HTML.
 * Extensible user input parsing and validation.
 * Sensible separation of functionality (Eg, input, controllers, models, utils, views) following standard patterns.
 
## Tests

 * Valid inputs are: integers (123), floats of arbitrary length (1.234), numbers prefaced with `£` and/or suffixed with `p`
 * Invalid inputs are anything other than valid inputs (e.g. `1x` is invalid)
 * Invalid inputs should raise an error (or be ignored) and return zero coins required

A [test cases](tests.csv) file is included of the form:

input: html input
pence: html input in pence
£2: number of two pound coins required
£1: number of one pound coins required
50p: number of fifty pence coins required
20p: number of twenty pence coins required
10p: number of ten pence coins required
5p: number of five pence coins required
2p: number of two pence coins required
1p: number of one pence coins required
test case: textual description of the test
sum: sum of numbers of each coin in pence
checksum: validates the test data (true if 'pence' matches 'sum'). May be ignored

**Note**: some test cases are expected to fail due to invalid input

These test cases are provided for convenience. They do not need to be incorporated into the code base in the provided format but their use is encouraged. They will be used for manual testing later along with similar variants.
