Problem Link : https://bigfrontend.dev/problem/implement-basic-throttle

```
function throttle(func, delay) {
 let lastArgs = null, timer = null;

 return (...args)=>{
   if(!timer){
     func(...args)
     timer = setTimeout(()=>{
       if(lastArgs){
         func(...lastArgs)
         lastArgs = null
       }
       timer = null
     },delay)
   }else{
     lastArgs = args
     return ;
   }
 }
}
```
