## 15 JavaScript Programs using Loops

### 1. Triangle Pattern - 1. Print the below pattern using loops.
```js
1

1 2

1 2 3 

1 2 3 4 

1 2 3 4 5 
```

```js
let x = 5;
let string = "";
for(let i=1;i<=x;i++){
    for(let j=1;j<=i;j++){  
        string += j+" ";    
    }
    string += "\n";  
}
console.log(string);
```

### 2.   Write a JS code to print a 2D array
```js
let arr = [
    [1,2,3],
    [4,5,6],
    [7,8,9],
];
for(let i=0;i<arr.length;i++){
    for(let j=0;j<arr[i].length;j++){
        console.log(arr[i][j]);
    }
}
```

### 3. Write a JS code to delete all occurrence of element in given array
```js

const inputArray = [1,1,2,3,4,4,5,6,5];
const OutputArray = inputArray.filter((x,y,z)=>z.indexOf(x)===y);
console.log(OutputArray);

```
### 4.  Write a JS code to find the power of a number using for loop
```js

function power(base,exponent){
    let result = 1;
    for(let i=0;i<exponent;i++){
        result *= base;
    }
    return result;
}
console.log(power(2,3));
```
### 5. Write a JS code to print a pattern using for loop
```js
   1 

   2 2 
   
   3 3 3 
   
   4 4 4 4 
   
   5 5 5 5 5 
```
```js
let x = 5;
let string = "";
for(let i=1;i<=x;i++){
    for(let j=1;j<=i;j++){
        string += i+" ";
    }
    string += "\n";
}
console.log(string);
```

### 6.  Write a JS code to find duplicate values in a given array
```js

let arr = [1,2,3,4,5,1,2,3];
function findDuplicate(arr){
    let duplicate=[];
    for(let i=0;i<arr.length;i++){
        for(let j=i+1;j<arr.length;j++){
            if(arr[i]==arr[j] && !duplicate.includes(arr[i])){
                duplicate.push(arr[i]);
            }
        }
    }
    return duplicate;
}
console.log(findDuplicate(arr));
```

### 7.  Write a JS code to calculate the sum of digits in a number

```js
function sumOfDigits(num){
    let sum = 0;
    while(num){
        sum+= num%10;
        num = Math.floor(num/10);
    }
    return sum;
}
console.log(sumOfDigits(123));
```

### 8.  Write a JS code to find product of two arrays

```js
let arr1 = [2,3,4];
let arr2 = [5,6,7];

let product1 = arr1.reduce(function(x,y){
    return x*y;
})
let product2 = arr2.reduce(function(x1,y1){
    return x1*y1;
})
let both = product1*product2;
console.log(both);
```

### 9. Write a JS code to print the Fibonacci series for a given value of N
```js
function fibonacci(n){
    let fib = [0,1];
    for(let i=2;i<=n;i++){
        fib[i] = fib[i-1]+fib[i-2];
    }
    return fib;
}
console.log(fibonacci(10));
```

### 10.  Write a JS code to find N value in the Fibonacci series for a given number
```js
function fibonacci(n){
    if(n<=1){
        return 1;
    }
    let fib = [0,1];
    for(let i=2;i<=n;i++){
        fib[i] = fib[i-1]+fib[i-2];
    }
    return fib[n];
}
console.log(fibonacci(7));
```
### 11. Iterate through all numbers from 1 to 45. Print the following:
   - For multiples of 3 print “Fizz”
   - For multiples of 5 print “Buzz”
   - For multiples of 3 and 5 print “FizzBuzz”
```js
   
for(let i =1;i<=45;i++){
    if(i%3==0 && i%5==0){
        console.log("FizzBuzz");
    }
    else if(i%3==0){
        console.log("Fizz");
    }
    else if(i%5==0){
        console.log("Buzz");
    }
    else{
        console.log(i);
    }
}
```
### 12. Pyramid Star Pattern
 ```js
         *
        ***
       *****
      *******
     *********
 ```
```js
 let x = 5;
let string = "";
for(let i=1;i<=x;i++){
    for(j=i;j<=x;j++){
        string += " ";
    }
    for(j=1;j<=i;j++){
        string += "*";
    }
    for(j=1;j<i;j++){
        string += "*";
    }
    string += "\n";
}
console.log(string);
```
### 13. Reversed Pyramid Star Pattern
```js
            *********
             *******
              *****
               ***
                *
```
```js
let x = 5;
let string = "";
for(let i=1;i<=x;i++){
    for(j=1;j<=i;j++){
        string += " ";
    }
    for(j=i;j<=x;j++){
        string += "*";
    }
    for(j=i;j<x;j++){
        string += "*";
    }
    string += "\n";
}
console.log(string);
```

### 14. Display the sum of "n" natural numbers.
```js
let n = 10;
let sum = 0;
for(let i=0;i<=n;i++){
    sum+=i;
}
console.log(sum);
```
### 15. Loop through an array of elements and find both, the minimum and the maximum of the elements present.
```js
let array = [1,2,3,4,5,6];
let max = array[0];
let min = array[0];

for(let i=0;i<array.length;i++){
    if(array[i]<min){
        min= array[i];
    }
    if(array[i]>max){
        max = array[i];
    }
}
console.log(min + " "+ max);
```
