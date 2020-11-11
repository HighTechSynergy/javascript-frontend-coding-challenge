# High-Tech Synergy Frontend Take-home Exercise

Hi there! Here is a coding exercise to help us assess your technical skills.
Please plan to spend no more than 4 hours on this. We understand we may not be
the only company asking for an exercise from you and want to be respectful of
your time. We recommend you focus on the core
requirements first, then work on any additional features if you have the time.

By 8 hours in, please feel free to stop working and explain what refactors /
code organization / enhancements you would have made with more time in the
MYSOLUTION.md file.

If you have any questions at any point, please reach us on email.

## Submission

Please **fork** this repository and commit all your changes to it.
When you're done, send us the email with your Github repository URL.

## Overview

We’ve built a simple Autocomplete/Typeahead component in vanilla ES2015 that
lets you type in a query and shows a list of matching results in a dropdown.

To see this component in action, let's set up the repo:

1. Run `npm install`
2. Run `npm start` (runs `webpack-dev-server`)
3. Open `http://localhost:8080` on your browser.

Type "new" in the input, and you'll get a list of matching US states that start
with "new".


## Task

Currently, the component can only query against a static data array. Your task is to:

1. Enhance the component so that it also accepts an HTTP endpoint as data source.

    For example, if you wire up the component to
    `https://api.github.com/search/users?q={query}&per_page={numOfResults}`,
    and if you type `foo` in the input, the component dropdown should show
    Github users with logins that start with `foo`. When you select a user from
    the results, `item` in the `onSelect(item)` callback should be the selected
    Github user's id.

    (The enhanced initialised component only needs to work with either a data array or a
    HTTP source, not both at the same time.)

2. Implement keyboard shortcuts to navigate the results dropdown using up/down
   arrow keys and to select a result using the Enter key.

3. When item in dropdown is selected by mouse click or Enter key, show the selected item in a
search field (same as Google is doing it).

Uncomment the relevant sections in `index.js` and `index.html` to implement a
demo that looks like this:

![Demo example screenshot](demo-example.png)


## Requirements

- The component should be reusable. It should be possible to have multiple
  instances of the component on the same page.
- The "States" example that uses a data array should be enhanced with your code and continue to work.
- Your component should work correctly in Chrome, don’t worry about
  cross-browser compatibility.
- You don't need to preserve any of the existing code; feel free to modify them
  as you wish.
- New APIs and your notes should be documented in `MYSOLUTION.md`.
