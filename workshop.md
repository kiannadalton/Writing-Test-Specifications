
UNIT
Prompt:
A function called "multiplication" that returns the product of the two input numbers.

Expectations:
Takes an array of 2 numbers
returns the product of the two numbers the user input
should return a number type
should through an error if you provide a string instead of a number
should be able to handle negative numbers
should throw an error if more than 2 numbers are input
would expect multiply([2, 20]) to return 40

Test Specs:
1. Expect multiply([2, 3]) to return 6
2. Expect multiply(["2", "3"]) to return an error
3. Expect multiply([2, -3]) to return -6
4. Expect multiply([]) to return 0
5. Expect multiply([2, 3, 4]) to return an error





Prompt:
A function called "concatOdds" takes two arrays of integers as arguments. It should return a single array that only contains the odd numbers, in ascending order, from both of the arrays.
    Example: concatOdds([3, 2, 1], [9, 1, 1, 1, 4, 15, -1])
        ...should result in [-1, 1, 3, 9, 15]

Expectations:
Takes 2 arrays of integers
returns a new array of odd integers and only lists each integer once
should be able to accept negative integers
should list them from lowest to highest
should remove even intergers
should throw an error if you provide a string instead of a number
should throw an error if integers are input with "" (string)
should throw an error if more than 2 numbes are input
should throw an error if only one array of integers is provided
would expect ([1, 2, 3], [4, 5, 6, -7]) to return [-7, 1, 3, 5]

Test Specs:


EX: 
Expect add([1, 2, 3], [4, 5, 6]) to return [1, 3, 5]
Expect add([1, 2, 3], [4, 5, 6, -7]) to return [-7, 1, 3, 5]
Expect add([1, 2, 3]) to return an error
Expect add(["1", "2", "3"], [4, 5, 6, -7]) to return an error
Expect add() to return 0


<!-- cut off to Functional Test -->



FUNCTIONAL
Prompt:
A shopping cart checkout feature that allows a user to check out as a guest (without an account), or as a logged-in user. They should be allowed to do either, but should be asked if they want to create an account or log in if they check out as a guest.

Expectations:
The user can click on a shopping cart icon and be led to the checkout page.
The user sees a form prompting them to either login to their valid account, checkout as a guest, or create an account at the top.
The form includes a place to login eith a field for email address and field for password. 
The form also includes a separate field for email address, password, and confirm password if they would like to create an account.
If a user enters in a string without a '@', they will receive an error.
If the password does not met al the requirements, they will receive an error.
If the user types in the password incorrectly 3 times, an email will be sent to reset password to the inputted email address.




Test Specs:
GIVEN I am a new user visiting the site

WHEN I navigate to the checkout page THEN I see a form to log in by entering my email and password, create a login, or checkout as a guest.

WHEN I enter a valid email and password AND click on the Create New Account THEN I see a new user confirmation message.

WHEN I enter only a valid password AND click the submit button THEN I see an error message

WHEN I click on Checkout as a Guest AND click the submit button THEN I see a confirmation message.



GIVEN I am an existing user visiting the site

WHEN I navigate to the register page THEN I see a form to enter my email and password

WHEN I enter only a valid email AND click the submit button THEN I see a message stating enter in a password.

WHEN I enter only a valid password AND click the submit button THEN I see a message telling me to enter in an email.
