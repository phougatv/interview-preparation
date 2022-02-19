# C# questions and answers

## 1. What is the difference between `class` and `struct`?
> class&#8594;
> ---
> 
> struct&#8594;
> ---
> 
## 2. What is the difference between `const` and `readonly`?
> `const`&#8594;<br>
> 1. Constants are implicitly `static`, you can use `ClassName.ConstantName` notation to access them.<br>
> 2. Use it to declare a constant field or constant local. They are not variables and cannot be modified, don't create a constant to represent any information that you expect to change at any time.<br>
> 3. If you're confident that the value of the constant won't change, use a `const`. Example: `public const int GMS_IN_A_KG = 1000;`
> 
> `readonly`&#8594;<br>
> 1. Readonly is instance type, unless you explicitly specifies it `static`.<br>
> 2. The assignment to the `readonly` field can only occur as part of the declaration or in a constructor in the same class.<br>
> 3. A `readonly` field can't be assigned after the constructor exits. This rule has different implications for value types and reference types:<br>
>   **i.** Because value types directly contain their data, a field that is a `readonly` value type is immutable.<br>
>   **ii.** Because reference types contain a reference to their data, a field that is a `readonly` reference type must always refer to the same object. That object isn't immutable. The `readonly` modifier prevents the field from being replaced by a different instance of the reference type. However, the modifier doesn't prevent the instance data of the field from being modified through the read-only field.<br>
> 4. An externally visible type that contains an externally visible read-only field that is a mutable reference type may be a security vulnerability and may trigger warning CA2104 : **_Do not declare read only mutable reference types_**.
> 5. If you have a value that may change (e.g. w.r.t. precision) or when in doubt, use a `readonly`. Example: `public readonly float PI = 3.14;`
>
> **A subtle difference&#8594;**<br>
> Consider a class defined in `AssemblyA`:<br>
> ```
> public class ConstVsReadonly
> {
>    public const int ConstantInt = 10;
>    public readonly int ReadonlyInt = 44;
> }
> ```
> `AssemblyB` references `AssemblyA` and uses these values. Upon compilation:<br>
>   1. In case of `ConstantInt`, the value&#8594;`10` is _baked into_ the `AssemblyB`'s IL, means if in future I update `ConstantInt` to 20, **_AssemblyB would still have 10 till I recompile it_**.<br>
>   2. In case of `ReadonlyInt`, it is like a `ref` to a memory location. This means that the value is not baked into the `AssemblyB`'s IL and if in future memory location is updated, `AssemblyB` gets the new value without recompilation. So if `ReadonlyInt` is updated to 7, you only need to compile `AssemblyA`, and all clients do not need to be recompiled.

_References&#8594;_
1. [_Difference between const and readonly in C#_](https://stackoverflow.com/questions/55984/what-is-the-difference-between-const-and-readonly-in-c#answers-header)
2. [_const (MSDN)_](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/const)
3. [_readonly (MSDN)_](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/readonly)
