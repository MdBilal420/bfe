Problem Link: https://bigfrontend.dev/problem/implement-Array-prototype.flat

```
function flat(arr, depth = 1) {
  let flatArr = arr.reduce((acc,val)=>{ 
    if(Array.isArray(val) && depth>0 ){
      acc.push(...flat(val,depth-1))
    }else{
      acc.push(val)
    }
    return acc
    },[])
    return flatArr
}
```
