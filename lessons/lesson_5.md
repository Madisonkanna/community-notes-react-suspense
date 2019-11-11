# Cache resources


## State coming from your server is not UI state but a cache of state. 

You determine how long that cache is around for. You can persist it in memory and get it later if needed. 

Caches are a hard problem in cs. Be careful of stale data bugs, memory leaks. 

Instead of creating a new resource every time, we can check if the resource is already there. We create our `pokemonResourceCache` with our key being the name of our pokemona nd the value is the resource created for that pokemon. 

-If resource is there, use it.
-If resource is not, create it. 

Q: What happens if we want to persist through refresh?
A: Use same kinds of techniques that you’d do for persisting anything.
Using Suspense would not change what you think of it, it’s more about *what* you are caching.