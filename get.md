# JavaScript

The first popular web browser with a graphical user interface, Mosaic, was released in 1993. Accessible to non-technical people, it played a prominent role in the rapid growth of the early World Wide Web. The lead developers of Mosaic then founded the Netscape corporation, which released a more polished browser, Netscape Navigator, in 1994. This quickly became the most-used.

During these formative years of the Web, web pages could only be static, lacking the capability for dynamic behavior after the page was loaded in the browser. There was a desire in the flourishing web development scene to remove this limitation, so in 1995, Netscape decided to add a programming language to Navigator. They pursued two routes to achieve this: collaborating with Sun Microsystems to embed the Java language, while also hiring Brendan Eich to embed the Scheme language.


Microsoft debuted Internet Explorer in 1995, leading to a browser war with Netscape. On the JavaScript front, Microsoft created its own interpreter called JScript.

There is no built-in Input/output functionality in JavaScript, instead it is provided by the run-time environment. The ECMAScript specification in edition 5.1 mentions that "there are no provisions in this specification for input of external data or output of computed results".[78] However, most runtime environments have a console object that can be used to print output.[79] Here is a minimalist "Hello, World!" program in JavaScript in a runtime environment with a console object:
```js
console.log("Hello, World!");
```

A simple recursive function to calculate the factorial of a natural number:
```js
function factorial(n) {
    
    if (isNaN(n)) {
        console.error("Non-numerical argument not allowed.");
        return NaN; 
    }
    if (n === 0)
        return 1;
    if (n < 0)
        return undefined; 
    if (n % 1) {
        console.warn(`${n} will be rounded to the closest integer. For non-integers consider using gamma function instead.`);
        n = Math.round(n);
    }
    const recursivelyCompute = a => a > 1 ? a * recursivelyCompute(a - 1) : 1; 
    return recursivelyCompute(n);
}

factorial(3);
```

An anonymous function (or lambda):
```js
const counter = function() {
    let count = 0;
    return function() {
        return ++count;
    }
};

const x = counter();
x();
x();
x();
```
THE END!!!