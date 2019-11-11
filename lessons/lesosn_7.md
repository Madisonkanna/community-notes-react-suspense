# Coordinate Suspending components with SuspenseList

Say you have a chat app with messages and the bottom messages load first. 
With a bigger app and code splitting, things start potting into place all over the place. Suspense list allows you to marshall that in a way that makes the user experience better.

With SuspenseList we can have a more predictable loading experience. 
More predictable loading experience even if data loads in different order.

`SuspenseList` is something you wrap around components that you suspend. They can be nested as well where you could have nested components. 

Everything that is a suspense component beneath the suspense list is managed by the suspense list. with `revealOrder`, you have the order in which the suspending components are to render. 
