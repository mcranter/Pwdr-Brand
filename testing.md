## Testing

- [Manual Testing.](#manual-testing)
  * [Functionality](#functionality)
- [Automatic Testing](#automatic-testing)
  * [Validators](#validators)

### Manual Testing.
#### Functionality

1. Search function: Home Page
    - Tested search fuctionality by submitting an empty search in order to verify that an error message appeared.
    - Result: An error message appeared, displaying the text: 'Error! You didn't enter any search criteria!'
    ![](media/test-search-none.png)


    - Tested search functionality for accuracy by submitting legitimate search for various whole terms ('berry', 'workout' etc.) with all  inputs valid.

    - Result: All expected search items were returned.
    ![](media/test-terms.png)


    - Tested search functionality by submitting searches for shortened terms of three and two letters (such as 'ber', 'wor' ,'ba') to see if all relevent items were returned.
    - Result: All expected search items were returned. 
    ![](media/test-search-small.png)


2. Login Page:
    - Tested login functionality by submitting incorrect login details in order to verify that an error message appeared.
    - Result: Error message appeared displaying the text: 'The username and/or password you specified are not correct.'
    ![](media/login-username.png)

3. Register Page
    - Tested registration functionality by attempting to log in using an existing username in order to verify an error message appeared.
    - Result: The registration page refreshed and displayed an error saying 'A user with that username already exists.'
    ![](media/test-reg-name.png)
   
    - Tested registraion functionality by attempting to log in using an existing email address in order to verify an error message appeared.
    - Result: The registration page refreshed and displayed an error saying 'A user is already registered with this e-mail address.'
    ![](media/test-reg-email.png)

    - Tested registration functionality by attempting to register a username using fewer than 4 letters in order to verify that an error message appeared.
    - Result: Error message is diplayed, reading 'Please lengthen this text to 4 characters or more (you are currently using 3')
    ![](media/test-signup3.png)


4. Product Page:
    - Attempted to add a number of products exceeding 99 to shopping bag in order verify that an error message appeared.
    - Result: An error message popped up displaying the text "Value must be less than or equal to 99"
    ![](media/product-page-greater-100.png)

    - Attempted to add on a sum of zero products to the shopping bag in order to verify an error message appeared.
    - Result: An error message popped up displaying the text "Value must be greater than or equal to one"
    ![](media/product-page-less.png)


5. Checkout Page:
    - Attempted to enter an email address without an @ symbol in order to verify the appearance of an error message.
    - Result: Error message appeared after clicking 'complete order' button, reading 'Please include an @ in the email address.'
    ![](media/checkout-@.png)
    - Attempted to include text in the phone number field in order to verify the appearance of an error message.
    - Result: Error message popped reading 'Please match the format requested'.
    ![](media/text-phone.png)

    - Attempted to enter an invalid credit card number in order to verify the appearance of an error message.
    - Result: An error message appeared, reading 'Your card number is invalid'. 
    ![](media/credit-card.png)

6. Blog Page:
    - Testing on this page revealed the following alarming information: 1) that any logged in user could see the edit/delete options available, and by extension edit or delete any blog post. 
    ![](media/blog-testing-edit.png)
    - Resolved: A simple line of code restricting the visibilty of the edit/delete buttons, as well as the ability to edit or delete any post, fixed this issue. 
    Once this change was made, I logged in under a non-superuser account and verified that the edit/delete options no longer appeared on either the blogs or blog_details pages. 
    ![](media/blog-testing.png)
    
## Browsers
This site was tested on, and is confirmed to function and appear correctly on, the following browsers: Chrome (v91), Safari (v14.0) and Firefox (86.0.1/64-bit), as well as a variety of mobile devices using Google Chrome's Developer tools. 

- Resolved issue: the index page's carousel and the footer were missing relevant CSS styling on the Safari browser. This was resolved by using a media query (found in this [stack overflow post](https://stackoverflow.com/questions/16348489/is-there-a-css-hack-for-safari-only-not-chrome/25975282#25975282) ) which specifically targets Safari only. 

## Automatic Testing

### Validators

 - **[HTML Validator](https://validator.w3.org/):** 
 Each HTML file on the site was run through this validator. For brevity, I include a selection of sample results. No errors were found. 
    
    **Sample Results:** 
    - Bag Total.html ![](media/bag-total-validatator.png)
    - Bag Html![](media/bag-validator.png)
    - Checkout buttons Html![](media/checkout-buttons-validatator.png)

- **[CSS Validator](https://jigsaw.w3.org/css-validator/):** Each CSS file on the site was run through this validator. For brevity, I include a selection of sample results. No errors were found.

    **Sample Results:**
    - 404 ![](media/css-validator.png)
    - 505 ![](media/css2-validator.png)


- **[JS Hint](https://jshint.com/):** 
Each Javascript file on the site was run through this validator. For brevity, I include a selection of sample results. No errors were found.
    
    **Sample Results:**
    -  Error:'template literal syntax' is only available in ES6 (use 'esversion: 6').
    -  Stripe_elements.js ![](media/stripe-js-validator.png)

- **[Python validator | PEP8](http://pep8online.com/):** Each Python file on the site was run through this validator. For brevity, I include a selection of sample results. No errors were found.

    **Results:** No errors found beyond those trigger by long lines which were auto-generated during migrations.

