![Logo](/assets/images/logo-image.jpg)

# MS-1 Project Testing Details #


[Main README.md file](https://github.com/simonjvardy/Aviation-Consultancy/blob/master/README.md)

[View the live project here.](https://simonjvardy.github.io/Aviation-Consultancy/)

---

## Table of Contents ##

- [Automated Testing](#automated-testing)
  - [Validation Services](#validation-services)
- [Manual Testing](#manual-testing)
  - [Unit Testing](#unit-testing)
  - [Functional Testing](#functional-testing-(combined-integration-and-system-testing))
  - [User Acceptance Testing (UAT)](#user-acceptance-testing-(uat))
  - [Testing undertaken on desktop](#testing-undertaken-on-desktop)
  - [Testing undertaken on tablet and phone devices](#testing-undertaken-on-tablet-and-phone-devices)
- [Bugs discovered](#bugs-discovered)
  - [Unsolved Bugs](#unsolved-bugs)


---
## Automated Testing ##

### Validation Services ###

The following **validation services** and **linter** were used to check the validity of the website code.

- [W3C Markup Validation](https://validator.w3.org/) 
  - This validator checks the markup validity of Web documents in HTML, XHTML, SMIL, MathML, etc.
- [W3C CSS validation](https://jigsaw.w3.org/css-validator/)
  - JSHint is a community-driven tool that detects errors and potential problems in JavaScript code.
- [Chrome DevTools Lighthouse](https://developers.google.com/web/tools/lighthouse)
  - An open-source automated tool for improving webpages by running audits for performance, accessibility, progressive web apps, SEO etc.

---
## Manual Testing ##

### Unit Testing ###
[Unit Testing document](testing/MS1-unit-test-plan.pdf) containing:
- Unit Test scope,
- The test cases,
- The pass / fail record for each test case.

### Functional Testing (combined Integration and System testing) ###
[Functional Testing document](testing/MS1-functional-test-plan.pdf) containing:
- UAT approach (scope, assumptions and constraints, team roles and responsibilities etc.), 
- Identified risks, 
- The test cases,
- The pass / fail record for each test case.

### User Acceptance Testing (UAT) ###
[UAT document](testing/MS1-uat-test-plan.pdf) containing:
- UAT approach (scope, assumptions and constraints, team roles and responsibilities etc.), 
- Identified risks, 
- The test cases,
- The pass / fail record for each test case.

### Testing undertaken on desktop ###

- Hardware:
    - Macbook Pro Laptop
    - Dell 5590 Laptop
- Tested Operating Systems:
    - Windows 10
    - OSX 10.11          
- Tested Browsers:
    - Windows 10:
        - Chrome
        - Firefox
        - Edge 
    - OSX 10.11
        - Chrome
        - Firefox
        - Safari  

### Testing undertaken on tablet and phone devices ###

- Hardware:
    - iPad Pro 12.9"
    - iPad Pro 10.5"
    - iPhone XS Max
- Tested Operating Systems:
    - iOS 13.6.1
    - iPadOS 13.6.1
- Tested Browsers:
    - iOS / iPadOS
        - Chrome
        - Firefox
        - Edge
        - Safari

---
## Bugs discovered ##

The issue log is managed on the [GitHub Project Issues section](https://github.com/simonjvardy/Aviation-Consultancy/issues) using the standard GitHub [bug\_report.md template](https://github.com/simonjvardy/Aviation-Consultancy/blob/master/.github/ISSUE_TEMPLATE/bug_report.md)


#### Unsolved Bugs ####

[Issue #60](https://github.com/simonjvardy/Aviation-Consultancy/issues/60)
- Unit Testing: Homepage callout image doesn’t resize on an iPad or iPhone display
  - CSS property `background-attachment: fixed;` is not recognised by Apple devices and causes the website hero images using this property to display incorrectly
  - The workaround is to set the property back to the default `background-attachment: scroll;` but this will affect all devices and remove the image effect I was aiming for.
  - An alternative solution, without resorting to JavaScript, is to add devices screen size specific `@media` queries to style.css to change from fixed to scroll but this can become difficult and messy.
    - This has been tested within the current [style.css](https://github.com/simonjvardy/Aviation-Consultancy/blob/master/assets/css/style.css) file for a specific iPhone model screen size and can be seen at the end of the file.
  - A more elegant solution to this problem by using only HTML & CSS is ongoing.

[Issue #](https://github.com/simonjvardy/Aviation-Consultancy/issues) 
- <description>