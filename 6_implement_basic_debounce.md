Problem Link: https://bigfrontend.dev/problem/implement-basic-debounce

```
function debounce(func, wait) {
  // your code here
  let timer;
  return (...args)=>{
    if(timer) clearTimeout(timer)
    timer = setTimeout(()=>{
      func(...args)
    },wait)
  }
}
```
