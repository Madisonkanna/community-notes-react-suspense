# Suspense with a custom hook

Create a `pokemon` resource hook. 

We’ll need a pokemon name. What’s the API we are looking for? We need an `isPending.`

We return the pokemon resource and isPending. Now we no longer have start transition or resource. Anytime stuff changes we’re going to do this in a React `useLayout` effect. There's currently a bug around `useEffect` so we use `useLayoutEffect.`

`useLayoutEffect` runs before that browser paint, and `useEffect` runs after. 

Most of the time the code you have running doesn’t need to run before the paint.