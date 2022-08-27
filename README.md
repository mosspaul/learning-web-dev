# Learning Javascript

### Working with Strings
There are a few main string methods:
* length
    ```js
    let str = "String";
    let strLength = str.length // Returns 6
    ```
* slice
    ```js
    let str = "String"
    let strSlice = str.slice(-2, -4) // Returns "ri"
    ```
* substring - Basically the same as slice, but counts starting with zero

* substr - also similar to slice, takes in two arguments, first being an index, the second the lenght of the substring

* replace
    ```js
    let text = "This is a js string"
    let newText = text.replace("js", "javascript")
    ```
    To make case insensitive:
    ```js
    let text = "This is a js string"
    let newText = text.replace(/JS/i, "javascript")
    ```
* toUpperCase - fairly self explantory

* toLowerCase - same as above

* concat - or you can use \`${}` or plus signs

* trim - js version of python strip(), also trimStart and TrimEnd

* padStart and padEnd, allow for arguments with a string to put at the start and or end

* charAt
    ```js
    let text = "Hello, world";
    let char = text.charAt(0); // Returns "H"
    ```
* charCodeAt - similat to charAt but returns the unicode for that character

* charAt - can also be accomplished by just doing this
    ```js
    let text = "Hello, world";
    let char = text[0]; // Returns "H"
    ```

* split
    ```js
    let text = "Hello, world";
    text.split(","); // Splits at every comma
    text.split(" "); // Split on spaces
    text.split(""); // Splits to individual characters
    ```

### Working with conditionals

* Some examples with numbers
    ```js
    alert( 2 > 1 );  // true 
    alert( 2 == 1 ); // false 
    alert( 2 != 1 ); // true 
    ```

* Some examples with strings
    ```js
    alert( "Z" > "A" ); // true, follows dictionary, Z is greater
    alert( "Glow" > "Glee" ); // true, goes through letters until one differs and is found to be greater
    alert( "Bee" > "Be" ); // true, same as above, but if it has more letters, obviously is greater
    ```

* Some examples with different types
    ```js
    alert( "2" > 1 ); // true, string "2" becomes a number 2
    alert( "01" == 1 ); // true, string "01" becomes a number 1
    alert( 0 == false ); // true
    alert( "" == false ); // true
    alert( 0 === false ); // false, because the types are different
    ```

* Null and Undefined 
    ```js
    alert( null === undefined ); // false

    alert( null == undefined ); // true
    
    alert( null > 0 );  // (1) false
    alert( null == 0 ); // (2) false
    alert( null >= 0 ); // (3) true

    alert( undefined > 0 ); // false (1)
    alert( undefined < 0 ); // false (2)
    alert( undefined == 0 ); // false (3)
    ```

### If, and else 

* if
    ```js
    if (condition) {
        // execute code if true
    }
    ```

* else
    ```js
    if (condition) {
        // execute code if true
    } else {
        // execute code if false
    }
    ```

* else if
    ```js
    if (condition1) {
        // execute code if condition1 is true
    } else if (condition2) {
        // execute code if condition2 is true and one is false
    } else {
        // execute code if they're all false
    }
    ```
If statements can be nested

### Logical operators
* and, or and not
    ```js
    if (weather === "sunny" && temp > 35) {
        alert("Boy, it's hot out here") // and
    } else if (!(choice === "sunny" || choice === "cloudy")) {
        alert("it's not too bad") // !() represents not, and || is or
    }
    ```

### Switch statements

* switch in action
    ```js
    switch (expression) {
    case choice1:
        run this code
        break;

    case choice2:
        run this code instead
        break;

    // include as many cases as you like

    default:
        actually, just run this code
    }
    ```

### Ternary operator

* tests a condition ? if true, runs this : if false, runs this - used for returning values not executing big blocks of code
``` js
const greeting = isSunny
? `Nice weather we're having, wouldn't you say, ${name}!`
: `I hate this place`