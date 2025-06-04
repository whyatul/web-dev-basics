# All About JavaScript 
### JavaScript OutPut
JavaScript has several ways to display and handle output

#### 1. Console Output
```
    console.log("Hello world!");
    console.log(43);
    console.log({name:"John", age:42});
    console.log("Value:", variable, "Type:", typeof variable);

    //Other Console Methods

    console.error("This is an error message");
    console.warn("This is a warning");
    console.info("This is info");
    console.table([{name: "Alice", age: 25}, {name: "Bob", age: 30}]);
    console.group("Group Title");
    console.log("Grouped message");
    console.groupEnd();
```
#### 2. DOM Manipulation (Browser)
```
document.write("Hello World!"); // Avoid using this
//Using document.write() after an HTML document is loaded, will delete all existing HTML

// HTML elements
document.getElementById("myDiv").innerHTML = "<h1>Hello World!</h1>";
document.getElementById("myDiv").textContent = "Plain text only";

// Creating elements
const newElement = document.createElement("p");
newElement.textContent = "Dynamic content";
document.body.appendChild(newElement);
```
#### 3. Alert Dialogs(Browser)
```
alert("Simple message");
const userInput = prompt("Enter your name:");
const confirmation = confirm("Are you sure?");
```
#### 4. Return Values
```
function calculateSum(a, b) {
    return a + b; // This is output that can be used elsewhere
}

const result = calculateSum(5, 3);
console.log(result); // 8
```

#### 5. Template Literals
```
const name = "Alice";
const age = 30;
console.log(`Hello ${name}, you are ${age} years old`);

// Multi-line output
const message = `
    Name: ${name}
    Age: ${age}
    Status: Active
`;
console.log(message);
```

#### 6. JSON Output
```
const obj = {name: "John", hobbies: ["reading", "coding"]};
console.log(JSON.stringify(obj, null, 2)); // Pretty printed JSON
```
#### 7. Error Handling Output
```
try {
    // Some risky code
    throw new Error("Something went wrong!");
} catch (error) {
    console.error("Error:", error.message);
    console.error("Stack:", error.stack);
}
```
#### 8. Formatting Output
```
// Numbers
const num = 3.14159;
console.log(num.toFixed(2)); // "3.14"
console.log(num.toPrecision(3)); // "3.14"

// Dates
const now = new Date();
console.log(now.toLocaleDateString()); // "12/25/2023"
console.log(now.toISOString()); // "2023-12-25T10:30:00.000Z"
```