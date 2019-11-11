# Simple data-fetching

- Enable [concurrent mode](https://kentcdodds.com/blog/how-to-enable-react-concurrent-mode)

Add an `error boundary` to take care of our suspense errors and regular errors. 

If there's an error, we throw it so our error boundary catches. 

If there's not data yet, we throw our promise. 

With concurrent mode you have no guarantee of how many times your component will render. If you create a promise during your render, make sure you are caching your promise.
