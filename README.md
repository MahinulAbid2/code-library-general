# code-library-general

<br>
<br>

# Tricky JavaScript
```javascript

const x = () => {
    return function () {
        console.log("hello");
    }
}

x()(); // hello = in the console
```


<br>
<br>

# basic usuage of async
```javascript
const x = async () =>{
    for(let i =0; i < 100000000; i++) {
        if( i == 10000000) {
            return ( i );
        }
    }
}

x().then( (res ) => {
    console.log(res);
})

console.log("hello world");

```
> result will be : 

<br>

> hello world 

<br>

> 10000000 

<br>

> Even if i called the x()  before hello world console for its async functionalities, x() result was logged in console after printing hello world
