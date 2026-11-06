# saucedemo-e2e-suite
End-to-end tests for saucedemo.com written with Playwright and TypeScript, structured with the Page Object Model.

## Structure
- `pages/` : page objects (LoginPage, InventoryPage, CartPage) that hold locators and actions for each page
- `tests/` : test files that read like user flows and contain no raw login locators

## What's covered
- Login, valid and invalid
- Add and remove an item from the cart
- Cart page lists the added item
- Logout

## Setup
npm install
npx playwright install

## Run the tests
npx playwright test

## Notes
- Tests run in Chromium, Firefox and WebKit.
- The cart test waits for exactly one cart item before checking its name, which fixed a WebKit-only timing failure.