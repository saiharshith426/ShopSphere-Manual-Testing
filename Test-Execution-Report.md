# Test Execution Report: ShopSphere
 
**Site:** https://practicesoftwaretesting.com \
**Tester:** A.Sai Harshith\
**Date:** 26 November 2026
 
## Summary
 
I ran 23 test cases across four modules. All 23 passed against their expected results, and I found 5 defects, all in the registration form.
 
| Module | Cases | Pass | Fail | Blocked |
|---|---|---|---|---|
| Login and Registration | 7 | 7 | 0 | 0 |
| Product Search | 6 | 6 | 0 | 0 |
| Shopping Cart | 5 | 5 | 0 | 0 |
| Coupon Application | not tested | | | |
| Checkout and Payment | 5 | 5 | 0 | 0 |
| **Total** | **23** | **23** | **0** | **0** |
 
## Defects
 
| ID | Title | Severity |
|---|---|---|
| BUG-01 | Asterisks for mandatory fields are placed inconsistently | Low |
| BUG-02 | First and last name accept numbers | Medium |
| BUG-03 | Address fields fill with details unrelated to the postal code | Medium |
| BUG-04 | Phone number accepts very short values | Medium |
| BUG-05 | Password message says minimum 6 characters, but the rule is 8 | Medium |
 
The registration test cases still passed because they checked the main flow. The bugs came from looking closer at individual fields.
 
## Things I want to be upfront about
 
- **Coupons:** not tested, because I couldn't find the feature on the site.
- **Quantity limits:** I checked that an out-of-stock product can't be added to the cart. I didn't test quantity above available stock, zero, or negative quantities.
- **Duplicate orders:** in Checkout TC-05 the payment button stayed disabled because of a badly formatted card number, so I never got to submit twice. This one needs a retest with a valid card.
- **Email:** the field rejects addresses without an `@`, but it can't tell whether an address really exists. I don't count that as a bug. Real shops usually handle it with a verification email.
## Conclusion
 
The main flows work: registering, logging in, searching, using the cart and checking out. The weak spot is validation on the registration form. The password message is the one I'd fix first, because it contradicts the 8-character rule shown on the same page.
 
