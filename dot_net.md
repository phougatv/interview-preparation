# .NET questions and answers

## 1. Memory management - [ref](https://docs.microsoft.com/en-us/dotnet/standard/managed-code)

### 1.1 [What is _"Managed Code"_?](https://docs.microsoft.com/en-us/dotnet/standard/managed-code#what-is-managed-code)
> Code whose execution is managed by a runtime (_in this case CLR, regardless of the implementation for e.g. Mono, .NET Framework, .NET Core/.NET 5+_) is called **_managed code_**.<br/>
> Managed code is written in one of the high-level languages that can be run on top of .NET such as C#, F# and others.
> <br/>
> <br/>
> CLR is in charge of taking the managed code, compiling it into machine code then executing it. On top of that, it provides important services such as, _automatic memory management, security boundaries, and type safety_ just to name a few.

#### 1.1.1 [Intermediate Language](https://docs.microsoft.com/en-us/dotnet/standard/managed-code#intermediate-language--execution)
> IL (intermediate language) is a product of compilation of code written in high-level .NET languages.<br/>
> Intermediate Language is sometimes also called Common Intermediate Language (CIL) or Microsoft Intermediate Language (MSIL).<br/>

#### 1.1.2 [Unmanaged code interoperability](https://docs.microsoft.com/en-us/dotnet/standard/managed-code#unmanaged-code-interoperability)
> When the runtime allows passing the boundaries between managed and unmanaged world, it is called **interoprability** or **interop**.

### 1.2 [Automatic Memory Management](https://docs.microsoft.com/en-us/dotnet/standard/automatic-memory-management#automatic-memory-management)
> It is a service provided by CLR during [Managed Execution](https://docs.microsoft.com/en-us/dotnet/standard/managed-execution-process#managed-execution-process).
> The CLR's GC (garbage collector) manages the allocation and release of memory for an application.

#### 1.2.1 [Allocating Memory](https://docs.microsoft.com/en-us/dotnet/standard/automatic-memory-management#allocating-memory)
#### 1.2.2 [Releasing Memory](https://docs.microsoft.com/en-us/dotnet/standard/automatic-memory-management#releasing-memory)
#### 1.2.3 [Generations and Performance](https://docs.microsoft.com/en-us/dotnet/standard/automatic-memory-management#generations-and-performance)
#### 1.2.4 [Releasing Memory for Unmanaged Resources](https://docs.microsoft.com/en-us/dotnet/standard/automatic-memory-management#releasing-memory-for-unmanaged-resources)

### Value / Reference types memory allocation
> [The Truth About Value Types](https://docs.microsoft.com/en-us/archive/blogs/ericlippert/the-truth-about-value-types)<br/>
> [The Stack Is An Implementation Detail, Part One](https://ericlippert.com/2009/04/27/the-stack-is-an-implementation-detail-part-one/)<br/>
> [The Stack Is An Implementation Detail, Part Two](https://ericlippert.com/2009/05/04/the-stack-is-an-implementation-detail-part-two/)<br/>
> [Allocating on the stack or the heap](https://devblogs.microsoft.com/dotnet/allocating-on-the-stack-or-the-heap/)<br/>
