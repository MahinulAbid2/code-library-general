# code-library-general

<br>
<br>

# Tricky JavaScript
```javascript
const myPromise = new Promise( (resolve, reject, name) => {
    ((nameArg) => {
        if(nameArg === "john") {
            console.log("success");
            resolve(nameArg);
        }
    })(name);
})



myPromise()
```
