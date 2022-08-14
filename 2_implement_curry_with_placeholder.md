Problem Link : https://bigfrontend.dev/problem/implement-curry-with-placeholder

```
function curry(fn) {
  return function curried(...args){
    const tempArgs = args.slice(0,fn.length)
    const hasPlaceholder = tempArgs.some((arg)=>arg===curry.placeholder)
    //filteredArgs = args.filter((arg)=>arg!==curry.placeholder)
    
    console.log("t",tempArgs,hasPlaceholder)
    if(!hasPlaceholder && tempArgs.length>= fn.length){
      return fn(...tempArgs)
    }
    return (...args2)=>{
      filteredArgs1 = tempArgs.filter((arg)=>arg!==curry.placeholder)
      filteredArgs2 = args2.filter((arg)=>arg!==curry.placeholder)
      const nextArgs = [...filteredArgs1,...filteredArgs2]
      nextArgs.sort((a,b)=>a-b)
      console.log(nextArgs)
      return curried(...nextArgs)
    }
  }
}
```
