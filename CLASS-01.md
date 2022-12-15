
# JavaScript

> ### Variable :-

***
A `Variable` is a `Container` where we can **store** something.

> ### Run a **js** file :-

***
When we run a file of few Js codes, It immediately creates an `Execution Context` .

> ### How is an `Execution Context`?

***

`Execution context` is is a Square Box.

- An `Execution Context` has two **Parts**.

  - Memory Component / Variable Environment
  - Code Component

- An `Execution Context` has two **Phases**.

  - Creation Phase / Memory Creation Phase
  - Execution Phase

> ### So

***
- Run a **js** file, Create the `Execution Context`, then initially starts with the `Creation Phase`.
- When the `Creation Phase` starts, **js** will read the codes from the first.
    - So, What is `Creation Phase`?
      - `Creation Phase` means It's a phase where js creates something. 
    - What creates in the `Creation Phase`?
      - **Memory**.
    - Where the **Memory** creates?
      - In `Memory Component`.

**Memory means `Variable` & `Function`.These two are the only memory of every programming Languages.**

***

**That's why, the other name of `"Creation Phase"` is `"Memory Creation Phase"` and `"Memory Component"` is `"Variable Environment"`.**

The only work of `Creation Phase` is create something in `Memory Component` and store the value of every variable nothing but as `Undefined`.


`Creation Phase` skips the line if it isn't a **variable or function**.

> ### Then

***
- After creating every variable as `Undefined` it starts the next phase which is `"Execution Phase"`. 
- `Execution Phase` reads every single line of code one by one.
- By reading a line of code, **js** takes it to the `Code Component`.
- Then the execution of the codes starts in `Code Component`. 

> ### How does `Code Component` **execute** the codes? 

***
> Let's see an Example..
```javascript
    var a = 10;
    console.log("a");
    console.log("b");
    var b = "Jihad";
```
> When we run the codes, As usual, It creates an `Execution Context` that has two parts `Memory Component` & `Code Component`.

> In `Creation Phase`, The memory creates every defined variable as an undefined value.
***
- | Memory Component | Code Component |
  | -- | -- | 
  | a : undefined |  |
  | b : undefined |  |
> In `Execution Phase`, **js** reads every single line of code one by one & takes it also one by one to the `Code Component`.
***
- | Memory Component | Code Component |
  | -- | -- | 
  | a : undefined | var a = 10; |
  | b : undefined |  |

- | Memory Component | Code Component |
  | -- | -- | 
  | a : ~~undefined~~ **10** | |
  | b : undefined |  |
> 1st line says to store 10 in the variable **a**.
***

- | Memory Component | Code Component |
  | -- | -- | 
  | a : **10** | console.log("a"); |
  | b : undefined |  |
> 2nd line says to print the value of **a** in the console. That's why `Code Component` asks to `Memory Component` in the `Execution Phase`, Is there anything like **a** to you? As it has **a=10**, Thats's why we can see **10** in console in the place of **a**.
***

- | Memory Component | Code Component |
  | -- | -- | 
  | a : **10** | console.log("b"); |
  | b : undefined |  |
> 3rd line says to print the value of **b** in the console. That's why `Code Component` asks to `Memory Component` in the `Execution Phase` , Is there anything like **b** to you? As it has **b=undefined**, Thats's why we can see **undefined** in console in the place of **b**.
> 
> Note: We can see in line 4th is **b="Jihad"**. But it hasn't defined yet because **js** executes the line of codes one by one.
***
- | Memory Component | Code Component |
  | -- | -- | 
  | a : **10** | var b = "Jihad"; |
  | b : undefined |  |
- | Memory Component | Code Component |
  | -- | -- | 
  | a : **10** |  |
  | b : ~~undefined~~ **"Jihad"** |  |
> 4th line says to to store **"Jihad"** in the variable **b**.
> 
> That means, In 3rd line, The value of **b** was till undefined. Now in 4th line, It has defined and the value of **b** is stored in `Memory Component` as **"Jihad"**. 
***

After completing `Creation Phase` & `Execution Phase`, **js** will remove the `Execution Context`. 
