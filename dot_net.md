# .NET questions and answers

## Memory management - [ref](https://docs.microsoft.com/en-us/dotnet/standard/managed-code)
### What is _"managed code"_?
> Code whose execution is managed by a runtime (_in this case CLR, regardless of the implementation for e.g. Mono, .NET Framework, .NET Core/.NET 5+_) is called **_managed code_**.
> <br/>
> <br/>
> CLR is in charge of taking the managed code, compiling it into machine code then executing it. On top of that, it provides important services such as, _automatic memory management, security boundaries, and type safety_ just to name a few.

### Value / Reference types memory allocation
> [The Truth About Value Types](https://docs.microsoft.com/en-us/archive/blogs/ericlippert/the-truth-about-value-types)<br/>
> [The Stack Is An Implementation Detail, Part One](https://ericlippert.com/2009/04/27/the-stack-is-an-implementation-detail-part-one/)<br/>
> [The Stack Is An Implementation Detail, Part Two](https://ericlippert.com/2009/05/04/the-stack-is-an-implementation-detail-part-two/)<br/>
