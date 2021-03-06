# .NET questions and answers

## 1. [Memory Management](https://docs.microsoft.com/en-us/dotnet/standard/managed-code)

### 1.1 What is _"Managed Code"_?
> Code whose execution is managed by a runtime (_in this case CLR, regardless of the implementation for e.g. Mono, .NET Framework, .NET Core/.NET 5+_) is called **_managed code_**.<br/>
> Managed code is written in one of the high-level languages that can be run on top of .NET such as C#, F# and others.
> <br/>
> <br/>
> CLR is in charge of taking the managed code, compiling it into machine code then executing it. On top of that, it provides important services such as, _automatic memory management, security boundaries, and type safety_ just to name a few...[more](https://docs.microsoft.com/en-us/dotnet/standard/managed-code#what-is-managed-code)

#### 1.1.1 Intermediate Language
> IL (intermediate language) is a product of compilation of code written in high-level .NET languages.<br/>
> Intermediate Language is sometimes also called Common Intermediate Language (CIL) or Microsoft Intermediate Language (MSIL)....[more](https://docs.microsoft.com/en-us/dotnet/standard/managed-code#intermediate-language--execution)

#### 1.1.2 Unmanaged code interoperability
> When the runtime allows passing the boundaries between managed and unmanaged world, it is called **interoprability** or **interop**...[more](https://docs.microsoft.com/en-us/dotnet/standard/managed-code#unmanaged-code-interoperability)

### 1.2 Automatic Memory Management
> It is a service provided by CLR during [Managed Execution](https://docs.microsoft.com/en-us/dotnet/standard/managed-execution-process#managed-execution-process).
> The CLR's GC (garbage collector) manages the allocation and release of memory for an application...[more](https://docs.microsoft.com/en-us/dotnet/standard/automatic-memory-management#automatic-memory-management)

#### 1.2.1 Allocating Memory
> Upon initialization of a new process, the CLR reserves a contiguous region of address space for the process.<br/>
> This reserved address space is called the managed heap. The managed heap maintains a pointer to the address where the next object in the heap will be allocated. Initially, this pointer is set to the managed heap's base address.<br/>
> All [reference types](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/reference-types) are allocated on the managed heap...[more](https://docs.microsoft.com/en-us/dotnet/standard/automatic-memory-management#allocating-memory)

#### 1.2.2 Releasing Memory
> The GC's optimizing engine determines the best time to perform a collection based on the allocations being made.<br/>
> When the GC performs a collection, it releases the memory for objects that are no longer being used by the application. It determines which objects are no longer being used by examining the application's roots. Every application has a set of roots. Each root either refers to an object on the managed heap or is set to null...[more](https://docs.microsoft.com/en-us/dotnet/standard/automatic-memory-management#releasing-memory)

#### 1.2.3 Generations and Performance
> ...[more](https://docs.microsoft.com/en-us/dotnet/standard/automatic-memory-management#generations-and-performance)

#### 1.2.4 Releasing Memory for Unmanaged Resources
> ...[more](https://docs.microsoft.com/en-us/dotnet/standard/automatic-memory-management#releasing-memory-for-unmanaged-resources)

### Value / Reference types memory allocation
> [The Truth About Value Types](https://docs.microsoft.com/en-us/archive/blogs/ericlippert/the-truth-about-value-types)<br/>
> [The Stack Is An Implementation Detail, Part One](https://ericlippert.com/2009/04/27/the-stack-is-an-implementation-detail-part-one/)<br/>
> [The Stack Is An Implementation Detail, Part Two](https://ericlippert.com/2009/05/04/the-stack-is-an-implementation-detail-part-two/)<br/>
> [Allocating on the stack or the heap](https://devblogs.microsoft.com/dotnet/allocating-on-the-stack-or-the-heap/)<br/>
