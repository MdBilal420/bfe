Problem Link: https://bigfrontend.dev/problem/implement-debounce-with-leading-and-trailing-option

```
function debounce(func, wait, option = {leading: false, trailing: true}) {
  // your code here
  let timerId;
  if(!option.leading && !option.trailing) return ()=>null
  
  return (...args)=>{
    const {leading,trailing} = option
    let called = false
    
    if(leading && !timerId){
      func(...args)
      called = true
    }
    clearTimeout(timerId)
    timerId = setTimeout(()=>{
      if(trailing && !called) func(...args)
      timerId = null
    },wait)
  }
}

```
