name: Bug Report3
description: Report a bug or issue with the webstore
title: "[Bug Report]: "
labels: ["bug", "triage", "priority"]
projects: ["octo-org/1", "octo-org/44"]
assignees:
  - octocat
body:
  - type: markdown
    attributes:
      value: |
        We appreciate your help in reporting bugs. Please provide the following details so that we can investigate and resolve the issue as quickly as possible.
  - type: input
    id: order-id
    attributes:
      label: Bugged page
      description: If this bug is related to a specific page, please provide the page that is bugged.
      placeholder: ex. 
    validations:
      required: false
  - type: input
    id: browser-version
    attributes:
      label: Browser Version
      description: What browser and version are you using when you encounter this bug?
      placeholder: ex. Chrome 90.0.4430.85
    validations:
      required: true
  - type: input
    id: operating-system
    attributes:
      label: Operating System
      description: Which operating system are you using?
      placeholder: ex. Windows 10, macOS Monterey, Linux Ubuntu
    validations:
      required: true
  - type: dropdown
    id: bug-severity
    attributes:
      label: Bug Severity
      description: How would you categorize the severity of this bug?
      options:
        - "Critical: Completely breaks the site or feature."
        - "High: Major issue, but workarounds may exist."
        - "Medium: Moderate issue, doesn’t prevent core functionality."
        - "Low: Minor issue, does not significantly impact user experience."
      default: "Medium"
    validations:
      required: true
  - type: textarea
    id: bug-description
    attributes:
      label: Bug Description
      description: Please provide a detailed description of the bug, including steps to reproduce.
      placeholder: Describe what happened in detail, including error messages, unexpected behavior, or anything else.
      value: "The checkout button is not responding when clicked."
    validations:
      required: true
  - type: textarea
    id: steps-to-reproduce
    attributes:
      label: Steps to Reproduce
      description: Please list the steps to reproduce the bug. The more specific, the better!
      placeholder: "1. Go to the product page, 2. Add to cart, 3. Click checkout."
    validations:
      required: true
  - type: textarea
    id: expected-behavior
    attributes:
      label: Expected Behavior
      description: What did you expect to happen when you performed the steps above?
      placeholder: e.g., "The checkout page should open as expected."
      value: "The checkout page should open and allow me to proceed with the payment."
    validations:
      required: true
  - type: textarea
    id: actual-behavior
    attributes:
      label: Actual Behavior
      description: What actually happened when you followed the steps above? 
      placeholder: "e.g., The page fails to load or shows an error message."
      value: "The page fails to load and shows an error message saying 'Checkout Failed.'"
    validations:
      required: true
  - type: input
    id: error-message
    attributes:
      label: Error Message (if any)
      description: If you received any error message or code, please provide it here.
      placeholder: ex. "Error 404: Page not found"
    validations:
      required: false
  - type: dropdown
    id: reproducibility
    attributes:
      label: Is the issue reproducible?
      description: Can the bug be reproduced with the same steps every time, or does it happen intermittently?
      options:
        - "Always"
        - "Sometimes"
        - "Rarely"
        - "Unable to reproduce"
      default: "Always"
    validations:
      required: true
  - type: input
    id: version
    attributes:
      label: Application Version
      description: What version of the webstore are you using (if known)?
      placeholder: ex. 1.2.3
    validations:
      required: false
  - type: textarea
    id: logs
    attributes:
      label: Browser Console Logs (Optional)
      description: If you know how to access the browser console, please copy any relevant logs here. This will help us troubleshoot the issue more effectively.
      placeholder: "Paste any relevant logs here. You can open the console by pressing F12 in most browsers."
    validations:
      required: false
  - type: file
    id: screenshot
    attributes:
      label: Upload Screenshot or Video (Optional)
      description: If possible, please upload a screenshot or screen recording that demonstrates the bug.
      accept: ".jpg, .png, .mp4, .avi"
    validations:
      required: false
  - type: checkboxes
    id: terms
    attributes:
      label: Code of Conduct
      description: By submitting this bug report, you agree to follow our [Code of Conduct](https://example.com).
      options:
        - label: I agree to follow the Code of Conduct
          required: true
