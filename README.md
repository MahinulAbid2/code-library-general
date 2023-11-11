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

<br>
<br>
<br>

# Use of promise 
If password is correct, it promises an object<br>
If the password is wrong it promises an error 

```javascript
const x = (password) => {
    const a = "here is your data";
    return new Promise( (resolve, reject ) => {
        if(password === "helloworld") {
            resolve(a);
        }
        else {
            reject(`Error: The password is wrong`);
        }
    })
}


x("helloworld")

.then( ( res ) => {
    console.log(res);
})

.catch( ( err ) => {
    console.log(err);
} )
```

<br>
<br>

# behaviour await

```javascript
const getData = async () => {  //created async function

    console.log("testing")
    let y = await "Hello World";
    console.log(y);
    console.log("testing Two")
    
}

getData(); 
console.log(1);
console.log(2);

```
<br>

```
output:

testing
1
2
Hello World
testing Two
```
