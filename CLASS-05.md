> ### Scope :-
***
**Scope** in Javascript refers to the accessibility of a **Memory (Variable & Function)**. 
***
> ### Scope Chain :-
***
In the `Local Execution Context`'s `Execution Phase`, When the `Code Component` tries to **execute** a **Memory (Variable & Function)** or checks the **Scope** of the **Memory** from the `Memory Component`, And if it doesn't exist, The `Local Execution Context`'s `Memory Component` checks it in its parents `Memory Component`, And if it doesn't exist yet, The process continues. A chain created in this way is called a **Scope Chain**.
>
Why it's **Scope Chain**? - As the chain creates for finding / Checking the **Scope**, that's why it's called **Scope Chain**.
***
## The Parent of `Global Execution Context` is **Null**.
> ### Lexical Environment :-
***
**Lexical Environment** is the `Memory Component` of an `Execution Context` and the **Lexical Environment** of its parent.
***
> ### Shadowing :-
***
When there is more than one **Variable** by the same name in the same **Lexical Environment** is called **Shadowing**. **Shadowing** accepts the first value from its **Lexical Environment**. 
