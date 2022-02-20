# .NET questions and answers

## Memory management - [ref](https://docs.microsoft.com/en-us/dotnet/standard/managed-code)
### What is _"managed code"_?
> Code whose execution is managed by a runtime (_in this case CLR, regardless of the implementation for e.g. Mono, .NET Framework, .NET Core/.NET 5+_) is called managed code.<br/>
> CLR is in charge of taking the managed code, compiling it into machine code then executing it. On top of that, it provides important services.<br/>
> Just to name a few&#8594;
>   _1. Automatic memory management
>   _2. Security boundaries
>   _3. Type safety
