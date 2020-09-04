![Logo](/assets/images/logo-image.jpg)

# Aviation-Consultancy Project Testing Details #


[Main README.md file](https://github.com/simonjvardy/Aviation-Consultancy/blob/master/README.md)

[View the live project here.](https://simonjvardy.github.io/Aviation-Consultancy/)

---

## Table of Contents ##

- [Aviation-Consultancy Project Testing Details](#aviation-consultancy-project-testing-details)
  - [Table of Contents](#table-of-contents)
  - [Automated Testing](#automated-testing)
    - [Validation Services](#validation-services)
  - [Manual Testing](#manual-testing)
    - [Unit Testing](#unit-testing)
    - [User Acceptance Testing (UAT)](#user-acceptance-testing-uat)
    - [Peer Code Review](#peer-code-review)
    - [Testing undertaken on desktop](#testing-undertaken-on-desktop)
    - [Testing undertaken on tablet and phone devices](#testing-undertaken-on-tablet-and-phone-devices)
  - [Bugs discovered](#bugs-discovered)
      - [Known Bugs](#known-bugs)
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
[Unit Testing document](testing/aviation-consultancy-unit-test-plan.pdf) containing:
- Unit Test scope,
- The test cases,
- The pass / fail record for each test case.


### User Acceptance Testing (UAT) ###
[UAT document](testing/aviation-consultancy-uat-test-plan.pdf) containing:
- UAT approach (scope, assumptions and constraints, team roles and responsibilities etc.), 
- Identified risks, 
- The test cases,
- The pass / fail record for each test case.

### Peer Code Review ###
The deployed website link was uploaded to the following sites for peer code review and testing:
- Code Institute Slack #peer-code-review channel
- Code Institute Slack #may-2020 channel
- LinkedIn for general review and feedback

### Testing undertaken on desktop ###

- Hardware:
    - Macbook Pro Laptop 17" (2009)
    - Macbook Pro Laptop 16" (2019)
    - Dell 5590 Laptop
- Tested Operating Systems:
    - Windows 10
    - OSX 10.11
    - OSX 10.15    
- Tested Browsers:
    - Windows 10:
        - Chrome
        - Firefox
        - Edge 
        - Opera
    - OSX 10.11
        - Chrome
        - Firefox
        - Safari

### Testing undertaken on tablet and phone devices ###

- Hardware:
    - iPad Pro 12.9"
    - iPad Pro 10.5"
    - iPhone XS Max
    - Samsung Galaxy S20 Ultra
- Tested Operating Systems:
    - iOS 13.6.1
    - iPadOS 13.6.1
    - Android 10 One UI 2.0
- Tested Browsers:
    - iOS / iPadOS
        - Chrome
        - Firefox
        - Edge
        - Safari

---
## Bugs discovered ##

The issue log is managed on the [GitHub Project Issues section](https://github.com/simonjvardy/Aviation-Consultancy/issues) using the standard GitHub [bug\_report.md template](https://github.com/simonjvardy/Aviation-Consultancy/blob/master/.github/ISSUE_TEMPLATE/bug_report.md)


#### Known Bugs ####

[Issue #60](https://github.com/simonjvardy/Aviation-Consultancy/issues/60)
- Unit Testing: Homepage callout image doesn’t resize on an iPad or iPhone display
  - CSS property `background-attachment: fixed;` is not recognised by Apple devices and causes the website hero images using this property to display incorrectly
  - The workaround is to set the property back to the default `background-attachment: scroll;` but this will affect all devices and remove the image effect I was aiming for.
    - Smaller versions of the background images were uploaded with a width of 960px to cover tablet and mobile devices
    - Media query with a `max-width: 1366px;` was added to the [style.css](https://github.com/simonjvardy/Aviation-Consultancy/blob/master/assets/css/style.css) file and included the container classes for each of the page background images with the background attributes set to `background: url('../images/image-file.pg') no-repeat center scroll; background-size: cover;`
    - This works correctly on all device types now but is not a completely satisfactory solution; in keeping with what I had designed.
    - I think the design has reached the limits of my experience for the time available but adding JavaScript at a later time may add the functionality to allow the original design on all device types.

#### Unsolved Bugs ####

