## JavaScript, the browser implementation of the specification ECMAScript
**ECMA** stands for `European Computer Manufacturers Association`<br>

![Javascript_badge](https://github.com/danielurra/javascript/assets/51704179/8e7091d2-ef91-4762-878c-420ab4cd67b4)<br>
`JavaScript` has nothing to do with `Java` they are two independent programming languages, JavaScript was created by Netscape<br>
To the server, JavaScript code is merely text, just like HTML. To the web browser, however, this text has special meaning <br>
that can be interpreted differently, JavaScript has become one of the pillars of the Web.<br>
You can write **client-side** programs to be executed in the web browser, JavaScript is useful because it’s deeply integrated with the browser.<br>
JavaScript uses what’s referred to as an `event-driven` model of execution. When you embed JavaScript code in a web page, <br>
it isn’t run until the event it’s associated with is triggered.<br>
The browser integration allows programmers to manipulate various aspects of the browser behavior, as well as objects included on the page.<br>
JavaScript uses what’s referred to as an event-driven model of execution. <br>
When you embed JavaScript code in a web page, it isn’t run until the event it’s associated with is triggered.<br>
The types of events that can call JavaScript include:<br>
* Loading the page
* Leaving the page
* Interacting with a form element
* Clicking a link
* Scrolling up or down
Plenty of other events are available, too.<br>
## Document Object Model - DOM
Modern browsers support core JavaScript, **DOM** manipulation, the XmlHttpRequest object (used to make Ajax requests), and basic CSS. <br>
In sum, modern browsers are capable of making the most of today’s dynamic Web technologies. <br>
It’s useful because it enables the developer to manipulate the contents of a web page after it has loaded, making it possible<br>
 to provide users with instant feedback when they make a change in a form.<br>
Loading resources on demand for performance reasons, or building full-blown user interfaces that resemble desktop applications.<br>

## Window object - top level of the DOM Hierarchy
Type **window** and press enter to see the `window object` along with a long list of **methods** and **properties**.<br>
![window-object](https://github.com/danielurra/javascript/assets/51704179/d2837180-6b39-44b9-ad8f-621e6522ec19)<br>
Just as an example if you want to use the console to go back to the previous page, then you can use the following command:<br>
```javascript
window.history.back();
```
<img width="502" alt="window-history-back" src="https://github.com/danielurra/javascript/assets/51704179/13f53c01-4433-4c4d-bcf5-8a59a900df81"><br>
<img width="503" alt="window-history-back-02" src="https://github.com/danielurra/javascript/assets/51704179/fff1b064-44bc-4ddd-a698-7167368a51a7"><br>

## Document object and its body
Type **document** and press enter to see the `document object`<br>
```javascript
document
```
<img width="1339" alt="document-body-v2" src="https://github.com/danielurra/javascript/assets/51704179/0ed5a155-024a-4da7-9ca7-0bfb9a726527"><br>
Another way would be to start from **window** (top level) and after that **document**:<br>
```javascript
window.document
```
<img width="1339" alt="window document" src="https://github.com/danielurra/javascript/assets/51704179/007caf4c-fced-45cc-b49f-5434c1ff02d6"><br>
## Document object methods and properties
Use the following command to see a long list of methods and properties of the **document object:**<br>
```javascript
console.dir(document);
```
<img width="349" alt="console-dir" src="https://github.com/danielurra/javascript/assets/51704179/b74d8eca-c110-4cac-83a7-0a87641ec5d2"><br>

## Browser interpreting JavaScript<br>
```javascript
document.body.innerHTML = "Hello World"
```
![document body innerhtml](https://github.com/danielurra/javascript/assets/51704179/9420ff43-a156-4a1e-9d6a-c905f2271933)<br>
The **innerHTML** will give you basically everything, all the HTML, which is inside the element.<br>
That's how we can insert HTML, **innerHTML** property of the `document.body` element's HTML.

## Browser Console - press F12
JavaScript changes the browser from an application for displaying documents to a platform for writing applications.<br>
<img src="images/javascript-and-browser-console.png" alt="" width="900px"><br>

## From the Browser to the Backend
JavaScript has expanded to the backend with `Node.js` or `Deno`<br>
![backend-Node-Deno](https://github.com/danielurra/javascript/assets/51704179/dee36d49-3348-4125-a491-7bd0beae2a78)<br>
## Addition example
The image below shows one small example of what can be done with JavaScript<br>
Notice that values are entered by filling two browser's input boxes but the result is only shown in the browser console (F12)<br>
![addition](https://github.com/danielurra/javascript/assets/51704179/62264941-ee3e-4fe4-8db0-659228b1b385)<br>

## Grab the HTML code
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>JavaScript</title>
    <script src="untyped-mitigation.js" defer></script>
  </head>
  <body>
    <input type="number" id="num1" placeholder="Number 1" />
    <input type="number" id="num2" placeholder="Number 2" />
    <button>Addition</button>
  </body>
</html>
```
## Working with numbers in JavaScript 
Do NOT fall into the wrong **data type** when working with numbers.<br>
JavaScript is a **loosely-typed** scripting language, and it will automatically convert any value to a string when it needs to.<br>
To avoid numbers from being considered as strings we must specify the **data type** by using `typeof num === 'number'`.<br>
![typeof_num_number](https://github.com/danielurra/javascript/assets/51704179/e23827c1-f552-403c-9e2c-c8646e9bb482)<br>
If we do not take meticulous care of the **data type**, we may easily get in trouble and our numbers will be **concatenated instead of added**.<br>
```javascript
const button = document.querySelector("button");
const input1 = document.getElementById("num1");
const input2 = document.getElementById("num2");

function add(num1, num2) {
  if ( typeof num1 === 'Number' && typeof num2 === 'Number' ){
    return num1 + num2;
  } else {
    return +num1 + +num2;
  }
}

button.addEventListener("click", function() {
  console.log(add(input1.value, input2.value));
});
```
## You better test, never assume anything
We can make use of **"typeof"** operator to test and see if we are getting the wrong data type.<br>
```javascript
function calculateValue(num) {
 if (typeof num !== 'number') {
 throw new TypeError(`Value [${num}] is not a number.`);
 }
}
```
