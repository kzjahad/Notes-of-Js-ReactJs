
> ### Stack :-
***
`Stack` means keeping something one on **top** of the last one and taking one after one from the **top**. The basics of **js** starts with `Stack`. It's called `Call Stack` in **js**.

> ### Call Stack :-
***
A `Call Stack` contains of `Execution Context`s. But initially it's empty.

> Let's see an Example..
```javascript
    var a = 10;
    
    function sayHello(){
        console.log("Hello World!");
    }

    console.log(a);

    sayHello();
```
> When we run the codes, As usual, It creates an `Execution Context` that has two parts `Memory Component` & `Code Component`.

> In `Creation Phase`, The memory creates every defined variable as an undefined value and every defined function as it is as function [Not as `Undefined`].
***
- | Memory Component | Code Component |
  | -- | -- | 
  | a : undefined |  |
  | sayHello : function sayHello(){ console.log("Hello World!"); } |  |
> In `Execution Phase`, **js** reads every single line of code one by one & takes it also one by one to the `Code Component`.
***
- | Memory Component | Code Component |
  | -- | -- | 
  | a : undefined | var a = 10; |
  | sayHello : function sayHello(){ console.log("Hello World!"); } |  |

- | Memory Component | Code Component |
  | -- | -- | 
  | a : ~~undefined~~ **10** |  |
  | sayHello : function sayHello(){ console.log("Hello World!"); } |  |
> 1st line says to store 10 in the variable **a**.
***
> 2nd line is..
***
```javascript
    function sayHello(){
        console.log("Hello World!");
    }
```
>This line will be skipped. We initially stored it in the `Creation Phase` to the `Memory Component`, That's why `Execution Phase` skips this line.
***
- | Memory Component | Code Component |
  | -- | -- | 
  | a : 10 | console.log(a) |
  | sayHello : function sayHello(){ console.log("Hello World!"); } |  |
> 3rd line says to print the value of **a** in the console. That's why `Code Component` asks to `Memory Component` in the `Execution Phase`, Is there anything like **a** to you? As it has **a=10**, Thats's why we can see **10** in console in the place of **a**.
***
- | Memory Component | Code Component |
  | -- | -- | 
  | a : 10 | sayHello() |
  | sayHello : function sayHello(){ console.log("Hello World!"); } |  |
> 4th line says **sayHello()**. That's why `Code Component` asks to `Memory Component` in the `Execution Phase`, Is there anything like **sayHello()** to you? As it has **sayHello : function sayHello(){ console.log("Hello World!")**, `Memory Component` will give it to the `Code Component`. And, It's a **function**.
***
> As it is a **function**. It has to run the **function** again to **execute** the **function**. And When `Code Component` will try to **execute** the **function**, The miracle will happen.. Jokes a part. 
***
> **execute** the **function** means creating another `Execution Context`.
***
> Last but not the least, the summery of all of this is "When `Code Component` tries to **execute** a **function**, It creates another `Execution Context` in `Call Stack`." 
***
> ### Global Execution Context :- 
The core `Execution Context` is the `Global Execution Context`. That means, `Global Execution Context` is that, from where all other `Local Execution Context` creates. 
> 
> ### Local Execution Context :- 
It can be named by the name of the function's name as like `sayHello Execution Context`, The name could be **etc etc Execution Context**, So all other `Execution Context`'s created from `Global Execution Context`'s are `Local Execution Context`.
> `Local Execution Context` will destroy when it's done.
***
> `Global Execution Context` will destroy when everything is done. 
***
> Only the `Call Stack` will remain. 