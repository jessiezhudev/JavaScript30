## Target:
When you type the key words, the filtered city list appears.

## Skills we need to grasp:
1. `fetch()` function to fetch ajax requests
2. Regex to match the key word with the list

## Steps:
1. Use `fetch()` function to fetch a list of cities. Pay attention to this function, it returns a promise.
2. Define a function named `findMatches`. It takes two parameters `wordToMatch` and `cities`. It uses Regex to match the key word with the cities in the list.
3. Add event listeners `change` and `keyup` for the `input`. Define a function named `displayMatches`
4. In the function `displayMatches`.
    
    - Get the `matchResult` by geting the value of the `input` and use `findMatches` function
    - Generating the `html` by mapping through `matchResult`. (Remember to add `join('')`)
    - Replace the `innerHTML` of `suggestions` by `html`
5. Highlight the key word in `html`
by `replace`. Add comma to the place's population by `numberWithCommas`

## Notes
Regex is quite important in programming, later I need to do more exercises to grasp it