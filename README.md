# React Cards - Custom Hooks
Practice writing your own custom hooks. Code could use some refactoring.

## Step One: Read the Code
Start by downloading the app, and getting it set up:
- The app uses two APIs, the Deck of Cards API and the Pokemon API, to generate different types of cards on the page
- Play around with the app to get a sense for how it works. Draw out the component hierarchy in your pair and make sure you understand how all of the pieces fit together.

## Step Two: useFlip
Both the PokemonCard and the PlayingCard components can be flipped over when clicked on. You may have noticed that there is some duplicate code in these components. Create a hooks.js file in src/, and in that file write a custom hook called useFlip which will hold the business logic for flipping any type of card. Once you’ve written this hook, refactor PokemonCard and PlayingCard to use this custom hook.

## Step Three: useAxios in PlayingCardList
In the PlayingCardList component, we initialize an empty array in state, and add to it via an AJAX request we make with axios. Since we use axios in a few components, let’s move this logic into a function called useAxios.

## Step Four: useAxios in PokeDex
PokeDex also make AJAX requests, but this one’s a bit trickier. PlayingCardList makes a request to the same endpoint every time, but the endpoint in PokeDex depends on the name of the pokemon.
Figure out a way to modify your useAxios hook so that when you call useAxios you can just provide a base url, and when you want to add to your array of response data in state, you can provide the rest of the url.  Once you’ve done this, refactor PokeDex to use useAxios. Make sure PlayingCardList still works too!

## Comments: 
This was challenging and I ran into issues when trying to refactor the response data into the appropriate format. I had to review the solution to help me out on this one. 