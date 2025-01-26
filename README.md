# Uncontrolled/Controlled Input Component State Desynchronization Bug

This repository demonstrates a subtle bug in a React component that mixes uncontrolled and controlled input behavior. The core issue is a desynchronization between the input's value and the component's internal state when non-numeric characters are entered into an input field that is attempting to manage numeric values.

## Bug Description:
The component uses a controlled input to manage a numeric counter.  However, the state update logic is conditional, only updating the state if the input is a valid number. If a user enters non-numeric characters, the input reflects the invalid input, but the component's state remains unchanged, leading to inconsistency and potential unexpected behavior.

## How to Reproduce:
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the behavior when entering non-numeric characters in the input field.

## Solution:
The solution addresses the issue by ensuring that the state is always updated to reflect the input value, regardless of whether the input is numeric.  Error handling (e.g., preventing non-numeric characters or gracefully handling invalid input) can be added separately.