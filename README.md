## JavaScript, the browser implementation of the specification ECMAScript
![Javascript_badge](https://github.com/danielurra/javascript/assets/51704179/8e7091d2-ef91-4762-878c-420ab4cd67b4)<br>
`JavaScript` has nothing to do with `Java` they are two independent programming languages, JavaScript was created by Netscape<br>
To the server, JavaScript code is merely text, just like HTML. To the web browser, however, this<br>
text has special meaning that can be interpreted differently, JavaScript has become one of the pillars of the Web.<br>
You can write **client-side** programs to be executed in the web browser, JavaScript is useful because it’s deeply integrated with the browser.<br>
Modern browsers support core JavaScript, **DOM** manipulation, the XmlHttpRequest object (used to make Ajax requests), and basic CSS. <br>
In sum, modern browsers are capable of making the most of today’s dynamic Web technologies. <br>
It’s useful because it enables the developer to manipulate the contents of a web page after it has loaded, making it possible<br>
 to provide users with instant feedback when they make a change in a form.<br>
Loading resources on demand for performance reasons, or building full-blown user interfaces that resemble desktop applications.<br>
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
## From the Browser to the Backend
JavaScript has expanded to the backend with `Node.js` or `Deno`<br>
![backend-Node-Deno](https://github.com/danielurra/javascript/assets/51704179/dee36d49-3348-4125-a491-7bd0beae2a78)<br>

## Browser Console - press F12
JavaScript changes the browser from an application for displaying documents to a platform for writing applications.<br>
<img src="images/javascript-and-browser-console.png" alt="" width="900px"><br>
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
## Grab the JavaScript code
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
