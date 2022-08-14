Problem Link : https://bigfrontend.dev/problem/implement-curry

```function curry(fn) {
  // your code here
  return function curried(...args){
    if(args.length>=fn.length) return fn(...args)
    return (...args2) => curried(...args,...args2)
  }
}```
