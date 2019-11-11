# Suspense Image

Loading images can be hard as we hand async state to browser. Suspense image lets us pre-load images into the browser's cache. 

Create a custom image component and make a promise in render. 

```javascript
//Create Cache 
const imgResourceCache = {}
``

Switch this to image wrapper. We want to say if this source is not in my cache, then we have no guarantee of knowing whether the browser displays this image. 
```javascript
resource = preloadimage(src)
//first check (let resource) and see if we have a source. We assume if the source remains unchanged or if the src url remains unchanged then we should have the same thing
```

## Extra credit exercise

Change our pokemon resource and make it so the pokemon resource has a data property that we can read, then make it so the pokemon resource has an image property. We can get our request for our image and data at the same time. This is part of the render as you fetch concept. 