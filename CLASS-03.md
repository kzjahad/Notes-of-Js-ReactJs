> ### Hoisting :-
***
In Javascript, The way in the `Creation Phase`, memory is being allocated, It's called `Hoisting`. 
That means, When the `Creation Phase` run, `Variable & Function` allocate in memory in the `Creation Phase`. That's why in the `Execution Phase`, we can find them and Don't show any Error. The process of allocating is basically `Hoisting`. 

***
If there are **Parameters** in **Function**, The Value of the **Parameters** store before in the `Memory Component` before starting the `Creation Phase`.

***
`Code Component` always start Executing from the last left of the line. 

***
**Function Declaration** never execute the **function** in the `Execution Phase`. It execute when it has **called**.

***
***
# FAQ in Interview from JS
***
> ## Function Statement / Function Declaration :-
> 
> When we create something by `Function` keyword, It's called **Function Statement or Function Declaration**.
> ***
> ## Function Expression  :-
> In js, Every single line is an expression. But **Function Expression** is, When a whole `Function` stored in a **Variable** is called a **Function Expression**.
> ***  
> ### What is the difference between Function Statement and Function Expression?
> The difference between **Function Statement** and **Function Expression** is -
> 
> In **Function Statement**, When a **Function** calls in the `Execution Phase` before declaration, It doesn't shows any error. Because the **Function** has already stored to the `Memory Component` in the `Creation Phase`.
> 
> But, In **Function Expression**, When a **Function** calls in the `Execution Phase` before declaration, It shows a **type error**. Because, the **Function** has stored in a **variable** as a **variable**. And, **Variable** always store as **undefined** in the `Creation Phase` to the `Memory Component`.
> 
> And, when a **Function** calls in the `Execution Phase` after declaration, It works! Because, As the **Function** has stored in a **Variable**. Initially it has created as **undefined** in the `Creation Phase`. And when in `Execution Phase`, the **variable** sees a value of the **variable** to store it at the place of **undefined**. That's why, It can easily detect it.  
> ***
> **type error** means, The type of you are calling something isn't the same **type**.
> ***
> Btw, **Errors** in js are,
> - Reference Error - That means, `Code Component` trying to **Execute** something, which doesn't exist in `Memory Component`. 
> - Type Error - That means, `Code Component` trying to **Execute** something in a specific way of calling a type, which isn't the similar type.
> ***
> ## Anonymous Function :-
> A **Function** without a name is called an **Anonymous Function**. An **Anonymous Function** must call right after the **Function Declaration**. An **Anonymous Function** is also known as **IIFE**. **IIFE** stands for **Immediately Invoked Function Expression**.
>
> For example,
 ```javascript
    (function () {
        console.log("Hello, Anonymous Function!");
    }) ();
```
> **Anonymous Function** wraps with a first bracket, and then Immediately calls right after wrapping.
> 
> It's not possible to call an **Anonymous Function** more than one time.
>
> **Anonymous Function** doesn't allocate to the **Memory Component**. That means, **Anonymous Function** doesn't hoist.
> ***
> ## Arrow Function :-
 ```javascript
 // Function Expression Arrow Function -
    var arrowFunction = () => {
        console.log("Hello, Function Expression Arrow Function!");
    };
// Anonymous Arrow Function -
    ( = () =>{
        console.log("Hello, Anonymous Arrow Function!");
    })();
```
> ***
> ## **Parameters** & **Arguments** in Function :-
```javascript
    function sayHello(message) {
        console.log(message);
    };

    sayHello("Hello World!");
```
> Here **Hello World!** is **Argument** & **message** is **Parameter**.
> 
> When we call a **Function**, that time what we pass is **Argument**. And what we receive from function is **Parameter**.
> ***
> ## First-Class Function :-
> When a **Function** passes another **Function** as **Argument** and receives as **Parameter** is called a **First-Class Function**. Or When a **Function** returns another **Function** is called a **First-Class Function**. And if it does both.
```javascript
// Structure of First-Class Function

//  When a Function passes another Function as Argument and receives as Parameter -
    function call(add) {
        add(4, 5);
    };

    function sum(a, b) {
        console.log(a+b);
    };

    call(sum);

// Or
    function call(add) {
        add(4, 5);
    };

    call(function sum(a, b) {
        console.log(a+b);
    };);

//  When a Function returns another Function -
    function call () {
        function sum (a, b) {
            console.log(a+b);
        }
        return sum;
    }

    var add = call(5, 5);

```
>***
> ## Call-Back Function :-
> The **Function** which being passed as **Argument** and received as **Parameter** by **First-Class Function** is call a **Call-Back Function**.
> ***