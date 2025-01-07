# Intermittent Tailwind CSS Class Application Failure

This repository demonstrates a bug where Tailwind CSS classes are not consistently applied, particularly within complex responsive designs.  The issue is not immediately apparent through standard debugging methods.

## Bug Description

Even with correctly configured Tailwind CSS and seemingly valid class names, some styles fail to apply while others, even with identical class names in different contexts, work correctly. Browser developer tools show no clear errors.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` (or `yarn install`) to install the dependencies.
3. Open `bug.html` in your browser.
4. Observe the inconsistent application of Tailwind CSS classes.  Some elements will be styled correctly, while others will not, despite using identical or similar class names.

## Solution

The solution is provided in `bugSolution.html` and involves adding a purge configuration in Tailwind's config file which solved the issue.  Specifically, carefully adding the purge option to ensure all necessary css is included.