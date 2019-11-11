# Render as you fetch

## Concept: get the data as soon as you have the info you need for the data.   

Render as you fetch allows you to get the data at the same time your code uses that data. In the future your router will likely say "On this route, I need this data" or something similar.

With suspense we initially show loading screen and resolve. If we select a second pokemon, it waits for a second before showing the fallback. This is because if your async things happen fast, there's no reason to show the fallback. Just go from one to another. 

To refactor to use suspense:
- Get rid of error and just use `error boundary`
- Refactor to be left with `fetchPokemon` and we add it in our app. 
- Create a mechanism for getting the resource down to our info, so we create `PokemonOnResource` in `React.UseState`. Instead of basing things off the pokemon name, we base it off the pokemon resource. 

# Additional resources

 [Why "Render As You Fetch" Matters](https://twitter.com/kentcdodds/status/1191922859762843649) 