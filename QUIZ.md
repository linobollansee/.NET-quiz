| id | question | answer | explanation |
| ---- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| 1 | Which GC generation is collected most frequently? | Generation 0 | Newly allocated objects are placed in Generation 0, making it the most frequently collected generation. |
| 2 | What does the JIT compiler primarily translate? | IL to native machine code | The Just-In-Time (JIT) compiler converts Intermediate Language (IL) into native machine code when methods are first executed. |
| 3 | Which collection guarantees O(1) average-time key lookup? | Dictionary<TKey,TValue> | Dictionary<TKey,TValue> uses a hash table internally, providing average O(1) lookup performance. |
| 4 | What is the primary purpose of Span<T>? | High-performance memory access without allocations | Span<T> provides a safe, allocation-free view over contiguous memory and is restricted to the stack. |
| 5 | Which keyword prevents a method from being overridden? | sealed | A sealed override method cannot be overridden by derived classes. |
| 6 | Which interface enables asynchronous disposal? | IAsyncDisposable | IAsyncDisposable enables asynchronous resource cleanup using the `await using` statement. |
| 7 | Which type is stack-only and cannot be boxed? | ref struct | ref struct types are restricted to the stack, preventing boxing and heap allocation. |
| 8 | What is the purpose of ConfigureAwait(false)? | Avoid capturing the current synchronization context | ConfigureAwait(false) prevents continuations from resuming on the original synchronization context, improving performance and avoiding deadlocks in many library scenarios. |
| 9 | Which keyword passes a parameter by readonly reference? | in | The `in` modifier passes arguments by reference while preventing modification inside the method. |
| 10 | Which operator performs pattern matching in C#? | is | The `is` operator supports type checks and modern pattern matching expressions. |
| 11 | What exception is typically thrown when awaiting a canceled Task? | OperationCanceledException | Awaiting a canceled task throws OperationCanceledException. TaskCanceledException derives from it and is commonly used internally by Task. |
| 12 | Which API provides high-performance pooling of arrays? | ArrayPool<T> | ArrayPool<T> reuses arrays to reduce allocations and garbage collection pressure. |
| 13 | Which collection preserves insertion order while providing hash-based lookup in modern .NET? | OrderedDictionary<TKey,TValue> | OrderedDictionary<TKey,TValue> maintains insertion order while still providing efficient key lookups. |
| 14 | What is the default equality comparer used by Dictionary<TKey,TValue>? | EqualityComparer<T>.Default | Dictionary<TKey,TValue> uses EqualityComparer<T>.Default unless a custom comparer is provided. |
| 15 | Which C# feature allows static abstract members in interfaces? | static abstract interface members | Introduced in C# 11, this feature enables generic math and compile-time polymorphism. |
| 16 | Which LINQ method forces immediate execution? | ToList() | Most LINQ operators use deferred execution. ToList() immediately evaluates the query and materializes the results. |
| 17 | Which type can reduce allocations for async methods that often complete synchronously? | ValueTask | ValueTask avoids allocating a Task object when an operation completes synchronously. |
| 18 | Which keyword indicates a method may execute asynchronously? | async | The `async` keyword allows a method to suspend execution using `await` and resume later. |
| 19 | What is the primary benefit of readonly struct? | Prevents mutation and reduces defensive copies | readonly struct guarantees immutability of instance fields and enables compiler optimizations. |
| 20 | Which namespace contains Span<T>? | System | Span<T> is defined in the System namespace. |
| 21 | What does the volatile keyword guarantee? | Visibility of reads and writes across threads | volatile ensures memory visibility between threads but does not make operations atomic. |
| 22 | Which type provides a lightweight view over contiguous memory without owning it? | Span<T> | Span<T> references existing memory without allocating or owning the underlying storage. |
| 23 | Which GC mode performs Generation 2 collections in the background to reduce pause times? | Background GC | Background GC allows long-running Generation 2 collections to occur concurrently, reducing application pauses. |
| 24 | How do you iterate over an IAsyncEnumerable<T>? | await foreach | IAsyncEnumerable<T> is consumed using the `await foreach` statement. |
| 25 | Which IL instruction creates a new object instance? | newobj | The `newobj` IL instruction allocates an object and invokes its constructor. |
| 26 | Which attribute generates compiled regular expressions at compile time? | GeneratedRegexAttribute | GeneratedRegexAttribute uses source generators to create optimized regex implementations. |
| 27 | What is the purpose of Unsafe.As<TFrom,TTo>()? | Reinterpret one type as another without runtime checks | Unsafe.As performs unchecked type reinterpretation for high-performance scenarios. |
| 28 | Which TaskStatus indicates a task has been created but not scheduled? | Created | A task in the Created state has not yet been started or scheduled. |
| 29 | Which generic constraint restricts a type parameter to unmanaged types? | unmanaged | The unmanaged constraint allows only unmanaged value types as generic arguments. |
| 30 | Which immutable collection is optimized for efficient updates through structural sharing? | ImmutableDictionary<TKey,TValue> | ImmutableDictionary creates modified copies that share most of their internal structure with previous versions, making updates efficient. |
| 31 | What is the purpose of the `required` keyword in C#? | Forces initialization of members during object creation | The `required` keyword ensures that specified properties or fields must be initialized when creating an object, improving correctness and reducing null-related issues. |
| 32 | What is the difference between `ReferenceEquals()` and `Equals()`? | ReferenceEquals compares object identity, Equals compares logical equality | ReferenceEquals checks whether two references point to the same object, while Equals can be overridden to compare values. |
| 33 | What is the purpose of the `init` accessor? | Allows assignment only during object initialization | The `init` accessor enables immutable-style properties that can only be set during construction or object initialization. |
| 34 | What does the `checked` keyword do? | Enables overflow checking for numeric operations | The `checked` keyword causes arithmetic overflow on integral types to throw an OverflowException instead of silently wrapping. |
| 35 | What does the `unchecked` keyword do? | Disables overflow checking | The `unchecked` keyword allows numeric overflow to occur without throwing exceptions. |
| 36 | What is the purpose of `Activator.CreateInstance()`? | Creates objects dynamically at runtime | Activator.CreateInstance() uses reflection to instantiate types when the concrete type is not known at compile time. |
| 37 | What is reflection in .NET? | Inspecting and interacting with metadata at runtime | Reflection allows applications to examine assemblies, types, methods, properties, and create objects dynamically. |
| 38 | What is the purpose of an assembly in .NET? | A compiled deployment unit containing IL and metadata | Assemblies are the primary units of deployment, versioning, and security boundaries in .NET applications. |
| 39 | What information is stored in assembly metadata? | Type definitions and references | Metadata describes types, members, dependencies, and attributes used by the CLR at runtime. |
| 40 | What is the difference between a value type and a reference type? | Value types store data directly, reference types store references to objects | Value types usually contain their data directly, while reference types point to objects stored on the managed heap. |
| 41 | What is the purpose of the IDisposable interface? | Defines deterministic resource cleanup | IDisposable allows objects to release unmanaged resources explicitly through the Dispose() method. |
| 42 | What is the purpose of a finalizer in C#? | Performs cleanup before garbage collection removes an object | Finalizers provide a last chance to release unmanaged resources when Dispose() was not called. |
| 43 | Why is IDisposable preferred over finalizers? | It provides predictable cleanup timing | IDisposable allows developers to release resources immediately instead of waiting for garbage collection. |
| 44 | What is the purpose of the using statement in C#? | Automatically calls Dispose() | The using statement ensures IDisposable objects are cleaned up even when exceptions occur. |
| 45 | What is the difference between `using` directive and `using` statement? | One imports namespaces, the other manages disposal | A using directive simplifies type references, while a using statement controls resource lifetime. |
| 46 | What is dependency injection in .NET? | A pattern for providing dependencies externally | Dependency injection reduces coupling by allowing required services to be supplied instead of created internally. |
| 47 | What are the three service lifetimes in ASP.NET Core DI? | Singleton, Scoped, Transient | Singleton creates one instance for the application lifetime, Scoped creates one per request scope, and Transient creates a new instance each time. |
| 48 | What is the purpose of IServiceCollection? | Registers services for dependency injection | IServiceCollection stores service registrations used later by the .NET dependency injection container. |
| 49 | What is middleware in ASP.NET Core? | Components that process HTTP requests and responses | Middleware forms a pipeline where each component can handle, modify, or pass requests to the next component. |
| 50 | What is the purpose of the ASP.NET Core request pipeline? | Processes HTTP requests through configured middleware | The request pipeline defines how incoming requests are handled and how responses are generated. |
| 51 | What is endpoint routing in ASP.NET Core? | A system that maps requests to application handlers | Endpoint routing matches incoming URLs and HTTP methods to controllers, minimal APIs, or other handlers. |
| 52 | What is the purpose of minimal APIs in ASP.NET Core? | Create lightweight HTTP APIs with minimal configuration | Minimal APIs provide a simplified approach for building HTTP services without requiring controllers. |
| 53 | What is Kestrel in ASP.NET Core? | The cross-platform web server used by ASP.NET Core | Kestrel is the default high-performance HTTP server used to host ASP.NET Core applications. |
| 54 | What is the purpose of appsettings.json? | Stores application configuration settings | appsettings.json provides structured configuration values that can be loaded by the .NET configuration system. |
| 55 | What is the Options pattern in ASP.NET Core? | Strongly typed access to configuration values | The Options pattern maps configuration sections to strongly typed classes using dependency injection. |
| 56 | What is the purpose of ILogger in .NET? | Provides structured application logging | ILogger enables consistent logging across applications with support for different providers and log levels. |
| 57 | What are logging scopes used for? | Adding contextual information to logs | Logging scopes attach shared metadata such as request IDs or user information to related log entries. |
| 58 | What is structured logging? | Logging data as named properties instead of formatted strings | Structured logging stores information in a machine-readable format, improving searching and analysis. |
| 59 | What is the purpose of Activity in .NET diagnostics? | Represents an operation for distributed tracing | Activity tracks operations across application boundaries and supports OpenTelemetry scenarios. |
| 60 | What is OpenTelemetry used for in .NET? | Collecting telemetry data such as traces and metrics | OpenTelemetry provides standardized APIs for observing application performance and behavior. |
| 61 | What is the purpose of the .NET Generic Host? | Provides infrastructure for running background services and applications | The Generic Host manages application startup, dependency injection, configuration, logging, and graceful shutdown. |
| 62 | What interface is used to create a hosted background service in .NET? | IHostedService | IHostedService defines lifecycle methods for services that run in the background. |
| 63 | What is the purpose of BackgroundService in .NET? | Provides a base class for long-running background tasks | BackgroundService simplifies implementing hosted services by providing an ExecuteAsync method. |
| 64 | What is graceful shutdown in .NET applications? | Allowing resources and operations to complete before termination | Graceful shutdown gives running operations time to finish and services time to release resources properly. |
| 65 | What is the purpose of CancellationToken during application shutdown? | Signals running operations to stop safely | CancellationToken allows background tasks and requests to respond to shutdown requests cooperatively. |
| 66 | What is the difference between Task and Thread? | Task represents asynchronous work, Thread represents an execution thread | Tasks are managed by the Task Parallel Library and usually use thread pool threads, while Threads represent actual OS threads. |
| 67 | What is the purpose of the ThreadPool in .NET? | Reuses worker threads to reduce creation overhead | The ThreadPool manages a collection of threads used for asynchronous operations and background work. |
| 68 | What is Task Parallel Library (TPL)? | A framework for parallel and asynchronous programming | TPL provides Task-based programming models, parallel loops, and task scheduling. |
| 69 | What is the purpose of Parallel.For()? | Executes loop iterations concurrently | Parallel.For distributes independent iterations across multiple threads to improve performance. |
| 70 | What is the difference between Parallel.ForEach() and Task.WhenAll()? | Parallel.ForEach is CPU-focused, Task.WhenAll is async I/O-focused | Parallel.ForEach is designed for parallel CPU work, while Task.WhenAll combines asynchronous operations. |
| 71 | What does Task.WhenAll() do? | Waits for multiple tasks to complete | Task.WhenAll creates a task that completes when all supplied tasks finish. |
| 72 | What does Task.WhenAny() do? | Completes when the first task finishes | Task.WhenAny returns the first completed task from a collection of tasks. |
| 73 | What is a deadlock in multithreading? | A state where threads wait indefinitely for each other | Deadlocks occur when competing operations hold resources while waiting for others to release them. |
| 74 | What is a race condition? | Incorrect behavior caused by unsynchronized access to shared data | Race conditions occur when multiple threads access shared state without proper coordination. |
| 75 | What is the purpose of Interlocked operations? | Provide atomic operations on shared variables | Interlocked methods perform thread-safe updates without requiring locks. |
| 76 | What is the difference between lock and Monitor? | lock is syntactic sugar for Monitor | The lock statement internally uses Monitor.Enter and Monitor.Exit with exception safety. |
| 77 | What is ReaderWriterLockSlim used for? | Allowing multiple readers but exclusive writers | ReaderWriterLockSlim improves concurrency when reads greatly outnumber writes. |
| 78 | What is a SemaphoreSlim used for? | Limiting concurrent access to resources | SemaphoreSlim controls how many operations can execute simultaneously. |
| 79 | What is the purpose of Mutex? | Provides synchronization across processes | Mutex can coordinate access between different application processes. |
| 80 | What is the difference between async I/O and multithreading? | Async I/O frees threads while waiting, multithreading uses multiple threads | Async programming improves scalability by avoiding blocked threads during I/O operations. |
| 81 | What is the purpose of Expression Trees in .NET? | Represent code as data structures | Expression trees allow code expressions to be inspected, modified, and translated at runtime. |
| 82 | Which namespace contains expression tree APIs? | System.Linq.Expressions | The System.Linq.Expressions namespace provides types for creating and working with expression trees. |
| 83 | What is the difference between Func<T> and Action<T>? | Func returns a value, Action returns void | Func delegates represent methods with return values, while Action delegates represent methods without returns. |
| 84 | What is a delegate in C#? | A type-safe reference to a method | Delegates store references to methods and allow methods to be passed as parameters. |
| 85 | What is a multicast delegate? | A delegate containing multiple method references | Multicast delegates invoke multiple methods when called. |
| 86 | What is an event in C#? | A restricted delegate used for notifications | Events allow objects to publish notifications while controlling who can invoke them. |
| 87 | What is the purpose of the nameof operator? | Returns a symbol name as a string | nameof provides compile-time safe names for variables, types, and members. |
| 88 | What is the purpose of the typeof operator? | Retrieves a Type object for a type | typeof allows runtime access to metadata for a known type. |
| 89 | What is pattern matching with switch expressions? | A concise way to match values against patterns | Switch expressions allow selecting results based on type, value, and property patterns. |
| 90 | What is a property pattern in C#? | Matching object properties during pattern matching | Property patterns inspect object members directly within pattern expressions. |
| 91 | What is the purpose of global using directives? | Share namespace imports across a project | Global usings reduce repeated namespace declarations in individual files. |
| 92 | What are file-scoped namespaces? | A shorter namespace declaration syntax | File-scoped namespaces remove indentation and reduce boilerplate. |
| 93 | What is a partial class? | A class definition split across multiple files | Partial classes allow multiple source files to contribute to the same type. |
| 94 | What are source generators in .NET? | Compile-time code generation tools | Source generators create additional C# code during compilation based on existing source or metadata. |
| 95 | What is the purpose of Roslyn? | Provides the C# and VB compiler platform APIs | Roslyn exposes compiler functionality for analysis, code generation, and tooling. |
| 96 | What is an analyzer in Roslyn? | A tool that detects code issues during compilation | Analyzers inspect source code and provide diagnostics or suggestions. |
| 97 | What is the difference between compile-time and runtime errors? | Compile-time errors occur during compilation, runtime errors occur during execution | The compiler catches invalid code before execution, while runtime errors happen while the program runs. |
| 98 | What is AOT compilation in .NET? | Compiling applications to native code before execution | Ahead-of-Time compilation reduces startup time and can improve deployment scenarios. |
| 99 | What is NativeAOT? | Publishing .NET applications as native executables | NativeAOT produces self-contained native binaries without requiring the full .NET runtime environment. |
| 100 | What is trimming in .NET publishing? | Removing unused code from application output | Trimming reduces application size by analyzing and removing unreachable assemblies and members. |
| 101 | What is the purpose of the .NET IL linker? | Removes unused code during publishing | The IL linker analyzes application dependencies and removes unreachable code to reduce deployment size. |
| 102 | What is single-file publishing in .NET? | Packaging an application into one executable file | Single-file publishing bundles application files into a single deployable artifact. |
| 103 | What is self-contained deployment in .NET? | Deploying an application with its own runtime | Self-contained applications include the required .NET runtime and do not require it to be installed separately. |
| 104 | What is framework-dependent deployment? | Deploying an application that requires an installed .NET runtime | Framework-dependent apps rely on the target machine having a compatible .NET runtime installed. |
| 105 | What is the purpose of AssemblyLoadContext? | Controls loading and isolation of assemblies | AssemblyLoadContext enables dynamic assembly loading and unloading, useful for plugins and isolation scenarios. |
| 106 | What is a collectible AssemblyLoadContext? | An AssemblyLoadContext that can be unloaded | Collectible contexts allow dynamically loaded assemblies to be removed from memory when no longer needed. |
| 107 | What is the purpose of the Global Assembly Cache (GAC)? | Stores shared .NET Framework assemblies | The GAC provided centralized storage and version management for assemblies in .NET Framework. |
| 108 | What replaced many GAC scenarios in modern .NET? | NuGet package management and application-local dependencies | Modern .NET typically uses NuGet packages and local deployment instead of a global assembly store. |
| 109 | What is strong naming an assembly? | Giving an assembly a unique identity using a public/private key pair | Strong names provide identity verification and version uniqueness for assemblies. |
| 110 | What is the purpose of InternalsVisibleToAttribute? | Allows another assembly to access internal members | InternalsVisibleToAttribute exposes internal types to specified friend assemblies, commonly used for testing. |
| 111 | What is a NuGet package? | A reusable .NET library distribution package | NuGet packages contain compiled libraries, dependencies, and metadata for project consumption. |
| 112 | What file describes a .NET project configuration? | .csproj file | The project file defines dependencies, build settings, target frameworks, and compilation options. |
| 113 | What is TargetFramework in a .NET project? | Specifies the runtime and API version targeted by the application | TargetFramework determines which .NET APIs and runtime features are available. |
| 114 | What is multi-targeting in .NET? | Building a project for multiple frameworks | Multi-targeting allows a library to support different .NET versions from the same codebase. |
| 115 | What is a RID in .NET publishing? | Runtime Identifier specifying a target platform | Runtime Identifiers define operating system and architecture combinations for deployments. |
| 116 | What is the purpose of Directory.Build.props? | Provides shared MSBuild properties across projects | Directory.Build.props centralizes common build configuration for multiple projects. |
| 117 | What is MSBuild? | The build engine used by .NET projects | MSBuild executes build tasks defined by project files and build targets. |
| 118 | What is a build target in MSBuild? | A named set of build actions | Targets define groups of tasks that run during different build phases. |
| 119 | What is incremental compilation? | Rebuilding only changed parts of a project | Incremental builds improve performance by avoiding unnecessary compilation work. |
| 120 | What is the purpose of .editorconfig in .NET projects? | Defines coding style and analyzer rules | .editorconfig provides consistent formatting and code style settings across development environments. |
| 121 | What is Entity Framework Core? | An object-relational mapper for .NET | EF Core allows developers to work with databases using .NET objects instead of raw SQL. |
| 122 | What is DbContext in EF Core? | A session with the database | DbContext manages entity tracking, queries, and database operations. |
| 123 | What is change tracking in EF Core? | Monitoring entity modifications | Change tracking allows EF Core to detect updates and generate database commands automatically. |
| 124 | What is AsNoTracking() used for in EF Core? | Improves query performance for read-only data | AsNoTracking disables change tracking when entities do not need to be updated. |
| 125 | What is a migration in EF Core? | A version-controlled database schema change | Migrations allow database structure changes to be applied incrementally. |
| 126 | What is the purpose of Include() in EF Core? | Loads related entities eagerly | Include() retrieves related navigation properties in the same query. |
| 127 | What is lazy loading in EF Core? | Loading related data only when accessed | Lazy loading delays database queries until navigation properties are requested. |
| 128 | What is eager loading in EF Core? | Loading related data during the initial query | Eager loading retrieves related entities immediately using Include(). |
| 129 | What is explicit loading in EF Core? | Manually loading related entities after retrieving an object | Explicit loading gives developers direct control over when related data is retrieved. |
| 130 | What is a LINQ provider? | A component that translates LINQ expressions into another query language | LINQ providers convert expressions into formats such as SQL queries. |
| 131 | What is IQueryable<T>? | A query representation that can be translated by providers | IQueryable<T> allows query expressions to be executed remotely, such as against a database. |
| 132 | What is IEnumerable<T>? | An in-memory sequence abstraction | IEnumerable<T> represents collections that are iterated locally. |
| 133 | What happens when IQueryable is converted to IEnumerable? | Query execution moves to local memory | Operations after conversion are executed by .NET rather than translated by the provider. |
| 134 | What is query translation in EF Core? | Converting LINQ expressions into SQL | EF Core analyzes expression trees and generates database-specific queries. |
| 135 | What is the N+1 query problem? | Excessive database queries caused by loading related data inefficiently | N+1 occurs when one query loads data and additional queries are executed repeatedly for related entities. |
| 136 | What is split query behavior in EF Core? | Loading related collections using multiple SQL queries | Split queries can avoid large joins and reduce duplicate data transfer. |
| 137 | What is optimistic concurrency? | Detecting conflicting updates using version checks | Optimistic concurrency assumes conflicts are rare and verifies changes before saving. |
| 138 | What is a concurrency token in EF Core? | A value used to detect conflicting updates | Concurrency tokens allow EF Core to determine whether data changed since it was loaded. |
| 139 | What is the purpose of SaveChangesAsync()? | Persists tracked changes asynchronously | SaveChangesAsync writes entity modifications to the database without blocking the calling thread. |
| 140 | What is database-first development? | Generating models from an existing database | Database-first creates entity models based on an existing database schema. |
| 141 | What is code-first development? | Creating database schemas from application models | Code-first uses entity classes and migrations to define database structure. |
| 142 | What is a value converter in EF Core? | Converts property values between CLR and database types | Value converters transform data during storage and retrieval. |
| 143 | What is a shadow property in EF Core? | A property tracked by EF but not defined in the entity class | Shadow properties store metadata such as foreign keys without appearing in the CLR model. |
| 144 | What is a keyless entity type in EF Core? | An entity without a primary key | Keyless entities are useful for database views and read-only query results. |
| 145 | What is compiled query support in EF Core? | Precompiling query execution plans | Compiled queries reduce overhead for frequently executed queries. |
| 146 | What is connection pooling? | Reusing database connections instead of recreating them | Connection pooling improves performance by maintaining reusable database connections. |
| 147 | What is a transaction? | A group of operations treated as a single unit | Transactions ensure operations either all succeed or all fail together. |
| 148 | What is isolation level? | A setting controlling transaction visibility and locking behavior | Isolation levels define how transactions interact with each other. |
| 149 | What is serialization in .NET? | Converting objects into a transferable format | Serialization transforms objects into formats such as JSON or binary data. |
| 150 | What is System.Text.Json? | The built-in high-performance JSON serializer in .NET | System.Text.Json provides fast JSON serialization with support for modern .NET features. |
| 151 | What is the purpose of JsonSerializerOptions in System.Text.Json? | Configures JSON serialization behavior | JsonSerializerOptions controls naming policies, converters, indentation, ignore rules, and other serialization settings. |
| 152 | What is a JsonConverter in System.Text.Json? | A custom serializer for specific types | JsonConverter allows developers to control how particular types are converted to and from JSON. |
| 153 | What is source-generated JSON serialization? | Compile-time generated serialization metadata | Source generation improves startup performance and reduces runtime reflection overhead in System.Text.Json. |
| 154 | What is the default naming policy in System.Text.Json? | Preserves property names | System.Text.Json keeps property names unchanged unless a naming policy is configured. |
| 155 | What is polymorphic serialization? | Serializing derived types through a base type reference | Polymorphic serialization preserves runtime type information when serializing inheritance hierarchies. |
| 156 | What is the purpose of the JsonIgnore attribute? | Excludes properties from JSON serialization | JsonIgnore prevents selected members from appearing in serialized output. |
| 157 | What is UTF-8 JSON support in .NET? | Native handling of JSON as UTF-8 data | System.Text.Json works efficiently with UTF-8 to reduce encoding overhead. |
| 158 | What is the difference between serialization and deserialization? | Serialization writes objects, deserialization recreates objects | Serialization converts objects into a data format, while deserialization converts data back into objects. |
| 159 | What is memory mapping in .NET? | Mapping files directly into memory | Memory-mapped files allow efficient access to large files by treating file contents as memory. |
| 160 | What is the purpose of Memory<T>? | Provides heap-compatible memory abstraction | Memory<T> represents contiguous memory that can safely cross async boundaries unlike Span<T>. |
| 161 | What is the difference between Span<T> and Memory<T>? | Span<T> is stack-only, Memory<T> can live on the heap | Memory<T> is designed for scenarios where memory must survive beyond the current stack frame. |
| 162 | What is ReadOnlySpan<T>? | A read-only view over contiguous memory | ReadOnlySpan<T> provides allocation-free access while preventing modification. |
| 163 | What is ReadOnlyMemory<T>? | A heap-compatible read-only memory abstraction | ReadOnlyMemory<T> allows read-only memory access across asynchronous operations. |
| 164 | What is the purpose of MemoryMarshal? | Provides advanced memory manipulation APIs | MemoryMarshal enables conversions between memory representations without unnecessary allocations. |
| 165 | What is pinning memory in .NET? | Preventing garbage collector movement of objects | Pinning keeps objects at fixed memory addresses for interoperability with unmanaged code. |
| 166 | What is unmanaged code? | Code executed outside the CLR | Unmanaged code is typically native code such as C or C++ that does not use .NET memory management. |
| 167 | What is P/Invoke? | Calling native functions from managed code | Platform Invocation Services allow .NET applications to interact with unmanaged libraries. |
| 168 | What is the purpose of DllImport? | Declares external native functions | DllImport specifies unmanaged libraries and functions that managed code can call. |
| 169 | What is COM interop? | Interaction between .NET and COM components | COM interop enables communication between managed applications and legacy COM systems. |
| 170 | What is unsafe code in C#? | Code that allows pointer operations | Unsafe code enables direct memory manipulation using pointers. |
| 171 | What keyword enables pointer operations in C#? | unsafe | The unsafe keyword allows blocks containing pointers and unmanaged operations. |
| 172 | What does the fixed keyword do? | Pins memory during pointer operations | fixed prevents the garbage collector from relocating an object while it is accessed through a pointer. |
| 173 | What is a pointer in C#? | A variable containing a memory address | Pointers store direct references to memory locations in unsafe contexts. |
| 174 | What is stackalloc used for? | Allocating memory on the stack | stackalloc creates temporary memory with very low allocation overhead. |
| 175 | What is the Large Object Heap (LOH)? | A heap area for large allocations | Objects larger than a threshold are allocated on the LOH and managed separately by the GC. |
| 176 | What triggers a garbage collection? | Memory pressure or allocation thresholds | The GC starts collections when it determines available memory needs management. |
| 177 | What is GC.TryStartNoGCRegion()? | Requests a period without garbage collection | This API allows performance-critical sections to avoid GC interruptions if enough memory is available. |
| 178 | What is finalization queue in .NET? | A queue containing objects requiring finalizers | Objects with finalizers are placed in this queue before final cleanup. |
| 179 | What is a weak reference? | A reference that does not prevent garbage collection | Weak references allow objects to be collected even while a reference exists. |
| 180 | What is ConditionalWeakTable used for? | Associating data with objects without preventing collection | ConditionalWeakTable stores metadata tied to object lifetimes. |
| 181 | What is the purpose of ConcurrentQueue<T>? | Thread-safe FIFO queue | ConcurrentQueue<T> supports multiple producers and consumers without manual locking. |
| 182 | What is the purpose of ConcurrentStack<T>? | Thread-safe LIFO collection | ConcurrentStack<T> allows concurrent push and pop operations. |
| 183 | What is BlockingCollection<T>? | A thread-safe producer-consumer collection | BlockingCollection<T> provides blocking and bounding capabilities for concurrent workflows. |
| 184 | What is ImmutableArray<T>? | An immutable array structure | ImmutableArray<T> provides fixed collections optimized for immutable scenarios. |
| 185 | What is ImmutableList<T>? | An immutable list collection | ImmutableList<T> creates new versions while preserving previous versions safely. |
| 186 | What is PriorityQueue<TElement,TPriority>? | A queue ordered by priority | PriorityQueue removes elements based on priority rather than insertion order. |
| 187 | What is a hash collision? | When multiple keys produce the same hash value | Hash collisions require additional comparisons to identify the correct entry. |
| 188 | What is the purpose of IEqualityComparer<T>? | Defines custom equality and hashing logic | IEqualityComparer<T> allows collections to use custom comparison rules. |
| 189 | What is sorting stability? | Maintaining relative order of equal elements | A stable sort keeps equal elements in their original order. |
| 190 | Which sorting algorithm does List<T>.Sort() use internally? | Introspective sort (IntroSort) | List<T>.Sort() combines quicksort, heapsort, and insertion sort techniques. |
| 191 | What is binary search complexity? | O(log n) | Binary search repeatedly divides a sorted collection in half to locate an item efficiently. |
| 192 | What requirement does binary search have? | The collection must be sorted | Binary search only works correctly when elements are ordered. |
| 193 | What is a tree data structure? | A hierarchical collection of nodes | Trees represent parent-child relationships between elements. |
| 194 | What is a binary tree? | A tree where each node has at most two children | Binary trees contain left and right child references. |
| 195 | What is a balanced tree? | A tree maintaining controlled height | Balanced trees prevent performance degradation during searching and insertion. |
| 196 | What is SortedDictionary<TKey,TValue> internally based on? | A balanced binary search tree | SortedDictionary maintains sorted keys using a tree-based structure. |
| 197 | What is SortedList<TKey,TValue> optimized for? | Memory efficiency and indexed access | SortedList stores keys and values in arrays, reducing memory usage compared to tree structures. |
| 198 | What is HashSet<T> used for? | Storing unique values | HashSet<T> provides fast membership testing without duplicate entries. |
| 199 | What is the purpose of LinkedList<T>? | Efficient insertion and removal with node references | LinkedList<T> allows fast changes when the node location is known. |
| 200 | What is the main advantage of arrays in .NET? | Fast indexed access and contiguous memory | Arrays provide efficient memory layout and constant-time element access. |
| 201 | What is the purpose of the `volatile` keyword when applied to fields? | Ensures reads and writes are not optimized away or cached across threads | volatile provides memory visibility guarantees between threads but does not make compound operations atomic. |
| 202 | What is memory fencing in .NET? | Controlling instruction and memory operation ordering | Memory fences prevent CPUs and compilers from reordering operations in ways that break thread synchronization. |
| 203 | What is the purpose of Thread.MemoryBarrier()? | Forces memory ordering between threads | Thread.MemoryBarrier ensures that memory operations before and after the barrier are observed in the correct order. |
| 204 | What is false sharing in multithreading? | Performance loss caused by threads modifying data on the same cache line | False sharing occurs when independent data shares CPU cache lines, causing unnecessary synchronization overhead. |
| 205 | What is lock contention? | Multiple threads competing for the same lock | Lock contention reduces performance because threads must wait for exclusive access. |
| 206 | What is a spin lock? | A lock that repeatedly checks availability instead of blocking | SpinLock can improve performance for very short critical sections by avoiding thread scheduling overhead. |
| 207 | What is the purpose of Lazy<T>? | Delays object creation until first use | Lazy<T> implements deferred initialization and can provide thread-safe creation. |
| 208 | What is double-checked locking? | An optimization pattern for lazy initialization | Double-checked locking reduces locking overhead by checking initialization state before and after acquiring a lock. |
| 209 | What is the purpose of ThreadLocal<T>? | Provides thread-specific storage | ThreadLocal<T> creates separate values for each executing thread. |
| 210 | What is ExecutionContext in .NET? | Stores ambient execution information | ExecutionContext flows information such as security context and async-local values across async operations. |
| 211 | What is AsyncLocal<T>? | Stores data that flows with asynchronous execution | AsyncLocal<T> provides context-specific storage that follows async continuations. |
| 212 | What is SynchronizationContext? | Represents an environment for scheduling continuations | SynchronizationContext determines where asynchronous continuations execute. |
| 213 | Why can ConfigureAwait(false) improve library code? | It avoids unnecessary context capture | Library code often does not require returning to the caller's synchronization context. |
| 214 | What is an async void method mainly used for? | Event handlers | async void cannot be awaited and should generally only be used where delegate signatures require it. |
| 215 | Why should async void methods be avoided for normal operations? | Exceptions cannot be easily observed and composition is difficult | Task-returning methods allow callers to await completion and handle failures. |
| 216 | What happens when an async method returns before its first await? | It executes synchronously | Code before the first incomplete await runs immediately on the calling thread. |
| 217 | What is a ValueTask limitation? | It should not usually be awaited multiple times | ValueTask is optimized for specific scenarios and has usage restrictions compared with Task. |
| 218 | What is IValueTaskSource? | A low-allocation mechanism for implementing ValueTask sources | IValueTaskSource allows reusable async operation implementations with reduced allocations. |
| 219 | What is asynchronous cancellation? | Stopping async operations cooperatively | Async cancellation uses tokens to request termination without forcibly aborting execution. |
| 220 | What is a continuation in Task-based programming? | Code executed after a task completes | Continuations allow additional work to run when an asynchronous operation finishes. |
| 221 | What is TaskScheduler? | Controls how tasks are executed | TaskScheduler determines where and how tasks are queued and run. |
| 222 | What is the default TaskScheduler? | ThreadPool-based scheduler | The default scheduler executes tasks using .NET ThreadPool threads. |
| 223 | What is a custom TaskScheduler used for? | Controlling task execution behavior | Custom schedulers can restrict concurrency or implement specialized scheduling strategies. |
| 224 | What is TaskCompletionSource<T>? | A way to manually control a Task's completion | TaskCompletionSource allows wrapping callback-based or external operations as Tasks. |
| 225 | What is the purpose of ConfigureAwaitOptions in modern .NET? | Provides more control over await behavior | ConfigureAwaitOptions allows advanced control over continuation handling. |
| 226 | What is exception aggregation in Task.WhenAll()? | Combining exceptions from multiple failed tasks | Task.WhenAll captures failures from all completed tasks and exposes them together. |
| 227 | What is an AggregateException? | A container for multiple exceptions | AggregateException represents one or more errors occurring during parallel operations. |
| 228 | What is exception filtering in C#? | Conditional handling of exceptions | Exception filters use the when keyword to decide whether a catch block should handle an exception. |
| 229 | What is the purpose of the finally block? | Executes cleanup code regardless of exceptions | finally runs after try/catch processing and is used for guaranteed cleanup. |
| 230 | What is the difference between throw and return inside catch? | throw propagates errors, return completes normally | Throwing preserves failure behavior while returning exits the method. |
| 231 | What is the purpose of ArgumentNullException? | Indicates a required argument was null | ArgumentNullException communicates invalid null input parameters. |
| 232 | What is the purpose of InvalidOperationException? | Indicates an invalid operation state | InvalidOperationException is used when a method call is inappropriate for the object's current state. |
| 233 | What is the purpose of NotSupportedException? | Indicates an unsupported operation | NotSupportedException signals that a requested operation is intentionally unavailable. |
| 234 | What is the purpose of NotImplementedException? | Indicates unfinished functionality | NotImplementedException is used when a feature exists but has not yet been implemented. |
| 235 | What is the purpose of ObjectDisposedException? | Indicates usage of a disposed object | ObjectDisposedException occurs when operations are attempted after disposal. |
| 236 | What is the difference between checked exceptions and unchecked exceptions in .NET? | .NET does not enforce checked exceptions | Unlike Java, .NET allows any exception type without compile-time declaration requirements. |
| 237 | What is the purpose of exception filters? | Avoid unnecessary catch processing | Filters allow checking exception conditions before entering a catch block. |
| 238 | What is the difference between a shallow copy and deep copy? | Shallow copies references, deep copies contained objects | Deep copying creates independent object graphs while shallow copying shares references. |
| 239 | What interface supports cloning objects? | ICloneable | ICloneable defines a Clone method, though its semantics are not strongly specified. |
| 240 | What is object initialization syntax? | A shorthand for assigning properties during creation | Object initializers simplify setting members after construction. |
| 241 | What is collection initialization syntax? | A shorthand for adding initial elements | Collection initializers call Add methods automatically during object creation. |
| 242 | What is constructor chaining? | Calling one constructor from another | Constructor chaining reduces duplicate initialization logic. |
| 243 | What is a static constructor? | A constructor that initializes static members | Static constructors run once before the type is first accessed. |
| 244 | When does a static constructor execute? | Before first use of the type | The CLR invokes static constructors automatically before accessing static members or creating instances. |
| 245 | What is the purpose of private constructors? | Restrict object creation | Private constructors are commonly used for singleton patterns or static-only classes. |
| 246 | What is an abstract class? | A class that cannot be instantiated directly | Abstract classes provide shared behavior while requiring derived implementations for abstract members. |
| 247 | What is an interface default implementation? | A method implementation provided inside an interface | Modern C# allows interfaces to provide default behavior for members. |
| 248 | What is explicit interface implementation? | Implementing members accessible only through the interface | Explicit implementation resolves naming conflicts and hides members from the concrete type. |
| 249 | What is the difference between virtual and abstract methods? | Virtual methods have implementations, abstract methods do not | Virtual methods provide overridable behavior while abstract methods require derived implementations. |
| 250 | What is method hiding in C#? | Replacing a base member using the new keyword | Method hiding creates a separate member rather than overriding the base implementation. |
| 251 | What is the purpose of the `base` keyword in C#? | Accesses members of a base class | The `base` keyword allows derived classes to call constructors, methods, or properties defined in their parent class. |
| 252 | What is the purpose of the `this` keyword in C#? | Refers to the current object instance | The `this` keyword accesses members of the current instance and resolves naming conflicts between fields and parameters. |
| 253 | What is constructor inheritance in C#? | A derived class does not automatically inherit constructors | Constructors must be explicitly defined or called using base constructor syntax. |
| 254 | What is the purpose of the `params` keyword? | Allows variable numbers of arguments | The `params` keyword lets methods accept an arbitrary number of parameters as an array. |
| 255 | What is method overloading? | Defining multiple methods with the same name but different signatures | Overloading allows compile-time selection of methods based on parameter types or counts. |
| 256 | What is method overriding? | Replacing inherited virtual behavior | Overriding allows derived classes to provide specialized implementations of base class members. |
| 257 | What is compile-time polymorphism? | Behavior selection during compilation | Method overloading is an example of compile-time polymorphism. |
| 258 | What is runtime polymorphism? | Behavior selection during execution | Method overriding through virtual dispatch is an example of runtime polymorphism. |
| 259 | What is virtual method dispatch? | Runtime selection of the correct overridden method | The CLR determines the actual implementation to execute based on the object's runtime type. |
| 260 | What is a vtable in .NET? | Internal structure used for virtual method lookup | The runtime uses method tables to resolve virtual calls efficiently. |
| 261 | What is the purpose of sealing a class? | Prevent inheritance | Sealed classes cannot be extended by other classes. |
| 262 | Why might a class be sealed for performance? | Enables runtime optimizations | The CLR can optimize calls when it knows a type cannot be inherited. |
| 263 | What is the difference between composition and inheritance? | Composition uses contained objects, inheritance extends behavior | Composition often provides more flexible designs by reducing tight coupling. |
| 264 | What is the dependency inversion principle? | High-level modules should not depend on low-level details | Both should depend on abstractions rather than concrete implementations. |
| 265 | What is the single responsibility principle? | A class should have one reason to change | The principle encourages focused classes with clear responsibilities. |
| 266 | What is the open/closed principle? | Software should be open for extension but closed for modification | New behavior should be added without changing existing tested code. |
| 267 | What is the Liskov substitution principle? | Derived types should be replaceable for their base types | Subclasses should preserve expected behavior of their base classes. |
| 268 | What is the interface segregation principle? | Clients should not depend on unnecessary methods | Interfaces should be small and focused. |
| 269 | What is the purpose of dependency injection scopes? | Control service lifetimes | Scopes define how long created dependency instances remain available. |
| 270 | What happens if a scoped service is injected into a singleton? | It creates a lifetime mismatch | A singleton cannot safely depend on scoped services because the scoped lifetime is shorter. |
| 271 | What is the service locator anti-pattern? | Resolving dependencies manually from a container | Service locator hides dependencies and reduces code clarity. |
| 272 | What is the decorator pattern? | Dynamically adding behavior to objects | Decorators wrap objects to extend functionality without modifying them. |
| 273 | What is the factory pattern? | Encapsulating object creation logic | Factories centralize creation decisions and hide construction details. |
| 274 | What is the strategy pattern? | Encapsulating interchangeable algorithms | Strategy allows selecting behavior at runtime through abstractions. |
| 275 | What is the observer pattern? | A publish-subscribe notification pattern | Observers receive updates when a subject changes state. |
| 276 | What is the singleton pattern? | Ensures one instance of a type exists | Singleton restricts creation and provides global access to one instance. |
| 277 | What is the adapter pattern? | Converts one interface into another | Adapters allow incompatible components to work together. |
| 278 | What is the mediator pattern? | Centralizes communication between objects | Mediators reduce direct dependencies between collaborating components. |
| 279 | What is the repository pattern? | Abstracts data access logic | Repositories provide a layer between business logic and persistence mechanisms. |
| 280 | What is the unit of work pattern? | Groups related database operations into one transaction boundary | Unit of work coordinates changes and commits them together. |
| 281 | What is the purpose of dependency injection in testing? | Allows replacing real dependencies with mocks | DI makes components easier to isolate and test. |
| 282 | What is mocking? | Creating simulated objects for testing | Mock objects verify interactions and provide controlled behavior. |
| 283 | What is a stub in testing? | A simple replacement providing predefined responses | Stubs supply fixed results without verifying behavior. |
| 284 | What is a fake implementation? | A simplified working implementation used in tests | Fakes behave like real components but are easier to control. |
| 285 | What is the purpose of unit testing? | Testing isolated pieces of functionality | Unit tests verify individual components independently. |
| 286 | What is integration testing? | Testing multiple components together | Integration tests verify interactions between systems or layers. |
| 287 | What is end-to-end testing? | Testing the complete application workflow | End-to-end tests simulate real user scenarios across the full system. |
| 288 | What is test-driven development (TDD)? | Writing tests before implementation | TDD uses failing tests to guide development and design. |
| 289 | What is the AAA testing pattern? | Arrange, Act, Assert | AAA structures tests into setup, execution, and verification phases. |
| 290 | What is code coverage? | A measurement of executed code during tests | Coverage indicates which parts of an application are exercised by tests. |
| 291 | What is mutation testing? | Testing the effectiveness of test suites by introducing code changes | Mutation testing checks whether tests detect intentionally introduced defects. |
| 292 | What is benchmarking in .NET? | Measuring application performance | Benchmarking evaluates execution speed, memory usage, and optimization impact. |
| 293 | What library is commonly used for .NET benchmarking? | BenchmarkDotNet | BenchmarkDotNet provides accurate performance measurements with statistical analysis. |
| 294 | Why should benchmarks include warmup iterations? | To allow JIT optimization before measurement | Warmup reduces distortion caused by first-run compilation costs. |
| 295 | What is benchmarking overhead? | Performance cost introduced by the measurement process | Benchmarking tools minimize overhead to produce reliable results. |
| 296 | What is profiling? | Analyzing application performance behavior | Profilers identify CPU usage, memory allocations, and bottlenecks. |
| 297 | What is allocation profiling? | Tracking memory allocations | Allocation profiling identifies unnecessary object creation and memory pressure. |
| 298 | What is CPU profiling? | Measuring processor usage by code paths | CPU profiling identifies methods consuming execution time. |
| 299 | What is EventPipe in .NET? | A cross-platform diagnostics data pipeline | EventPipe collects runtime events for profiling and monitoring. |
| 300 | What is dotnet-trace used for? | Collecting runtime tracing information | dotnet-trace captures diagnostic events from running .NET applications. |
| 301 | What is dotnet-counters used for? | Monitoring real-time performance metrics | dotnet-counters displays runtime counters such as CPU usage, GC activity, and thread pool statistics. |
| 302 | What is dotnet-dump used for? | Analyzing memory dumps from .NET processes | dotnet-dump collects and inspects managed process dumps for debugging issues. |
| 303 | What is a memory leak in managed code? | Unintended object retention preventing garbage collection | Managed applications can leak memory when references remain reachable but are no longer needed. |
| 304 | What commonly causes memory leaks in .NET? | Long-lived references, static fields, and event subscriptions | Objects remain alive when something still holds references to them. |
| 305 | Why can events cause memory leaks? | Publishers keep references to subscribers | Event subscriptions prevent subscribers from being garbage collected unless unsubscribed. |
| 306 | What is object retention? | Keeping objects reachable longer than intended | Retained objects consume memory even if they are no longer useful. |
| 307 | What is GC pressure? | Increased workload placed on the garbage collector | Frequent allocations create more collections and can reduce application performance. |
| 308 | What is allocation rate? | The amount of memory allocated over time | High allocation rates can increase garbage collection frequency. |
| 309 | What is object pooling? | Reusing existing objects instead of creating new ones | Object pooling reduces allocation overhead for frequently created objects. |
| 310 | What .NET API provides reusable object pooling support? | Microsoft.Extensions.ObjectPool | ObjectPool provides infrastructure for reusing expensive objects. |
| 311 | What is a StringBuilder used for? | Efficiently building mutable strings | StringBuilder avoids creating many intermediate string objects during concatenation. |
| 312 | Why are strings immutable in .NET? | To improve safety, caching, and thread sharing | Immutable strings cannot be changed after creation, making them safer to reuse. |
| 313 | What happens when two strings have the same value? | They may reference the same interned string | The runtime can reuse identical string instances through string interning. |
| 314 | What is string interning? | Storing identical strings in a shared pool | String interning reduces duplicate string allocations. |
| 315 | What is the difference between ordinal and culture-sensitive comparison? | Ordinal compares characters directly, culture-sensitive uses language rules | Ordinal comparison is preferred for identifiers and technical data. |
| 316 | What is StringComparison.OrdinalIgnoreCase used for? | Case-insensitive culture-independent comparison | It compares strings without considering culture-specific casing rules. |
| 317 | What is globalization in .NET? | Supporting different cultures and languages | .NET provides APIs for formatting, sorting, and localization across cultures. |
| 318 | What is CultureInfo? | Represents culture-specific information | CultureInfo controls formatting rules such as dates, numbers, and currency. |
| 319 | What is localization? | Adapting applications for different languages and regions | Localization replaces user-facing content based on culture settings. |
| 320 | What is resource localization in .NET? | Storing translated resources separately | Resource files allow applications to provide culture-specific text and assets. |
| 321 | What is satellite assembly localization? | Storing localized resources in separate assemblies | Satellite assemblies contain resources for specific cultures. |
| 322 | What is the purpose of ResourceManager? | Retrieves localized resources at runtime | ResourceManager loads resources based on the current culture. |
| 323 | What is globalization-invariant mode? | Running without culture-specific data | It reduces application size by removing globalization data dependencies. |
| 324 | What is regular expression backtracking? | Trying alternative matches during pattern evaluation | Backtracking allows flexible matching but can cause performance issues. |
| 325 | What is catastrophic regex backtracking? | Excessive backtracking causing severe slowdown | Poor regex patterns can cause extremely long execution times. |
| 326 | How can regex performance be improved in .NET? | Use compiled or source-generated regex and efficient patterns | Optimized regex avoids unnecessary parsing and backtracking. |
| 327 | What is RegexOptions.Compiled? | Compiles regex patterns for faster repeated execution | Compiled regex trades startup cost for improved runtime performance. |
| 328 | What is RegexGenerator in modern .NET? | Source generation for regular expressions | Regex source generation creates optimized regex code during compilation. |
| 329 | What is networking in .NET based on? | System.Net APIs | .NET provides networking APIs for HTTP, sockets, DNS, and communication protocols. |
| 330 | What is HttpClient used for? | Sending HTTP requests and receiving responses | HttpClient provides asynchronous HTTP communication capabilities. |
| 331 | Why should HttpClient instances usually be reused? | To avoid socket exhaustion | Reusing HttpClient allows connection pooling and proper resource management. |
| 332 | What is IHttpClientFactory? | A factory for managing HttpClient instances | IHttpClientFactory handles client creation, configuration, and lifetime management. |
| 333 | What is a typed HttpClient? | A strongly typed wrapper around HttpClient | Typed clients encapsulate HTTP communication logic in dedicated classes. |
| 334 | What is a named HttpClient? | A configured HttpClient identified by name | Named clients allow multiple configurations within one application. |
| 335 | What is HTTP content negotiation? | Selecting response formats based on client preferences | Content negotiation determines how data is represented, such as JSON or XML. |
| 336 | What is REST? | An architectural style for web APIs | REST uses resources, HTTP methods, and stateless communication principles. |
| 337 | What does HTTP GET typically represent? | Retrieving a resource | GET requests should generally be safe and idempotent. |
| 338 | What does HTTP POST typically represent? | Creating or processing data | POST sends data to a server for processing. |
| 339 | What does HTTP PUT typically represent? | Replacing a resource | PUT usually performs full updates and is idempotent. |
| 340 | What does HTTP PATCH typically represent? | Partial updates to a resource | PATCH modifies only selected fields of a resource. |
| 341 | What does HTTP DELETE typically represent? | Removing a resource | DELETE requests remove resources identified by a URI. |
| 342 | What is an HTTP status code 200? | Successful request | Status code 200 indicates the request completed successfully. |
| 343 | What is an HTTP status code 201? | Resource created successfully | Status code 201 indicates a new resource was created. |
| 344 | What is an HTTP status code 400? | Client sent an invalid request | Status code 400 indicates malformed or invalid client input. |
| 345 | What is an HTTP status code 401? | Authentication required or failed | Status code 401 indicates the client is not authenticated. |
| 346 | What is an HTTP status code 403? | Access is forbidden | Status code 403 indicates the client is authenticated but lacks permission. |
| 347 | What is an HTTP status code 404? | Resource not found | Status code 404 indicates the requested resource does not exist. |
| 348 | What is an HTTP status code 500? | Server-side failure | Status code 500 indicates an unexpected server error. |
| 349 | What is middleware exception handling in ASP.NET Core? | Centralized error processing | Exception middleware catches unhandled exceptions and formats responses consistently. |
| 350 | What is ProblemDetails in ASP.NET Core? | A standardized error response format | ProblemDetails provides structured HTTP API error responses based on RFC standards. |
| 351 | What is authentication in ASP.NET Core? | Verifying the identity of a user or client | Authentication determines who is making a request, usually through credentials or tokens. |
| 352 | What is authorization in ASP.NET Core? | Determining whether an authenticated user can access a resource | Authorization applies rules and permissions after identity verification. |
| 353 | What is claims-based authentication? | Using claims to represent user information | Claims contain identity details such as roles, permissions, and user attributes. |
| 354 | What is a ClaimsPrincipal? | Represents the current authenticated user | ClaimsPrincipal contains one or more identities and their associated claims. |
| 355 | What is a ClaimsIdentity? | Represents an authentication identity | ClaimsIdentity stores authentication information and claims for a user. |
| 356 | What is JWT authentication? | Authentication using signed JSON Web Tokens | JWT tokens contain claims and are validated without storing session state on the server. |
| 357 | What are the three parts of a JWT? | Header, payload, and signature | JWTs contain metadata, claims, and a cryptographic signature. |
| 358 | Why should JWT payload data not contain secrets? | JWT payloads are encoded but not encrypted by default | Anyone with the token can decode the payload contents. |
| 359 | What is token validation? | Checking whether a security token is trustworthy | Validation verifies signatures, expiration, issuer, and audience values. |
| 360 | What is OAuth 2.0? | An authorization framework for delegated access | OAuth allows applications to access resources on behalf of users without sharing passwords. |
| 361 | What is OpenID Connect? | An identity layer built on OAuth 2.0 | OpenID Connect provides authentication capabilities on top of OAuth. |
| 362 | What is a refresh token? | A token used to obtain new access tokens | Refresh tokens allow longer sessions without repeatedly asking users to authenticate. |
| 363 | What is cookie authentication? | Authentication using encrypted browser cookies | Cookies store authentication tickets that identify signed-in users. |
| 364 | What is antiforgery protection? | Protection against cross-site request forgery attacks | Antiforgery tokens verify that requests originate from trusted pages. |
| 365 | What is CORS? | A browser security mechanism controlling cross-origin requests | CORS defines which external origins are allowed to access resources. |
| 366 | Why is CORS enforced by browsers? | To prevent unauthorized cross-origin access | Browsers restrict scripts from accessing resources on different origins. |
| 367 | What is CSRF? | An attack that tricks users into submitting unwanted requests | CSRF exploits existing authenticated sessions to perform unauthorized actions. |
| 368 | What is XSS? | An attack involving injected client-side scripts | Cross-site scripting allows malicious scripts to execute in users' browsers. |
| 369 | What is SQL injection? | An attack using malicious SQL input | SQL injection manipulates database queries through unsafe input handling. |
| 370 | How does EF Core help prevent SQL injection? | By using parameterized queries | Parameters separate data from SQL commands. |
| 371 | What is HTTPS? | HTTP communication protected with TLS encryption | HTTPS encrypts traffic between clients and servers. |
| 372 | What is TLS? | A cryptographic protocol for secure communication | TLS provides encryption, authentication, and integrity for network connections. |
| 373 | What is hashing? | One-way transformation of data into a fixed-length value | Hashes are commonly used for integrity checks and password storage. |
| 374 | What is salting passwords? | Adding random data before hashing | Salts prevent identical passwords from producing identical hashes. |
| 375 | Why should passwords not be encrypted for storage? | Encryption can be reversed | Passwords should use slow one-way hashing algorithms instead. |
| 376 | What is the purpose of PBKDF2? | Secure password hashing with key stretching | PBKDF2 increases computational cost to slow brute-force attacks. |
| 377 | What is the purpose of Data Protection API in ASP.NET Core? | Protecting sensitive application data | The Data Protection API provides encryption and key management services. |
| 378 | What is dependency injection of IDataProtectionProvider used for? | Creating data protectors | IDataProtectionProvider creates components for encrypting and decrypting data. |
| 379 | What is secure configuration management? | Safely storing secrets and settings | Secure configuration prevents sensitive data exposure. |
| 380 | What is User Secrets in .NET? | Local development secret storage | User Secrets stores sensitive development values outside source control. |
| 381 | What is Azure Key Vault integration used for? | Managing application secrets securely | Key Vault stores keys, certificates, and secrets outside applications. |
| 382 | What is environment-based configuration? | Loading settings based on deployment environment | .NET supports different configuration values for development, testing, and production. |
| 383 | What is the purpose of IHostEnvironment? | Provides information about the application environment | IHostEnvironment identifies environments such as Development and Production. |
| 384 | What is environment-specific configuration? | Configuration loaded based on environment name | Files such as appsettings.Development.json override base settings. |
| 385 | What is feature management? | Dynamically controlling application features | Feature flags allow enabling or disabling functionality without redeployment. |
| 386 | What are feature flags? | Configuration switches controlling application behavior | Feature flags support gradual releases and experimentation. |
| 387 | What is blue-green deployment? | A deployment strategy using two environments | One environment serves traffic while the other is updated and tested. |
| 388 | What is canary deployment? | Gradually releasing changes to a subset of users | Canary releases reduce risk by limiting exposure. |
| 389 | What is health checking in ASP.NET Core? | Monitoring application availability | Health checks expose endpoints that report service status. |
| 390 | What interface defines health checks? | IHealthCheck | IHealthCheck implements custom health monitoring logic. |
| 391 | What is readiness in health checks? | Whether an application can accept traffic | Readiness indicates that dependencies are available and the service can operate. |
| 392 | What is liveness in health checks? | Whether an application is running correctly | Liveness indicates whether the process should be restarted. |
| 393 | What is rate limiting? | Controlling the number of requests allowed | Rate limiting protects systems from overload and abuse. |
| 394 | What is throttling? | Restricting resource usage under load | Throttling prevents excessive consumption of resources. |
| 395 | What is caching? | Storing frequently used data for faster access | Caching reduces repeated computation and external calls. |
| 396 | What is IMemoryCache? | An in-process memory cache | IMemoryCache stores temporary application data in server memory. |
| 397 | What is distributed caching? | Cache storage shared across multiple servers | Distributed caches allow scaled applications to share cached data. |
| 398 | What is IDistributedCache? | An abstraction for distributed cache providers | IDistributedCache supports external cache implementations such as Redis. |
| 399 | What is cache invalidation? | Removing or updating stale cached data | Cache invalidation ensures cached values remain accurate. |
| 400 | What is cache stampede? | Many requests rebuilding the same expired cache entry | Cache stampedes can overload systems when popular data expires simultaneously. |
| 401 | What is Redis commonly used for in .NET applications? | Distributed caching and fast data storage | Redis provides high-speed in-memory storage commonly used for caching, sessions, and messaging. |
| 402 | What is session state in ASP.NET Core? | Storing user-specific data between requests | Session state allows applications to maintain temporary user information across HTTP requests. |
| 403 | Why is session state difficult in distributed applications? | User requests may hit different servers | Distributed applications require shared session storage or sticky sessions. |
| 404 | What is SignalR in ASP.NET Core? | A framework for real-time communication | SignalR enables server-to-client communication using WebSockets and fallback transports. |
| 405 | What is a SignalR hub? | A high-level communication endpoint | Hubs allow clients and servers to call methods on each other. |
| 406 | What protocol does SignalR prefer when available? | WebSockets | WebSockets provide efficient full-duplex communication between client and server. |
| 407 | What is gRPC in .NET? | A high-performance RPC framework | gRPC enables strongly typed service communication using HTTP/2 and Protocol Buffers. |
| 408 | What are Protocol Buffers? | A binary serialization format used by gRPC | Protocol Buffers provide compact and fast message serialization. |
| 409 | What is HTTP/2? | A newer HTTP protocol with multiplexing support | HTTP/2 allows multiple requests over a single connection. |
| 410 | What is HTTP/3? | HTTP over QUIC transport | HTTP/3 improves performance using UDP-based QUIC. |
| 411 | What is WebSocket communication? | Persistent two-way communication over a single connection | WebSockets allow servers and clients to exchange messages continuously. |
| 412 | What is a socket? | A network communication endpoint | Sockets allow applications to communicate over networks using protocols like TCP and UDP. |
| 413 | What is TCP? | A reliable connection-oriented protocol | TCP guarantees ordered delivery of data between endpoints. |
| 414 | What is UDP? | A connectionless protocol optimized for speed | UDP provides lower overhead but does not guarantee delivery. |
| 415 | What is DNS resolution? | Translating domain names into IP addresses | DNS allows applications to locate network resources by name. |
| 416 | What is System.Net.Sockets used for? | Low-level network communication | The namespace provides APIs for TCP, UDP, and socket programming. |
| 417 | What is serialization versioning? | Managing changes to serialized data formats | Versioning ensures compatibility when object structures evolve. |
| 418 | What is backward compatibility in serialization? | Reading older data with newer code | Backward compatibility allows newer versions to understand previous formats. |
| 419 | What is forward compatibility in serialization? | Allowing older code to handle newer data | Forward compatibility allows systems to tolerate future changes. |
| 420 | What is MessagePack? | A compact binary serialization format | MessagePack reduces payload size compared with text-based formats like JSON. |
| 421 | What is Protocol Buffers schema evolution? | Maintaining compatibility when messages change | Protobuf supports adding fields while preserving older readers. |
| 422 | What is the purpose of compression? | Reducing data size | Compression lowers storage and network transfer requirements. |
| 423 | What compression libraries are available in .NET? | System.IO.Compression APIs | .NET provides GZip, Brotli, and Deflate compression support. |
| 424 | What is Brotli compression? | A modern compression algorithm optimized for web content | Brotli often provides better compression ratios than older algorithms. |
| 425 | What is GZip compression? | A widely supported compression format | GZip is commonly used for HTTP response compression. |
| 426 | What is Deflate compression? | A compression algorithm based on LZ77 and Huffman coding | Deflate is used by formats such as ZIP and GZip. |
| 427 | What is file streaming? | Processing files incrementally instead of loading them entirely | Streams allow handling large files efficiently. |
| 428 | What is the Stream class in .NET? | An abstraction for sequential data access | Stream provides a common API for reading and writing data. |
| 429 | What is FileStream used for? | Reading and writing files asynchronously or synchronously | FileStream provides direct file access through streams. |
| 430 | What is MemoryStream used for? | Reading and writing data stored in memory | MemoryStream behaves like a stream backed by memory instead of a file. |
| 431 | What is BufferedStream used for? | Adding buffering to stream operations | BufferedStream reduces expensive I/O operations by batching reads and writes. |
| 432 | What is StreamReader used for? | Reading text from streams | StreamReader converts byte streams into text using an encoding. |
| 433 | What is StreamWriter used for? | Writing text to streams | StreamWriter writes characters to streams using a selected encoding. |
| 434 | What is encoding? | Mapping characters to bytes | Encoding defines how text is represented in binary form. |
| 435 | What is UTF-8? | A variable-length Unicode encoding | UTF-8 represents Unicode characters efficiently and is widely used on the web. |
| 436 | What is Unicode? | A standard for representing characters worldwide | Unicode assigns unique code points to characters from different writing systems. |
| 437 | What is a byte order mark (BOM)? | A marker identifying text encoding | BOM helps identify encoding but is not always required. |
| 438 | What is file locking? | Restricting simultaneous access to files | File locking prevents conflicting reads and writes. |
| 439 | What is FileShare in .NET? | Controls file access sharing behavior | FileShare specifies whether other processes can access an opened file. |
| 440 | What is Path.Combine used for? | Safely joining file system paths | Path.Combine handles directory separators correctly across platforms. |
| 441 | What is DirectoryInfo? | An object-oriented wrapper for directory operations | DirectoryInfo provides methods for inspecting and managing directories. |
| 442 | What is FileInfo? | An object-oriented wrapper for file operations | FileInfo provides metadata and operations for individual files. |
| 443 | What is FileSystemWatcher? | Monitoring file system changes | FileSystemWatcher raises events when files or directories change. |
| 444 | What is temporary file storage in .NET handled by? | Path.GetTempPath and related APIs | .NET provides APIs for safely working with temporary files and directories. |
| 445 | What is serialization security risk? | Executing or processing unsafe data | Unsafe deserialization can allow attacks through malicious payloads. |
| 446 | Why is BinaryFormatter considered unsafe? | It can execute dangerous deserialization behavior | BinaryFormatter has been deprecated due to security risks. |
| 447 | What is the recommended general-purpose serializer in modern .NET? | System.Text.Json | System.Text.Json provides secure and high-performance JSON serialization. |
| 448 | What is a DTO? | Data Transfer Object | DTOs carry data between application boundaries without exposing domain models. |
| 449 | Why use DTOs in APIs? | To control data contracts and prevent overexposure | DTOs separate internal models from external representations. |
| 450 | What is model binding in ASP.NET Core? | Mapping HTTP data to .NET objects | Model binding converts request data into action parameters or objects. |
| 451 | What is model validation in ASP.NET Core? | Checking whether incoming data meets requirements | Validation ensures models satisfy defined rules before processing. |
| 452 | What are data annotations? | Attributes defining validation and metadata rules | Data annotations specify requirements such as required fields and string lengths. |
| 453 | What is FluentValidation? | A library for defining validation rules in code | FluentValidation provides expressive programmatic validation. |
| 454 | What is the purpose of ModelState? | Stores validation results during model binding | ModelState contains binding errors and validation failures. |
| 455 | What is automatic model validation in APIs? | Framework-generated validation responses | ASP.NET Core can automatically return errors for invalid models. |
| 456 | What is API versioning? | Supporting multiple versions of an API | API versioning allows changes without breaking existing clients. |
| 457 | What is content negotiation in APIs? | Selecting response format based on request headers | APIs can return different representations depending on client requirements. |
| 458 | What is HATEOAS? | Adding hypermedia links to API responses | HATEOAS allows clients to discover available actions dynamically. |
| 459 | What is OpenAPI? | A specification for describing HTTP APIs | OpenAPI documents API endpoints, schemas, and operations. |
| 460 | What is Swagger? | A toolset for OpenAPI documentation | Swagger generates interactive API documentation and testing interfaces. |
| 461 | What is NSwag? | An alternative OpenAPI toolset for .NET | NSwag generates API documentation and client code. |
| 462 | What is Minimal API endpoint metadata? | Information attached to API endpoints | Metadata supports documentation, authorization, and filtering behavior. |
| 463 | What is API rate limiting middleware? | Middleware controlling request frequency | It protects APIs from excessive traffic. |
| 464 | What is request throttling strategy? | Limiting requests based on rules | Throttling controls resource usage under heavy load. |
| 465 | What is API gateway architecture? | A centralized entry point for services | API gateways handle routing, authentication, and cross-cutting concerns. |
| 466 | What is microservice architecture? | Splitting applications into independent services | Microservices organize systems as separately deployable components. |
| 467 | What is service discovery? | Finding available service instances dynamically | Service discovery helps distributed applications locate dependencies. |
| 468 | What is containerization? | Packaging applications with dependencies | Containers provide consistent deployment environments. |
| 469 | What is Docker commonly used for in .NET? | Building and running containerized applications | Docker packages .NET applications with required runtime dependencies. |
| 470 | What is Kubernetes used for? | Container orchestration | Kubernetes manages deployment, scaling, and availability of containers. |
| 471 | What is horizontal scaling? | Adding more application instances | Horizontal scaling increases capacity by running additional instances. |
| 472 | What is vertical scaling? | Increasing resources of an existing instance | Vertical scaling adds CPU, memory, or other resources to one machine. |
| 473 | What is stateless application design? | Applications that do not store user state locally | Stateless services scale more easily because any instance can handle requests. |
| 474 | What is idempotency in APIs? | Repeating an operation produces the same result | Idempotent operations are safer for retries in distributed systems. |
| 475 | What is a message queue? | A system for asynchronous communication | Message queues decouple producers and consumers. |
| 476 | What is the producer-consumer pattern? | Separating message creation from processing | Producers generate work while consumers process it independently. |
| 477 | What is event-driven architecture? | Systems communicating through events | Components react to events rather than directly calling each other. |
| 478 | What is domain-driven design (DDD)? | Modeling software around business concepts | DDD focuses on domain logic and business boundaries. |
| 479 | What is an aggregate in DDD? | A group of related entities managed as a unit | Aggregates define consistency boundaries in domain models. |
| 480 | What is an entity in DDD? | An object with a unique identity | Entities are identified by identity rather than only their values. |
| 481 | What is a value object in DDD? | An immutable object defined by its values | Value objects have no identity and are compared by content. |
| 482 | What is a domain event? | A business event that occurred | Domain events represent important changes within a domain. |
| 483 | What is CQRS? | Separating read and write models | CQRS divides commands and queries to optimize different workloads. |
| 484 | What is event sourcing? | Storing changes as a sequence of events | Event sourcing reconstructs state by replaying events. |
| 485 | What is eventual consistency? | Data becoming consistent over time | Distributed systems may temporarily contain different states. |
| 486 | What is a distributed transaction? | A transaction spanning multiple systems | Distributed transactions coordinate changes across separate resources. |
| 487 | What is the CAP theorem? | A principle describing distributed system trade-offs | CAP states that systems cannot simultaneously guarantee consistency, availability, and partition tolerance. |
| 488 | What is resilience engineering? | Designing systems to handle failures | Resilient systems recover gracefully from unexpected problems. |
| 489 | What is Polly in .NET? | A resilience and transient fault handling library | Polly provides retries, circuit breakers, and timeout strategies. |
| 490 | What is a circuit breaker pattern? | Preventing repeated calls to failing services | Circuit breakers stop requests temporarily when failures exceed limits. |
| 491 | What is retry with exponential backoff? | Increasing wait time between retries | Exponential backoff reduces pressure on failing services. |
| 492 | What is timeout handling? | Limiting operation duration | Timeouts prevent operations from blocking indefinitely. |
| 493 | What is fallback behavior? | Providing an alternative result after failure | Fallbacks maintain availability when dependencies fail. |
| 494 | What is bulkhead isolation? | Separating resources to contain failures | Bulkheads prevent one failing component from exhausting shared resources. |
| 495 | What is chaos engineering? | Testing system resilience through controlled failures | Chaos engineering identifies weaknesses before real incidents occur. |
| 496 | What is observability? | Understanding system behavior through telemetry | Observability uses logs, metrics, and traces to diagnose systems. |
| 497 | What are the three pillars of observability? | Logs, metrics, and traces | These signals provide different views into system behavior. |
| 498 | What is distributed tracing? | Tracking requests across multiple services | Distributed tracing follows operations through service boundaries. |
| 499 | What is correlation ID? | An identifier linking related operations | Correlation IDs connect logs and traces belonging to the same request. |
| 500 | What is structured logging important for? | Machine-readable analysis of application events | Structured logs make searching and aggregation easier in monitoring systems. |
| 501 | What is the purpose of ILogger in .NET? | Provides a standardized logging abstraction | ILogger allows applications to write structured logs without depending on a specific logging implementation. |
| 502 | What are logging levels in .NET? | Categories representing message importance | Logging levels such as Trace, Debug, Information, Warning, Error, and Critical control log filtering. |
| 503 | What is structured logging? | Logging data as named properties instead of plain text | Structured logging allows log systems to query and analyze individual fields. |
| 504 | What is log enrichment? | Adding additional context to log messages | Enrichment attaches metadata such as request IDs, users, or machine information. |
| 505 | What is OpenTelemetry? | A standard framework for collecting telemetry | OpenTelemetry provides APIs and tools for distributed tracing, metrics, and logs. |
| 506 | What is a trace span? | A single operation within a distributed trace | Spans represent individual steps of a request across services. |
| 507 | What is a root span? | The first span representing an entire operation | Child spans are created beneath the root span to represent sub-operations. |
| 508 | What is telemetry sampling? | Reducing collected telemetry volume | Sampling keeps representative data while lowering storage and processing costs. |
| 509 | What is application performance monitoring (APM)? | Monitoring application behavior and performance | APM tools analyze failures, latency, and resource usage. |
| 510 | What is latency? | The time required to complete an operation | Lower latency generally means faster responses. |
| 511 | What is throughput? | The amount of work completed over time | Throughput measures system capacity. |
| 512 | What is scalability? | The ability to handle increased workload | Scalable systems maintain performance as demand grows. |
| 513 | What is availability? | The percentage of time a system is operational | Availability measures uptime and reliability. |
| 514 | What is reliability? | The ability to perform correctly over time | Reliable systems consistently deliver expected behavior. |
| 515 | What is fault tolerance? | The ability to continue operating despite failures | Fault-tolerant systems isolate and recover from faults. |
| 516 | What is graceful degradation? | Maintaining partial functionality during failures | Systems continue providing reduced service instead of failing completely. |
| 517 | What is a health probe? | A request used to check service status | Health probes allow monitoring systems to determine application state. |
| 518 | What is a readiness probe commonly used for? | Determining whether traffic should be sent | Readiness prevents unhealthy instances from receiving requests. |
| 519 | What is a liveness probe commonly used for? | Determining whether a restart is needed | Liveness checks whether the process is still functioning. |
| 520 | What is configuration binding in .NET? | Mapping configuration values to strongly typed objects | Configuration binding converts settings into .NET classes. |
| 521 | What is the Options pattern in .NET? | Accessing configuration through strongly typed classes | The Options pattern improves configuration organization and validation. |
| 522 | What is IOptions<T>? | Provides configured option values | IOptions<T> injects configuration settings into services. |
| 523 | What is IOptionsSnapshot<T>? | Provides refreshed scoped option values | IOptionsSnapshot<T> reloads configuration values per request scope. |
| 524 | What is IOptionsMonitor<T>? | Provides change-aware configuration access | IOptionsMonitor<T> detects configuration updates while the application runs. |
| 525 | What is options validation? | Checking configuration correctness at startup or runtime | Validation prevents invalid settings from causing failures later. |
| 526 | What is the .NET Generic Host? | A framework for building application hosts | The Generic Host manages dependency injection, configuration, logging, and application lifetime. |
| 527 | What is IHostBuilder? | A builder for configuring the Generic Host | IHostBuilder configures services and hosting behavior. |
| 528 | What is IHostedService? | A service that runs background tasks | IHostedService allows long-running processes inside a hosted application. |
| 529 | What is BackgroundService? | A base class for hosted background workers | BackgroundService simplifies implementing continuous background operations. |
| 530 | What is ExecuteAsync in BackgroundService? | The method containing worker execution logic | ExecuteAsync runs the background task until cancellation is requested. |
| 531 | What is graceful shutdown in .NET hosting? | Allowing services to finish work before stopping | Graceful shutdown prevents abrupt termination of active operations. |
| 532 | What is application lifetime management? | Controlling startup and shutdown behavior | Lifetime services handle application lifecycle events. |
| 533 | What is IHostApplicationLifetime? | Provides application lifetime events | It exposes callbacks for application start, stopping, and stopped states. |
| 534 | What is dependency injection container disposal? | Cleaning up registered services automatically | The container disposes disposable dependencies according to their lifetimes. |
| 535 | What is IServiceScopeFactory? | Creates dependency injection scopes | IServiceScopeFactory allows manual creation of scoped service lifetimes. |
| 536 | What is the purpose of IServiceProvider? | Resolving registered services | IServiceProvider retrieves dependency injection services at runtime. |
| 537 | Why is resolving services manually discouraged? | It hides dependencies and reduces testability | Constructor injection makes dependencies explicit. |
| 538 | What is a transient service lifetime? | A new instance every time it is requested | Transient services are suitable for lightweight stateless dependencies. |
| 539 | What is a scoped service lifetime? | One instance per scope | Scoped services commonly represent request-level operations. |
| 540 | What is a singleton service lifetime? | One instance for the application's lifetime | Singleton services are shared throughout the application. |
| 541 | What happens if a singleton stores scoped data? | It can cause incorrect shared state | Singleton objects outlive scopes and may accidentally retain request data. |
| 542 | What is middleware ordering importance? | Middleware executes in registration order | Incorrect ordering can change authentication, routing, and response behavior. |
| 543 | What is terminal middleware? | Middleware that ends the request pipeline | Terminal middleware does not call the next delegate. |
| 544 | What is UseRouting()? | Adds endpoint routing capabilities | UseRouting selects matching endpoints for requests. |
| 545 | What is UseAuthentication()? | Adds authentication processing | UseAuthentication establishes the current user's identity. |
| 546 | What is UseAuthorization()? | Adds authorization checks | UseAuthorization enforces access policies. |
| 547 | What is MapControllers()? | Maps controller endpoints | MapControllers connects controller actions to routing. |
| 548 | What is endpoint routing? | A routing system based on endpoint metadata | Endpoint routing separates route matching from execution. |
| 549 | What is attribute routing? | Defining routes using attributes | Attributes such as Route and HttpGet specify endpoint paths. |
| 550 | What is conventional routing? | Defining routes through patterns | Conventional routing uses centralized route templates instead of attributes. |
| 551 | What is endpoint metadata in ASP.NET Core? | Information attached to endpoints | Endpoint metadata stores attributes and configuration used by routing, authorization, and documentation systems. |
| 552 | What is route constraint in ASP.NET Core? | A rule restricting which values match a route | Route constraints prevent invalid values from reaching endpoints. |
| 553 | What is a route parameter? | A variable section of a URL pattern | Route parameters allow endpoints to receive values from request paths. |
| 554 | What is URL generation in ASP.NET Core? | Creating URLs from route information | URL generation builds links based on registered routes and endpoint metadata. |
| 555 | What is model binding source inference? | Automatically determining where values come from | ASP.NET Core can infer values from route, query, headers, or body. |
| 556 | What does the FromBody attribute do? | Binds data from the request body | FromBody deserializes incoming request content into an object. |
| 557 | What does the FromQuery attribute do? | Binds values from query string parameters | FromQuery maps URL query values to action parameters. |
| 558 | What does the FromRoute attribute do? | Binds values from route parameters | FromRoute retrieves values embedded in the URL path. |
| 559 | What does the FromHeader attribute do? | Binds values from HTTP headers | FromHeader maps request header values to parameters. |
| 560 | What does the FromServices attribute do? | Resolves a parameter from dependency injection | FromServices injects services directly into controller actions. |
| 561 | What is Minimal API in ASP.NET Core? | A lightweight API programming model | Minimal APIs define endpoints with less ceremony than controllers. |
| 562 | What is a route handler in Minimal API? | A delegate that processes an endpoint request | Route handlers contain endpoint execution logic. |
| 563 | What is endpoint filtering in Minimal APIs? | Logic executed before or after endpoint handlers | Endpoint filters provide reusable request processing. |
| 564 | What is Results<T> in Minimal APIs? | A typed result union | Results<T> provides strongly typed HTTP responses. |
| 565 | What is IResult in ASP.NET Core? | An abstraction representing an HTTP response | IResult allows endpoints to return different response types. |
| 566 | What is ControllerBase? | A base class for API controllers | ControllerBase provides HTTP-specific controller functionality without view support. |
| 567 | What is ActionResult<T>? | A controller return type supporting typed responses | ActionResult<T> combines data responses and HTTP result responses. |
| 568 | What is the difference between IActionResult and ActionResult<T>? | ActionResult<T> provides stronger typing | ActionResult<T> improves API metadata and compile-time checking. |
| 569 | What is ApiControllerAttribute? | Enables API-specific controller behavior | ApiController enables automatic validation and binding conventions. |
| 570 | What is automatic HTTP 400 generation? | Framework-generated bad request responses | Invalid model states can automatically produce validation responses. |
| 571 | What is content-type negotiation? | Selecting request and response media formats | Content negotiation determines how data is represented. |
| 572 | What is a media type? | A value describing data format | Examples include application/json and text/plain. |
| 573 | What is formatter in ASP.NET Core? | Component converting objects to HTTP content | Formatters handle serialization and deserialization. |
| 574 | What is output formatting? | Converting objects into response data | Output formatting serializes server objects for clients. |
| 575 | What is input formatting? | Converting request data into objects | Input formatting deserializes incoming request bodies. |
| 576 | What is MVC in ASP.NET Core? | Model-View-Controller architectural framework | MVC separates application data, presentation, and request handling. |
| 577 | What is a view in MVC? | A UI representation generated from data | Views typically use Razor syntax to generate HTML. |
| 578 | What is Razor syntax? | A template syntax combining HTML and C# | Razor allows server-side C# expressions inside markup. |
| 579 | What is Razor Pages? | A page-focused web development model | Razor Pages organizes UI logic around individual pages. |
| 580 | What is a PageModel in Razor Pages? | The code-behind model for a Razor Page | PageModel contains handlers and page logic. |
| 581 | What is a tag helper? | A server-side component modifying HTML elements | Tag helpers simplify generating dynamic HTML. |
| 582 | What is a view component? | A reusable rendering component in MVC | View components encapsulate UI logic and rendering. |
| 583 | What is partial view? | A reusable fragment of a view | Partial views allow sharing markup between pages. |
| 584 | What is layout in Razor? | A shared page template | Layouts provide common HTML structure across views. |
| 585 | What is Razor compilation? | Converting Razor templates into executable code | Razor files are compiled for efficient rendering. |
| 586 | What is Blazor? | A .NET web UI framework using C# | Blazor allows building interactive web applications with .NET. |
| 587 | What is Blazor Server? | Blazor running UI logic on the server | Blazor Server communicates UI updates through SignalR connections. |
| 588 | What is Blazor WebAssembly? | Blazor running .NET code in the browser | Blazor WebAssembly executes .NET applications client-side through WebAssembly. |
| 589 | What is a Blazor component? | A reusable UI building block | Components contain markup, logic, and state. |
| 590 | What is component lifecycle in Blazor? | Events controlling component creation and updates | Lifecycle methods run during initialization, rendering, and disposal. |
| 591 | What is StateHasChanged()? | Triggers a Blazor component re-render | StateHasChanged notifies Blazor that component state changed. |
| 592 | What is dependency injection in Blazor? | Providing services to components | Blazor supports injecting services into components. |
| 593 | What is cascading parameter in Blazor? | Passing values through a component hierarchy | Cascading parameters avoid manually passing values through every component. |
| 594 | What is EventCallback in Blazor? | A mechanism for component event communication | EventCallback allows child components to notify parent components. |
| 595 | What is JavaScript interop in Blazor? | Communication between C# and JavaScript | JS interop allows Blazor applications to call browser APIs. |
| 596 | What is prerendering in Blazor? | Rendering components before full client activation | Prerendering improves initial page loading experience. |
| 597 | What is WebAssembly? | A portable binary execution format | WebAssembly allows high-performance code execution in browsers. |
| 598 | What is AOT compilation in .NET? | Ahead-of-time compilation | AOT produces native code before execution to improve startup performance. |
| 599 | What is Native AOT? | Publishing .NET applications as native executables | Native AOT removes runtime compilation requirements and reduces startup time. |
| 600 | What is trimming in .NET publishing? | Removing unused assemblies and members | Trimming reduces application size by analyzing reachable code. |
| 601 | What is reflection in .NET? | Inspecting and interacting with types at runtime | Reflection allows applications to discover metadata and invoke members dynamically. |
| 602 | What metadata does reflection access? | Information about assemblies, types, members, and attributes | The CLR stores metadata that reflection can query at runtime. |
| 603 | What is Type in .NET? | A runtime representation of a type | Type objects provide metadata and reflection capabilities. |
| 604 | What is Activator.CreateInstance used for? | Creating objects dynamically | Activator.CreateInstance creates instances when the concrete type is known only at runtime. |
| 605 | What is MethodInfo? | Represents metadata about a method | MethodInfo allows inspection and invocation of methods through reflection. |
| 606 | What is PropertyInfo? | Represents metadata about a property | PropertyInfo allows reading and modifying properties dynamically. |
| 607 | What is FieldInfo? | Represents metadata about a field | FieldInfo provides access to field information and values. |
| 608 | What is Assembly metadata? | Information describing a compiled assembly | Assembly metadata contains names, versions, references, and attributes. |
| 609 | What is an attribute in C#? | Metadata attached to program elements | Attributes provide additional information to the compiler or runtime. |
| 610 | What is AttributeUsageAttribute? | Defines where an attribute can be applied | AttributeUsage controls targets, inheritance, and repetition behavior. |
| 611 | What is a custom attribute? | A user-defined metadata annotation | Custom attributes allow applications to attach specialized information to code. |
| 612 | What is source generation in .NET? | Generating code during compilation | Source generators create additional C# code based on project information. |
| 613 | What interface do source generators implement? | IIncrementalGenerator or ISourceGenerator | These interfaces define how generators produce code during compilation. |
| 614 | What is incremental source generation? | A source generation model that tracks changes efficiently | Incremental generators avoid repeating unnecessary work during builds. |
| 615 | What is Roslyn? | The .NET compiler platform | Roslyn provides APIs for analyzing and transforming C# and VB code. |
| 616 | What is a syntax tree in Roslyn? | A structured representation of source code | Syntax trees represent code tokens and language structure. |
| 617 | What is a semantic model in Roslyn? | Provides meaning and symbol information about code | Semantic models resolve types, symbols, and references. |
| 618 | What is a code analyzer? | A tool that examines code quality | Analyzers detect potential bugs, style issues, and performance problems. |
| 619 | What is a diagnostic in Roslyn? | A reported issue from analysis | Diagnostics describe warnings, errors, or suggestions. |
| 620 | What is a code fix provider? | Automatically applies corrections to diagnostics | Code fix providers generate suggested source changes. |
| 621 | What is the difference between compile-time and runtime errors? | Compile-time errors occur during compilation, runtime errors occur during execution | The compiler catches syntax and type issues before running the program. |
| 622 | What is nullable reference type analysis? | Compile-time checking for possible null references | Nullable analysis helps prevent NullReferenceException issues. |
| 623 | What does the `?` annotation mean on reference types? | The reference may contain null | Nullable annotations describe possible null states. |
| 624 | What does the null-forgiving operator `!` do? | Suppresses nullable warnings | It tells the compiler a value is assumed not to be null. |
| 625 | What is the null-coalescing operator `??`? | Provides an alternative value when null | The operator returns the left value unless it is null. |
| 626 | What is the null-conditional operator `?.`? | Safely accesses members on possibly null values | It returns null instead of throwing when the target is null. |
| 627 | What is the null-coalescing assignment operator `??=`? | Assigns only when a value is null | It simplifies lazy initialization patterns. |
| 628 | What is pattern matching with property patterns? | Matching based on object properties | Property patterns inspect object members during matching. |
| 629 | What is a relational pattern in C#? | Pattern matching using comparison operators | Relational patterns compare values using operators like < and >=. |
| 630 | What is a list pattern in C#? | Pattern matching against collection elements | List patterns inspect array or collection structures. |
| 631 | What is a switch expression? | An expression-based form of switch | Switch expressions return values directly from matching cases. |
| 632 | What is exhaustive pattern matching? | Ensuring all possible cases are handled | Exhaustive matching reduces missing-case errors. |
| 633 | What is a discard pattern `_`? | Matches any remaining value | Discards handle cases where the value is not important. |
| 634 | What is a tuple pattern? | Pattern matching multiple values together | Tuple patterns allow matching several values at once. |
| 635 | What is deconstruction in C#? | Extracting values from objects into variables | Deconstruction simplifies working with tuples and custom types. |
| 636 | What method enables custom deconstruction? | Deconstruct() | Types can define Deconstruct methods to support tuple-style assignment. |
| 637 | What are records in C#? | Reference types designed for immutable data models | Records provide value-based equality and concise syntax. |
| 638 | What are record structs? | Value-type records | Record structs combine record features with value-type behavior. |
| 639 | How do records compare equality? | By values rather than references | Records automatically generate value-based equality members. |
| 640 | What is the with expression in C#? | Creates modified copies of immutable objects | The with expression copies an object while changing selected members. |
| 641 | What is init-only property? | A property assignable only during initialization | Init properties support immutable object designs. |
| 642 | What is required member in C#? | A member that must be initialized during object creation | Required members enforce initialization at compile time. |
| 643 | What attribute supports required members? | RequiredMemberAttribute | The compiler uses required member metadata to enforce initialization rules. |
| 644 | What is a file-scoped namespace? | A namespace declaration applying to the whole file | File-scoped namespaces reduce indentation and boilerplate. |
| 645 | What are global using directives? | Shared using directives across files | Global usings reduce repeated namespace imports. |
| 646 | What is a top-level statement? | C# code written without an explicit Main method | The compiler generates the program entry point automatically. |
| 647 | What is implicit usings in .NET projects? | Automatically included namespaces | Implicit usings reduce common using statements in project files. |
| 648 | What is an interpolated string handler? | A customizable string interpolation mechanism | Interpolated string handlers improve performance by controlling formatting behavior. |
| 649 | What is constant interpolation? | Compile-time evaluation of interpolated strings | Certain interpolated strings can be evaluated during compilation. |
| 650 | What is raw string literal syntax? | A string syntax allowing fewer escaping rules | Raw strings simplify embedding quotes and multiline content. |
| 651 | What is the purpose of the `nameof` operator in C#? | Returns the name of a symbol as a string | nameof provides compile-time safe names for variables, members, and types. |
| 652 | What is the purpose of the `typeof` operator? | Gets a Type object representing a type | typeof is used to obtain runtime type metadata. |
| 653 | What is the difference between `nameof` and `typeof`? | nameof returns a string, typeof returns type metadata | nameof is resolved at compile time while typeof creates a Type reference. |
| 654 | What is the `default` literal in C#? | Represents the default value of a type | default produces null for references and zero-equivalent values for value types. |
| 655 | What is target-typed new expression? | Creating objects without repeating the type name | The compiler infers the type from the assignment context. |
| 656 | What is implicit conversion? | A conversion performed automatically by the compiler | Implicit conversions occur when no data loss is expected. |
| 657 | What is explicit conversion? | A conversion requiring a cast | Explicit conversions are used when the compiler cannot guarantee safety. |
| 658 | What is boxing? | Converting a value type into an object reference | Boxing wraps a value type inside a heap object. |
| 659 | What is unboxing? | Extracting a value type from an object | Unboxing requires the object to contain the correct original value type. |
| 660 | Why is boxing expensive? | It allocates and copies data to the heap | Boxing introduces allocation and garbage collection overhead. |
| 661 | What is covariance in C# generics? | Allowing a more derived type where a base type is expected | Covariance applies to output-only generic parameters. |
| 662 | What is contravariance in C# generics? | Allowing a base type where a derived type is expected | Contravariance applies to input-only generic parameters. |
| 663 | Which keyword defines covariance? | out | The out keyword enables covariance on generic interfaces and delegates. |
| 664 | Which keyword defines contravariance? | in | The in keyword enables contravariance on generic interfaces and delegates. |
| 665 | What is generic type inference? | Compiler determination of generic type arguments | The compiler can infer generic types from method arguments. |
| 666 | What is generic specialization? | Creating optimized versions of generic code for value types | The runtime can generate specialized code paths for certain generic usages. |
| 667 | Why are generics faster than object-based collections? | They avoid boxing and casting | Generics provide compile-time type safety and better performance. |
| 668 | What is a generic constraint? | A rule limiting allowed type arguments | Constraints restrict which types can be used with a generic parameter. |
| 669 | What does the `class` generic constraint mean? | Requires a reference type | The type argument must be a class or reference type. |
| 670 | What does the `struct` generic constraint mean? | Requires a non-nullable value type | The type argument must be a value type. |
| 671 | What does the `new()` generic constraint require? | A public parameterless constructor | The type must provide a parameterless constructor. |
| 672 | What does the `notnull` constraint require? | Prevents nullable type arguments | The type argument cannot be a nullable reference or nullable value type. |
| 673 | What does the `default` generic constraint do? | Resolves overrides involving nullable constraints | It allows overriding methods without repeating conflicting constraints. |
| 674 | What is generic math in .NET? | Performing mathematical operations through generic interfaces | Static abstract interface members enable generic numeric algorithms. |
| 675 | What interface enables generic numeric operations? | INumber<T> | INumber<T> defines common numeric operations for generic math. |
| 676 | What is operator overloading? | Defining custom behavior for operators | Types can specify how operators work with their instances. |
| 677 | Which operators cannot be overloaded? | Some operators such as assignment and member access | C# restricts overloading of certain language operators. |
| 678 | What is user-defined conversion? | A custom implicit or explicit type conversion | Types can define conversions using conversion operators. |
| 679 | What is the difference between implicit and explicit operators? | Implicit conversions happen automatically, explicit require casting | Explicit operators indicate potential loss or ambiguity. |
| 680 | What is an extension method? | A method that adds functionality to an existing type | Extension methods appear as instance methods while being static methods internally. |
| 681 | What keyword identifies extension method declarations? | this | The first parameter marked with this specifies the extended type. |
| 682 | What are extension method limitations? | They cannot access private members | Extension methods do not become actual members of the extended type. |
| 683 | What is partial class? | A class split across multiple files | Partial classes allow generated and manual code to coexist. |
| 684 | What is partial method? | A method declaration split between partial class files | Partial methods allow optional implementations. |
| 685 | What is an anonymous type? | A compiler-generated immutable-like type | Anonymous types are useful for temporary projections. |
| 686 | What is an anonymous function? | A function without a declared name | Lambdas and anonymous methods create anonymous functions. |
| 687 | What is a lambda expression? | A concise way to define anonymous functions | Lambdas are commonly used with LINQ and delegates. |
| 688 | What is a delegate? | A type-safe reference to a method | Delegates allow methods to be passed as values. |
| 689 | What is a multicast delegate? | A delegate containing multiple method references | Multicast delegates invoke multiple methods in sequence. |
| 690 | What is Action<T>? | A delegate returning void | Action represents methods that perform operations without returning values. |
| 691 | What is Func<T>? | A delegate returning a value | Func represents methods that produce results. |
| 692 | What is Predicate<T>? | A delegate returning a Boolean result | Predicate is commonly used for filtering conditions. |
| 693 | What is delegate covariance? | Allowing compatible return type conversions | Delegate covariance applies to output parameters. |
| 694 | What is delegate contravariance? | Allowing compatible parameter type conversions | Delegate contravariance applies to input parameters. |
| 695 | What is event in C#? | A restricted delegate for notifications | Events allow subscribers to listen without directly invoking the delegate. |
| 696 | Why are events usually exposed instead of delegates? | To restrict external invocation | Only the declaring type can raise an event. |
| 697 | What is EventHandler<TEventArgs>? | A standard event delegate pattern | It provides a common structure for .NET events. |
| 698 | What is the EventArgs class? | Base class for event data | EventArgs represents information passed with events. |
| 699 | What is the observer pattern implemented with in .NET? | Events and delegates | .NET events provide a built-in observer mechanism. |
| 700 | What is the purpose of multicast event invocation? | Notifying multiple subscribers | Events can notify multiple registered handlers. |
| 701 | What is the purpose of IDisposable in .NET? | Defines deterministic resource cleanup | IDisposable allows objects to release unmanaged resources or perform cleanup before garbage collection. |
| 702 | What language construct automatically calls Dispose()? | using statement | The using statement ensures IDisposable resources are cleaned up even when exceptions occur. |
| 703 | What is a using declaration? | A shorter syntax for automatic disposal | Using declarations dispose resources at the end of the containing scope. |
| 704 | What is the Dispose pattern? | A standard pattern for releasing resources | The Dispose pattern combines managed cleanup and unmanaged resource release. |
| 705 | Why does Dispose sometimes call GC.SuppressFinalize()? | To avoid unnecessary finalizer execution | Suppressing finalization improves performance when cleanup has already occurred. |
| 706 | What is a finalizer in C#? | A method executed before garbage collection reclaims an object | Finalizers provide a backup mechanism for unmanaged resource cleanup. |
| 707 | What syntax defines a finalizer? | ~ClassName() | A finalizer uses a destructor-like syntax in C#. |
| 708 | Why should finalizers be avoided when possible? | They delay garbage collection and add overhead | Finalizable objects require additional GC processing. |
| 709 | What is SafeHandle in .NET? | A safer wrapper for unmanaged handles | SafeHandle provides reliable cleanup of operating system resources. |
| 710 | What is unmanaged resource? | A resource not automatically managed by the CLR | Examples include file handles, sockets, and native memory. |
| 711 | What is managed resource? | Memory or objects controlled by the CLR | Managed resources are automatically handled by garbage collection. |
| 712 | What is P/Invoke? | Calling native functions from managed code | Platform Invocation allows .NET applications to interact with native libraries. |
| 713 | What namespace contains P/Invoke attributes? | System.Runtime.InteropServices | This namespace provides interop types and attributes. |
| 714 | What is DllImportAttribute used for? | Declaring external native functions | DllImport allows managed code to call functions from native libraries. |
| 715 | What is marshalling? | Converting data between managed and unmanaged representations | Marshalling allows data exchange across runtime boundaries. |
| 716 | What is COM interop? | Communication between .NET and COM components | COM interop allows managed applications to use legacy COM technologies. |
| 717 | What is unmanaged function pointer support in C#? | Calling native functions using function pointers | Function pointers provide lower-level interop capabilities. |
| 718 | What is unsafe code in C#? | Code allowing direct memory manipulation | Unsafe code enables pointers and advanced performance scenarios. |
| 719 | What keyword enables unsafe blocks? | unsafe | The unsafe keyword allows pointer operations. |
| 720 | What is a pointer in C#? | A variable storing a memory address | Pointers provide direct access to memory locations. |
| 721 | What is stackalloc? | Allocating memory on the stack | stackalloc creates temporary stack-based memory buffers. |
| 722 | Why is stackalloc faster than heap allocation? | It avoids garbage collection overhead | Stack memory is automatically released when the scope ends. |
| 723 | What types can stackalloc create? | Unmanaged types and Span-compatible buffers | Stack allocation requires memory-safe layouts. |
| 724 | What is fixed statement used for? | Preventing garbage collector movement of objects | fixed allows obtaining stable pointers to managed memory. |
| 725 | Why does the GC move objects? | To compact heap memory | Moving objects reduces fragmentation and improves allocation efficiency. |
| 726 | What is object pinning? | Preventing an object from being moved by GC | Pinning is required when unmanaged code accesses managed memory directly. |
| 727 | What is GCHandle? | A mechanism for controlling managed object references | GCHandle allows objects to be pinned or referenced manually. |
| 728 | What is memory fragmentation? | Scattered unused memory regions | Fragmentation can reduce allocation efficiency. |
| 729 | What is the Large Object Heap (LOH)? | Heap area for large allocations | Large objects are allocated separately due to their size. |
| 730 | What size typically places objects on the LOH? | Around 85 KB or larger | Objects above the threshold are allocated on the Large Object Heap. |
| 731 | Why can LOH allocations hurt performance? | Large objects are expensive to allocate and collect | Frequent large allocations increase memory pressure. |
| 732 | What is LOH compaction? | Rearranging large objects to reduce fragmentation | LOH compaction is optional because it can be expensive. |
| 733 | What is the Pinned Object Heap (POH)? | A heap for objects intended to remain pinned | POH reduces fragmentation caused by pinned objects. |
| 734 | What is GC.TryStartNoGCRegion used for? | Temporarily preventing garbage collections | It reserves memory for latency-sensitive operations. |
| 735 | What happens if NoGCRegion memory is exceeded? | A garbage collection may occur or the operation fails | The runtime cannot continue indefinitely without collection. |
| 736 | What is latency mode in GC? | Controls garbage collector responsiveness behavior | GC latency modes adjust pause-time versus throughput trade-offs. |
| 737 | What is SustainedLowLatency GC mode? | A mode minimizing pauses during long operations | It reduces blocking collections while maintaining throughput. |
| 738 | What is Batch GC mode? | A mode optimized for maximum throughput | Batch mode favors completed work over responsiveness. |
| 739 | What is Server GC? | A garbage collector optimized for high-throughput applications | Server GC uses multiple heaps and is designed for servers. |
| 740 | What is Workstation GC? | A garbage collector optimized for desktop applications | Workstation GC prioritizes responsiveness. |
| 741 | What is GC.GetAllocatedBytesForCurrentThread used for? | Measuring allocations made by a thread | It helps analyze allocation behavior. |
| 742 | What is WeakReference? | A reference that does not prevent garbage collection | Weak references allow objects to be collected when memory is needed. |
| 743 | What is ConditionalWeakTable? | A table storing weakly associated object data | Entries are removed when keys are collected. |
| 744 | What is object resurrection? | Bringing an object back during finalization | Resurrection occurs when a finalizer stores a reference to the object. |
| 745 | Why is object resurrection discouraged? | It complicates memory management | Resurrection can create unpredictable object lifetimes. |
| 746 | What is memory pressure notification? | Informing the GC about unmanaged memory usage | It helps the GC make better collection decisions. |
| 747 | What API reports memory pressure? | GC.AddMemoryPressure | It informs the runtime about significant unmanaged allocations. |
| 748 | What API removes reported memory pressure? | GC.RemoveMemoryPressure | It signals that previously reported unmanaged memory is released. |
| 749 | What is runtime hosting? | Embedding or controlling the CLR from another application | Hosting APIs allow native applications to load and interact with .NET. |
| 750 | What is the CLR? | The Common Language Runtime | CLR manages execution, memory, exceptions, and type safety for .NET applications. |
| 751 | What is the purpose of the CTS in .NET? | Defines a common type system | The Common Type System ensures different .NET languages can interact using compatible types. |
| 752 | What is CLS in .NET? | A set of rules for language interoperability | The Common Language Specification defines features supported by all .NET languages. |
| 753 | What is a Common Intermediate Language (CIL)? | A CPU-independent instruction set | CIL is generated by .NET compilers before runtime compilation. |
| 754 | What is metadata in a .NET assembly? | Information describing types and members | Metadata allows the CLR to understand and manage compiled code. |
| 755 | What is a manifest in an assembly? | Assembly information describing identity and dependencies | The manifest contains version, references, and security information. |
| 756 | What is a strong-named assembly? | An assembly signed with a cryptographic key | Strong naming provides identity and version uniqueness. |
| 757 | What is the purpose of assembly versioning? | Managing compatibility between assembly releases | Versioning allows applications to identify compatible dependencies. |
| 758 | What are the four parts of a .NET assembly version? | Major, minor, build, revision | Assembly versions follow a structured numbering system. |
| 759 | What is binding redirect? | Redirecting assembly version requests | Binding redirects allow applications to use newer dependency versions. |
| 760 | What is assembly loading context? | The environment controlling how assemblies are loaded | Loading contexts determine assembly resolution behavior. |
| 761 | What is AssemblyLoadContext? | A mechanism for loading assemblies dynamically | AssemblyLoadContext enables isolation and custom loading behavior. |
| 762 | Why use AssemblyLoadContext? | To isolate plugins or load multiple versions of assemblies | It provides controlled assembly loading boundaries. |
| 763 | What is reflection-only loading? | Loading metadata without executing code | It allows inspection of assemblies without running them. |
| 764 | What is a plugin architecture? | A system allowing extensions to be loaded dynamically | Plugins add functionality without modifying the core application. |
| 765 | What interface is commonly used for .NET plugins? | A shared contract interface | Plugins implement a known interface so the host can interact with them. |
| 766 | What is an application domain in .NET Framework? | An isolation boundary for managed code | AppDomains separated applications within the same process in older .NET versions. |
| 767 | Why are AppDomains less common in modern .NET? | AssemblyLoadContext replaced many isolation scenarios | Modern .NET uses lighter mechanisms for assembly isolation. |
| 768 | What is the difference between process and thread? | A process is an isolated application, a thread is an execution path within it | Processes contain memory spaces while threads execute code. |
| 769 | What is a managed thread? | A thread controlled by the CLR | Managed threads integrate with .NET scheduling and runtime services. |
| 770 | What is Thread class used for? | Creating and controlling operating system threads | Thread provides low-level thread management. |
| 771 | What is ThreadPool? | A pool of reusable worker threads | ThreadPool avoids the overhead of repeatedly creating threads. |
| 772 | Why use ThreadPool instead of creating threads manually? | It improves efficiency through reuse | ThreadPool manages thread creation and scheduling automatically. |
| 773 | What is a thread pool starvation? | When available worker threads are exhausted | Starvation causes delayed execution of queued work. |
| 774 | What commonly causes thread pool starvation? | Blocking calls and long-running synchronous work | Blocking prevents threads from returning to the pool. |
| 775 | What is TaskScheduler? | Controls how tasks are executed | TaskScheduler determines where and when tasks run. |
| 776 | What is the default TaskScheduler? | ThreadPool-based scheduler | Most tasks execute on ThreadPool threads. |
| 777 | What is Task.Run used for? | Scheduling CPU-bound work asynchronously | Task.Run queues work to the thread pool. |
| 778 | Why should Task.Run not wrap every async method? | It adds unnecessary scheduling overhead | Async I/O already avoids blocking without extra threads. |
| 779 | What is async-over-sync? | Wrapping synchronous work as asynchronous | It often wastes threads because the operation still blocks. |
| 780 | What is sync-over-async? | Blocking on asynchronous operations | It can cause deadlocks and thread pool starvation. |
| 781 | What does Task.Wait() do? | Blocks the current thread until completion | Wait synchronously blocks execution. |
| 782 | What does GetAwaiter().GetResult() do? | Synchronously waits for an async operation | It unwraps exceptions but can still cause blocking issues. |
| 783 | What is a continuation in TPL? | Code executed after a task completes | Continuations allow chaining operations after asynchronous work. |
| 784 | What is TaskContinuationOptions? | Configuration options for task continuations | Options control when and how continuations execute. |
| 785 | What is TaskCompletionSource? | A way to manually control task completion | It creates tasks that complete through explicit signaling. |
| 786 | What is TaskCompletionSource useful for? | Wrapping callback APIs as tasks | It bridges older asynchronous patterns with Task-based APIs. |
| 787 | What is a cancellation token? | A cooperative cancellation mechanism | Cancellation tokens allow operations to observe cancellation requests. |
| 788 | What is CancellationTokenSource? | Creates and controls cancellation tokens | It signals cancellation to linked operations. |
| 789 | What is linked cancellation token source? | Combines multiple cancellation signals | Linked tokens cancel when any parent token is canceled. |
| 790 | What happens when a CancellationToken is canceled? | It signals listeners but does not force termination | Operations must check and respond to cancellation. |
| 791 | What is cooperative cancellation? | Tasks voluntarily stop after receiving a cancellation request | .NET cancellation does not forcibly terminate threads. |
| 792 | What is Parallel.For? | A parallel loop for CPU-bound operations | Parallel.For distributes iterations across multiple threads. |
| 793 | What is Parallel.ForEachAsync? | Asynchronous parallel iteration | It combines parallel execution with async delegates. |
| 794 | What is PLINQ? | Parallel Language Integrated Query | PLINQ executes LINQ queries using multiple processors. |
| 795 | What extension method enables PLINQ? | AsParallel() | AsParallel converts LINQ queries into parallel queries. |
| 796 | What is the danger of excessive parallelism? | Overhead can exceed performance benefits | Too many tasks can reduce efficiency. |
| 797 | What is thread safety? | Correct behavior when accessed concurrently | Thread-safe code prevents race conditions. |
| 798 | What is a race condition? | Incorrect behavior caused by timing-dependent access | Race conditions occur when threads access shared data unsafely. |
| 799 | What is a critical section? | Code requiring exclusive access | Critical sections protect shared resources from concurrent modification. |
| 800 | What is a lock in C#? | A synchronization mechanism using Monitor | lock ensures only one thread enters a protected section at a time. |
| 801 | What is Monitor in C#? | A synchronization primitive for controlling access to critical sections | Monitor provides locking, waiting, and signaling capabilities for threads. |
| 802 | What is the difference between lock and Monitor? | lock is syntactic sugar for Monitor usage | lock internally calls Monitor.Enter and Monitor.Exit with exception safety. |
| 803 | What does Monitor.Wait() do? | Releases a lock and waits for a signal | Wait allows another thread to acquire the lock and perform work. |
| 804 | What does Monitor.Pulse() do? | Signals one waiting thread | Pulse wakes a thread waiting on the same lock object. |
| 805 | What does Monitor.PulseAll() do? | Signals all waiting threads | PulseAll wakes every thread waiting on the synchronization object. |
| 806 | What is a Mutex? | A synchronization object that can work across processes | Mutex provides exclusive access between different processes. |
| 807 | What is a Semaphore? | A synchronization primitive limiting concurrent access | Semaphore allows a fixed number of threads to enter a section. |
| 808 | What is SemaphoreSlim? | A lightweight semaphore for managed code | SemaphoreSlim is optimized for in-process asynchronous scenarios. |
| 809 | What is ReaderWriterLockSlim? | A lock optimized for multiple readers | ReaderWriterLockSlim allows concurrent reads but exclusive writes. |
| 810 | What is Interlocked in .NET? | Provides atomic operations | Interlocked performs thread-safe operations without traditional locks. |
| 811 | What operations does Interlocked provide? | Atomic increment, decrement, exchange, and compare operations | Interlocked supports lock-free synchronization primitives. |
| 812 | What is CompareExchange? | An atomic conditional replacement operation | CompareExchange updates a value only if it matches an expected value. |
| 813 | What is lock-free programming? | Writing concurrent code without traditional locks | Lock-free algorithms use atomic operations instead of blocking synchronization. |
| 814 | What is volatile used for? | Ensuring memory visibility between threads | volatile prevents compiler and CPU optimizations from hiding updates. |
| 815 | Why does volatile not make operations atomic? | It only guarantees visibility | Compound operations still require synchronization. |
| 816 | What is a memory barrier? | A mechanism controlling memory operation ordering | Memory barriers ensure operations are observed consistently across threads. |
| 817 | What is false sharing? | Performance loss from threads modifying nearby memory locations | Cache line contention can reduce parallel performance. |
| 818 | What is thread affinity? | Restricting execution to specific CPU cores | Thread affinity controls processor assignment. |
| 819 | What is a synchronization context? | An abstraction for scheduling continuations | SynchronizationContext determines where asynchronous callbacks execute. |
| 820 | What synchronization context does UI applications use? | A UI thread context | UI frameworks require continuations to return to the UI thread. |
| 821 | What is ExecutionContext? | Ambient execution information flowing across async calls | ExecutionContext carries security and async-local data. |
| 822 | What is AsyncLocal<T>? | Stores data local to an asynchronous execution flow | AsyncLocal values flow with async operations. |
| 823 | What is ThreadLocal<T>? | Stores data specific to a thread | ThreadLocal values are isolated per physical thread. |
| 824 | What is ConcurrentDictionary<TKey,TValue>? | A thread-safe dictionary implementation | ConcurrentDictionary supports concurrent reads and writes. |
| 825 | What is ConcurrentQueue<T>? | A thread-safe FIFO queue | ConcurrentQueue allows multiple producers and consumers. |
| 826 | What is ConcurrentStack<T>? | A thread-safe LIFO collection | ConcurrentStack supports concurrent push and pop operations. |
| 827 | What is BlockingCollection<T>? | A thread-safe producer-consumer collection | BlockingCollection supports bounded capacity and blocking operations. |
| 828 | What is Channel<T> in .NET? | A high-performance asynchronous producer-consumer queue | Channels support async data pipelines between tasks. |
| 829 | What is an unbounded channel? | A channel without a fixed capacity limit | Unbounded channels continue accepting items until memory is exhausted. |
| 830 | What is a bounded channel? | A channel with a maximum capacity | Bounded channels provide backpressure when full. |
| 831 | What is backpressure? | Slowing producers when consumers cannot keep up | Backpressure prevents excessive memory growth. |
| 832 | What is a dataflow block? | A component in TPL Dataflow pipelines | Dataflow blocks process and pass messages asynchronously. |
| 833 | What namespace contains TPL Dataflow? | System.Threading.Tasks.Dataflow | The namespace provides blocks for parallel data processing. |
| 834 | What is an ActionBlock? | A dataflow block that executes actions | ActionBlock processes incoming messages asynchronously. |
| 835 | What is TransformBlock? | A dataflow block that transforms data | TransformBlock converts input values into output values. |
| 836 | What is BufferBlock? | A dataflow block that stores messages | BufferBlock acts as an asynchronous message buffer. |
| 837 | What is BroadcastBlock? | A block that sends each value to multiple targets | BroadcastBlock duplicates messages for multiple consumers. |
| 838 | What is JoinBlock? | A block combining multiple inputs | JoinBlock waits for matching values from multiple sources. |
| 839 | What is a pipeline architecture? | Processing data through connected stages | Pipelines divide work into independent processing steps. |
| 840 | What is producer-consumer architecture? | Separating creation and processing of work items | Producers generate data while consumers process it independently. |
| 841 | What is the actor model? | A concurrency model based on isolated actors | Actors communicate through asynchronous messages. |
| 842 | What is message passing? | Communication through exchanged messages | Message passing avoids direct shared memory access. |
| 843 | What is immutable data in concurrency? | Data that cannot change after creation | Immutable objects reduce synchronization requirements. |
| 844 | Why does immutability help concurrency? | Multiple threads can safely read shared data | Immutable objects eliminate many race conditions. |
| 845 | What is a deadlock? | A state where threads wait permanently for each other | Deadlocks occur when locks are acquired in conflicting orders. |
| 846 | What are the four deadlock conditions? | Mutual exclusion, hold and wait, no preemption, circular wait | All four conditions must exist for deadlock. |
| 847 | What is livelock? | Threads continuously react but make no progress | Livelock involves activity without useful completion. |
| 848 | What is starvation in concurrency? | A thread never receives required resources | Starvation prevents fair execution. |
| 849 | What is fairness in scheduling? | Providing reasonable resource access among threads | Fair scheduling reduces starvation. |
| 850 | What is async coordination? | Managing multiple asynchronous operations together | Async coordination combines tasks safely and efficiently. |
| 851 | What is Task.WhenAll used for? | Waiting for multiple tasks to complete together | Task.WhenAll creates a task that completes when all supplied tasks finish. |
| 852 | What is Task.WhenAny used for? | Waiting for the first task to complete | Task.WhenAny returns when any supplied task finishes. |
| 853 | What happens if one task fails in Task.WhenAll? | The returned task becomes faulted | Exceptions from completed tasks are aggregated. |
| 854 | What happens if a task is canceled in Task.WhenAll? | The combined task may become canceled | Cancellation is propagated when tasks do not complete successfully. |
| 855 | What is ValueTask pooling? | Reusing ValueTask-related resources in certain scenarios | Pooling can reduce allocations but requires careful implementation. |
| 856 | Why should ValueTask usually not be awaited multiple times? | It may wrap reusable state machines | Unlike Task, ValueTask has usage restrictions. |
| 857 | What is IValueTaskSource? | An interface for custom ValueTask implementations | It enables allocation-free asynchronous operations. |
| 858 | What is an async iterator? | A method producing asynchronous sequences | Async iterators return IAsyncEnumerable<T>. |
| 859 | What keyword creates an async iterator? | yield return with async | Async iterators combine asynchronous execution with streaming results. |
| 860 | What is await foreach used for? | Consuming asynchronous streams | It asynchronously retrieves elements from IAsyncEnumerable<T>. |
| 861 | What is cancellation support in async streams? | Allowing enumeration to stop early | Async streams can observe cancellation tokens during iteration. |
| 862 | What attribute enables async stream cancellation? | EnumeratorCancellationAttribute | It marks parameters used for async iterator cancellation. |
| 863 | What is ConfigureAwait in library code? | Controlling synchronization context capture | Libraries often use ConfigureAwait(false) to avoid context dependencies. |
| 864 | What is an async state machine? | Compiler-generated structure managing async execution | The compiler transforms async methods into state machines. |
| 865 | What does the async compiler transformation create? | A state machine and continuation logic | Async methods are rewritten into resumable operations. |
| 866 | What happens before the first await in an async method? | Code executes synchronously | Execution begins immediately until an incomplete await is reached. |
| 867 | What happens after an incomplete await? | Execution returns to the caller | The continuation resumes when the awaited operation completes. |
| 868 | Why are async void methods discouraged? | They cannot be awaited or easily observed | Exceptions from async void methods are difficult to handle. |
| 869 | Where is async void appropriate? | Event handlers | Event handlers require void return types. |
| 870 | What is an exception filter? | A conditional exception handler | Exception filters decide whether a catch block should handle an exception. |
| 871 | What keyword creates exception filters? | when | The when clause adds conditions to catch statements. |
| 872 | What is exception propagation? | Passing an exception up the call stack | Unhandled exceptions travel until caught or terminate execution. |
| 873 | What does throw preserve? | The original exception stack trace | A bare throw rethrows while maintaining stack information. |
| 874 | What does throw ex do? | Rethrows with a modified stack trace | Throwing the variable resets stack information from the current location. |
| 875 | What is an AggregateException? | A collection of multiple exceptions | AggregateException represents multiple failures from parallel operations. |
| 876 | What method flattens AggregateException? | Flatten() | Flatten removes nested AggregateException structures. |
| 877 | What is FirstChanceException? | An event raised when exceptions are initially thrown | It allows monitoring exceptions before handling occurs. |
| 878 | What is unhandled exception handling? | Processing exceptions that escape normal handling | Applications can log or respond before termination. |
| 879 | What is exception handling policy? | Rules for managing application failures | Policies define logging, recovery, and escalation behavior. |
| 880 | Why should exceptions not control normal program flow? | They are expensive and hide intent | Exceptions should represent exceptional situations. |
| 881 | What is ArgumentException? | Exception for invalid method arguments | It indicates supplied arguments are not valid. |
| 882 | What is ArgumentNullException? | Exception for unexpected null arguments | It identifies required arguments that are null. |
| 883 | What is ArgumentOutOfRangeException? | Exception for invalid argument ranges | It occurs when a value is outside an accepted range. |
| 884 | What is InvalidOperationException? | Exception for invalid object state operations | It indicates an operation is not valid in the current state. |
| 885 | What is ObjectDisposedException? | Exception for accessing disposed objects | It occurs when using resources after disposal. |
| 886 | What is NotSupportedException? | Exception for unsupported operations | It indicates a method or operation is not implemented or allowed. |
| 887 | What is TimeoutException? | Exception for operations exceeding time limits | It signals that an operation did not complete in time. |
| 888 | What is IOException? | Exception for I/O failures | It represents errors during file or stream operations. |
| 889 | What is UnauthorizedAccessException? | Exception for insufficient permissions | It occurs when access to a resource is denied. |
| 890 | What is StackOverflowException? | Exception caused by excessive stack usage | It commonly results from uncontrolled recursion. |
| 891 | Why cannot StackOverflowException usually be caught safely? | The runtime may not have enough stack space | Recovery is generally unreliable after stack exhaustion. |
| 892 | What is OutOfMemoryException? | Exception when memory allocation fails | It indicates the runtime cannot allocate required memory. |
| 893 | What is a custom exception? | A user-defined exception type | Custom exceptions represent domain-specific failures. |
| 894 | What should custom exceptions usually inherit from? | Exception | Custom exceptions should follow the standard exception hierarchy. |
| 895 | Why include constructors in custom exceptions? | To support standard exception creation patterns | Constructors allow messages, inner exceptions, and serialization support. |
| 896 | What is an inner exception? | The original exception causing another exception | Inner exceptions preserve underlying failure details. |
| 897 | What is exception wrapping? | Creating a new exception containing another | Wrapping adds context while preserving the original cause. |
| 898 | What is fail-fast behavior? | Immediately stopping on unrecoverable errors | Fail-fast prevents continuing in an invalid state. |
| 899 | What is defensive programming? | Writing code that anticipates invalid conditions | Defensive programming improves reliability and safety. |
| 900 | What is guard clause programming? | Validating conditions early and returning quickly | Guard clauses simplify control flow and reduce nesting. |
| 901 | What is the purpose of ArgumentNullException.ThrowIfNull()? | Quickly validates that a value is not null | It provides a concise and optimized null argument check. |
| 902 | What is a guard clause? | An early validation check that prevents invalid execution | Guard clauses simplify methods by handling invalid states immediately. |
| 903 | What is defensive copying? | Creating copies to prevent external mutation | Defensive copying protects internal state from unwanted changes. |
| 904 | What is encapsulation? | Hiding internal implementation details | Encapsulation exposes only controlled access to an object's state. |
| 905 | What is information hiding? | Restricting access to implementation details | Information hiding reduces coupling between components. |
| 906 | What is a private setter? | A property setter accessible only within the declaring type | Private setters protect object state from external modification. |
| 907 | What is a protected member? | A member accessible by derived classes | Protected members support inheritance-based access. |
| 908 | What is an internal member? | A member accessible within the same assembly | Internal visibility limits access to the current compiled unit. |
| 909 | What is InternalsVisibleToAttribute? | Allows another assembly to access internal members | It is commonly used for testing internal implementation. |
| 910 | What is a friend assembly? | An assembly granted access to another assembly's internals | Friend assemblies use InternalsVisibleToAttribute. |
| 911 | What is an abstract class? | A class that can define incomplete behavior | Abstract classes cannot be instantiated directly. |
| 912 | What is an abstract method? | A method declaration without implementation | Derived classes must provide implementations for abstract methods. |
| 913 | Can an abstract class contain implemented methods? | Yes | Abstract classes can mix abstract members with normal implementations. |
| 914 | What is an interface default implementation? | An implementation provided directly in an interface | Modern C# allows interfaces to contain method implementations. |
| 915 | Why were default interface methods introduced? | To evolve interfaces without breaking implementations | Existing implementations can continue working when interfaces gain members. |
| 916 | What is explicit interface implementation? | Implementing an interface member with a qualified name | It hides the member unless accessed through the interface type. |
| 917 | Why use explicit interface implementation? | To resolve naming conflicts or hide members | It allows different interfaces to define members with the same name. |
| 918 | What is multiple interface inheritance? | A type implementing multiple interfaces | C# supports multiple interface implementations. |
| 919 | Why does C# not support multiple class inheritance? | To avoid ambiguity and complexity | Multiple class inheritance can create conflicting behavior. |
| 920 | What is the diamond problem? | Ambiguity caused by multiple inheritance paths | C# avoids this problem by restricting class inheritance. |
| 921 | What is object slicing? | Losing derived-type information when copied as a base type | This issue is common in value-type inheritance systems. |
| 922 | What is a virtual property? | A property that can be overridden | Virtual properties participate in runtime polymorphism. |
| 923 | What is an override property? | A replacement implementation of an inherited virtual property | Override changes inherited behavior. |
| 924 | What is the difference between new and override keywords? | new hides a member, override replaces virtual behavior | Override participates in polymorphism while new does not. |
| 925 | What is member hiding? | Creating a member with the same name as an inherited member | The new keyword explicitly indicates hiding. |
| 926 | What is a sealed override? | An override that prevents further overriding | Sealed overrides stop additional derived customization. |
| 927 | What is constructor chaining? | Calling one constructor from another | Constructor chaining reduces duplicated initialization logic. |
| 928 | What keyword calls another constructor in the same class? | this | The this constructor initializer calls another constructor in the same type. |
| 929 | What keyword calls a base constructor? | base | The base initializer invokes a parent class constructor. |
| 930 | What is object initialization syntax? | Creating objects while assigning properties | Object initializers simplify construction code. |
| 931 | What is collection initialization syntax? | Creating and populating collections in one expression | Collection initializers use Add methods internally. |
| 932 | What are collection expressions in C#? | A modern syntax for creating collections | Collection expressions provide simplified collection creation. |
| 933 | What is the spread operator in collection expressions? | Expands another collection into a collection expression | It inserts elements from another enumerable source. |
| 934 | What is an index from end operator? | Accessing elements relative to the end | The ^ operator counts positions backward from the end. |
| 935 | What is a range operator? | Selecting a subsection of a sequence | The .. operator creates slices. |
| 936 | What type represents ranges in C#? | Range | Range describes start and end positions for slicing. |
| 937 | What type represents indexes in C#? | Index | Index represents a position that can count from either end. |
| 938 | What is slicing? | Creating a view or subset of data | Slicing avoids unnecessary copying in many scenarios. |
| 939 | Why is Span<T> useful with slicing? | It provides allocation-free views | Span slices reference existing memory without copying. |
| 940 | What is ReadOnlySpan<T>? | A read-only view over contiguous memory | ReadOnlySpan prevents modification while avoiding allocation. |
| 941 | What is Memory<T>? | A heap-friendly memory representation | Memory<T> can be stored and used across asynchronous operations. |
| 942 | Why can Span<T> not be used across await? | It is stack-only | Span references stack memory that may become invalid after suspension. |
| 943 | Why can Memory<T> cross await boundaries? | It is heap-based | Memory<T> is designed for asynchronous scenarios. |
| 944 | What is ArraySegment<T>? | A view over part of an array | ArraySegment references an array range without copying. |
| 945 | What is the difference between ArraySegment<T> and Span<T>? | Span provides safer modern memory access | Span offers better performance and broader memory support. |
| 946 | What is MemoryMarshal? | Provides advanced memory conversion utilities | MemoryMarshal enables low-level memory operations. |
| 947 | What is CollectionsMarshal? | Provides optimized access to collection internals | CollectionsMarshal enables high-performance scenarios with caution. |
| 948 | What is ref return? | Returning a reference to a variable | Ref returns avoid copying large values. |
| 949 | What is ref local? | A local variable holding a reference | Ref locals allow direct manipulation of referenced storage. |
| 950 | What is ref readonly? | A read-only reference | Ref readonly avoids copying while preventing modification. |
| 951 | What is the purpose of `in` parameters with large structs? | Avoid copying while preventing modification | `in` passes structs by readonly reference to improve performance. |
| 952 | What is a readonly reference return? | Returning a reference that cannot be modified | It provides efficient access without allowing changes. |
| 953 | What is a ref struct restriction? | It cannot be stored on the heap or used across async boundaries | ref structs must remain stack-bound for memory safety. |
| 954 | Why can ref structs not implement interfaces? | They cannot participate in boxing | Interface usage would require heap-compatible behavior. |
| 955 | Why can ref structs not be fields of normal classes? | The reference could outlive stack memory | The CLR prevents unsafe lifetime scenarios. |
| 956 | What is a stack-only type? | A type restricted to stack allocation | Stack-only types provide high-performance memory access safely. |
| 957 | What is Unsafe.SkipInit<T>() used for? | Avoiding unnecessary initialization | It can improve performance when values are immediately assigned. |
| 958 | What is default initialization of value types? | Setting all fields to zero values | Value types receive default values automatically. |
| 959 | What is a blittable type? | A type whose memory layout can be copied directly | Blittable types simplify native interoperability. |
| 960 | What is StructLayoutAttribute used for? | Controlling memory layout of structs | It defines how fields are arranged in memory. |
| 961 | What is explicit struct layout? | Manually defining field offsets | Explicit layout is used for interop and low-level scenarios. |
| 962 | What is sequential struct layout? | Fields stored in declared order | Sequential layout provides predictable memory arrangement. |
| 963 | What is Auto layout? | Runtime-controlled field arrangement | Auto layout allows the CLR to optimize memory layout. |
| 964 | What is a field offset? | The position of a field within memory | Field offsets determine struct memory representation. |
| 965 | What is fixed-size buffer in C#? | An inline array inside an unsafe struct | Fixed buffers support native-compatible data layouts. |
| 966 | What is SIMD in .NET? | Parallel processing of multiple values in CPU instructions | SIMD improves performance for numeric computations. |
| 967 | What namespace provides SIMD vector types? | System.Numerics | System.Numerics contains Vector<T> and related APIs. |
| 968 | What is Vector<T>? | A SIMD-enabled generic vector type | Vector<T> performs operations on multiple values simultaneously. |
| 969 | What determines SIMD vector size? | Hardware capabilities | The CPU determines how many values fit into a vector. |
| 970 | What is hardware acceleration? | Using specialized CPU features for performance | Hardware acceleration improves execution of suitable workloads. |
| 971 | What is intrinsic API support in .NET? | Direct access to CPU instructions | Intrinsics allow optimized hardware-specific operations. |
| 972 | What namespace contains hardware intrinsics? | System.Runtime.Intrinsics | It exposes CPU-specific vector instructions. |
| 973 | What is the JIT optimizer? | A component that improves generated machine code | The JIT applies runtime optimizations during compilation. |
| 974 | What is method inlining? | Replacing a method call with its body | Inlining removes call overhead for small methods. |
| 975 | What factors affect JIT inlining? | Method size, complexity, and runtime heuristics | The JIT decides whether inlining is beneficial. |
| 976 | What is tiered compilation? | Compiling methods at different optimization levels | Tiered compilation improves startup while allowing later optimization. |
| 977 | What is Tier 0 compilation? | Quick initial compilation | Tier 0 prioritizes startup speed over optimization. |
| 978 | What is Tier 1 compilation? | Optimized recompilation | Tier 1 improves performance after methods become frequently used. |
| 979 | What is profile-guided optimization (PGO)? | Optimization based on runtime behavior data | PGO allows the runtime to optimize common execution paths. |
| 980 | What is dynamic PGO? | Runtime collection of profiling information for optimization | Dynamic PGO adapts optimizations while the application runs. |
| 981 | What is ReadyToRun compilation? | Precompiling assemblies before execution | ReadyToRun reduces startup JIT requirements. |
| 982 | What is Crossgen2? | The tool used for ReadyToRun compilation | Crossgen2 generates native code ahead of execution. |
| 983 | What is ahead-of-time compilation? | Generating native code before runtime | AOT reduces runtime compilation overhead. |
| 984 | What is startup performance optimization? | Reducing time before an application becomes usable | Techniques include trimming, AOT, and ReadyToRun. |
| 985 | What is cold startup? | Performance when an application runs for the first time | Cold startup includes loading and initialization costs. |
| 986 | What is warm startup? | Performance after resources are already loaded | Warm startup benefits from caches and previous initialization. |
| 987 | What is lazy initialization? | Creating resources only when first needed | Lazy initialization reduces unnecessary startup work. |
| 988 | What type supports lazy initialization in .NET? | Lazy<T> | Lazy<T> provides thread-safe deferred creation. |
| 989 | What execution modes does Lazy<T> support? | Different thread-safety strategies | Lazy<T> can optimize for single-threaded or concurrent scenarios. |
| 990 | What is the LazyThreadSafetyMode? | Controls Lazy<T> synchronization behavior | It defines how multiple threads initialize values. |
| 991 | What is double-checked locking? | A pattern minimizing lock overhead during initialization | It requires careful memory ordering to be correct. |
| 992 | Why can double-checked locking fail without memory barriers? | Threads may observe partially initialized state | Memory reordering can break assumptions. |
| 993 | What is static initialization in C#? | Initialization performed when a type is first accessed | Static initialization is managed by the CLR. |
| 994 | What is a static constructor? | A constructor for static members | Static constructors run once per type. |
| 995 | When does a static constructor execute? | Before first use of the type | The CLR guarantees initialization before access. |
| 996 | What is beforefieldinit? | A CLR optimization for static initialization timing | It allows earlier execution of static initialization. |
| 997 | What is deterministic initialization? | Initialization at a predictable time | It provides stronger control over startup behavior. |
| 998 | What is module initializer? | Code executed when an assembly loads | Module initializers run before normal application code. |
| 999 | What attribute defines a module initializer? | ModuleInitializerAttribute | It marks methods that run during module loading. |
| 1000 | What is the benefit of module initializers? | Running setup code without explicit calls | They automate assembly-level initialization tasks. |
| 1001 | What is dependency injection lifetime scope? | The duration an injected service instance exists | Lifetimes control how long DI-created objects are reused. |
| 1002 | What are the three built-in .NET DI lifetimes? | Transient, Scoped, Singleton | These define service creation and reuse behavior. |
| 1003 | What is a transient service? | A service created every time it is requested | Transient services are suitable for lightweight stateless operations. |
| 1004 | What is a scoped service? | A service created once per scope | Scoped services are commonly used per web request. |
| 1005 | What is a singleton service? | A service created once for the application's lifetime | Singleton services share one instance across all consumers. |
| 1006 | What is a captive dependency? | A longer-lived service holding a shorter-lived dependency | Captive dependencies can cause incorrect lifetime behavior. |
| 1007 | Why should scoped services not usually be injected into singletons? | The scoped object may outlive its intended lifetime | This can create stale state and disposal issues. |
| 1008 | What is IServiceCollection? | A collection used to register services | It stores dependency injection registrations. |
| 1009 | What is IServiceProvider? | A service resolution container | It creates registered service instances. |
| 1010 | What is service resolution? | Retrieving an instance from the DI container | Resolution creates or returns registered services. |
| 1011 | What is constructor injection? | Providing dependencies through a constructor | It is the preferred DI pattern in .NET. |
| 1012 | What is property injection? | Providing dependencies through properties | It is less commonly used because dependencies may be missing. |
| 1013 | What is method injection? | Passing dependencies directly into methods | It is useful for occasional dependencies. |
| 1014 | What is the service locator pattern? | Retrieving dependencies manually from a container | It hides dependencies and is generally discouraged. |
| 1015 | What is the Options pattern in .NET? | A way to access strongly typed configuration | Options map configuration values to classes. |
| 1016 | What interface provides options access? | IOptions<T> | IOptions provides configured option values through DI. |
| 1017 | What is IOptionsSnapshot<T>? | Scoped options access with refreshed values | It reloads options per scope. |
| 1018 | What is IOptionsMonitor<T>? | Options access supporting change notifications | It observes configuration changes dynamically. |
| 1019 | What is Options validation? | Checking configuration values before use | Validation prevents invalid application settings. |
| 1020 | What attribute supports options validation? | ValidateDataAnnotationsAttribute | It validates options using data annotations. |
| 1021 | What is configuration provider? | A source supplying configuration values | Providers load settings from files, environment variables, and other sources. |
| 1022 | What is IConfiguration? | An abstraction for accessing configuration data | It provides key-value configuration access. |
| 1023 | What is appsettings.json? | A common JSON configuration file | It stores application settings. |
| 1024 | What is environment-specific configuration? | Configuration varying by deployment environment | Examples include development and production settings. |
| 1025 | What is environment variable configuration? | Reading settings from operating system variables | Environment variables are commonly used for deployment secrets. |
| 1026 | What is user secrets in .NET? | A development-time secret storage mechanism | User secrets avoid storing sensitive values in source code. |
| 1027 | Why should secrets not be committed to source control? | They can expose credentials and sensitive access | Secret leakage can compromise systems. |
| 1028 | What is configuration binding? | Mapping configuration sections to objects | Binding creates strongly typed settings classes. |
| 1029 | What is a configuration section? | A logical grouping of configuration keys | Sections organize related settings. |
| 1030 | What is logging abstraction in .NET? | A common API for application logging | Logging abstractions allow interchangeable providers. |
| 1031 | What interface represents logging? | ILogger<T> | ILogger provides structured logging capabilities. |
| 1032 | What is structured logging? | Logging data as named fields instead of plain text | Structured logs improve searching and analysis. |
| 1033 | What is ILoggerFactory? | Creates logger instances | Logger factories manage logging providers. |
| 1034 | What is a logging provider? | A component that writes log messages | Providers send logs to files, consoles, or external systems. |
| 1035 | What are logging levels in .NET? | Trace, Debug, Information, Warning, Error, Critical | Levels categorize message importance. |
| 1036 | What is log filtering? | Controlling which logs are recorded | Filtering reduces unnecessary logging overhead. |
| 1037 | What is EventSource? | A high-performance tracing API | EventSource provides structured runtime events. |
| 1038 | What is EventPipe? | A cross-platform diagnostics pipeline | EventPipe collects runtime events without platform-specific tools. |
| 1039 | What is dotnet-trace? | A command-line diagnostics tool | It collects performance traces from .NET applications. |
| 1040 | What is dotnet-counters? | A monitoring tool for runtime metrics | It displays real-time performance counters. |
| 1041 | What is dotnet-dump? | A tool for analyzing process dumps | It helps investigate runtime issues. |
| 1042 | What is dotnet-gcdump? | A tool for collecting GC heap information | It analyzes managed memory usage. |
| 1043 | What is diagnostic source? | An API for emitting application diagnostics | DiagnosticSource supports tracing and instrumentation. |
| 1044 | What is Activity in .NET diagnostics? | Represents an operation span for tracing | Activities are used for distributed tracing. |
| 1045 | What is ActivitySource? | Creates diagnostic activities | It integrates with observability systems. |
| 1046 | What is OpenTelemetry? | A standard framework for telemetry collection | OpenTelemetry collects traces, metrics, and logs. |
| 1047 | What is distributed tracing? | Tracking requests across multiple services | It helps diagnose microservice performance issues. |
| 1048 | What is a trace identifier? | A value connecting related operations | Trace IDs correlate events across systems. |
| 1049 | What is a span in tracing? | A single operation within a trace | Spans represent individual service actions. |
| 1050 | What is observability? | Understanding system behavior through telemetry | Observability combines logs, metrics, and traces. |
| 1051 | What is middleware ordering in ASP.NET Core? | The sequence in which middleware components execute | Middleware order determines request processing and response behavior. |
| 1052 | Why does middleware order matter? | Each component can affect later components | Incorrect ordering can break authentication, routing, or error handling. |
| 1053 | What is terminal middleware? | Middleware that does not call the next component | Terminal middleware ends the request pipeline. |
| 1054 | What is Use versus Run in ASP.NET Core? | Use continues the pipeline, Run terminates it | Run creates terminal middleware. |
| 1055 | What is Map in ASP.NET Core middleware? | Branches the pipeline based on request paths | Map creates separate middleware pipelines. |
| 1056 | What is MapWhen? | Branches middleware based on a predicate | MapWhen allows custom branching conditions. |
| 1057 | What is request delegate? | A function processing an HTTP request | Middleware is built around request delegates. |
| 1058 | What is HttpContext? | An object representing the current HTTP request and response | HttpContext provides access to request, response, user, and services. |
| 1059 | What is HttpRequest? | Represents incoming HTTP request data | HttpRequest contains headers, query values, body, and route data. |
| 1060 | What is HttpResponse? | Represents outgoing HTTP response data | HttpResponse controls status codes, headers, and body content. |
| 1061 | What is HttpContext.Items? | A per-request key-value storage collection | Items allows middleware and components to share request data. |
| 1062 | What is HttpContext.User? | Represents the authenticated user | It contains identity and claims information. |
| 1063 | What is ClaimsPrincipal? | A representation of user identities and claims | ClaimsPrincipal supports authorization decisions. |
| 1064 | What is ClaimsIdentity? | Represents a single identity containing claims | A user can contain multiple identities. |
| 1065 | What is a claim? | A piece of information about an identity | Claims store user attributes such as roles or permissions. |
| 1066 | What is authentication? | Verifying who a user is | Authentication establishes identity. |
| 1067 | What is authorization? | Determining what an authenticated user can access | Authorization checks permissions. |
| 1068 | What is authentication scheme? | A configured method for authenticating users | Schemes define how credentials are processed. |
| 1069 | What is cookie authentication? | Authentication using encrypted browser cookies | Cookies store authentication tickets. |
| 1070 | What is JWT authentication? | Authentication using JSON Web Tokens | JWTs carry signed identity information. |
| 1071 | What is a JWT claim? | Data stored inside a token payload | Claims describe identity or permissions. |
| 1072 | What is JWT signature validation? | Checking token authenticity | Validation ensures the token was issued by a trusted source. |
| 1073 | What is token expiration? | The time after which a token is invalid | Expiration limits token lifetime. |
| 1074 | What is refresh token? | A credential used to obtain new access tokens | Refresh tokens allow continued authentication without re-login. |
| 1075 | What is OpenID Connect? | An identity layer built on OAuth 2.0 | It provides authentication using identity providers. |
| 1076 | What is OAuth 2.0? | An authorization framework | OAuth allows delegated access to resources. |
| 1077 | What is an access token? | A credential granting access to protected resources | APIs validate access tokens before allowing operations. |
| 1078 | What is a bearer token? | A token sent as proof of access | Whoever possesses it can use it unless protected. |
| 1079 | What is policy-based authorization? | Authorization using named requirements | Policies combine requirements and handlers. |
| 1080 | What is role-based authorization? | Authorization based on assigned roles | Roles group users into permission categories. |
| 1081 | What is a policy requirement? | A rule that must be satisfied | Requirements define authorization conditions. |
| 1082 | What is an authorization handler? | Code that evaluates requirements | Handlers determine whether requirements succeed. |
| 1083 | What is IAuthorizationService? | Service for performing authorization checks | It evaluates policies programmatically. |
| 1084 | What is resource-based authorization? | Authorization depending on a specific object | Decisions can consider both user and resource data. |
| 1085 | What is CORS? | Cross-Origin Resource Sharing | CORS controls browser access across origins. |
| 1086 | Why is CORS enforced by browsers? | To prevent unauthorized cross-origin requests | Browsers apply same-origin security rules. |
| 1087 | What is a CORS policy? | Rules defining allowed origins and methods | Policies configure cross-origin access. |
| 1088 | What is preflight request? | An OPTIONS request checking permissions | Browsers send it before certain cross-origin requests. |
| 1089 | What is CSRF? | Cross-Site Request Forgery | CSRF tricks authenticated users into sending unwanted requests. |
| 1090 | How is CSRF prevented? | Anti-forgery tokens | Tokens verify requests originated from the legitimate application. |
| 1091 | What is antiforgery middleware? | Middleware that validates CSRF protection tokens | It protects state-changing requests. |
| 1092 | What is HTTPS redirection middleware? | Middleware redirecting HTTP requests to HTTPS | It enforces encrypted connections. |
| 1093 | What is HSTS? | HTTP Strict Transport Security | HSTS instructs browsers to use HTTPS only. |
| 1094 | What is response compression? | Reducing response size before transmission | Compression improves network efficiency. |
| 1095 | What compression algorithms are commonly supported? | Brotli and Gzip | They reduce HTTP response payload sizes. |
| 1096 | What is output caching? | Storing generated responses for reuse | Output caching improves performance for repeated requests. |
| 1097 | What is response caching? | Client and proxy-based response caching | It uses HTTP caching semantics. |
| 1098 | What is distributed caching? | Shared cache accessible across application instances | It supports scalable applications. |
| 1099 | What interface represents distributed cache? | IDistributedCache | It provides a common caching abstraction. |
| 1100 | What is cache invalidation? | Removing or updating stale cached data | Correct invalidation keeps cached results accurate. |
| 1101 | What is the purpose of a health check in ASP.NET Core? | Monitoring application availability and dependencies | Health checks report whether an application is functioning correctly. |
| 1102 | What interface defines a custom health check? | IHealthCheck | Custom health checks implement application-specific monitoring logic. |
| 1103 | What is a liveness check? | Determines if an application is running | Liveness checks detect failed application instances. |
| 1104 | What is a readiness check? | Determines if an application can accept traffic | Readiness checks verify dependencies required for serving requests. |
| 1105 | What is a health check publisher? | A component that executes health checks periodically | Publishers can send health results to monitoring systems. |
| 1106 | What is Kestrel? | The cross-platform ASP.NET Core web server | Kestrel handles HTTP request processing for ASP.NET Core applications. |
| 1107 | What is a reverse proxy? | A server forwarding requests to another server | Reverse proxies provide routing, security, and load balancing. |
| 1108 | Why use a reverse proxy with Kestrel? | To add security and infrastructure features | Proxies can handle TLS termination and traffic management. |
| 1109 | What is HTTP/2 support in ASP.NET Core? | Support for the HTTP/2 protocol | HTTP/2 improves performance through multiplexing and compression. |
| 1110 | What is HTTP/3 support based on? | QUIC protocol | HTTP/3 uses QUIC over UDP. |
| 1111 | What is WebSocket? | A protocol for persistent two-way communication | WebSockets allow real-time client-server communication. |
| 1112 | What is SignalR? | A framework for real-time communication | SignalR abstracts persistent connections and messaging. |
| 1113 | What transport does SignalR prefer? | WebSockets when available | SignalR falls back to other transports when necessary. |
| 1114 | What is a SignalR hub? | A high-level communication endpoint | Hubs allow clients and servers to call methods. |
| 1115 | What is a SignalR client method? | A server or client callable function | Clients can receive messages through registered methods. |
| 1116 | What is a SignalR group? | A collection of connected clients | Groups allow targeted message broadcasting. |
| 1117 | What is gRPC? | A high-performance RPC framework | gRPC uses HTTP/2 and Protocol Buffers for communication. |
| 1118 | What serialization format does gRPC commonly use? | Protocol Buffers | Protobuf provides compact binary serialization. |
| 1119 | What is a gRPC service contract? | A definition of available RPC methods | Contracts describe communication between clients and servers. |
| 1120 | What is a .proto file? | A Protocol Buffer definition file | It defines messages and services for gRPC. |
| 1121 | What is unary gRPC call? | A single request and single response call | Unary calls work similarly to traditional API requests. |
| 1122 | What is server streaming in gRPC? | Server sending multiple responses | The client receives a stream of messages. |
| 1123 | What is client streaming in gRPC? | Client sending multiple requests | The server receives a stream of messages. |
| 1124 | What is bidirectional streaming in gRPC? | Both sides stream messages independently | It enables continuous two-way communication. |
| 1125 | What is protobuf serialization? | Encoding structured data into binary format | Protobuf is efficient for network communication. |
| 1126 | What is minimal hosting model in .NET? | Simplified application startup configuration | It combines host and application configuration. |
| 1127 | What is WebApplicationBuilder? | The builder used for modern ASP.NET Core apps | It configures services, logging, and application settings. |
| 1128 | What is WebApplication? | The built ASP.NET Core application pipeline | It represents the configured running app. |
| 1129 | What is Generic Host? | A hosting model for .NET applications | It manages services, configuration, logging, and lifetime. |
| 1130 | What is IHost? | The abstraction representing a running host | It controls application lifetime and hosted services. |
| 1131 | What is BackgroundService? | A base class for long-running hosted tasks | It simplifies implementing background workers. |
| 1132 | What interface creates hosted services? | IHostedService | Hosted services run background tasks with the application. |
| 1133 | What methods does IHostedService define? | StartAsync and StopAsync | They control service startup and shutdown. |
| 1134 | What is ExecuteAsync in BackgroundService? | The main asynchronous worker loop | It runs the background operation. |
| 1135 | What is graceful shutdown? | Stopping an application while allowing cleanup | It prevents abrupt termination of operations. |
| 1136 | What is application lifetime management? | Controlling startup and shutdown behavior | It handles application lifecycle events. |
| 1137 | What interface provides application lifetime events? | IHostApplicationLifetime | It exposes started, stopping, and stopped events. |
| 1138 | What is startup task execution? | Running initialization logic during application startup | It prepares required resources before serving traffic. |
| 1139 | What is dependency injection scope creation? | Creating a service lifetime boundary manually | Scopes allow resolving scoped services outside requests. |
| 1140 | What method creates a DI scope? | CreateScope() | It creates a new IServiceScope instance. |
| 1141 | Why create scopes in background services? | To safely use scoped dependencies | Background services do not automatically have request scopes. |
| 1142 | What is Entity Framework Core? | An object-relational mapper for .NET | EF Core maps .NET objects to database records. |
| 1143 | What is DbContext? | The main EF Core database session class | DbContext manages queries and changes. |
| 1144 | What is DbSet<T>? | A collection representing an entity set | DbSet provides querying and persistence operations. |
| 1145 | What is change tracking in EF Core? | Tracking entity modifications | It allows EF Core to generate update commands. |
| 1146 | What is AsNoTracking()? | Disables entity tracking for queries | It improves performance for read-only operations. |
| 1147 | What is migration in EF Core? | A way to update database schemas | Migrations synchronize database structure with models. |
| 1148 | What is model-first development? | Designing models before database structure | EF generates database changes from models. |
| 1149 | What is database-first development? | Generating models from an existing database | Existing schemas are reverse engineered into classes. |
| 1150 | What is code-first development? | Defining database structure using C# classes | EF Core creates schema from application models. |
| 1151 | What is EF Core query translation? | Converting LINQ expressions into database queries | EF Core translates supported expressions into SQL. |
| 1152 | What is IQueryable<T>? | A query representation executed by a provider | IQueryable allows remote query translation. |
| 1153 | What is IEnumerable<T>? | An in-memory sequence abstraction | IEnumerable operations execute locally after data retrieval. |
| 1154 | What is deferred execution in EF Core? | Delaying query execution until results are requested | LINQ queries are not executed until enumerated. |
| 1155 | What method executes an EF Core query immediately? | ToListAsync() | It sends the query to the database and materializes results. |
| 1156 | What is FirstOrDefaultAsync()? | Retrieves the first matching entity or default value | It executes an asynchronous single-result query. |
| 1157 | What is SingleAsync()? | Retrieves exactly one matching result | It throws if zero or multiple results exist. |
| 1158 | What is Include() in EF Core? | Loads related entities | Include enables eager loading of navigation properties. |
| 1159 | What is ThenInclude()? | Loads nested related entities | ThenInclude continues eager loading relationships. |
| 1160 | What is eager loading? | Loading related data with the initial query | It retrieves related entities immediately. |
| 1161 | What is lazy loading? | Loading related data when accessed | Lazy loading delays database queries until needed. |
| 1162 | What is explicit loading? | Manually loading related entities | It gives precise control over when relationships load. |
| 1163 | What is the N+1 query problem? | Excessive queries caused by repeated loading | It often occurs with careless lazy loading. |
| 1164 | What is split query behavior in EF Core? | Executing multiple queries for related data | Split queries can avoid large join results. |
| 1165 | What is single query behavior in EF Core? | Loading related data through one SQL query | It can reduce round trips but create large joins. |
| 1166 | What is optimistic concurrency? | Assuming conflicts are rare and checking during updates | EF Core detects conflicting changes before saving. |
| 1167 | What is a concurrency token? | A value used to detect conflicting updates | EF compares tokens during database updates. |
| 1168 | What is rowversion in SQL Server? | A database-generated concurrency value | It detects whether a row changed. |
| 1169 | What is DbUpdateConcurrencyException? | Exception thrown when concurrency conflicts occur | It indicates another process modified the data. |
| 1170 | What is SaveChangesAsync()? | Asynchronously persists tracked changes | It sends insert, update, and delete commands. |
| 1171 | What is the EF Core change tracker? | A component tracking entity state | It determines database operations during saving. |
| 1172 | What are EF Core entity states? | Added, Modified, Deleted, Unchanged, Detached | States determine how entities are persisted. |
| 1173 | What is a detached entity? | An entity not tracked by a DbContext | Changes are ignored until attached. |
| 1174 | What is Attach()? | Begins tracking an existing entity | Attach marks an entity as unchanged by default. |
| 1175 | What is Update()? | Marks an entity as modified | Update causes EF Core to send update commands. |
| 1176 | What is Remove()? | Marks an entity for deletion | Remove schedules a database delete. |
| 1177 | What is value conversion in EF Core? | Transforming values between model and database types | Conversions map incompatible representations. |
| 1178 | What is a shadow property? | A property tracked by EF but not defined in the class | Shadow properties exist only in the model. |
| 1179 | What is an owned entity type? | A type whose lifecycle belongs to another entity | Owned entities cannot exist independently. |
| 1180 | What is table splitting? | Mapping multiple entities to one database table | It allows shared table storage. |
| 1181 | What is inheritance mapping in EF Core? | Mapping class hierarchies to database structures | EF supports multiple inheritance storage strategies. |
| 1182 | What is TPH inheritance? | Table-per-hierarchy mapping | All derived types share one table with a discriminator. |
| 1183 | What is TPT inheritance? | Table-per-type mapping | Each type has its own database table. |
| 1184 | What is TPC inheritance? | Table-per-concrete-type mapping | Each concrete class has its own table. |
| 1185 | What is a database provider in EF Core? | A component translating EF operations for a database | Providers support different database engines. |
| 1186 | What is relational EF Core provider? | Provider for SQL-based databases | It maps EF operations to relational SQL. |
| 1187 | What is LINQ expression tree? | A representation of code as data | Providers analyze expression trees for translation. |
| 1188 | What is IQueryable provider? | A component executing query expressions | Providers translate and execute queries. |
| 1189 | What is raw SQL querying in EF Core? | Executing custom SQL commands through EF | It allows database-specific queries. |
| 1190 | What is FromSql()? | Executes SQL returning entity results | FromSql integrates raw SQL with EF queries. |
| 1191 | What is ExecuteSqlRaw()? | Executes SQL commands without returning entities | It is used for commands such as updates. |
| 1192 | What is parameterized SQL? | SQL using parameters instead of string concatenation | It helps prevent SQL injection. |
| 1193 | What is SQL injection? | An attack inserting malicious SQL into queries | Parameterization prevents unauthorized query manipulation. |
| 1194 | What is a database transaction? | A group of operations executed atomically | Transactions ensure consistency. |
| 1195 | What are ACID properties? | Atomicity, Consistency, Isolation, Durability | They define reliable transaction behavior. |
| 1196 | What is transaction isolation level? | Controls visibility of concurrent changes | Isolation affects consistency and performance. |
| 1197 | What is DbTransaction? | Represents a database transaction | It controls commit and rollback operations. |
| 1198 | What is Savepoint? | A checkpoint inside a transaction | Savepoints allow partial rollback. |
| 1199 | What is connection pooling? | Reusing database connections | Pooling reduces connection creation overhead. |
| 1200 | What is DbContext pooling? | Reusing DbContext instances | It reduces allocation overhead for high-throughput applications. |
| 1201 | What is the purpose of middleware exception handling? | Centralizing error processing | Exception middleware provides consistent error responses and logging. |
| 1202 | What is UseExceptionHandler()? | Middleware for handling unhandled exceptions | It provides a centralized exception handling pipeline. |
| 1203 | What is ProblemDetails in ASP.NET Core? | A standard format for HTTP API errors | ProblemDetails provides consistent machine-readable error responses. |
| 1204 | What is RFC 7807? | A specification for HTTP problem details | It defines a standard error response format. |
| 1205 | What is IProblemDetailsService? | A service for generating problem detail responses | It centralizes API error formatting. |
| 1206 | What is developer exception page? | A detailed error page for development environments | It displays stack traces and debugging information. |
| 1207 | Why should detailed exceptions not be shown in production? | They may expose sensitive information | Production errors should avoid leaking internal details. |
| 1208 | What is status code pages middleware? | Middleware generating responses for empty error status codes | It improves error responses for certain HTTP failures. |
| 1209 | What is HTTP status code 400? | Bad Request | It indicates invalid client input. |
| 1210 | What is HTTP status code 401? | Unauthorized | It indicates missing or invalid authentication. |
| 1211 | What is HTTP status code 403? | Forbidden | It indicates authenticated but unauthorized access. |
| 1212 | What is HTTP status code 404? | Not Found | It indicates the requested resource does not exist. |
| 1213 | What is HTTP status code 409? | Conflict | It indicates a request conflict with current state. |
| 1214 | What is HTTP status code 422? | Unprocessable Entity | It indicates valid syntax but invalid semantic data. |
| 1215 | What is HTTP status code 429? | Too Many Requests | It indicates rate limiting has been triggered. |
| 1216 | What is HTTP status code 500? | Internal Server Error | It indicates an unexpected server failure. |
| 1217 | What is HTTP status code 503? | Service Unavailable | It indicates the server cannot currently handle requests. |
| 1218 | What is REST? | An architectural style for web APIs | REST uses resources and HTTP operations. |
| 1219 | What is a REST resource? | An entity exposed through an API | Resources are identified by URLs. |
| 1220 | What does HTTP GET represent? | Retrieving a resource | GET should not modify server state. |
| 1221 | What does HTTP POST represent? | Creating or processing data | POST commonly creates new resources. |
| 1222 | What does HTTP PUT represent? | Replacing a resource | PUT generally performs full updates. |
| 1223 | What does HTTP PATCH represent? | Partial resource modification | PATCH updates selected fields. |
| 1224 | What does HTTP DELETE represent? | Removing a resource | DELETE requests resource removal. |
| 1225 | What is idempotency? | Producing the same result when repeated | Some HTTP methods are designed to be idempotent. |
| 1226 | Which HTTP methods are typically idempotent? | GET, PUT, DELETE | Repeating these operations should have predictable results. |
| 1227 | What is API versioning? | Managing changes between API contracts | Versioning allows clients to migrate gradually. |
| 1228 | What are common API versioning strategies? | URL, header, and query string versioning | Different approaches expose versions differently. |
| 1229 | What is content negotiation versioning? | Selecting API versions through request headers | It keeps URLs cleaner. |
| 1230 | What is OpenAPI? | A specification for describing APIs | OpenAPI documents endpoints and schemas. |
| 1231 | What is Swagger? | A toolset based around OpenAPI | Swagger generates API documentation and clients. |
| 1232 | What is Swagger UI? | An interactive API documentation interface | It allows testing endpoints from a browser. |
| 1233 | What is Swashbuckle? | A library generating OpenAPI documents for ASP.NET Core | It integrates Swagger generation. |
| 1234 | What is API explorer? | A service describing API endpoints | It provides metadata for documentation tools. |
| 1235 | What is NSwag? | An OpenAPI generation and client generation tool | NSwag creates API clients and documentation. |
| 1236 | What is rate limiting? | Controlling request frequency | It protects services from excessive traffic. |
| 1237 | What is fixed window rate limiting? | Limiting requests within fixed time periods | Requests reset after each window. |
| 1238 | What is sliding window rate limiting? | A smoother time-based rate limit algorithm | It tracks requests across moving periods. |
| 1239 | What is token bucket rate limiting? | A limiter using refillable tokens | Tokens represent allowed requests. |
| 1240 | What is concurrency limiter? | Limiting simultaneous operations | It controls active requests rather than request count. |
| 1241 | What is request throttling? | Reducing request processing speed | It prevents overload situations. |
| 1242 | What is load balancing? | Distributing requests across servers | It improves scalability and availability. |
| 1243 | What is horizontal scaling? | Adding more application instances | Horizontal scaling increases capacity by replication. |
| 1244 | What is vertical scaling? | Increasing resources of one instance | Vertical scaling adds CPU or memory. |
| 1245 | What is stateless application design? | Avoiding server-side client session dependency | Stateless services scale more easily. |
| 1246 | What is session state? | Stored information about a user's interaction | Sessions maintain user-specific data. |
| 1247 | What is distributed session storage? | Shared session data across servers | It supports multi-instance deployments. |
| 1248 | What is sticky session? | Routing a user to the same server repeatedly | Sticky sessions reduce synchronization needs but limit scalability. |
| 1249 | What is CDN? | A distributed network for delivering content | CDNs reduce latency for static resources. |
| 1250 | What is reverse proxy caching? | Storing responses at the proxy layer | It reduces backend processing requirements. |
| 1251 | What is the purpose of antiforgery tokens in ASP.NET Core? | Verifying that requests originate from the intended application | Antiforgery tokens protect against cross-site request forgery attacks. |
| 1252 | Where are antiforgery tokens commonly used? | State-changing operations such as POST requests | They protect operations that modify server data. |
| 1253 | What is a cookie policy in ASP.NET Core? | Rules controlling cookie behavior | Cookie policies configure consent, security, and storage behavior. |
| 1254 | What does the HttpOnly cookie flag do? | Prevents JavaScript access to cookies | It reduces the risk of cookie theft through XSS. |
| 1255 | What does the Secure cookie flag do? | Allows cookies only over HTTPS | It prevents transmission over insecure connections. |
| 1256 | What does the SameSite cookie attribute control? | Cross-site cookie sending behavior | SameSite helps prevent CSRF attacks. |
| 1257 | What are the SameSite modes? | Strict, Lax, and None | They define cross-site cookie restrictions. |
| 1258 | What is a session cookie? | A cookie removed when the browser closes | Session cookies do not have a persistent expiration. |
| 1259 | What is a persistent cookie? | A cookie stored until expiration | Persistent cookies survive browser restarts. |
| 1260 | What is data protection in ASP.NET Core? | A framework for protecting sensitive data | It provides encryption and key management services. |
| 1261 | What interface represents ASP.NET Core data protection? | IDataProtector | IDataProtector creates protected data payloads. |
| 1262 | What is key rotation in data protection? | Periodically replacing encryption keys | Rotation improves security over time. |
| 1263 | Where are ASP.NET Core data protection keys stored? | In a configured key repository | Keys can be stored in files, databases, or external stores. |
| 1264 | What is machine key in ASP.NET Framework? | A key used for cryptographic operations | ASP.NET Core uses the newer data protection system instead. |
| 1265 | What is antiforgery token storage? | A mechanism storing validation data | Tokens are commonly stored in cookies and request fields. |
| 1266 | What is XSS? | Cross-Site Scripting | XSS injects malicious scripts into web pages. |
| 1267 | How does Razor help prevent XSS? | It automatically HTML encodes output | Encoding prevents scripts from executing. |
| 1268 | What is HTML encoding? | Converting special characters into safe representations | It prevents interpreted markup execution. |
| 1269 | What is Content Security Policy? | A browser security policy controlling resource loading | CSP reduces script injection risks. |
| 1270 | What is security header middleware? | Middleware adding HTTP security headers | It improves browser security behavior. |
| 1271 | What is HSTS preload? | A browser-enforced HTTPS-only configuration | It prevents initial insecure connections. |
| 1272 | What is TLS termination? | Decrypting HTTPS traffic at an intermediary | Reverse proxies often perform TLS termination. |
| 1273 | What is certificate validation? | Checking whether a certificate is trusted | It ensures secure communication endpoints. |
| 1274 | What is mutual TLS? | Authentication using certificates on both sides | Both client and server verify certificates. |
| 1275 | What is secure secret management? | Protecting sensitive configuration values | Secrets should be stored outside application code. |
| 1276 | What is Azure Key Vault? | A managed service for storing secrets and keys | Applications can retrieve secrets securely. |
| 1277 | What is managed identity? | An identity provided by a cloud platform | It removes the need to store credentials. |
| 1278 | What is dependency health monitoring? | Checking whether required services are available | It detects failures in dependencies. |
| 1279 | What is resilience engineering? | Designing systems to handle failures | It focuses on reliability under unexpected conditions. |
| 1280 | What is retry policy? | Logic that repeats failed operations | Retries can recover from temporary failures. |
| 1281 | What is exponential backoff? | Increasing retry delays after failures | It reduces pressure on failing services. |
| 1282 | What is jitter in retry strategies? | Random delay added to retries | Jitter prevents synchronized retry storms. |
| 1283 | What is circuit breaker pattern? | Temporarily stopping calls to failing services | It prevents cascading failures. |
| 1284 | What are circuit breaker states? | Closed, Open, Half-Open | They represent normal, blocked, and testing states. |
| 1285 | What is timeout policy? | Limiting how long an operation may run | Timeouts prevent indefinite waiting. |
| 1286 | What is bulkhead pattern? | Isolating failures by limiting resources | Bulkheads prevent one failure from exhausting everything. |
| 1287 | What is Polly in .NET? | A resilience and transient-fault-handling library | Polly provides retries, timeouts, and circuit breakers. |
| 1288 | What is IHttpClientFactory? | A factory for creating configured HttpClient instances | It manages HttpClient lifetimes and handlers. |
| 1289 | Why is creating HttpClient repeatedly discouraged? | It can exhaust sockets | IHttpClientFactory manages connections efficiently. |
| 1290 | What is a named HttpClient? | A client configured with a specific name | Named clients provide reusable configurations. |
| 1291 | What is a typed HttpClient? | A strongly typed wrapper around HttpClient | Typed clients encapsulate API communication logic. |
| 1292 | What is a delegating handler? | A component processing outgoing HTTP requests | Handlers can add logging, authentication, or policies. |
| 1293 | What is HttpMessageHandler? | The component responsible for HTTP transport | It sends requests and receives responses. |
| 1294 | What is HttpRequestMessage? | An object representing an HTTP request | It provides detailed request configuration. |
| 1295 | What is HttpResponseMessage? | An object representing an HTTP response | It contains status, headers, and content. |
| 1296 | What is HTTP message content? | The body of an HTTP request or response | Content represents transmitted data. |
| 1297 | What is multipart/form-data? | A content type for sending multiple data parts | It is commonly used for file uploads. |
| 1298 | What is streaming HTTP content? | Sending data without loading everything into memory | Streaming improves large transfer efficiency. |
| 1299 | What is request cancellation in HttpClient? | Stopping requests through cancellation tokens | It frees resources when requests are no longer needed. |
| 1300 | What is connection pooling in HttpClient? | Reusing network connections | Pooling improves HTTP performance. |
| 1301 | What is the purpose of cancellation tokens in .NET? | Coordinating cooperative cancellation | Cancellation tokens allow operations to stop gracefully. |
| 1302 | What type represents a cancellation request source? | CancellationTokenSource | It creates and controls cancellation tokens. |
| 1303 | What type represents a cancellation signal? | CancellationToken | It is passed to operations that support cancellation. |
| 1304 | What happens when CancellationTokenSource.Cancel() is called? | Registered callbacks are triggered and cancellation is signaled | Consumers decide how to stop their operations. |
| 1305 | What is cooperative cancellation? | Allowing code to voluntarily stop execution | .NET cancellation does not forcibly terminate threads. |
| 1306 | What is CancellationToken.ThrowIfCancellationRequested()? | A method that throws when cancellation is requested | It provides a standard cancellation check. |
| 1307 | What exception represents cancellation? | OperationCanceledException | It indicates an operation stopped due to cancellation. |
| 1308 | What is linked cancellation? | Combining multiple cancellation tokens | Cancellation occurs when any linked token is canceled. |
| 1309 | What method creates linked cancellation tokens? | CreateLinkedTokenSource() | It combines multiple cancellation sources. |
| 1310 | What is timeout cancellation? | Automatically canceling after a time limit | It prevents operations from running indefinitely. |
| 1311 | What method creates a token that cancels after a delay? | CancelAfter() | It schedules automatic cancellation. |
| 1312 | What is PeriodicTimer? | A timer designed for asynchronous loops | It supports async waiting between intervals. |
| 1313 | What is System.Threading.Timer? | A callback-based timer | It executes callbacks on thread pool threads. |
| 1314 | What is System.Timers.Timer? | An event-based timer | It raises elapsed events periodically. |
| 1315 | What is DispatcherTimer? | A timer tied to a UI dispatcher | It executes callbacks on the UI thread. |
| 1316 | What is Stopwatch? | A high-resolution timing utility | Stopwatch measures elapsed time. |
| 1317 | What does Stopwatch use internally? | A high-resolution performance counter | It provides precise timing measurements. |
| 1318 | What is BenchmarkDotNet? | A framework for benchmarking .NET code | It provides reliable performance measurements. |
| 1319 | Why should benchmarks avoid Debug builds? | Debug builds do not represent optimized performance | Release builds better reflect production behavior. |
| 1320 | What is warmup in benchmarking? | Running code before measurement | Warmup reduces startup effects. |
| 1321 | What is benchmark iteration? | A single measured execution cycle | Multiple iterations improve accuracy. |
| 1322 | What is statistical benchmarking? | Measuring performance using multiple samples | It accounts for runtime variation. |
| 1323 | What is allocation profiling? | Measuring memory allocations | It identifies allocation-heavy code paths. |
| 1324 | What is Gen 0 allocation? | Allocation of new short-lived objects | Frequent Gen 0 collections reclaim temporary objects. |
| 1325 | What is LOH compaction? | Reducing fragmentation in the Large Object Heap | It can improve large allocation efficiency. |
| 1326 | What objects go to the Large Object Heap? | Large objects typically around 85KB or larger | LOH stores large memory allocations. |
| 1327 | What is pinned memory? | Memory prevented from moving by the GC | Pinning is required for some native operations. |
| 1328 | Why can excessive pinning hurt performance? | It prevents GC compaction | Fragmentation and slower collection can occur. |
| 1329 | What is GCHandle? | A mechanism for controlling object handles | It provides advanced GC interaction. |
| 1330 | What is a weak reference? | A reference that does not prevent garbage collection | Weak references allow objects to be collected. |
| 1331 | What is WeakReference<T>? | A generic weak reference type | It provides type-safe weak referencing. |
| 1332 | What is ConditionalWeakTable<TKey,TValue>? | A table associating values without preventing key collection | It supports metadata storage tied to object lifetime. |
| 1333 | What is object resurrection? | Bringing an object back during finalization | It is possible but generally discouraged. |
| 1334 | What is finalization? | Cleanup performed before garbage collection reclaims an object | Finalizers release unmanaged resources. |
| 1335 | Why are finalizers expensive? | They require extra GC processing | Finalizable objects survive longer before collection. |
| 1336 | What method suppresses finalization? | GC.SuppressFinalize() | It avoids unnecessary finalizer execution. |
| 1337 | What is SafeHandle? | A safer wrapper for unmanaged resources | SafeHandle improves reliability of native resource cleanup. |
| 1338 | What is CriticalHandle? | A base class for critical unmanaged handles | It provides stronger reliability guarantees. |
| 1339 | What is unmanaged resource cleanup? | Releasing resources outside managed memory | Examples include file handles and native memory. |
| 1340 | What is IDisposable? | An interface for deterministic cleanup | IDisposable enables explicit resource release. |
| 1341 | What pattern implements IDisposable correctly? | Dispose pattern | It separates managed and unmanaged cleanup logic. |
| 1342 | What is the purpose of Dispose(bool)? | Separating explicit and finalizer cleanup | It controls cleanup behavior. |
| 1343 | What is the dispose ownership concept? | Defining which object is responsible for cleanup | Clear ownership prevents leaks. |
| 1344 | What does using declaration do? | Automatically disposes a resource at scope end | It simplifies IDisposable usage. |
| 1345 | What does await using do? | Asynchronously disposes resources | It works with IAsyncDisposable. |
| 1346 | What is a resource leak? | Failure to release allocated resources | Leaks can degrade application performance. |
| 1347 | What is memory pressure? | Increased demand on available memory | High memory pressure affects GC behavior. |
| 1348 | What is GC.AddMemoryPressure()? | Informing GC about unmanaged allocations | It helps GC make better collection decisions. |
| 1349 | What is GC.RemoveMemoryPressure()? | Removing previously reported unmanaged pressure | It balances GC memory tracking. |
| 1350 | What is server GC? | A GC mode optimized for throughput | Server GC uses multiple heaps and threads. |
| 1351 | What is workstation GC? | A garbage collector optimized for client applications | Workstation GC prioritizes responsiveness and lower latency. |
| 1352 | What is concurrent GC? | A mode allowing background collection work | It reduces application pause times during Gen 2 collections. |
| 1353 | What is GC latency mode? | A setting controlling garbage collection behavior | Latency modes balance throughput and responsiveness. |
| 1354 | What is GCLatencyMode.Batch? | A mode optimized for maximum throughput | It allows more aggressive garbage collection. |
| 1355 | What is GCLatencyMode.LowLatency? | A mode minimizing collection pauses temporarily | It is useful during short critical operations. |
| 1356 | What is GCLatencyMode.SustainedLowLatency? | A mode maintaining low pauses over longer periods | It supports applications requiring consistent responsiveness. |
| 1357 | What is GC.TryStartNoGCRegion()? | Attempts to prevent collections temporarily | It reserves memory for allocation-sensitive operations. |
| 1358 | Why use No GC Region? | To avoid pauses during critical sections | It is useful for latency-sensitive workloads. |
| 1359 | What ends a No GC Region? | Calling EndNoGCRegion() or exceeding limits | It restores normal GC behavior. |
| 1360 | What is allocation rate? | The amount of memory allocated over time | High allocation rates increase GC activity. |
| 1361 | What is memory fragmentation? | Unusable gaps between allocated memory blocks | Fragmentation reduces allocation efficiency. |
| 1362 | What is heap compaction? | Moving objects to reduce fragmentation | The GC compacts movable objects. |
| 1363 | What is object promotion? | Moving objects to older GC generations | Long-lived objects survive collections and are promoted. |
| 1364 | What triggers a Gen 0 collection? | Allocation pressure in the young generation | New object allocations eventually trigger collection. |
| 1365 | What triggers a Gen 2 collection? | High memory pressure or full heap collection requests | Gen 2 collections are less frequent and more expensive. |
| 1366 | What is LOH fragmentation? | Fragmentation caused by large object allocations | Large objects require special heap management. |
| 1367 | What is pinned object heap (POH)? | A heap for pinned objects | POH reduces fragmentation from long-lived pinned objects. |
| 1368 | When was the pinned object heap introduced? | .NET 5 | It isolates pinned allocations from normal heaps. |
| 1369 | What is a GC root? | A reference that keeps objects alive | Objects reachable from roots cannot be collected. |
| 1370 | Examples of GC roots? | Static fields, stack references, and handles | GC uses roots to determine object reachability. |
| 1371 | What is reachability analysis? | Determining which objects are still referenced | Unreachable objects become eligible for collection. |
| 1372 | What is a memory leak in managed code? | Keeping references to objects unnecessarily | Managed leaks are usually caused by unwanted references. |
| 1373 | What commonly causes managed memory leaks? | Events, static collections, and caches | References prevent garbage collection. |
| 1374 | Why can events cause memory leaks? | Subscribers remain referenced by publishers | Event handlers must sometimes be unsubscribed. |
| 1375 | What is a static reference leak? | A static object retaining unnecessary data | Static lifetime can accidentally keep objects alive. |
| 1376 | What is a memory profiler? | A tool analyzing memory usage | Profilers identify allocation and retention issues. |
| 1377 | What is dotnet-dump heap analysis? | Inspecting managed objects in a dump | It helps find memory retention problems. |
| 1378 | What is SOS debugging extension? | A tool for inspecting CLR internals | SOS provides runtime debugging commands. |
| 1379 | What is ClrMD? | A managed API for analyzing .NET processes | ClrMD enables custom diagnostic tooling. |
| 1380 | What is runtime instrumentation? | Collecting execution data while code runs | Instrumentation supports diagnostics and monitoring. |
| 1381 | What is reflection? | Inspecting metadata at runtime | Reflection allows dynamic type discovery. |
| 1382 | What namespace contains reflection APIs? | System.Reflection | It provides runtime metadata access. |
| 1383 | What is Type in reflection? | Represents metadata about a type | Type provides information about members and attributes. |
| 1384 | What is Assembly in reflection? | Represents a compiled .NET assembly | Assemblies contain types and metadata. |
| 1385 | What is AssemblyLoadContext? | A mechanism for loading assemblies dynamically | It supports plugin scenarios and isolation. |
| 1386 | What is the default AssemblyLoadContext? | The main application loading context | It loads normal application dependencies. |
| 1387 | What is collectible AssemblyLoadContext? | A load context that can be unloaded | It allows plugin unloading. |
| 1388 | What is reflection-only loading? | Loading metadata without executing code | It is used for inspection scenarios. |
| 1389 | What is an attribute in .NET? | Metadata attached to program elements | Attributes provide additional information. |
| 1390 | What base class do attributes inherit from? | Attribute | All custom attributes derive from Attribute. |
| 1391 | What is AttributeUsageAttribute? | Controls where attributes can be applied | It defines targets and repetition rules. |
| 1392 | What are attribute targets? | Program elements where attributes can be placed | Examples include classes, methods, and properties. |
| 1393 | What is conditional compilation? | Compiling code based on symbols | It enables environment-specific code. |
| 1394 | What directive enables conditional compilation? | #if | It conditionally includes source code. |
| 1395 | What directive defines a compilation symbol? | #define | It creates preprocessor symbols. |
| 1396 | What is CallerMemberNameAttribute? | Provides the calling member name automatically | It simplifies logging and diagnostics. |
| 1397 | What is CallerFilePathAttribute? | Provides the caller source file path | It helps with diagnostic information. |
| 1398 | What is CallerLineNumberAttribute? | Provides the caller line number | It helps locate source calls. |
| 1399 | What is source generation in .NET? | Generating code during compilation | It reduces runtime reflection and improves performance. |
| 1400 | What interface is commonly used for source generators? | IIncrementalGenerator | It enables efficient incremental code generation. |
| 1401 | What is a Roslyn analyzer? | A tool that analyzes C# code during compilation | Analyzers detect issues and enforce coding rules. |
| 1402 | What API powers C# and VB compilation? | Roslyn compiler platform | Roslyn provides compiler APIs and code analysis capabilities. |
| 1403 | What is a syntax tree? | A structured representation of source code | Roslyn analyzes code through syntax trees. |
| 1404 | What is a semantic model? | Information about code meaning and symbols | It resolves types, references, and relationships. |
| 1405 | What is a symbol in Roslyn? | A representation of a code element | Symbols describe types, methods, properties, and variables. |
| 1406 | What is an incremental source generator? | A generator that tracks only changed inputs | It improves compilation performance. |
| 1407 | What is partial class generation? | Adding generated code to an existing class | Source generators commonly use partial types. |
| 1408 | What is a partial method? | A method declaration split across partial types | It allows generated implementations. |
| 1409 | What is compile-time evaluation? | Calculating values during compilation | It can reduce runtime work. |
| 1410 | What is a constant expression? | An expression evaluated at compile time | Constants must be known before execution. |
| 1411 | What is the difference between const and readonly? | const is compile-time, readonly is runtime-initialized | readonly values can be assigned in constructors. |
| 1412 | What is static readonly? | A value initialized once per type | It provides immutable type-level state. |
| 1413 | What is a record type? | A reference type designed for immutable data models | Records provide value-based equality. |
| 1414 | What is a record struct? | A value type with record semantics | Record structs combine structs with value equality. |
| 1415 | What is positional record syntax? | A concise way to define record data | It creates primary constructors and properties. |
| 1416 | What is a primary constructor? | A constructor defined directly in the type declaration | It reduces constructor boilerplate. |
| 1417 | Which C# types support primary constructors? | Classes and structs | Modern C# allows simplified constructor declarations. |
| 1418 | What is a with expression? | A syntax for creating modified copies | It is commonly used with records. |
| 1419 | What does record equality compare? | Values rather than references | Records use generated value-based equality. |
| 1420 | What is a generated Deconstruct method? | A method that extracts object values | It enables deconstruction syntax. |
| 1421 | What is tuple deconstruction? | Assigning tuple elements to separate variables | It simplifies handling grouped values. |
| 1422 | What is ValueTuple<T1,T2>? | A mutable value tuple type | ValueTuple stores multiple values efficiently. |
| 1423 | What is System.Tuple? | A reference tuple type | Tuple stores grouped values as objects. |
| 1424 | Why prefer ValueTuple over Tuple? | It avoids allocations and supports better syntax | ValueTuple is generally more lightweight. |
| 1425 | What is pattern matching? | Checking and extracting values based on shape | It provides expressive type handling. |
| 1426 | What is a switch expression? | A switch returning a value | It provides concise branching logic. |
| 1427 | What is a property pattern? | Matching object properties | It checks values inside objects. |
| 1428 | What is a relational pattern? | Comparing values using operators | It supports conditions like greater than or less than. |
| 1429 | What is a logical pattern? | Combining patterns using and, or, and not | It allows complex matching rules. |
| 1430 | What is list pattern matching? | Matching elements inside collections | It supports array and list shape checks. |
| 1431 | What is exhaustive pattern matching? | Handling every possible input case | It improves correctness and compiler analysis. |
| 1432 | What is a discard pattern? | Ignoring a value during matching | The underscore (\_) represents ignored data. |
| 1433 | What is a constant pattern? | Matching an exact constant value | It compares against known values. |
| 1434 | What is a type pattern? | Matching based on runtime type | It checks object types safely. |
| 1435 | What is pattern variable scope? | The region where a matched variable exists | The compiler controls accessibility. |
| 1436 | What is nullable reference type analysis? | Compiler analysis of possible null values | It reduces null reference errors. |
| 1437 | What operator suppresses nullable warnings? | ! | The null-forgiving operator tells the compiler a value is not null. |
| 1438 | What is the null-coalescing operator? | ?? | It provides a fallback value when null. |
| 1439 | What is the null-coalescing assignment operator? | ??= | It assigns only when a value is null. |
| 1440 | What is the null conditional operator? | ?. | It safely accesses members on nullable references. |
| 1441 | What is nullable value type syntax? | T? | It allows value types to contain null. |
| 1442 | What is Nullable<T>? | A struct wrapping nullable value types | It represents optional value types. |
| 1443 | What property checks Nullable<T> has a value? | HasValue | It indicates whether a nullable value contains data. |
| 1444 | What property retrieves Nullable<T> data? | Value | It returns the underlying value. |
| 1445 | What exception occurs accessing Value without a value? | InvalidOperationException | Nullable.Value requires an existing value. |
| 1446 | What is boxing? | Converting a value type into an object reference | Boxing allocates an object on the heap. |
| 1447 | What is unboxing? | Extracting a value type from an object | Unboxing requires the exact original value type. |
| 1448 | Why is boxing expensive? | It creates heap allocations | Excessive boxing increases GC pressure. |
| 1449 | What is generic specialization? | Creating optimized generic code for types | It can avoid boxing for value types. |
| 1450 | Why do generics improve performance? | They provide type safety without many casts or boxing | Generics allow efficient reusable code. |
| 1451 | What is covariance in C# generics? | Allowing a more derived type to be used where a base type is expected | Covariance applies to output-only generic parameters. |
| 1452 | What keyword enables covariance? | out | The out modifier marks a generic parameter as covariant. |
| 1453 | What is contravariance in C# generics? | Allowing a base type to be used where a derived type is expected | Contravariance applies to input-only generic parameters. |
| 1454 | What keyword enables contravariance? | in | The in modifier marks a generic parameter as contravariant. |
| 1455 | What is invariant generic behavior? | Requiring exact type matches | Most generic types are invariant by default. |
| 1456 | Why are List<T> types invariant? | Allowing variance would break type safety | A List<Derived> cannot safely act as List<Base>. |
| 1457 | Which interfaces commonly support covariance? | IEnumerable<T> and IQueryable<T> | They only produce values. |
| 1458 | Which interfaces commonly support contravariance? | IComparer<T> and IEqualityComparer<T> | They consume values. |
| 1459 | What is generic type constraint? | A restriction on allowed type arguments | Constraints improve safety and available operations. |
| 1460 | What does the class constraint mean? | The type parameter must be a reference type | It restricts generic arguments to classes. |
| 1461 | What does the struct constraint mean? | The type parameter must be a value type | It restricts generic arguments to structs. |
| 1462 | What does the new() constraint require? | A public parameterless constructor | It allows creating instances with new T(). |
| 1463 | What does the notnull constraint enforce? | Preventing nullable type arguments | It restricts generic arguments from being nullable. |
| 1464 | What does the base class constraint allow? | Restricting types to inherit from a specific class | It enables operations from that base type. |
| 1465 | What does the interface constraint allow? | Restricting types to implement an interface | It guarantees required members exist. |
| 1466 | What is generic method type inference? | Compiler determining generic arguments automatically | It removes the need to specify type parameters. |
| 1467 | What is generic type erasure? | Removing generic type information at runtime | .NET does not use full generic type erasure. |
| 1468 | How does CLR handle generics? | It maintains runtime generic metadata | Generic types remain available at runtime. |
| 1469 | What is open generic type? | A generic type without specific type arguments | Example: List<>. |
| 1470 | What is closed generic type? | A generic type with actual type arguments | Example: List<int>. |
| 1471 | What is reflection on generic types? | Inspecting generic definitions and arguments | Reflection can examine generic metadata. |
| 1472 | What method creates generic types dynamically? | MakeGenericType() | It creates constructed generic types at runtime. |
| 1473 | What is expression compilation? | Converting expression trees into executable delegates | It enables dynamic code execution. |
| 1474 | What is Expression<TDelegate>? | A representation of a lambda expression tree | Providers can analyze it before execution. |
| 1475 | What is a compiled expression cache? | Reusing generated delegates | It avoids repeated compilation overhead. |
| 1476 | What is dynamic dispatch? | Runtime selection of members based on actual type | It bypasses some compile-time checks. |
| 1477 | What keyword enables dynamic dispatch? | dynamic | It defers binding decisions until runtime. |
| 1478 | What binder handles dynamic operations? | Runtime binder | It resolves dynamic member access. |
| 1479 | What exception occurs for missing dynamic members? | RuntimeBinderException | It indicates failed dynamic resolution. |
| 1480 | What is the DLR? | Dynamic Language Runtime | It supports dynamic behavior in .NET. |
| 1481 | What is duck typing? | Using objects based on available members instead of declared types | Dynamic languages often use this approach. |
| 1482 | What is reflection emit? | Generating Intermediate Language dynamically | It allows runtime code generation. |
| 1483 | What namespace contains Reflection.Emit? | System.Reflection.Emit | It provides APIs for dynamic assemblies and methods. |
| 1484 | What is a dynamic method? | A method generated at runtime | It avoids creating full assemblies. |
| 1485 | What is Expression Tree rewriting? | Modifying expression structures before execution | It enables query transformations. |
| 1486 | What is serialization? | Converting objects into a transferable format | Serialization enables storage or communication. |
| 1487 | What is deserialization? | Reconstructing objects from serialized data | It restores object state. |
| 1488 | What is System.Text.Json? | The built-in JSON serialization library | It provides high-performance JSON processing. |
| 1489 | What is JsonSerializerOptions? | Configuration for JSON serialization | It controls naming, converters, and behavior. |
| 1490 | What is a JSON converter? | Custom serialization logic for a type | Converters control reading and writing. |
| 1491 | What is JsonConverter<T>? | Base class for custom JSON converters | It allows custom type handling. |
| 1492 | What is source-generated JSON serialization? | Compile-time generated serialization code | It reduces reflection overhead. |
| 1493 | What attribute enables JSON source generation? | JsonSerializableAttribute | It defines types for generated metadata. |
| 1494 | What is polymorphic serialization? | Serializing derived types through base references | It requires explicit configuration for security. |
| 1495 | What is serialization contract? | Rules describing how a type is represented | Contracts define serialized structure. |
| 1496 | What is schema validation? | Checking data against a defined structure | It ensures incoming data matches expectations. |
| 1497 | What is binary serialization? | Serializing objects into binary format | It is generally avoided for untrusted data. |
| 1498 | Why is BinaryFormatter obsolete? | It is unsafe for untrusted input | It can enable dangerous object deserialization attacks. |
| 1499 | What is interoperability? | Communication between different systems | .NET supports native and managed interoperability. |
| 1500 | What is P/Invoke? | Calling native functions from managed code | It enables interaction with unmanaged libraries. |
| 1501 | What attribute declares a P/Invoke method? | DllImportAttribute | It specifies an external native function to call. |
| 1502 | What namespace contains DllImportAttribute? | System.Runtime.InteropServices | It provides interoperability APIs. |
| 1503 | What is a native library? | A compiled library containing unmanaged code | Native libraries are commonly written in C or C++. |
| 1504 | What is marshalling? | Converting data between managed and unmanaged representations | Marshalling enables communication across runtime boundaries. |
| 1505 | What is blittable marshalling? | Copying memory directly between managed and native code | It avoids conversion overhead. |
| 1506 | What is COM interop? | Communication with Component Object Model components | It allows .NET applications to use COM objects. |
| 1507 | What is a COM callable wrapper? | A wrapper exposing .NET objects to COM | It allows unmanaged clients to call managed code. |
| 1508 | What is a runtime callable wrapper? | A wrapper allowing .NET to call COM objects | It adapts COM objects for managed usage. |
| 1509 | What is unmanaged memory allocation? | Allocating memory outside the GC heap | It requires manual cleanup. |
| 1510 | What class allocates unmanaged memory? | Marshal | Marshal provides unmanaged memory helpers. |
| 1511 | What method allocates unmanaged memory? | AllocHGlobal() | It allocates memory from the unmanaged heap. |
| 1512 | What method releases unmanaged memory? | FreeHGlobal() | It releases memory allocated with AllocHGlobal(). |
| 1513 | What is stack allocation in C#? | Allocating memory directly on the stack | stackalloc creates temporary stack memory. |
| 1514 | What keyword enables stack allocation? | stackalloc | It allocates memory in stack storage. |
| 1515 | What type can safely represent stackalloc memory? | Span<T> | Span provides safe access to stack memory. |
| 1516 | What is unsafe code? | Code allowing direct memory manipulation | It enables pointers and low-level operations. |
| 1517 | What keyword enables pointer operations? | unsafe | It allows pointer syntax in C#. |
| 1518 | What symbol declares a pointer type? | \* | Pointer types use the asterisk symbol. |
| 1519 | What operator obtains an address? | & | It returns the memory address of a variable. |
| 1520 | What operator dereferences a pointer? | \* | It accesses the value at an address. |
| 1521 | What is fixed statement used for? | Pinning managed memory | It prevents GC movement during pointer operations. |
| 1522 | Why must managed objects be pinned for pointers? | The GC can move objects during compaction | Pinning keeps addresses stable. |
| 1523 | What is native-sized integer? | An integer whose size matches the platform | It uses IntPtr or UIntPtr. |
| 1524 | What is IntPtr? | A signed native-sized integer type | It represents pointers safely. |
| 1525 | What is UIntPtr? | An unsigned native-sized integer type | It represents unsigned pointer-sized values. |
| 1526 | What is NativeMemory API? | Modern unmanaged memory allocation API | It provides low-level allocation functions. |
| 1527 | What namespace contains NativeMemory? | System.Runtime.InteropServices | It provides native memory operations. |
| 1528 | What is memory-mapped file? | A file mapped directly into memory | It allows efficient large-file access. |
| 1529 | What namespace contains memory-mapped files? | System.IO.MemoryMappedFiles | It provides memory-mapped file support. |
| 1530 | What is file stream buffering? | Temporarily storing file data in memory | Buffering improves I/O performance. |
| 1531 | What is BufferedStream? | A stream adding buffering to another stream | It reduces expensive I/O operations. |
| 1532 | What is FileStream? | A stream for file access | It supports synchronous and asynchronous operations. |
| 1533 | What is Stream base class? | An abstraction for byte-oriented data sources | Streams represent sequential data flow. |
| 1534 | What are common Stream implementations? | FileStream, MemoryStream, NetworkStream | Different streams target different data sources. |
| 1535 | What is MemoryStream? | A stream backed by memory | It allows in-memory byte operations. |
| 1536 | What is NetworkStream? | A stream over network connections | It enables socket-based communication. |
| 1537 | What is PipeStream? | A stream for inter-process communication | It allows processes to exchange data. |
| 1538 | What is System.IO.Pipelines? | A high-performance streaming API | Pipelines optimize parsing and network processing. |
| 1539 | What is PipeReader? | Reads data from a pipeline | It provides efficient buffered reading. |
| 1540 | What is PipeWriter? | Writes data into a pipeline | It provides efficient buffered writing. |
| 1541 | What is backpressure in pipelines? | Controlling data production speed | It prevents excessive buffering. |
| 1542 | What is zero-copy processing? | Processing data without unnecessary memory copying | It improves throughput and reduces allocations. |
| 1543 | What is buffering strategy? | Managing temporary storage during data transfer | Good buffering balances speed and memory usage. |
| 1544 | What is asynchronous I/O? | Performing I/O without blocking threads | It improves scalability for waiting operations. |
| 1545 | What is IO completion port? | An OS mechanism for efficient asynchronous I/O | Windows uses IOCP for scalable networking. |
| 1546 | What is epoll? | A Linux mechanism for scalable I/O events | It supports efficient asynchronous networking. |
| 1547 | What is kqueue? | A BSD/macOS event notification mechanism | It supports scalable I/O operations. |
| 1548 | What abstraction hides OS I/O mechanisms in .NET? | Socket and async I/O APIs | .NET provides cross-platform abstractions. |
| 1549 | What is socket programming? | Direct network communication using sockets | Sockets provide low-level networking. |
| 1550 | What protocol does TCP provide? | Reliable ordered byte communication | TCP guarantees delivery and ordering. |
| 1551 | What protocol does UDP provide? | Connectionless datagram communication | UDP provides faster communication without delivery guarantees. |
| 1552 | What is a TCP connection handshake? | The process establishing a TCP connection | TCP uses synchronization packets to create a connection. |
| 1553 | What is a socket endpoint? | An address and port combination | Endpoints identify network communication locations. |
| 1554 | What class represents an IP address in .NET? | IPAddress | It represents IPv4 and IPv6 addresses. |
| 1555 | What class represents an IP endpoint? | IPEndPoint | It combines an IP address and port. |
| 1556 | What class represents TCP connections? | TcpClient | It provides a higher-level TCP client API. |
| 1557 | What class provides TCP listening? | TcpListener | It accepts incoming TCP connections. |
| 1558 | What class provides UDP communication? | UdpClient | It simplifies UDP sending and receiving. |
| 1559 | What is DNS resolution? | Translating domain names into IP addresses | DNS allows applications to locate hosts. |
| 1560 | What class performs DNS operations? | Dns | It provides hostname and address resolution APIs. |
| 1561 | What is network latency? | The delay between sending and receiving data | Lower latency improves responsiveness. |
| 1562 | What is throughput? | Amount of data transferred over time | Higher throughput increases transfer capacity. |
| 1563 | What is packet loss? | Failure of network packets to reach their destination | Packet loss can reduce reliability. |
| 1564 | What is serialization overhead? | Extra cost of converting data formats | Efficient formats reduce communication cost. |
| 1565 | What is compression overhead? | CPU cost of compressing and decompressing data | Compression trades CPU for bandwidth savings. |
| 1566 | What is connection timeout? | Maximum time allowed to establish communication | It prevents indefinite connection attempts. |
| 1567 | What is keep-alive? | Maintaining an existing network connection | It avoids repeated connection setup costs. |
| 1568 | What is HTTP keep-alive? | Reusing TCP connections for multiple requests | It reduces connection overhead. |
| 1569 | What is DNS caching? | Storing DNS results temporarily | It reduces repeated DNS lookups. |
| 1570 | What is a proxy server? | An intermediary forwarding network requests | Proxies can provide filtering and routing. |
| 1571 | What is WebClient? | An older .NET HTTP client API | It is largely replaced by HttpClient. |
| 1572 | Why prefer HttpClient over WebClient? | Better async support and connection management | HttpClient is designed for modern applications. |
| 1573 | What is HttpClientHandler? | The default HTTP message handler | It manages low-level HTTP behavior. |
| 1574 | What is SocketsHttpHandler? | The modern HttpClient transport handler | It provides connection pooling and HTTP features. |
| 1575 | What is DNS refresh behavior in HttpClient? | How often host addresses are re-resolved | Handler lifetime controls DNS updates. |
| 1576 | What is HttpClient timeout? | Maximum duration for an HTTP request | It cancels requests exceeding the limit. |
| 1577 | What is HTTP content negotiation? | Selecting response format based on client preferences | Headers determine supported representations. |
| 1578 | What is Accept header? | Header specifying desired response formats | Servers use it for content selection. |
| 1579 | What is Content-Type header? | Header describing request or response body format | It identifies data representation. |
| 1580 | What is MIME type? | A format identifier for transmitted content | Examples include application/json and text/plain. |
| 1581 | What is JSON Patch? | A format describing partial JSON changes | It supports fine-grained updates. |
| 1582 | What is JSON Merge Patch? | A simpler partial update format | It modifies JSON objects through merging. |
| 1583 | What is API pagination? | Splitting large result sets into smaller responses | Pagination improves performance and usability. |
| 1584 | What is offset pagination? | Pagination using skip and take values | It is simple but can become inefficient. |
| 1585 | What is cursor pagination? | Pagination using continuation tokens | It performs better for large changing datasets. |
| 1586 | What is filtering in APIs? | Restricting results based on criteria | Filtering reduces unnecessary data transfer. |
| 1587 | What is sorting in APIs? | Ordering returned data | Sorting improves client usability. |
| 1588 | What is projection in APIs? | Returning only selected fields | Projection reduces payload size. |
| 1589 | What is over-fetching? | Returning more data than needed | It increases bandwidth and processing costs. |
| 1590 | What is under-fetching? | Requiring multiple requests to obtain needed data | It increases network round trips. |
| 1591 | What is GraphQL? | A query language for APIs | GraphQL allows clients to request specific data. |
| 1592 | What is a GraphQL resolver? | Code that retrieves requested data | Resolvers provide field values. |
| 1593 | What is a GraphQL schema? | A definition of available API types and operations | It describes the API contract. |
| 1594 | What is REST versus GraphQL difference? | REST exposes resources while GraphQL exposes queries | They use different approaches to data retrieval. |
| 1595 | What is gRPC versus REST difference? | gRPC uses binary contracts while REST commonly uses HTTP JSON | gRPC targets high-performance service communication. |
| 1596 | What is microservice architecture? | Splitting applications into independent services | Services communicate over networks. |
| 1597 | What is service discovery? | Finding available service instances dynamically | It supports distributed systems. |
| 1598 | What is API gateway? | A single entry point for multiple services | Gateways handle routing and cross-cutting concerns. |
| 1599 | What is distributed configuration? | Sharing configuration across services | It keeps service settings consistent. |
| 1600 | What is eventual consistency? | Data becoming consistent over time | Distributed systems often trade immediate consistency for scalability. |
| 1601 | What is dependency inversion principle? | High-level modules should depend on abstractions | It reduces coupling between components. |
| 1602 | What is SOLID? | A set of object-oriented design principles | SOLID improves maintainability and extensibility. |
| 1603 | What does the S in SOLID represent? | Single Responsibility Principle | A class should have one reason to change. |
| 1604 | What does the O in SOLID represent? | Open/Closed Principle | Software should be open for extension but closed for modification. |
| 1605 | What does the L in SOLID represent? | Liskov Substitution Principle | Derived types should be replaceable for base types. |
| 1606 | What does the I in SOLID represent? | Interface Segregation Principle | Clients should not depend on unused members. |
| 1607 | What does the D in SOLID represent? | Dependency Inversion Principle | Code should depend on abstractions. |
| 1608 | What is cohesion? | How closely related responsibilities are within a component | High cohesion improves maintainability. |
| 1609 | What is coupling? | The dependency between components | Lower coupling improves flexibility. |
| 1610 | What is tight coupling? | Strong dependency between components | It makes changes more difficult. |
| 1611 | What is loose coupling? | Minimal dependency between components | It improves testability and reuse. |
| 1612 | What is composition over inheritance? | Building behavior by combining objects | Composition often reduces rigid hierarchies. |
| 1613 | What is an abstraction? | A simplified representation exposing important behavior | Abstractions hide implementation details. |
| 1614 | What is encapsulation? | Hiding internal state and implementation | It protects object invariants. |
| 1615 | What is polymorphism? | Ability to treat different types through a common interface | It enables flexible behavior. |
| 1616 | What is inheritance? | Deriving a type from another type | It enables code reuse through relationships. |
| 1617 | What is virtual dispatch? | Runtime selection of overridden methods | It enables polymorphic behavior. |
| 1618 | What is method hiding? | Replacing a member using the new keyword | It does not provide true overriding. |
| 1619 | What is abstract class? | A class that cannot be instantiated directly | It provides shared implementation and contracts. |
| 1620 | What is interface default implementation? | Providing method bodies inside interfaces | It allows interface evolution without breaking implementations. |
| 1621 | What is explicit interface implementation? | Implementing interface members with qualified names | It hides members from the class interface. |
| 1622 | What is dependency injection lifetime? | The duration a service instance exists | Lifetimes control object creation and disposal. |
| 1623 | What is singleton lifetime? | One instance for the application lifetime | Singleton services are shared globally. |
| 1624 | What is scoped lifetime? | One instance per scope | In web apps, usually one per request. |
| 1625 | What is transient lifetime? | A new instance every resolution | Transient services are short-lived. |
| 1626 | What is captive dependency? | A longer-lived service holding a shorter-lived service | It can cause incorrect lifetimes and memory issues. |
| 1627 | What is service locator pattern? | Resolving dependencies manually from a container | It hides dependencies and is generally discouraged. |
| 1628 | What is constructor injection? | Providing dependencies through constructors | It makes dependencies explicit. |
| 1629 | What is property injection? | Providing dependencies through properties | It can make required dependencies unclear. |
| 1630 | What is method injection? | Passing dependencies directly into methods | It limits dependency scope. |
| 1631 | What is an IoC container? | A framework managing object creation | It implements inversion of control. |
| 1632 | What is IServiceCollection? | A collection of registered services | It configures dependency injection. |
| 1633 | What is IServiceProvider? | A service resolution mechanism | It creates requested services. |
| 1634 | What is ActivatorUtilities? | A helper for creating objects with DI support | It combines manual creation with dependency injection. |
| 1635 | What is options pattern? | A way to access strongly typed configuration | It maps configuration to classes. |
| 1636 | What interface represents options access? | IOptions<T> | It provides configured option values. |
| 1637 | What is IOptionsSnapshot<T>? | Scoped options that can reload configuration | It provides updated values per scope. |
| 1638 | What is IOptionsMonitor<T>? | Options that support change notifications | It observes configuration changes. |
| 1639 | What is configuration binding? | Mapping configuration values to objects | It simplifies settings management. |
| 1640 | What is configuration provider? | A source supplying configuration values | Providers can read files, environment variables, or secrets. |
| 1641 | What is appsettings.json? | A JSON configuration file | It stores application settings. |
| 1642 | What is environment-specific configuration? | Configuration loaded based on environment | It supports development and production differences. |
| 1643 | What is ASPNETCORE_ENVIRONMENT? | An environment variable selecting the application environment | It controls environment-specific behavior. |
| 1644 | What are common ASP.NET Core environments? | Development, Staging, Production | They represent deployment stages. |
| 1645 | What is configuration precedence? | The order configuration sources override each other | Later providers typically override earlier ones. |
| 1646 | What is environment variable configuration? | Configuration loaded from OS variables | It is commonly used for deployment settings. |
| 1647 | What is command-line configuration? | Configuration provided through startup arguments | It allows runtime overrides. |
| 1648 | What is user secrets storage? | Local development secret storage | It prevents secrets being committed to source control. |
| 1649 | What is logging abstraction in .NET? | A common API for application logs | It separates logging from providers. |
| 1650 | What interface represents logging? | ILogger<T> | It provides structured logging capabilities. |
| 1651 | What is structured logging? | Logging data as named properties instead of formatted strings | Structured logs are easier to search and analyze. |
| 1652 | What is ILoggerFactory? | A factory for creating logger instances | It manages logger providers. |
| 1653 | What is a logging provider? | A component that receives log messages | Providers send logs to destinations. |
| 1654 | What are common .NET logging providers? | Console, Debug, EventSource, and third-party providers | Providers determine where logs are written. |
| 1655 | What is log level filtering? | Controlling which messages are recorded | It reduces unnecessary logging overhead. |
| 1656 | What are common log levels? | Trace, Debug, Information, Warning, Error, Critical | Levels indicate message importance. |
| 1657 | What is EventSource? | A .NET tracing mechanism | It provides high-performance diagnostic events. |
| 1658 | What is EventListener? | A component that consumes EventSource events | It allows runtime event monitoring. |
| 1659 | What is EventPipe? | A cross-platform diagnostic tracing system | It powers many dotnet diagnostic tools. |
| 1660 | What is dotnet-trace? | A tool for collecting runtime traces | It captures performance and diagnostic events. |
| 1661 | What is dotnet-counters? | A tool for monitoring runtime metrics | It displays live performance counters. |
| 1662 | What is dotnet-monitor? | A diagnostics tool for .NET applications | It exposes metrics, traces, and dumps. |
| 1663 | What is distributed tracing? | Tracking requests across multiple services | It helps diagnose distributed system behavior. |
| 1664 | What is OpenTelemetry? | A standard observability framework | It collects traces, metrics, and logs. |
| 1665 | What is a trace? | A record of an operation across systems | Traces show request flow. |
| 1666 | What is a span? | A single operation within a trace | Spans represent individual work units. |
| 1667 | What is trace context propagation? | Passing tracing identifiers between services | It connects distributed operations. |
| 1668 | What is correlation ID? | An identifier linking related operations | It helps follow requests through logs. |
| 1669 | What is metrics collection? | Recording numerical measurements over time | Metrics show system behavior trends. |
| 1670 | What is a counter metric? | A value that only increases | Counters measure totals. |
| 1671 | What is a gauge metric? | A value that can increase or decrease | Gauges measure current state. |
| 1672 | What is histogram metric? | Measuring value distributions | Histograms show ranges and percentiles. |
| 1673 | What is percentile latency? | A latency value below which a percentage of requests complete | It shows performance distribution. |
| 1674 | What is p50 latency? | Median request latency | Half of requests complete faster. |
| 1675 | What is p95 latency? | Latency experienced by 95% of requests or less | It highlights slower requests. |
| 1676 | What is p99 latency? | High-percentile latency measurement | It reveals worst common performance cases. |
| 1677 | What is application logging versus metrics? | Logs describe events while metrics summarize behavior | They serve different diagnostic purposes. |
| 1678 | What is an audit log? | A record of important user or system actions | It supports compliance and investigation. |
| 1679 | What is log enrichment? | Adding additional context to log events | It improves troubleshooting. |
| 1680 | What is a logging scope? | A context applied to related log messages | Scopes add shared metadata. |
| 1681 | What is ILogger.BeginScope()? | Creates a logging scope | It attaches contextual information to logs. |
| 1682 | What is exception logging? | Recording exception details for diagnosis | It helps identify failures. |
| 1683 | Why avoid logging sensitive data? | It can expose confidential information | Logs must protect private data. |
| 1684 | What is redaction? | Removing or hiding sensitive information | It prevents accidental data exposure. |
| 1685 | What is performance counter? | A measurement of runtime behavior | Counters expose system statistics. |
| 1686 | What is EventCounters? | Runtime metrics exposed through EventSource | They provide application measurements. |
| 1687 | What is a health metric? | A measurement indicating service condition | It helps monitor availability. |
| 1688 | What is SLI? | Service Level Indicator | It measures service performance. |
| 1689 | What is SLO? | Service Level Objective | It defines target reliability goals. |
| 1690 | What is SLA? | Service Level Agreement | It defines contractual service expectations. |
| 1691 | What is error budget? | Allowed amount of failure within an SLO | It balances reliability and feature delivery. |
| 1692 | What is chaos engineering? | Testing systems by introducing failures | It validates resilience. |
| 1693 | What is fault injection? | Deliberately creating failures for testing | It reveals weaknesses. |
| 1694 | What is production debugging? | Investigating issues in live environments | It requires safe diagnostic practices. |
| 1695 | What is crash dump? | A snapshot of process memory after failure | It helps analyze crashes. |
| 1696 | What is first chance exception? | Notification when an exception is thrown | It occurs before catch handling. |
| 1697 | What is unhandled exception? | An exception that reaches the runtime boundary | It can terminate the application. |
| 1698 | What is AppDomain? | An isolation boundary from older .NET Framework | .NET Core replaced many AppDomain scenarios with AssemblyLoadContext. |
| 1699 | What is process isolation? | Separating applications at the OS level | It provides stronger isolation than threads. |
| 1700 | What is containerization? | Packaging applications with dependencies | Containers provide consistent deployment environments. |
| 1701 | What is Docker? | A platform for building and running containers | Docker packages applications with their dependencies. |
| 1702 | What is a container image? | A read-only template used to create containers | Images contain application code and dependencies. |
| 1703 | What is a container? | A running instance of an image | Containers isolate application execution. |
| 1704 | What is a Dockerfile? | A file describing how to build an image | It defines image creation steps. |
| 1705 | What is a Docker layer? | A filesystem change stored as part of an image | Layers enable caching and smaller builds. |
| 1706 | What is a container registry? | A repository for storing container images | Registries distribute images. |
| 1707 | What is Docker Hub? | A public container image registry | It hosts and distributes images. |
| 1708 | What is Kubernetes? | A container orchestration platform | Kubernetes manages deployment and scaling. |
| 1709 | What is a Kubernetes pod? | The smallest deployable Kubernetes unit | Pods contain one or more containers. |
| 1710 | What is a Kubernetes deployment? | A resource managing application replicas | Deployments maintain desired state. |
| 1711 | What is Kubernetes service discovery? | Finding and connecting to running services | Services provide stable network access. |
| 1712 | What is Kubernetes ConfigMap? | A resource storing non-secret configuration | ConfigMaps separate configuration from images. |
| 1713 | What is Kubernetes Secret? | A resource storing sensitive values | Secrets store credentials and tokens. |
| 1714 | What is container orchestration? | Automated management of containers | It handles scheduling, scaling, and recovery. |
| 1715 | What is horizontal pod autoscaling? | Automatically adjusting pod count | It scales based on metrics. |
| 1716 | What is readiness probe? | A Kubernetes check for traffic availability | It determines whether a pod receives requests. |
| 1717 | What is liveness probe? | A Kubernetes check for application health | It determines whether a container should restart. |
| 1718 | What is startup probe? | A check for slow-starting applications | It delays other health checks during startup. |
| 1719 | What is infrastructure as code? | Managing infrastructure through configuration files | It enables repeatable deployments. |
| 1720 | What is Terraform? | An infrastructure as code tool | It manages cloud resources declaratively. |
| 1721 | What is CI/CD? | Continuous integration and continuous delivery/deployment | It automates software delivery processes. |
| 1722 | What is continuous integration? | Automatically building and testing code changes | It detects issues early. |
| 1723 | What is continuous delivery? | Keeping software ready for release | Deployment requires a manual decision. |
| 1724 | What is continuous deployment? | Automatically releasing successful changes | Production deployment is fully automated. |
| 1725 | What is a build artifact? | A generated output from a build process | Examples include binaries and packages. |
| 1726 | What is NuGet? | The package manager for .NET | It distributes reusable libraries. |
| 1727 | What is a NuGet package? | A packaged .NET library or tool | Packages include compiled code and metadata. |
| 1728 | What is a package dependency? | A library required by another package | Dependencies are resolved during restore. |
| 1729 | What is PackageReference? | The modern NuGet dependency format | It defines package dependencies in project files. |
| 1730 | What is NuGet restore? | Downloading required packages | Restore prepares dependencies before building. |
| 1731 | What is semantic versioning? | A versioning scheme using major, minor, patch numbers | It communicates compatibility changes. |
| 1732 | What does a major version change indicate? | Breaking changes | Existing consumers may require updates. |
| 1733 | What does a minor version change indicate? | Backward-compatible features | New functionality is added safely. |
| 1734 | What does a patch version change indicate? | Backward-compatible fixes | It usually contains bug fixes. |
| 1735 | What is assembly version? | Version metadata stored in an assembly | It identifies compiled binaries. |
| 1736 | What is file version? | Version information for a file | It describes the physical file version. |
| 1737 | What is informational version? | Human-readable version metadata | It can include build information. |
| 1738 | What is strong naming? | Signing assemblies with a key pair | It provides assembly identity verification. |
| 1739 | What is an assembly identity? | Name, version, culture, and public key information | It uniquely identifies an assembly. |
| 1740 | What is assembly binding? | Resolving assembly references at runtime | The CLR loads required assemblies. |
| 1741 | What is dependency conflict? | Multiple incompatible versions of a library | It can prevent successful builds or execution. |
| 1742 | What is transitive dependency? | A dependency brought in indirectly | Packages can depend on other packages. |
| 1743 | What is lock file? | A file recording resolved dependency versions | It ensures reproducible restores. |
| 1744 | What is deterministic build? | Producing identical output from identical input | It improves build reliability. |
| 1745 | What is source link? | Embedding source control information in binaries | It allows debugging original source. |
| 1746 | What is symbol file? | A file containing debugging information | It maps compiled code to source. |
| 1747 | What is portable PDB? | The modern .NET debugging symbol format | It works across platforms. |
| 1748 | What is Ahead-of-Time compilation? | Compiling code before execution | It reduces runtime compilation overhead. |
| 1749 | What is Native AOT? | Publishing .NET applications as native binaries | It improves startup time and reduces dependencies. |
| 1750 | What is ReadyToRun compilation? | Precompiling assemblies for faster startup | It reduces JIT work while retaining runtime features. |
| 1751 | What is trimming in .NET publishing? | Removing unused code from assemblies | Trimming reduces application size. |
| 1752 | What attribute preserves code during trimming? | DynamicDependencyAttribute | It informs the linker about required members. |
| 1753 | What is ILLink? | The .NET assembly trimming tool | It analyzes and removes unused code. |
| 1754 | What is single-file publishing? | Packaging an application into one executable | It simplifies deployment. |
| 1755 | What is self-contained deployment? | Publishing an app with its own runtime | The target machine does not need .NET installed. |
| 1756 | What is framework-dependent deployment? | Publishing an app requiring an installed runtime | It produces smaller outputs. |
| 1757 | What is runtime identifier (RID)? | A value identifying a target platform | RIDs select platform-specific assets. |
| 1758 | What is a RID graph? | A mapping of compatible runtime identifiers | It helps resolve platform assets. |
| 1759 | What is dotnet publish? | The command that prepares an application for deployment | It creates deployable output. |
| 1760 | What is dotnet build? | The command that compiles a project | It produces build artifacts. |
| 1761 | What is dotnet restore? | The command that resolves dependencies | It downloads NuGet packages. |
| 1762 | What is dotnet test? | The command that runs tests | It executes test projects. |
| 1763 | What is dotnet pack? | The command that creates NuGet packages | It packages libraries for distribution. |
| 1764 | What is dotnet tool? | A command-line tool distribution mechanism | It installs and runs .NET CLI tools. |
| 1765 | What is global tool? | A .NET tool installed for the user or machine | It is available across projects. |
| 1766 | What is local tool? | A .NET tool scoped to a project | Its version is tracked with the project. |
| 1767 | What is Directory.Build.props? | A shared MSBuild properties file | It applies common project settings. |
| 1768 | What is Directory.Build.targets? | A shared MSBuild targets file | It adds common build steps. |
| 1769 | What is MSBuild? | The .NET build engine | It executes project build logic. |
| 1770 | What is a target in MSBuild? | A group of build tasks | Targets define build phases. |
| 1771 | What is a task in MSBuild? | An executable build operation | Tasks perform individual build actions. |
| 1772 | What is a project file? | A file describing build configuration | SDK-style projects use .csproj files. |
| 1773 | What is SDK-style project format? | Modern simplified .NET project format | It reduces project file complexity. |
| 1774 | What is TargetFramework? | The framework version a project targets | It determines available APIs. |
| 1775 | What is TargetFrameworks? | Multiple target frameworks in one project | It enables multi-targeting. |
| 1776 | What is multi-targeting? | Building a library for multiple frameworks | It improves compatibility. |
| 1777 | What is conditional compilation symbol? | A symbol controlling compiled code paths | It enables framework-specific behavior. |
| 1778 | What is InternalsVisibleToAttribute? | Allowing another assembly to access internal members | It is commonly used for testing. |
| 1779 | What is friend assembly? | An assembly granted internal access | It uses InternalsVisibleTo. |
| 1780 | What is unit testing? | Testing individual pieces of code in isolation | It validates component behavior. |
| 1781 | What is integration testing? | Testing multiple components together | It verifies system interactions. |
| 1782 | What is end-to-end testing? | Testing complete application workflows | It simulates real user scenarios. |
| 1783 | What is test fixture? | Shared setup and state for tests | It reduces repeated initialization. |
| 1784 | What is mocking? | Replacing dependencies with controlled objects | It isolates code under test. |
| 1785 | What is a mock object? | An object simulating another dependency | It verifies interactions and behavior. |
| 1786 | What is a stub? | A simplified dependency returning predefined results | It supports controlled testing. |
| 1787 | What is fake implementation? | A working lightweight replacement | It provides realistic behavior without production complexity. |
| 1788 | What is test double? | A general term for mock, stub, or fake objects | It replaces real dependencies. |
| 1789 | What is assertion? | A statement verifying expected behavior | Assertions determine test success. |
| 1790 | What is xUnit? | A .NET testing framework | It provides modern unit testing features. |
| 1791 | What is NUnit? | A popular .NET testing framework | It supports attribute-based testing. |
| 1792 | What is MSTest? | Microsoft's testing framework | It integrates with Visual Studio. |
| 1793 | What is test discovery? | Finding tests automatically | Frameworks locate executable test methods. |
| 1794 | What is parameterized testing? | Running a test with multiple inputs | It reduces duplicated test code. |
| 1795 | What is code coverage? | Measuring executed code during tests | It shows tested areas. |
| 1796 | What is mutation testing? | Changing code to evaluate test quality | It checks whether tests detect faults. |
| 1797 | What is flaky test? | A test that sometimes passes and sometimes fails | Flaky tests reduce confidence in results. |
| 1798 | What is test isolation? | Ensuring tests do not affect each other | It improves reliability. |
| 1799 | What is Arrange-Act-Assert pattern? | A structure for organizing tests | It separates setup, execution, and verification. |
| 1800 | What is regression testing? | Testing to ensure existing behavior still works | It prevents new changes from breaking features. |
| 1801 | What is a clean architecture? | An architecture separating business rules from external concerns | It improves maintainability and testability. |
| 1802 | What are the typical layers in clean architecture? | Domain, Application, Infrastructure, Presentation | Layers separate responsibilities and dependencies. |
| 1803 | What is the dependency rule in clean architecture? | Dependencies point toward inner layers | Business logic should not depend on external details. |
| 1804 | What is the domain layer? | The layer containing core business rules | It should have minimal external dependencies. |
| 1805 | What is the application layer? | The layer coordinating business operations | It contains use cases and workflows. |
| 1806 | What is the infrastructure layer? | The layer handling external systems | It contains databases, APIs, and external services. |
| 1807 | What is the presentation layer? | The layer handling user interaction | It exposes application functionality. |
| 1808 | What is domain-driven design? | Designing software around business concepts | It focuses on domain models and language. |
| 1809 | What is an entity in DDD? | An object defined by identity over time | Entities remain distinct even with equal values. |
| 1810 | What is a value object in DDD? | An object defined only by its values | Value objects are usually immutable. |
| 1811 | What is an aggregate in DDD? | A cluster of related domain objects | Aggregates enforce consistency boundaries. |
| 1812 | What is an aggregate root? | The main entity controlling an aggregate | External access goes through the root. |
| 1813 | What is a domain event? | A record of something meaningful that happened | Domain events represent business changes. |
| 1814 | What is a repository pattern? | An abstraction for data access | It separates persistence logic from business logic. |
| 1815 | What is a unit of work pattern? | Coordinating multiple changes as one operation | It manages transactional consistency. |
| 1816 | What is CQRS? | Command Query Responsibility Segregation | It separates reading and writing models. |
| 1817 | What is a command in CQRS? | A request to change state | Commands represent actions. |
| 1818 | What is a query in CQRS? | A request to retrieve data | Queries should not modify state. |
| 1819 | What is event sourcing? | Storing state changes as events | Current state is rebuilt from history. |
| 1820 | What is an event store? | A database storing domain events | It preserves event history. |
| 1821 | What is eventual consistency in CQRS? | Read models updating after writes | It allows scalable architectures. |
| 1822 | What is a mediator pattern? | Routing requests through a central component | It reduces direct dependencies. |
| 1823 | What is MediatR? | A library implementing mediator patterns in .NET | It supports requests, notifications, and handlers. |
| 1824 | What is a command handler? | A component processing a command | It contains command execution logic. |
| 1825 | What is a notification handler? | A component reacting to events | It handles published notifications. |
| 1826 | What is pipeline behavior in MediatR? | Middleware around request handling | It enables logging, validation, and transactions. |
| 1827 | What is a specification pattern? | Encapsulating query rules into reusable objects | It improves query composition. |
| 1828 | What is an anti-corruption layer? | A boundary protecting one domain from another | It translates between models. |
| 1829 | What is bounded context? | A defined area where a domain model applies | Different contexts can have different models. |
| 1830 | What is ubiquitous language? | Shared terminology between developers and domain experts | It reduces misunderstandings. |
| 1831 | What is a monolith application? | An application deployed as one unit | All components run together. |
| 1832 | What is a modular monolith? | A monolith split into strong internal modules | It provides separation without distributed complexity. |
| 1833 | What is a distributed system? | Multiple components communicating over a network | Components operate independently. |
| 1834 | What is a service boundary? | A separation between system components | Good boundaries reduce coupling. |
| 1835 | What is an integration event? | An event shared between services | It communicates changes externally. |
| 1836 | What is message queue? | A system for asynchronous message delivery | It decouples producers and consumers. |
| 1837 | What is message broker? | Software managing message communication | It routes and stores messages. |
| 1838 | What is RabbitMQ? | A message broker using AMQP | It supports asynchronous messaging. |
| 1839 | What is Apache Kafka? | A distributed event streaming platform | It handles high-throughput event streams. |
| 1840 | What is producer in messaging? | A component sending messages | Producers publish events or commands. |
| 1841 | What is consumer in messaging? | A component receiving messages | Consumers process messages. |
| 1842 | What is message acknowledgment? | Confirmation that a message was processed | It controls delivery reliability. |
| 1843 | What is at-least-once delivery? | Messages may be delivered multiple times | Consumers must handle duplicates. |
| 1844 | What is at-most-once delivery? | Messages are delivered zero or one time | It may lose messages. |
| 1845 | What is exactly-once processing? | Processing a message only once logically | It usually requires additional mechanisms. |
| 1846 | What is idempotent message handling? | Safe processing of duplicate messages | It prevents duplicate effects. |
| 1847 | What is dead letter queue? | Storage for failed messages | It allows later investigation. |
| 1848 | What is retry queue? | A queue for messages waiting for retry | It handles temporary failures. |
| 1849 | What is saga pattern? | Managing distributed transactions through steps | It coordinates long-running operations. |
| 1850 | What is compensation action? | An action reversing a previous step | It handles failures in sagas. |
| 1851 | What is a distributed transaction? | A transaction involving multiple independent systems | It coordinates changes across boundaries. |
| 1852 | Why are distributed transactions difficult? | Networks can fail and systems have independent states | Coordination adds complexity. |
| 1853 | What is two-phase commit? | A protocol coordinating distributed commits | It ensures participants agree before committing. |
| 1854 | What is a transaction coordinator? | A component managing distributed transaction flow | It coordinates participating resources. |
| 1855 | What is CAP theorem? | A principle describing distributed system tradeoffs | It states consistency, availability, and partition tolerance cannot all be fully guaranteed. |
| 1856 | What does consistency mean in CAP theorem? | All nodes see the same data state | Reads return the latest committed value. |
| 1857 | What does availability mean in CAP theorem? | Every request receives a response | The system remains operational. |
| 1858 | What does partition tolerance mean? | The system continues despite network failures | Distributed systems must handle communication loss. |
| 1859 | What is PACELC theorem? | A model extending CAP tradeoffs | It considers latency and consistency tradeoffs. |
| 1860 | What is leader election? | Selecting a primary node in a distributed system | It coordinates certain operations. |
| 1861 | What is consensus algorithm? | A method for nodes to agree on state | It enables distributed coordination. |
| 1862 | What is Raft? | A consensus algorithm | It simplifies distributed agreement. |
| 1863 | What is quorum? | A minimum number of nodes needed for agreement | It provides fault tolerance. |
| 1864 | What is replication? | Maintaining copies of data across nodes | It improves availability. |
| 1865 | What is primary-replica replication? | One node accepts writes and others replicate data | It separates read and write workloads. |
| 1866 | What is read replica? | A copy used for read operations | It improves read scalability. |
| 1867 | What is database sharding? | Splitting data across multiple databases | It enables horizontal scaling. |
| 1868 | What is shard key? | A value determining data distribution | Good shard keys balance load. |
| 1869 | What is consistent hashing? | A hashing technique for distributed systems | It minimizes data movement when nodes change. |
| 1870 | What is cache invalidation? | Removing or updating outdated cached data | It keeps cached data accurate. |
| 1871 | What is cache-aside pattern? | Application manually loads and updates cache | It separates cache from database operations. |
| 1872 | What is write-through caching? | Writing data to cache and storage together | It keeps cache immediately updated. |
| 1873 | What is write-behind caching? | Updating storage asynchronously after cache writes | It improves write performance. |
| 1874 | What is read-through caching? | Cache automatically retrieves missing data | It hides cache retrieval logic. |
| 1875 | What is distributed cache? | A cache shared between application instances | It supports scaled deployments. |
| 1876 | What interface represents distributed cache in .NET? | IDistributedCache | It provides a common caching abstraction. |
| 1877 | What is IMemoryCache? | An in-process memory cache | It stores data inside one application instance. |
| 1878 | What is cache eviction? | Removing items from cache | It manages limited cache capacity. |
| 1879 | What is absolute expiration? | Cache expiration at a fixed time | The item expires after a duration. |
| 1880 | What is sliding expiration? | Expiration extended when accessed | Frequently used items remain cached. |
| 1881 | What is cache stampede? | Many requests rebuilding the same cache item | It can overload backend systems. |
| 1882 | What is cache warming? | Preloading cache before requests arrive | It improves initial performance. |
| 1883 | What is CDN caching? | Storing content closer to users | It reduces latency. |
| 1884 | What is ETag? | An identifier representing resource version | It supports cache validation. |
| 1885 | What is conditional request? | A request depending on resource state | It reduces unnecessary transfers. |
| 1886 | What is If-None-Match header? | A header using ETags for validation | It enables conditional GET requests. |
| 1887 | What is If-Match header? | A header requiring a matching resource version | It prevents conflicting updates. |
| 1888 | What is optimistic concurrency control? | Detecting conflicts before committing changes | It avoids locking resources. |
| 1889 | What is pessimistic concurrency control? | Locking resources during operations | It prevents simultaneous modifications. |
| 1890 | What is database locking? | Preventing conflicting database access | It controls concurrent operations. |
| 1891 | What is deadlock? | Two operations waiting on each other indefinitely | Databases detect and resolve deadlocks. |
| 1892 | What is lock escalation? | Increasing many small locks into a larger lock | It reduces lock overhead. |
| 1893 | What is isolation anomaly? | Incorrect results caused by concurrency | Isolation levels control these behaviors. |
| 1894 | What is dirty read? | Reading uncommitted data | It can return invalid values. |
| 1895 | What is non-repeatable read? | Reading different values within one transaction | Another transaction changed the data. |
| 1896 | What is phantom read? | Seeing new rows appear during a transaction | Another transaction inserted matching rows. |
| 1897 | What is snapshot isolation? | Using row versions for consistent reads | It reduces locking. |
| 1898 | What is optimistic concurrency token? | A value used to detect changes | It prevents accidental overwrites. |
| 1899 | What is database normalization? | Organizing data to reduce duplication | It improves data consistency. |
| 1900 | What is denormalization? | Adding duplication for performance reasons | It can improve read speed. |
| 1901 | What is first normal form (1NF)? | Ensuring columns contain atomic values | It removes repeating groups and multi-valued fields. |
| 1902 | What is second normal form (2NF)? | Removing partial dependency on composite keys | It requires 1NF compliance first. |
| 1903 | What is third normal form (3NF)? | Removing transitive dependencies | It reduces unnecessary data duplication. |
| 1904 | What is a primary key? | A column or set of columns uniquely identifying rows | Primary keys enforce row identity. |
| 1905 | What is a foreign key? | A reference to another table's primary key | Foreign keys enforce relationships. |
| 1906 | What is a candidate key? | A possible unique identifier for rows | One candidate key becomes the primary key. |
| 1907 | What is a composite key? | A key made of multiple columns | It identifies rows using combined values. |
| 1908 | What is a surrogate key? | An artificial identifier generated for rows | It avoids dependence on business values. |
| 1909 | What is an index? | A structure improving data lookup speed | Indexes reduce query search time. |
| 1910 | What is clustered index? | An index determining physical row order | A table usually has one clustered index. |
| 1911 | What is non-clustered index? | An index storing references to data rows | Tables can have multiple non-clustered indexes. |
| 1912 | What is covering index? | An index containing all required query columns | It can avoid additional table lookups. |
| 1913 | What is index seek? | Directly locating matching rows through an index | It is usually efficient. |
| 1914 | What is index scan? | Reading many index entries to find results | It can be slower for large datasets. |
| 1915 | What is query execution plan? | A strategy chosen by the database engine | It describes how a query runs. |
| 1916 | What is query optimizer? | A component selecting efficient execution plans | It evaluates possible strategies. |
| 1917 | What is database statistics? | Information about data distribution | The optimizer uses statistics for decisions. |
| 1918 | What is a stored procedure? | A database-side executable routine | It encapsulates SQL logic. |
| 1919 | What is a database view? | A virtual table based on a query | Views simplify data access. |
| 1920 | What is a materialized view? | A stored result of a query | It improves expensive read operations. |
| 1921 | What is a trigger? | Code automatically executed by database events | Triggers react to changes. |
| 1922 | What is a database constraint? | A rule enforcing data validity | Constraints protect data integrity. |
| 1923 | What is a unique constraint? | Ensuring values are not duplicated | It enforces uniqueness. |
| 1924 | What is a check constraint? | Restricting allowed column values | It validates inserted data. |
| 1925 | What is a default constraint? | Providing automatic column values | It supplies missing values. |
| 1926 | What is referential integrity? | Maintaining valid relationships between tables | Foreign keys enforce it. |
| 1927 | What is cascade delete? | Automatically deleting related records | It propagates deletions through relationships. |
| 1928 | What is cascade update? | Automatically updating related keys | It maintains relationship consistency. |
| 1929 | What is database migration? | Updating schema changes over time | It tracks database evolution. |
| 1930 | What is schema drift? | Database structure differing from expected state | It can cause deployment issues. |
| 1931 | What is connection string? | Configuration describing database connection details | It contains server and authentication information. |
| 1932 | What is connection pooling in databases? | Reusing existing database connections | It improves performance. |
| 1933 | What is command timeout? | Maximum allowed database command duration | It prevents indefinitely running queries. |
| 1934 | What is parameterized query? | Query using separate parameters for values | It improves security and performance. |
| 1935 | What is prepared statement? | A precompiled parameterized SQL command | It reduces repeated parsing overhead. |
| 1936 | What is ORM? | Object-relational mapping technology | It maps objects to database records. |
| 1937 | What is impedance mismatch? | Difference between object models and relational models | ORMs address this challenge. |
| 1938 | What is lazy evaluation? | Delaying computation until required | It can improve efficiency. |
| 1939 | What is eager evaluation? | Performing computation immediately | It provides immediate results. |
| 1940 | What is materialization? | Creating objects from query results | ORMs materialize database rows. |
| 1941 | What is projection query? | Selecting specific fields into another shape | It reduces unnecessary data loading. |
| 1942 | What is anonymous type in LINQ? | A compiler-generated type without a name | It is useful for temporary projections. |
| 1943 | What is grouping in LINQ? | Combining elements by a key | It creates grouped results. |
| 1944 | What is Join in LINQ? | Combining sequences based on matching keys | It represents relational joins. |
| 1945 | What is GroupJoin in LINQ? | Joining while preserving grouped matches | It resembles a left outer join. |
| 1946 | What is SelectMany in LINQ? | Flattening nested collections | It projects multiple sequences into one. |
| 1947 | What is Aggregate in LINQ? | Combining sequence elements into one result | It performs custom accumulation. |
| 1948 | What is Zip in LINQ? | Combining elements from two sequences by position | It pairs matching indexes. |
| 1949 | What is Chunk in LINQ? | Splitting a sequence into smaller arrays | It groups elements by size. |
| 1950 | What is DistinctBy in LINQ? | Removing duplicates based on a selected key | It keeps one element per key. |
| 1951 | What is Entity Framework Core? | A modern object-relational mapper for .NET | It enables database access using .NET objects. |
| 1952 | What is DbContext in EF Core? | The main class coordinating database operations | It manages entities and database connections. |
| 1953 | What is DbSet<T>? | A representation of an entity collection in EF Core | It enables querying and saving entity types. |
| 1954 | What is change tracking in EF Core? | Monitoring entity state changes | It allows automatic updates during SaveChanges(). |
| 1955 | What are EF Core entity states? | Added, Modified, Deleted, Unchanged, Detached | States determine database operations. |
| 1956 | What is AsNoTracking()? | A query option disabling change tracking | It improves performance for read-only queries. |
| 1957 | What is EF Core migration snapshot? | A representation of the current model state | It helps generate future migrations. |
| 1958 | What is Fluent API in EF Core? | A code-based way to configure models | It provides advanced mapping control. |
| 1959 | What is data annotation in EF Core? | Attributes configuring entity behavior | It provides simple model configuration. |
| 1960 | What is model builder in EF Core? | An API for configuring entity mappings | It runs during model creation. |
| 1961 | What is owned entity type in EF Core? | An entity that belongs to another entity | It shares the owner's lifecycle. |
| 1962 | What is value conversion in EF Core? | Transforming values when storing and retrieving | It maps incompatible representations. |
| 1963 | What is shadow property in EF Core? | A property tracked without being defined in the CLR class | It exists only in the EF model. |
| 1964 | What is global query filter? | A filter automatically applied to queries | It is commonly used for soft deletes. |
| 1965 | What is soft delete? | Marking data as deleted instead of removing it | It preserves historical information. |
| 1966 | What is concurrency token in EF Core? | A value used to detect conflicting updates | It prevents accidental overwrites. |
| 1967 | What is row version column? | A database-generated concurrency value | It detects changes between updates. |
| 1968 | What exception indicates concurrency conflict in EF Core? | DbUpdateConcurrencyException | It occurs when expected updates fail. |
| 1969 | What is Include() in EF Core? | Loading related entities with a query | It performs eager loading. |
| 1970 | What is ThenInclude()? | Loading deeper related navigation properties | It extends Include chains. |
| 1971 | What is eager loading? | Loading related data with the initial query | It avoids later queries. |
| 1972 | What is lazy loading? | Loading related data when accessed | It can cause unexpected queries. |
| 1973 | What is explicit loading? | Manually loading related entities | It gives control over loading. |
| 1974 | What is N+1 query problem? | Executing many queries due to repeated loading | It can severely reduce performance. |
| 1975 | What is EF Core query translation? | Converting LINQ expressions into SQL | The provider determines supported operations. |
| 1976 | What happens when EF Core cannot translate a query? | It throws or requires client-side evaluation depending on the operation | Unsupported translations cause issues. |
| 1977 | What is compiled query in EF Core? | A cached query execution plan | It reduces repeated query compilation overhead. |
| 1978 | What is raw SQL query in EF Core? | Executing SQL directly through EF Core | It provides database-specific control. |
| 1979 | What is FromSql() in EF Core? | Executing SQL that returns entities | It integrates raw queries with EF tracking. |
| 1980 | What is ExecuteSql() in EF Core? | Executing SQL commands without returning entities | It is used for updates and commands. |
| 1981 | What is database provider in EF Core? | A component connecting EF Core to a database engine | Providers implement database-specific behavior. |
| 1982 | What is relational provider? | An EF Core provider for relational databases | It maps objects to tables. |
| 1983 | What is in-memory provider in EF Core? | A provider storing data in memory | It is mainly used for testing. |
| 1984 | What is EF Core execution strategy? | Logic for handling transient failures | It enables retry behavior. |
| 1985 | What is transaction in EF Core? | A group of database operations treated as one unit | It ensures consistency. |
| 1986 | What is BeginTransaction()? | Starting an explicit database transaction | It gives manual transaction control. |
| 1987 | What is SaveChanges transaction behavior? | Automatic transaction handling during saves | EF Core wraps multiple changes when needed. |
| 1988 | What is batching in EF Core? | Combining multiple database commands | It improves database communication efficiency. |
| 1989 | What is bulk operation? | Processing many records efficiently at once | It avoids individual operations. |
| 1990 | What is EF Core interception? | Hooking into database operations | It enables logging and customization. |
| 1991 | What is DbCommandInterceptor? | An interceptor for database commands | It monitors or modifies SQL execution. |
| 1992 | What is connection interceptor? | Intercepting database connection events | It handles connection lifecycle events. |
| 1993 | What is model caching in EF Core? | Reusing built metadata models | It improves startup performance. |
| 1994 | What is keyless entity type? | An entity without a primary key | It is used for query results and views. |
| 1995 | What is table splitting? | Mapping multiple entities to one table | It shares database rows between types. |
| 1996 | What is entity splitting? | Mapping one entity across multiple tables | It separates entity storage. |
| 1997 | What is inheritance mapping in EF Core? | Mapping class hierarchies to tables | It supports object inheritance in databases. |
| 1998 | What is TPH inheritance? | Table-per-hierarchy mapping | All types share one table. |
| 1999 | What is TPT inheritance? | Table-per-type mapping | Each type has its own table. |
| 2000 | What is TPC inheritance? | Table-per-concrete-type mapping | Each concrete type has its own table. |
| 2001 | What is a database provider abstraction in EF Core? | A layer allowing EF Core to work with different databases | Providers translate operations for specific database engines. |
| 2002 | What is LINQ provider? | A component translating LINQ expressions into another language | EF Core uses one to generate SQL. |
| 2003 | What is expression tree translation? | Converting expression structures into executable queries | It enables database-side execution. |
| 2004 | What is client-side evaluation? | Executing query logic in application memory | It can cause performance problems. |
| 2005 | What is server-side evaluation? | Executing query logic in the database | It reduces data transfer. |
| 2006 | What is query projection in EF Core? | Selecting specific fields instead of full entities | It improves query efficiency. |
| 2007 | What is split query in EF Core? | Loading related data using multiple SQL queries | It avoids large join results. |
| 2008 | What is single query mode in EF Core? | Loading related data through one SQL query | It may produce large result sets. |
| 2009 | What is Cartesian explosion? | Excessive duplicated rows from multiple joins | Split queries can reduce this issue. |
| 2010 | What is query tracking behavior? | How EF Core monitors returned entities | It affects performance and updates. |
| 2011 | What is QueryTrackingBehavior.NoTracking? | A setting disabling tracking by default | It optimizes read-only workloads. |
| 2012 | What is EF Core compiled model? | A pre-generated model representation | It improves startup performance. |
| 2013 | What is design-time DbContext creation? | Creating DbContext during tooling operations | Migrations require it. |
| 2014 | What is IDesignTimeDbContextFactory? | An interface for creating DbContext during design time | It supports migration tooling. |
| 2015 | What is migration rollback? | Reverting database schema changes | It moves the database to an earlier migration. |
| 2016 | What is migration bundle? | A deployable executable applying migrations | It simplifies production updates. |
| 2017 | What is database seeding? | Adding initial data automatically | It prepares required records. |
| 2018 | What is model seeding in EF Core? | Defining initial data through model configuration | It is applied during migrations. |
| 2019 | What is connection resiliency? | Handling temporary database failures | It improves reliability. |
| 2020 | What is transient fault? | A temporary failure likely to succeed later | Retries can handle it. |
| 2021 | What is Polly? | A .NET resilience library | It provides retries, circuit breakers, and policies. |
| 2022 | What is retry policy? | A strategy for repeating failed operations | It handles temporary failures. |
| 2023 | What is exponential backoff? | Increasing retry delays after failures | It prevents overwhelming services. |
| 2024 | What is jitter in retries? | Random delay added to retry timing | It prevents synchronized retries. |
| 2025 | What is circuit breaker pattern? | Temporarily stopping calls after repeated failures | It prevents cascading failures. |
| 2026 | What are circuit breaker states? | Closed, Open, Half-Open | They control request flow. |
| 2027 | What does closed circuit state mean? | Requests flow normally | Failures are monitored. |
| 2028 | What does open circuit state mean? | Requests are blocked temporarily | The failing service is given recovery time. |
| 2029 | What does half-open circuit state mean? | Testing whether recovery occurred | Limited requests are allowed. |
| 2030 | What is timeout policy? | Limiting operation execution duration | It prevents long waits. |
| 2031 | What is bulkhead pattern? | Isolating resources between workloads | It prevents one failure from consuming everything. |
| 2032 | What is fallback policy? | Providing alternative behavior after failure | It improves user experience. |
| 2033 | What is rate limiting? | Restricting request frequency | It protects resources. |
| 2034 | What is token bucket algorithm? | A rate limiting algorithm using tokens | It allows controlled bursts. |
| 2035 | What is leaky bucket algorithm? | A rate limiting algorithm with fixed output flow | It smooths traffic. |
| 2036 | What is concurrency limiter? | Restricting simultaneous operations | It protects system capacity. |
| 2037 | What is ASP.NET Core middleware? | A component in the HTTP request pipeline | Middleware processes requests and responses. |
| 2038 | What is request pipeline? | The sequence of middleware execution | Requests pass through each component. |
| 2039 | What method adds middleware? | Use() | It registers custom pipeline components. |
| 2040 | What method adds terminal middleware? | Run() | It ends request processing. |
| 2041 | What method maps endpoints? | Map() | It connects routes to handlers. |
| 2042 | What is middleware ordering importance? | Middleware executes in registration order | Incorrect order changes behavior. |
| 2043 | What is endpoint routing? | Routing based on endpoint metadata | It separates route matching from execution. |
| 2044 | What is RoutePattern? | A representation of a route template | It defines matching rules. |
| 2045 | What is route constraint? | A restriction on route parameters | It controls valid matches. |
| 2046 | What is minimal API? | A lightweight ASP.NET Core API style | It reduces boilerplate. |
| 2047 | What is endpoint metadata? | Information attached to endpoints | Middleware can inspect endpoint behavior. |
| 2048 | What is authorization middleware? | Middleware enforcing access rules | It checks user permissions. |
| 2049 | What is authentication middleware? | Middleware identifying users | It creates user identities. |
| 2050 | What is claims-based identity? | Identity represented through claims | Claims describe user information and permissions. |
| 2051 | What is a claim in ASP.NET Core? | A piece of information about an authenticated user | Claims represent identity data such as roles or permissions. |
| 2052 | What is ClaimsPrincipal? | An object representing the current user | It contains one or more identities. |
| 2053 | What is ClaimsIdentity? | A collection of claims from one authentication source | It represents an authentication identity. |
| 2054 | What is authentication scheme? | A named mechanism used to authenticate requests | Schemes define how identities are created. |
| 2055 | What is authorization policy? | A set of requirements controlling access | Policies determine whether access is allowed. |
| 2056 | What is policy-based authorization? | Authorization using named policies | It separates access rules from controllers. |
| 2057 | What is role-based authorization? | Authorization using user roles | Roles group permissions. |
| 2058 | What is resource-based authorization? | Authorization depending on the specific object being accessed | It evaluates the resource and user together. |
| 2059 | What is IAuthorizationHandler? | A component evaluating authorization requirements | It implements custom authorization logic. |
| 2060 | What is AuthorizationHandler<TRequirement>? | A base class for custom authorization handlers | It simplifies requirement handling. |
| 2061 | What is an authorization requirement? | A rule that must be satisfied | Requirements are evaluated by handlers. |
| 2062 | What is JWT? | A signed token format for transmitting claims | It is commonly used for API authentication. |
| 2063 | What are JWT parts? | Header, payload, and signature | Each part has a specific purpose. |
| 2064 | What is JWT header? | Metadata describing the token | It contains algorithm information. |
| 2065 | What is JWT payload? | The section containing claims | It stores identity information. |
| 2066 | What is JWT signature? | A cryptographic verification value | It proves token integrity. |
| 2067 | What is token validation? | Checking whether a token is trustworthy | It verifies issuer, audience, and signature. |
| 2068 | What is token expiration? | The time after which a token is invalid | It limits token lifetime. |
| 2069 | What is refresh token? | A token used to obtain new access tokens | It avoids frequent reauthentication. |
| 2070 | What is OAuth 2.0? | An authorization framework | It enables delegated access. |
| 2071 | What is OpenID Connect? | An identity layer built on OAuth 2.0 | It provides authentication capabilities. |
| 2072 | What is access token? | A credential used to access protected resources | APIs validate it before allowing access. |
| 2073 | What is bearer token? | A token presented directly for authorization | Whoever possesses it can use it. |
| 2074 | What is HTTPS? | HTTP over TLS encryption | It protects data in transit. |
| 2075 | What is TLS handshake? | The process establishing encrypted communication | It negotiates encryption parameters. |
| 2076 | What is certificate authority? | An entity issuing trusted certificates | Browsers and systems validate certificates. |
| 2077 | What is X.509 certificate? | A digital certificate format | It contains identity and public key information. |
| 2078 | What is public key cryptography? | Cryptography using public and private key pairs | It enables encryption and signatures. |
| 2079 | What is symmetric encryption? | Encryption using the same key for encryption and decryption | It is efficient for large data. |
| 2080 | What is asymmetric encryption? | Encryption using separate public and private keys | It enables secure key exchange. |
| 2081 | What is hashing? | A one-way transformation into a fixed-size value | It verifies data integrity. |
| 2082 | What is salt in password hashing? | Random data added before hashing | It prevents identical passwords having identical hashes. |
| 2083 | What is key derivation function? | A function generating cryptographic keys from input data | It strengthens password security. |
| 2084 | What is PBKDF2? | A password-based key derivation algorithm | It slows brute-force attacks. |
| 2085 | What is bcrypt? | A password hashing algorithm | It includes adaptive cost factors. |
| 2086 | What is Argon2? | A modern password hashing algorithm | It is designed to resist hardware attacks. |
| 2087 | What is CSRF? | Cross-Site Request Forgery | It tricks authenticated users into unwanted actions. |
| 2088 | What is XSS? | Cross-Site Scripting | It injects malicious scripts into web content. |
| 2089 | What is SQL injection? | Injecting malicious SQL through input | Parameterized queries prevent it. |
| 2090 | What is input validation? | Checking user input before processing | It improves security and reliability. |
| 2091 | What is output encoding? | Escaping output before displaying it | It prevents script execution. |
| 2092 | What is security header? | An HTTP header improving browser security | Examples include CSP and HSTS. |
| 2093 | What is Content Security Policy? | A browser security policy controlling allowed resources | It reduces XSS risks. |
| 2094 | What is HSTS? | HTTP Strict Transport Security | It forces HTTPS connections. |
| 2095 | What is SameSite cookie attribute? | A cookie setting controlling cross-site sending | It helps mitigate CSRF. |
| 2096 | What is secure cookie flag? | A flag allowing cookies only over HTTPS | It protects cookie transmission. |
| 2097 | What is HttpOnly cookie flag? | A flag preventing JavaScript cookie access | It reduces cookie theft risk. |
| 2098 | What is security principle of least privilege? | Giving only required permissions | It limits damage from misuse. |
| 2099 | What is defense in depth? | Using multiple security layers | It prevents single-point security failures. |
| 2100 | What is threat modeling? | Identifying and analyzing possible threats | It guides security decisions. |
| 2101 | What is STRIDE threat modeling? | A framework for identifying security threats | It categorizes threats into spoofing, tampering, repudiation, information disclosure, denial of service, and elevation of privilege. |
| 2102 | What is spoofing? | Pretending to be another identity | Authentication mechanisms prevent spoofing. |
| 2103 | What is tampering? | Unauthorized modification of data | Integrity checks help detect tampering. |
| 2104 | What is repudiation? | Denying an action occurred | Audit logs help prevent repudiation. |
| 2105 | What is information disclosure? | Exposing data to unauthorized parties | Encryption and access control reduce this risk. |
| 2106 | What is denial of service? | Making a system unavailable | Rate limiting helps mitigate attacks. |
| 2107 | What is elevation of privilege? | Gaining permissions beyond authorization | Proper authorization prevents it. |
| 2108 | What is secure coding? | Writing software resistant to vulnerabilities | It applies security practices throughout development. |
| 2109 | What is OWASP Top 10? | A list of common web application risks | It guides application security efforts. |
| 2110 | What is dependency scanning? | Checking libraries for known vulnerabilities | It identifies insecure packages. |
| 2111 | What is static application security testing (SAST)? | Analyzing source code for vulnerabilities | It finds issues before execution. |
| 2112 | What is dynamic application security testing (DAST)? | Testing running applications for vulnerabilities | It detects runtime security issues. |
| 2113 | What is software composition analysis? | Analyzing third-party dependencies | It identifies vulnerable components. |
| 2114 | What is secret management? | Secure handling of credentials and keys | It prevents accidental exposure. |
| 2115 | What is managed identity? | An identity provided by a cloud platform | It removes the need to store credentials. |
| 2116 | What is environment variable secret storage? | Storing secrets outside source code | It separates configuration from code. |
| 2117 | What is key vault? | A secure service for storing secrets and keys | It centralizes secret management. |
| 2118 | What is dependency injection security benefit? | It reduces hard-coded dependencies | It improves maintainability and testability. |
| 2119 | What is serialization security risk? | Executing unsafe behavior during object reconstruction | Untrusted serialized data must be handled carefully. |
| 2120 | What is deserialization attack? | Exploiting unsafe object reconstruction | It can lead to code execution. |
| 2121 | What is allow-list validation? | Accepting only known valid values | It is safer than blocking known bad values. |
| 2122 | What is deny-list validation? | Blocking known invalid values | It can miss new attack patterns. |
| 2123 | What is fuzz testing? | Providing unexpected inputs to find bugs | It discovers reliability and security issues. |
| 2124 | What is property-based testing? | Testing general rules across generated inputs | It explores broader input spaces. |
| 2125 | What is randomized testing? | Testing with automatically generated values | It can uncover edge cases. |
| 2126 | What is boundary testing? | Testing values at limits of allowed ranges | It finds edge-case failures. |
| 2127 | What is equivalence partitioning? | Dividing inputs into groups with similar behavior | It reduces test cases while maintaining coverage. |
| 2128 | What is defensive programming? | Writing code that handles unexpected situations | It improves reliability. |
| 2129 | What is guard clause? | An early validation check | It simplifies control flow. |
| 2130 | What is fail-fast principle? | Detecting invalid states immediately | It prevents hidden errors. |
| 2131 | What is exception filter? | Logic determining whether an exception handler applies | It runs before catch blocks. |
| 2132 | What keyword defines exception filters? | when | It adds conditions to catch statements. |
| 2133 | What is global exception handling? | Centralized processing of unhandled errors | It provides consistent error responses. |
| 2134 | What is ExceptionHandler middleware? | Middleware for handling application exceptions | It provides centralized error processing. |
| 2135 | What is ProblemDetails? | A standardized HTTP error response format | It improves API error consistency. |
| 2136 | What is RFC 7807? | A standard describing HTTP problem details | It defines machine-readable error responses. |
| 2137 | What is status code 400? | Bad Request | The server cannot process invalid input. |
| 2138 | What is status code 401? | Unauthorized | Authentication is required or failed. |
| 2139 | What is status code 403? | Forbidden | The user is authenticated but not allowed. |
| 2140 | What is status code 404? | Not Found | The requested resource does not exist. |
| 2141 | What is status code 409? | Conflict | The request conflicts with current state. |
| 2142 | What is status code 429? | Too Many Requests | The client exceeded rate limits. |
| 2143 | What is status code 500? | Internal Server Error | The server encountered an unexpected failure. |
| 2144 | What is status code 502? | Bad Gateway | A gateway received an invalid upstream response. |
| 2145 | What is status code 503? | Service Unavailable | The service cannot currently handle requests. |
| 2146 | What is status code 504? | Gateway Timeout | An upstream service took too long to respond. |
| 2147 | What is REST constraint of statelessness? | Each request contains all required information | Servers do not store client session state. |
| 2148 | What is REST resource? | An identifiable object exposed through an API | Resources are accessed through URLs. |
| 2149 | What is idempotent HTTP method? | A method producing the same result when repeated | PUT and DELETE are commonly idempotent. |
| 2150 | What is safe HTTP method? | A method that does not modify server state | GET and HEAD are safe methods. |
| 2151 | What is HTTP middleware short-circuiting? | Ending request processing before reaching later middleware | It prevents unnecessary pipeline execution. |
| 2152 | What is request delegate in ASP.NET Core? | A function processing an HTTP request | Middleware uses delegates to handle requests. |
| 2153 | What is IMiddleware interface? | An interface for class-based middleware | It enables dependency injection in middleware. |
| 2154 | What is middleware activation? | Creating middleware instances for requests | It determines middleware lifetime behavior. |
| 2155 | What is endpoint filter in minimal APIs? | A component running around endpoint execution | It adds reusable endpoint logic. |
| 2156 | What is IEndpointFilter? | Interface for minimal API endpoint filters | It allows request and response interception. |
| 2157 | What is model binding? | Mapping HTTP data to .NET objects | It converts request data into action parameters. |
| 2158 | What is model validation? | Checking whether bound models satisfy rules | It prevents invalid data processing. |
| 2159 | What attribute marks a required property? | RequiredAttribute | It ensures a value must be supplied. |
| 2160 | What is DataAnnotations validation? | Attribute-based validation system | It provides declarative validation rules. |
| 2161 | What is IValidatableObject? | An interface for custom model validation | It allows object-level validation logic. |
| 2162 | What is custom validation attribute? | A user-defined validation rule | It extends DataAnnotations. |
| 2163 | What is binding source? | Where model binding obtains values from | Sources include route, query, body, and headers. |
| 2164 | What attribute binds from request body? | FromBodyAttribute | It deserializes request content. |
| 2165 | What attribute binds from route values? | FromRouteAttribute | It uses URL route parameters. |
| 2166 | What attribute binds from query string? | FromQueryAttribute | It uses query parameters. |
| 2167 | What attribute binds from HTTP headers? | FromHeaderAttribute | It reads request headers. |
| 2168 | What is ApiController attribute behavior? | Automatic API-specific conventions | It enables automatic validation and binding behavior. |
| 2169 | What is automatic 400 response behavior? | Returning validation errors automatically | ApiController enables this behavior. |
| 2170 | What is action filter? | Code executed before or after controller actions | It adds cross-cutting behavior. |
| 2171 | What is authorization filter? | A filter running authorization checks | It runs early in the pipeline. |
| 2172 | What is resource filter? | A filter surrounding model binding and execution | It can optimize request handling. |
| 2173 | What is exception filter? | A filter handling MVC exceptions | It processes controller exceptions. |
| 2174 | What is result filter? | A filter around action result execution | It modifies response processing. |
| 2175 | What is filter order? | The sequence filters execute | Ordering affects behavior. |
| 2176 | What is controller action? | A method handling an HTTP request | It returns an action result. |
| 2177 | What is IActionResult? | An abstraction representing an HTTP response | Controllers can return different results. |
| 2178 | What is ActionResult<T>? | A strongly typed action response wrapper | It supports typed results and HTTP responses. |
| 2179 | What is OkObjectResult? | An HTTP 200 response containing data | It returns successful results. |
| 2180 | What is CreatedAtActionResult? | A response indicating resource creation | It returns HTTP 201 with a location. |
| 2181 | What is NoContentResult? | An HTTP 204 response | It indicates success without content. |
| 2182 | What is BadRequestResult? | An HTTP 400 response | It indicates invalid client input. |
| 2183 | What is UnauthorizedResult? | An HTTP 401 response | It indicates missing or invalid authentication. |
| 2184 | What is ForbidResult? | An HTTP 403 response | It indicates insufficient permissions. |
| 2185 | What is NotFoundResult? | An HTTP 404 response | It indicates a missing resource. |
| 2186 | What is ContentResult? | A response containing custom content | It controls response text and type. |
| 2187 | What is FileResult? | A response returning file content | It sends files to clients. |
| 2188 | What is streaming response? | Sending data progressively instead of all at once | It reduces memory usage. |
| 2189 | What is response compression? | Compressing HTTP responses | It reduces network transfer size. |
| 2190 | What is ResponseCompressionMiddleware? | Middleware enabling compressed responses | It supports formats like gzip and Brotli. |
| 2191 | What is Brotli compression? | A modern compression algorithm | It often provides good web compression ratios. |
| 2192 | What is gzip compression? | A widely supported compression format | It reduces HTTP payload size. |
| 2193 | What is HTTP/2? | A newer HTTP protocol version | It supports multiplexing and header compression. |
| 2194 | What is HTTP/3? | HTTP over QUIC | It improves performance over modern networks. |
| 2195 | What is QUIC? | A transport protocol built on UDP | It provides secure low-latency communication. |
| 2196 | What is HTTP/2 multiplexing? | Multiple requests sharing one connection | It reduces connection overhead. |
| 2197 | What is HPACK? | Header compression for HTTP/2 | It reduces header transmission size. |
| 2198 | What is QPACK? | Header compression for HTTP/3 | It adapts compression for QUIC. |
| 2199 | What is gRPC streaming? | Continuous data exchange through gRPC | It supports client, server, and bidirectional streams. |
| 2200 | What is protobuf? | A binary serialization format used by gRPC | It provides efficient message encoding. |
| 2201 | What is a protobuf message? | A structured data definition used for serialization | It defines fields and their types. |
| 2202 | What is a protobuf field number? | A unique identifier assigned to a field | It preserves compatibility between versions. |
| 2203 | What is protobuf backward compatibility? | Ability for newer code to read older messages | Field numbers must remain stable. |
| 2204 | What is protobuf schema evolution? | Changing message definitions over time | It requires careful field management. |
| 2205 | What is gRPC service contract? | A definition of available remote procedures | It is described using protobuf files. |
| 2206 | What is .proto file? | A file defining protobuf messages and services | It generates client and server code. |
| 2207 | What is gRPC stub? | Generated client or server communication code | It hides network details. |
| 2208 | What is unary gRPC call? | A single request and single response call | It resembles traditional RPC. |
| 2209 | What is server streaming gRPC? | A call where the server sends multiple responses | It supports continuous data delivery. |
| 2210 | What is client streaming gRPC? | A call where the client sends multiple requests | The server responds after receiving data. |
| 2211 | What is bidirectional streaming gRPC? | Both sides can stream messages independently | It enables real-time communication. |
| 2212 | What is gRPC deadline? | The maximum allowed duration for an RPC call | It prevents indefinite waiting. |
| 2213 | What is gRPC cancellation? | Stopping an ongoing RPC operation | It releases resources early. |
| 2214 | What is gRPC interceptor? | Middleware for gRPC calls | It adds cross-cutting behavior. |
| 2215 | What is gRPC metadata? | Key-value information attached to RPC calls | It carries headers and context. |
| 2216 | What is gRPC status code? | A standardized result code for RPC operations | It communicates success or failure. |
| 2217 | What is SignalR? | A .NET library for real-time communication | It enables server-to-client messaging. |
| 2218 | What is a SignalR hub? | A high-level communication abstraction | Clients call hub methods. |
| 2219 | What is SignalR connection? | A communication link between client and server | It enables real-time updates. |
| 2220 | What is SignalR transport fallback? | Switching between available communication methods | It improves compatibility. |
| 2221 | What transports does SignalR support? | WebSockets, Server-Sent Events, and Long Polling | It selects the best available option. |
| 2222 | What is WebSocket? | A full-duplex communication protocol | It enables persistent client-server communication. |
| 2223 | What is long polling? | A technique where requests remain open for updates | It simulates real-time communication. |
| 2224 | What is server-sent events? | A one-way server-to-client streaming mechanism | It uses HTTP connections. |
| 2225 | What is real-time application? | An application providing immediate updates | Examples include chats and dashboards. |
| 2226 | What is background service in .NET? | A long-running hosted process | It runs independently of HTTP requests. |
| 2227 | What is BackgroundService? | A base class for hosted background tasks | It simplifies worker creation. |
| 2228 | What is IHostedService? | An interface for managed background services | The host controls its lifecycle. |
| 2229 | What is hosted service lifecycle? | Starting and stopping managed background work | It follows application lifetime. |
| 2230 | What is ExecuteAsync()? | The main method for BackgroundService work | It runs the background operation. |
| 2231 | What is Worker Service template? | A .NET project template for background processes | It is used for long-running services. |
| 2232 | What is cancellation token in background services? | A signal requesting shutdown | It enables graceful stopping. |
| 2233 | What is graceful shutdown? | Stopping an application while completing active work | It avoids data loss. |
| 2234 | What is hosted service scope problem? | Incorrectly using scoped dependencies in singleton services | A scope must be created manually. |
| 2235 | What is IServiceScopeFactory? | A service for creating dependency injection scopes | It resolves scoped services in long-lived objects. |
| 2236 | What is a timer-based background service? | A service running work at intervals | Timers schedule repeated execution. |
| 2237 | What is Channel<T>? | A thread-safe producer-consumer data structure | It supports asynchronous pipelines. |
| 2238 | What namespace contains Channel<T>? | System.Threading.Channels | It provides async communication primitives. |
| 2239 | What is producer-consumer pattern? | Separating data creation from data processing | Channels commonly implement it. |
| 2240 | What is bounded channel? | A channel with a fixed capacity | It applies backpressure. |
| 2241 | What is unbounded channel? | A channel without a fixed capacity | It can grow until memory limits. |
| 2242 | What is channel reader? | The component consuming channel data | It receives messages. |
| 2243 | What is channel writer? | The component producing channel data | It publishes messages. |
| 2244 | What is async coordination? | Managing asynchronous operations safely | It prevents race conditions. |
| 2245 | What is SemaphoreSlim? | A lightweight async-compatible semaphore | It limits concurrent access. |
| 2246 | What is Mutex? | A synchronization primitive allowing one owner | It provides exclusive access. |
| 2247 | What is Monitor? | A locking mechanism in .NET | It synchronizes threads. |
| 2248 | What is lock keyword? | A simplified Monitor usage | It protects critical sections. |
| 2249 | What is ReaderWriterLockSlim? | A lock allowing multiple readers | It improves read-heavy concurrency. |
| 2250 | What is Interlocked class? | Atomic operation helpers | It performs thread-safe primitive updates. |
| 2251 | What is a race condition? | A bug caused by unpredictable timing between concurrent operations | Synchronization prevents inconsistent results. |
| 2252 | What is a critical section? | Code that accesses shared resources | It requires synchronization for safety. |
| 2253 | What is thread starvation? | A thread being unable to obtain required resources | Poor scheduling or locking can cause it. |
| 2254 | What is livelock? | Threads continuously reacting without making progress | Unlike deadlock, threads remain active. |
| 2255 | What is deadlock prevention? | Techniques avoiding circular resource waiting | Lock ordering is a common approach. |
| 2256 | What is lock contention? | Multiple threads competing for the same lock | It can reduce performance. |
| 2257 | What is spin lock? | A lock that repeatedly checks availability | It is useful for very short waits. |
| 2258 | What is SpinWait? | A helper for efficient spinning behavior | It balances spinning and blocking. |
| 2259 | What is volatile read? | Reading a value with memory visibility guarantees | It prevents stale reads. |
| 2260 | What is memory barrier? | A mechanism controlling memory operation ordering | It affects visibility between threads. |
| 2261 | What is Task Parallel Library (TPL)? | A framework for parallel and asynchronous programming | It simplifies task-based concurrency. |
| 2262 | What is Parallel.For()? | A parallel loop construct | It executes iterations concurrently. |
| 2263 | What is Parallel.ForEach()? | A parallel collection iteration method | It distributes work across threads. |
| 2264 | What is Parallel LINQ (PLINQ)? | A parallel version of LINQ | It executes queries using multiple cores. |
| 2265 | What is AsParallel()? | A LINQ extension enabling PLINQ | It converts a query to parallel execution. |
| 2266 | What is degree of parallelism? | The maximum number of concurrent operations | It controls parallel workload size. |
| 2267 | What is TaskScheduler? | A component deciding how tasks execute | It manages task scheduling. |
| 2268 | What is ThreadPool? | A pool of reusable worker threads | It avoids creating excessive threads. |
| 2269 | What is ThreadPool starvation? | Insufficient available worker threads | It delays task execution. |
| 2270 | What is async over sync? | Wrapping synchronous work in asynchronous APIs | It can waste thread resources. |
| 2271 | What is sync over async? | Blocking on asynchronous operations | It can cause deadlocks and thread starvation. |
| 2272 | What is GetAwaiter().GetResult()? | A synchronous wait on an async operation | It can bypass AggregateException wrapping but has risks. |
| 2273 | What is Task.Run()? | Scheduling work on the thread pool | It is useful for CPU-bound operations. |
| 2274 | What is Task.WhenAll()? | Awaiting multiple tasks together | It completes when all tasks finish. |
| 2275 | What is Task.WhenAny()? | Awaiting the first completed task | It enables racing operations. |
| 2276 | What is Task.Delay()? | An asynchronous timer operation | It does not block a thread. |
| 2277 | What is Task.Yield()? | Forcing asynchronous continuation | It allows other work to execute first. |
| 2278 | What is async state machine? | Compiler-generated structure for async methods | It manages suspension and continuation. |
| 2279 | What is AsyncTaskMethodBuilder? | A compiler helper for async Task methods | It builds asynchronous state machines. |
| 2280 | What is ValueTaskSource? | A lower-level async result provider | It enables allocation-efficient ValueTask usage. |
| 2281 | What is IValueTaskSource? | Interface representing reusable async operations | It supports advanced async performance scenarios. |
| 2282 | What is pooling in async programming? | Reusing objects to reduce allocations | It improves performance in high-throughput systems. |
| 2283 | What is object pooling? | Reusing object instances instead of allocating new ones | It reduces garbage collection pressure. |
| 2284 | What is ObjectPool<T>? | A .NET abstraction for reusable objects | It manages pooled instances. |
| 2285 | What is ArrayPool<T>.Shared? | The shared array pool instance | It provides reusable arrays. |
| 2286 | What is MemoryPool<T>? | A pool for memory blocks | It supports efficient memory reuse. |
| 2287 | What is IMemoryOwner<T>? | An owner of rented memory | It controls memory lifetime. |
| 2288 | What is ReadOnlyMemory<T>? | A heap-safe read-only memory representation | It can be stored and passed asynchronously. |
| 2289 | What is Memory<T>? | A heap-safe writable memory representation | It works across async boundaries. |
| 2290 | What is Span safety restriction? | Span cannot cross async or iterator boundaries | It is stack-only. |
| 2291 | What is stackalloc? | Allocating memory on the stack | It avoids heap allocations. |
| 2292 | What is fixed statement? | Pinning managed memory | It prevents garbage collector relocation. |
| 2293 | What is GCHandle? | A way to control garbage collector interaction | It can pin or reference managed objects. |
| 2294 | What is pinned object? | An object prevented from moving by GC | It enables native interoperability. |
| 2295 | What is unmanaged memory? | Memory outside the managed heap | It requires manual management. |
| 2296 | What is Marshal class? | API for managed-unmanaged interoperation | It converts data between representations. |
| 2297 | What is P/Invoke? | Calling native functions from managed code | It enables platform API access. |
| 2298 | What is DllImportAttribute? | Attribute declaring external native methods | It enables P/Invoke declarations. |
| 2299 | What is COM interop? | Interaction between .NET and COM components | It supports legacy component integration. |
| 2300 | What is Native AOT? | Ahead-of-time compilation producing native executables | It improves startup time and deployment scenarios. |
| 2301 | What is ahead-of-time (AOT) compilation? | Compiling code into native machine code before execution | It reduces runtime compilation overhead. |
| 2302 | What is Native AOT limitation? | Some runtime features requiring dynamic code may not work | Reflection-heavy applications may need changes. |
| 2303 | What is ReadyToRun compilation? | Precompiling assemblies to improve startup performance | It combines native code with IL. |
| 2304 | What is crossgen2? | A tool used to generate ReadyToRun images | It improves application startup. |
| 2305 | What is tiered compilation? | A runtime optimization strategy using multiple compilation levels | It balances startup speed and performance. |
| 2306 | What is Tier 0 JIT code? | Quickly generated code for fast startup | It prioritizes compilation speed. |
| 2307 | What is Tier 1 JIT code? | Optimized JIT-compiled code | It improves long-running performance. |
| 2308 | What is dynamic PGO? | Runtime-guided optimization using execution data | It improves generated machine code. |
| 2309 | What is profile-guided optimization? | Optimizing code based on usage patterns | It targets frequently executed paths. |
| 2310 | What is devirtualization? | Removing virtual dispatch when the target is known | It improves performance. |
| 2311 | What is method inlining? | Replacing a method call with its body | It reduces call overhead. |
| 2312 | What is JIT intrinsic? | A method recognized specially by the compiler | It enables optimized machine instructions. |
| 2313 | What is hardware intrinsic? | Direct access to CPU-specific instructions | It enables low-level optimizations. |
| 2314 | What namespace contains hardware intrinsics? | System.Runtime.Intrinsics | It provides CPU instruction APIs. |
| 2315 | What is SIMD? | Processing multiple data values with one instruction | It improves numerical performance. |
| 2316 | What is Vector<T>? | A SIMD-enabled generic vector type | It performs parallel operations. |
| 2317 | What is CPU cache locality? | Keeping frequently accessed data close to the processor | It improves execution speed. |
| 2318 | What is false sharing? | Threads modifying nearby memory locations causing cache contention | It reduces parallel performance. |
| 2319 | What is branch prediction? | CPU prediction of future code paths | Correct predictions improve performance. |
| 2320 | What is allocation pressure? | Frequent memory allocation causing GC activity | Reducing allocations improves throughput. |
| 2321 | What is GC latency mode? | A setting controlling garbage collector behavior | It balances throughput and pauses. |
| 2322 | What is GCLatencyMode.Interactive? | A GC mode optimized for responsive applications | It balances pauses and throughput. |
| 2323 | What is GCLatencyMode.Batch? | A GC mode optimized for throughput | It allows longer pauses. |
| 2324 | What is GCLatencyMode.LowLatency? | A mode reducing full collections temporarily | It is useful for short performance-sensitive periods. |
| 2325 | What is SustainedLowLatency mode? | A GC mode for long-running low-pause applications | It reduces large pauses during workloads. |
| 2326 | What is LOH compaction? | Compacting the Large Object Heap | It reduces fragmentation. |
| 2327 | What is GC fragmentation? | Unused gaps in managed memory | It can increase memory usage. |
| 2328 | What is pinned object heap (POH)? | A GC heap for long-lived pinned objects | It reduces fragmentation from pinned objects. |
| 2329 | What triggers garbage collection? | Memory pressure and allocation thresholds | The runtime decides when collection occurs. |
| 2330 | What is GC.TryStartNoGCRegion()? | Requesting a period without garbage collection | It supports latency-sensitive operations. |
| 2331 | What is WeakReference? | A reference that does not prevent garbage collection | It allows objects to be collected. |
| 2332 | What is ConditionalWeakTable<TKey,TValue>? | A table associating data with object lifetimes | Entries disappear when keys are collected. |
| 2333 | What is finalizer queue? | A queue containing objects needing finalization | The GC processes finalizable objects separately. |
| 2334 | What is SafeHandle? | A safer wrapper for unmanaged handles | It manages native resource cleanup. |
| 2335 | What is CriticalHandle? | A reliability-focused handle wrapper | It provides stronger cleanup guarantees. |
| 2336 | What is IDisposable pattern? | A standard pattern for releasing resources | It enables deterministic cleanup. |
| 2337 | What is Dispose(bool)? | A method pattern separating managed and unmanaged cleanup | It supports inheritance scenarios. |
| 2338 | What is finalization suppression? | Preventing a finalizer from running | GC.SuppressFinalize improves cleanup efficiency. |
| 2339 | What is using declaration? | A C# feature automatically disposing variables | It reduces disposal boilerplate. |
| 2340 | What is await using? | Asynchronous disposal syntax | It calls DisposeAsync(). |
| 2341 | What is IAsyncDisposable.DisposeAsync()? | An asynchronous cleanup method | It releases resources asynchronously. |
| 2342 | What is resource lifetime? | The period an object or resource remains valid | Correct lifetime management prevents leaks. |
| 2343 | What is transient service lifetime? | A new dependency instance per resolution | It is used for lightweight services. |
| 2344 | What is scoped service lifetime? | One instance per dependency injection scope | It is commonly used per web request. |
| 2345 | What is singleton service lifetime? | One instance for the application's lifetime | It must be thread-safe. |
| 2346 | What is captive dependency? | A longer-lived service holding a shorter-lived dependency | It can cause incorrect lifetimes. |
| 2347 | What is dependency inversion principle? | High-level modules should not depend on low-level details | Abstractions should define dependencies. |
| 2348 | What is SOLID? | Five object-oriented design principles | It improves maintainability. |
| 2349 | What is single responsibility principle? | A class should have one reason to change | It encourages focused designs. |
| 2350 | What is open/closed principle? | Software should be open for extension but closed for modification | It reduces risky changes. |
| 2351 | What is Liskov substitution principle? | Derived types must be usable wherever base types are expected | It ensures inheritance correctness. |
| 2352 | What is interface segregation principle? | Clients should not depend on unnecessary interfaces | It encourages smaller interfaces. |
| 2353 | What is dependency inversion principle benefit? | Reducing coupling between components | It improves flexibility and testing. |
| 2354 | What is coupling? | The level of dependency between components | Lower coupling improves maintainability. |
| 2355 | What is cohesion? | How closely related responsibilities within a component are | Higher cohesion improves design quality. |
| 2356 | What is abstraction? | Hiding implementation details behind contracts | It reduces complexity. |
| 2357 | What is encapsulation? | Restricting direct access to internal state | It protects object invariants. |
| 2358 | What is polymorphism? | Allowing different types to share a common interface | It enables flexible behavior. |
| 2359 | What is inheritance? | Deriving a type from another type | It enables code reuse and specialization. |
| 2360 | What is composition? | Building objects from other objects | It is often preferred over inheritance. |
| 2361 | What is dependency injection container? | A system managing object creation and dependencies | It automates dependency resolution. |
| 2362 | What is service registration? | Adding services to the dependency injection container | It defines available dependencies. |
| 2363 | What is service resolution? | Retrieving an instance from the container | It creates required objects. |
| 2364 | What is IServiceProvider? | The interface used to resolve services | It represents the service container. |
| 2365 | What is constructor injection? | Providing dependencies through constructors | It is the recommended DI approach. |
| 2366 | What is property injection? | Assigning dependencies through properties | It is less commonly preferred. |
| 2367 | What is method injection? | Passing dependencies through method parameters | It limits dependency scope. |
| 2368 | What is dependency graph? | The network of object dependencies | The container builds objects from it. |
| 2369 | What is service locator anti-pattern? | Retrieving dependencies manually from a container | It hides dependencies. |
| 2370 | What is options pattern in .NET? | A way to access configuration values through classes | It provides strongly typed settings. |
| 2371 | What is IOptions<T>? | A wrapper providing configuration options | It accesses configuration values. |
| 2372 | What is IOptionsSnapshot<T>? | Scoped options providing refreshed values | It updates between scopes. |
| 2373 | What is IOptionsMonitor<T>? | Options supporting change notifications | It observes configuration changes. |
| 2374 | What is configuration provider? | A source supplying configuration values | Examples include JSON and environment variables. |
| 2375 | What is IConfiguration? | An abstraction for application configuration | It reads hierarchical settings. |
| 2376 | What is appsettings.json? | A JSON configuration file | It stores application settings. |
| 2377 | What is appsettings.Development.json? | Environment-specific configuration file | It overrides development settings. |
| 2378 | What is configuration precedence? | The order configuration sources override each other | Later sources usually take priority. |
| 2379 | What is user secrets? | Local development secret storage | It avoids storing secrets in source code. |
| 2380 | What is environment-specific configuration? | Different settings for different deployment environments | It supports development, testing, and production differences. |
| 2381 | What is IWebHostEnvironment? | Provides hosting environment information | It exposes environment names and paths. |
| 2382 | What is IHostEnvironment? | General host environment abstraction | It works beyond web applications. |
| 2383 | What is environment name? | A value identifying the current runtime environment | It controls environment-specific behavior. |
| 2384 | What is Development environment? | An environment intended for local development | It enables developer features. |
| 2385 | What is Production environment? | The deployed application environment | It prioritizes stability and security. |
| 2386 | What is Staging environment? | A pre-production environment | It validates deployments. |
| 2387 | What is logging abstraction in .NET? | A common API for application logging | It separates logging from providers. |
| 2388 | What is ILogger<T>? | A typed logging interface | It associates logs with a category. |
| 2389 | What is logging provider? | A component writing logs to a destination | Examples include console and files. |
| 2390 | What is structured logging? | Logging data as named fields instead of formatted text | It improves searching and analysis. |
| 2391 | What is logging scope? | A context applied to multiple log entries | It adds shared metadata. |
| 2392 | What is log level Trace? | The most detailed logging level | It is used for deep diagnostics. |
| 2393 | What is log level Debug? | Detailed diagnostic logging | It is useful during development. |
| 2394 | What is log level Information? | Normal application activity logging | It records significant events. |
| 2395 | What is log level Warning? | Logging a potentially problematic situation | The application can continue. |
| 2396 | What is log level Error? | Logging a failure condition | An operation failed. |
| 2397 | What is log level Critical? | Logging a severe failure | The application may be unusable. |
| 2398 | What is OpenTelemetry? | An observability standard for telemetry data | It collects traces, metrics, and logs. |
| 2399 | What is distributed tracing? | Tracking requests across multiple services | It identifies performance bottlenecks. |
| 2400 | What is trace context propagation? | Passing trace identifiers between services | It connects distributed operations. |
| 2401 | What is an activity in .NET diagnostics? | A representation of an operation being traced | It is used for distributed tracing. |
| 2402 | What is System.Diagnostics.ActivitySource? | A factory for creating tracing activities | It integrates with OpenTelemetry. |
| 2403 | What is a span in distributed tracing? | A single operation within a trace | Spans show timing and relationships. |
| 2404 | What is a trace in observability? | A collection of spans representing a request flow | It follows work across services. |
| 2405 | What is a metric? | A numerical measurement collected over time | It describes system behavior. |
| 2406 | What is a counter metric? | A metric that only increases | It tracks totals such as requests. |
| 2407 | What is a gauge metric? | A metric representing a current value | It tracks values like memory usage. |
| 2408 | What is a histogram metric? | A metric recording value distributions | It measures latency and sizes. |
| 2409 | What is health check in ASP.NET Core? | A mechanism for reporting application health | It helps monitor availability. |
| 2410 | What is IHealthCheck? | Interface for custom health checks | It defines health evaluation logic. |
| 2411 | What is liveness check? | A check indicating whether an application is running | It detects crashed instances. |
| 2412 | What is readiness check? | A check indicating whether an application can accept traffic | It supports deployment systems. |
| 2413 | What is dependency health check? | A check verifying external dependencies | It tests databases and services. |
| 2414 | What is graceful degradation? | Continuing operation with reduced functionality | It improves resilience during failures. |
| 2415 | What is availability? | The ability of a system to provide service | It is measured by uptime. |
| 2416 | What is reliability? | The ability to operate correctly over time | It focuses on consistent behavior. |
| 2417 | What is resilience? | The ability to recover from failures | It keeps systems operational. |
| 2418 | What is scalability? | The ability to handle increasing workload | It can involve vertical or horizontal scaling. |
| 2419 | What is vertical scaling? | Increasing resources of one machine | It improves capacity of a single instance. |
| 2420 | What is horizontal scaling? | Adding more application instances | It distributes workload. |
| 2421 | What is load balancing? | Distributing traffic across multiple servers | It improves availability and performance. |
| 2422 | What is round-robin load balancing? | Sending requests sequentially to servers | It provides simple distribution. |
| 2423 | What is least-connections load balancing? | Routing traffic to the server with fewest active connections | It adapts to workload differences. |
| 2424 | What is sticky session? | Keeping a client connected to the same server | It maintains server-local state. |
| 2425 | What is stateless application design? | Designing services without stored client state | It simplifies scaling. |
| 2426 | What is containerization? | Packaging applications with dependencies | It improves deployment consistency. |
| 2427 | What is Docker image? | A template containing an application environment | Containers are created from images. |
| 2428 | What is Docker container? | A running instance of an image | It isolates application execution. |
| 2429 | What is Dockerfile? | A script describing image creation steps | It automates container builds. |
| 2430 | What is container registry? | A repository storing container images | It distributes images. |
| 2431 | What is Kubernetes? | A container orchestration platform | It manages containerized applications. |
| 2432 | What is Kubernetes pod? | The smallest deployable Kubernetes unit | It contains one or more containers. |
| 2433 | What is Kubernetes deployment? | A resource managing application replicas | It handles updates and scaling. |
| 2434 | What is Kubernetes service? | A stable network endpoint for pods | It enables service discovery. |
| 2435 | What is Kubernetes ingress? | A way to route external HTTP traffic | It exposes services. |
| 2436 | What is container orchestration? | Automated management of containers | It handles scaling and recovery. |
| 2437 | What is blue-green deployment? | Deployment strategy using two environments | It enables quick switching between versions. |
| 2438 | What is canary deployment? | Gradual release to a subset of users | It reduces deployment risk. |
| 2439 | What is rolling deployment? | Replacing instances gradually | It avoids downtime. |
| 2440 | What is CI/CD? | Continuous integration and continuous delivery | It automates software delivery. |
| 2441 | What is continuous integration? | Automatically building and testing changes | It detects issues early. |
| 2442 | What is continuous delivery? | Keeping software ready for release | Deployment requires minimal manual steps. |
| 2443 | What is continuous deployment? | Automatically releasing validated changes | It removes manual release approval. |
| 2444 | What is build pipeline? | Automated steps producing application artifacts | It compiles and tests code. |
| 2445 | What is deployment pipeline? | Automated process delivering software | It moves applications through environments. |
| 2446 | What is artifact? | A generated build output | Examples include packages and binaries. |
| 2447 | What is artifact repository? | Storage for build outputs | It manages versioned artifacts. |
| 2448 | What is semantic versioning? | A versioning scheme using major, minor, and patch numbers | It communicates compatibility changes. |
| 2449 | What is breaking change? | A change that requires consumers to modify code | It affects compatibility. |
| 2450 | What is backward compatibility? | Ability for older clients to work with newer versions | It reduces upgrade friction. |
| 2451 | What is forward compatibility? | Ability for newer clients to work with older versions | It allows gradual system upgrades. |
| 2452 | What is API versioning? | Managing multiple versions of an API contract | It supports controlled evolution. |
| 2453 | What is URL-based API versioning? | Including the version in the request path | It makes versions explicit. |
| 2454 | What is header-based API versioning? | Specifying the API version in request headers | It keeps URLs unchanged. |
| 2455 | What is query-string API versioning? | Passing the version as a query parameter | It provides simple version selection. |
| 2456 | What is content negotiation? | Selecting a response format based on request headers | It allows flexible representations. |
| 2457 | What is Accept header? | A header indicating desired response formats | Servers use it for content negotiation. |
| 2458 | What is Content-Type header? | A header describing request or response data format | It identifies the media type. |
| 2459 | What is media type? | A format identifier for transmitted data | Examples include application/json. |
| 2460 | What is JSON serialization? | Converting objects into JSON text | It enables data exchange. |
| 2461 | What is System.Text.Json? | The built-in .NET JSON serialization library | It provides high-performance JSON support. |
| 2462 | What is JsonSerializerOptions? | Configuration settings for JSON serialization | It controls serialization behavior. |
| 2463 | What is JsonConverter? | A custom serializer component | It controls conversion of specific types. |
| 2464 | What is JsonConverterFactory? | A factory creating converters dynamically | It supports generic conversion scenarios. |
| 2465 | What is JSON naming policy? | Rules controlling property name formatting | It can convert names to camelCase. |
| 2466 | What is reference handling in JSON? | Managing object reference cycles during serialization | It prevents infinite loops. |
| 2467 | What is JSON polymorphism? | Serializing derived types through base references | It requires configured type metadata. |
| 2468 | What is source generation in System.Text.Json? | Compile-time generation of serialization metadata | It improves performance and trimming support. |
| 2469 | What is Utf8JsonReader? | A high-performance JSON reader | It parses UTF-8 JSON data. |
| 2470 | What is Utf8JsonWriter? | A high-performance JSON writer | It creates JSON output efficiently. |
| 2471 | What is serialization contract? | Rules defining how objects map to serialized data | It controls data representation. |
| 2472 | What is binary serialization? | Encoding objects into binary data | It is efficient but requires compatibility considerations. |
| 2473 | What is serialization versioning? | Managing changes to serialized formats | It preserves compatibility. |
| 2474 | What is DTO? | A data transfer object | It separates transport models from domain models. |
| 2475 | What is view model? | A model designed for presentation needs | It shapes data for UI usage. |
| 2476 | What is AutoMapper? | A library for object-to-object mapping | It reduces manual mapping code. |
| 2477 | What is projection mapping? | Mapping directly during query execution | It avoids unnecessary object creation. |
| 2478 | What is anti-corruption mapping? | Translating between different domain models | It protects domain boundaries. |
| 2479 | What is API gateway? | A service acting as a single entry point | It manages routing and cross-cutting concerns. |
| 2480 | What is reverse proxy? | A server forwarding requests to backend services | It hides internal infrastructure. |
| 2481 | What is YARP? | A .NET reverse proxy toolkit | It enables custom proxy implementations. |
| 2482 | What is load balancing proxy? | A proxy distributing requests among servers | It improves availability. |
| 2483 | What is service discovery? | Finding available service instances dynamically | It supports distributed systems. |
| 2484 | What is DNS-based discovery? | Discovering services through DNS records | It provides simple service lookup. |
| 2485 | What is configuration-based discovery? | Discovering services from configuration data | It is common in simpler deployments. |
| 2486 | What is sidecar pattern? | Running helper functionality beside an application | It separates infrastructure concerns. |
| 2487 | What is service mesh? | Infrastructure managing service-to-service communication | It provides observability and control. |
| 2488 | What is Envoy proxy? | A proxy commonly used in service meshes | It manages network communication. |
| 2489 | What is mutual TLS (mTLS)? | TLS authentication between both parties | It verifies client and server identities. |
| 2490 | What is zero trust architecture? | Security model requiring verification of every access request | It assumes no implicit trust. |
| 2491 | What is identity provider? | A service managing user authentication | It issues identities and tokens. |
| 2492 | What is single sign-on (SSO)? | One authentication allowing access to multiple systems | It improves user experience. |
| 2493 | What is multi-factor authentication (MFA)? | Authentication requiring multiple verification methods | It increases account security. |
| 2494 | What is authorization server? | A server issuing access tokens | It implements OAuth flows. |
| 2495 | What is resource server? | A server hosting protected resources | It validates access tokens. |
| 2496 | What is OAuth authorization code flow? | A secure OAuth flow using an authorization code | It is commonly used for web applications. |
| 2497 | What is PKCE? | Proof Key for Code Exchange | It protects authorization code flow. |
| 2498 | What is client credentials flow? | OAuth flow for service-to-service authentication | It uses application identity. |
| 2499 | What is delegated authorization? | Allowing an application to act on behalf of a user | User permissions are delegated. |
| 2500 | What is application permission? | Permission granted directly to an application | It is used for machine-to-machine access. |
| 2501 | What is refresh token rotation? | Replacing refresh tokens after use | It reduces replay attack risk. |
| 2502 | What is token revocation? | Invalidating previously issued tokens | It prevents further token usage. |
| 2503 | What is identity federation? | Linking authentication across different identity systems | It enables external identity providers. |
| 2504 | What is SAML? | An XML-based authentication and authorization protocol | It is commonly used for enterprise SSO. |
| 2505 | What is OpenID Connect discovery document? | A document describing identity provider endpoints | Clients use it for configuration. |
| 2506 | What is JWKS endpoint? | An endpoint exposing public signing keys | It enables JWT signature validation. |
| 2507 | What is issuer claim? | A claim identifying who issued a token | Validators compare it against expected values. |
| 2508 | What is audience claim? | A claim identifying token recipients | It prevents tokens being used by wrong services. |
| 2509 | What is nonce in authentication? | A unique value preventing replay attacks | It links requests and responses securely. |
| 2510 | What is state parameter in OAuth? | A value protecting authorization requests | It helps prevent CSRF attacks. |
| 2511 | What is PKI? | Public Key Infrastructure | It manages certificates and trust relationships. |
| 2512 | What is certificate chain? | A sequence of certificates leading to a trusted root | It establishes certificate trust. |
| 2513 | What is certificate pinning? | Trusting a specific certificate or key | It reduces certain interception risks. |
| 2514 | What is key rotation? | Replacing cryptographic keys periodically | It limits exposure from compromised keys. |
| 2515 | What is cryptographic agility? | Ability to replace cryptographic algorithms easily | It supports future security requirements. |
| 2516 | What is HMAC? | A keyed hash message authentication code | It verifies message integrity and authenticity. |
| 2517 | What is AES? | A symmetric encryption algorithm | It is widely used for data encryption. |
| 2518 | What is RSA? | An asymmetric encryption algorithm | It uses public and private keys. |
| 2519 | What is elliptic curve cryptography? | Public key cryptography based on elliptic curves | It provides strong security with smaller keys. |
| 2520 | What is digital signature? | A cryptographic proof of authenticity and integrity | It uses private keys to sign data. |
| 2521 | What is entropy in security? | Measurement of randomness | Higher entropy improves secret strength. |
| 2522 | What is brute force attack? | Trying many possible values until success | Strong secrets resist it. |
| 2523 | What is dictionary attack? | Trying common words or leaked passwords | Password hashing helps mitigate it. |
| 2524 | What is replay attack? | Reusing captured valid data | Nonces and expiration prevent it. |
| 2525 | What is man-in-the-middle attack? | Intercepting communication between parties | Encryption and authentication prevent it. |
| 2526 | What is privilege escalation? | Gaining higher access rights than allowed | Proper authorization prevents it. |
| 2527 | What is horizontal privilege escalation? | Accessing another user's resources at the same privilege level | Authorization checks prevent it. |
| 2528 | What is vertical privilege escalation? | Gaining higher privileges | Role enforcement prevents it. |
| 2529 | What is audit logging? | Recording security-relevant actions | It supports investigation and compliance. |
| 2530 | What is immutable audit log? | A log that cannot be modified after creation | It improves trustworthiness. |
| 2531 | What is compliance logging? | Logging required for regulatory requirements | It supports audits. |
| 2532 | What is data masking? | Hiding sensitive data values | It protects information exposure. |
| 2533 | What is tokenization? | Replacing sensitive data with non-sensitive tokens | It reduces exposure of original data. |
| 2534 | What is data classification? | Categorizing data based on sensitivity | It guides protection requirements. |
| 2535 | What is personally identifiable information (PII)? | Data that can identify an individual | It requires protection. |
| 2536 | What is encryption at rest? | Encrypting stored data | It protects databases and files. |
| 2537 | What is encryption in transit? | Encrypting data during communication | TLS provides this protection. |
| 2538 | What is secure deletion? | Permanently removing data | It prevents recovery. |
| 2539 | What is data retention policy? | Rules defining how long data is stored | It supports compliance and storage control. |
| 2540 | What is backup strategy? | A plan for protecting data copies | It enables recovery. |
| 2541 | What is recovery point objective (RPO)? | Maximum acceptable data loss period | It defines backup frequency requirements. |
| 2542 | What is recovery time objective (RTO)? | Maximum acceptable downtime period | It defines restoration speed requirements. |
| 2543 | What is disaster recovery plan? | A plan for restoring systems after major failures | It maintains business continuity. |
| 2544 | What is business continuity plan? | A plan for continuing operations during disruption | It covers broader organizational recovery. |
| 2545 | What is chaos engineering? | Testing resilience by intentionally causing failures | It discovers weaknesses proactively. |
| 2546 | What is fault injection? | Introducing controlled failures into systems | It tests recovery behavior. |
| 2547 | What is game day exercise? | A planned resilience testing event | Teams practice incident response. |
| 2548 | What is incident response? | The process of handling security or operational incidents | It limits damage and restores service. |
| 2549 | What is root cause analysis? | Finding the underlying reason for a failure | It prevents repeated incidents. |
| 2550 | What is postmortem analysis? | Reviewing an incident after resolution | It identifies improvements. |
| 2551 | What is a memory leak? | Memory that is no longer needed but remains referenced | It increases application memory usage. |
| 2552 | What is resource leak? | Failure to release resources such as handles or connections | It can degrade system reliability. |
| 2553 | What is handle leak? | Excessive unreleased operating system handles | It can exhaust system resources. |
| 2554 | What is connection leak? | Database connections not returned to the pool | It can prevent new connections. |
| 2555 | What is socket exhaustion? | Running out of available network sockets | Improper HTTP client usage can cause it. |
| 2556 | What is HttpClientFactory? | A factory for creating managed HttpClient instances | It handles connection lifetime correctly. |
| 2557 | What is typed HttpClient? | A strongly typed wrapper around HttpClient | It organizes API communication. |
| 2558 | What is named HttpClient? | An HttpClient configured with a specific name | It allows multiple configurations. |
| 2559 | What is delegating handler? | A component processing HttpClient requests and responses | It adds middleware-like behavior. |
| 2560 | What is HttpMessageHandler? | The component responsible for sending HTTP requests | HttpClient uses handlers internally. |
| 2561 | What is SocketsHttpHandler? | The default HTTP handler in modern .NET | It manages connections efficiently. |
| 2562 | What is connection pooling in HttpClient? | Reusing TCP connections for requests | It improves network performance. |
| 2563 | What is DNS refresh issue in HttpClient? | Stale DNS resolution due to long-lived connections | Handler lifetime management addresses it. |
| 2564 | What is HTTP retry? | Repeating failed HTTP operations | It should only be used for suitable failures. |
| 2565 | What HTTP failures are usually retryable? | Temporary failures such as 5xx responses | Permanent client errors usually should not retry. |
| 2566 | What is idempotency key? | A unique value preventing duplicate request effects | It supports safe retries. |
| 2567 | What is API throttling? | Limiting API usage rates | It protects services from overload. |
| 2568 | What is API quota? | A maximum allowed usage amount | It controls resource consumption. |
| 2569 | What is pagination? | Splitting large result sets into smaller pages | It improves API efficiency. |
| 2570 | What is offset pagination? | Pagination using skipped item counts | It is simple but can become inefficient. |
| 2571 | What is cursor pagination? | Pagination using a position marker | It performs better for large datasets. |
| 2572 | What is continuation token? | A token representing the next page position | It supports cursor-style pagination. |
| 2573 | What is filtering in APIs? | Restricting returned data based on criteria | It reduces unnecessary responses. |
| 2574 | What is sorting in APIs? | Ordering returned data by fields | It improves client control. |
| 2575 | What is field selection? | Returning only requested fields | It reduces payload size. |
| 2576 | What is HATEOAS? | Hypermedia-driven API navigation | It adds links describing available actions. |
| 2577 | What is REST maturity model? | A model describing REST API levels | It measures API design maturity. |
| 2578 | What is Richardson maturity level 0? | Using HTTP as a transport tunnel | It does not follow REST principles. |
| 2579 | What is Richardson maturity level 1? | Using resources instead of one endpoint | It introduces resource-based URLs. |
| 2580 | What is Richardson maturity level 2? | Using HTTP verbs and status codes correctly | It follows core REST practices. |
| 2581 | What is Richardson maturity level 3? | Using hypermedia controls | It represents mature REST APIs. |
| 2582 | What is API contract? | A defined agreement between client and server | It describes communication rules. |
| 2583 | What is OpenAPI? | A specification for describing HTTP APIs | It enables documentation and tooling. |
| 2584 | What is Swagger? | A set of tools based on OpenAPI | It generates API documentation and clients. |
| 2585 | What is Swagger UI? | An interactive API documentation interface | It allows testing endpoints. |
| 2586 | What is OpenAPI schema? | A machine-readable API description | It defines endpoints and models. |
| 2587 | What is API client generation? | Creating client code from an API definition | It reduces manual HTTP code. |
| 2588 | What is contract testing? | Testing that services follow agreed contracts | It prevents integration mismatches. |
| 2589 | What is consumer-driven contract testing? | Contracts defined by service consumers | It protects client expectations. |
| 2590 | What is integration boundary? | A point where systems communicate | It requires stable contracts. |
| 2591 | What is anti-corruption layer benefit? | Preventing external models from leaking internally | It preserves domain integrity. |
| 2592 | What is strangler pattern? | Gradually replacing a legacy system | New functionality replaces old components incrementally. |
| 2593 | What is legacy modernization? | Updating old systems to newer architectures | It improves maintainability and capability. |
| 2594 | What is technical debt? | Future cost caused by design shortcuts | It accumulates maintenance effort. |
| 2595 | What is refactoring? | Improving internal code structure without changing behavior | It reduces complexity. |
| 2596 | What is code smell? | A sign of possible design problems | It suggests areas for improvement. |
| 2597 | What is duplicated code smell? | Repeated logic across multiple locations | It increases maintenance cost. |
| 2598 | What is god class smell? | A class containing too many responsibilities | It violates separation of concerns. |
| 2599 | What is long method smell? | A method containing excessive logic | It reduces readability. |
| 2600 | What is feature envy smell? | A class relying heavily on another class's data | It suggests misplaced responsibility. |
| 2601 | What is clean architecture? | An architecture emphasizing separation of concerns and dependency direction | Business rules remain independent of external systems. |
| 2602 | What is hexagonal architecture? | An architecture separating application logic from external interfaces | It uses ports and adapters. |
| 2603 | What is onion architecture? | An architecture organizing code around the domain layer | Dependencies point inward. |
| 2604 | What is domain-driven design (DDD)? | An approach modeling software around business concepts | It emphasizes domain knowledge. |
| 2605 | What is bounded context? | A defined boundary where a domain model applies | It prevents model conflicts. |
| 2606 | What is entity in DDD? | An object with a unique identity over time | Identity distinguishes entities. |
| 2607 | What is value object in DDD? | An immutable object defined by its values | It has no identity. |
| 2608 | What is aggregate in DDD? | A cluster of domain objects with one consistency boundary | The aggregate root controls access. |
| 2609 | What is aggregate root? | The main entity controlling an aggregate | External code accesses the aggregate through it. |
| 2610 | What is domain event? | A record of something meaningful that happened in the domain | It communicates state changes. |
| 2611 | What is application service? | A service coordinating use cases | It connects domain logic and infrastructure. |
| 2612 | What is domain service? | A service containing domain logic without natural ownership | It represents business operations. |
| 2613 | What is repository pattern? | An abstraction for data access | It separates persistence from domain logic. |
| 2614 | What is unit of work pattern? | A pattern managing a group of database operations | It coordinates transactions. |
| 2615 | What is CQRS? | Separating read and write operations | It allows independent optimization. |
| 2616 | What is command in CQRS? | A request to change system state | Commands represent intent. |
| 2617 | What is query in CQRS? | A request to retrieve data | Queries should not modify state. |
| 2618 | What is event sourcing? | Storing state changes as events | Current state is rebuilt from history. |
| 2619 | What is snapshot in event sourcing? | A stored intermediate state | It speeds up event replay. |
| 2620 | What is eventual consistency? | Data becoming consistent over time | It is common in distributed systems. |
| 2621 | What is strong consistency? | Reads always return the latest committed value | It prioritizes correctness. |
| 2622 | What is CAP theorem? | A theorem describing trade-offs in distributed systems | Systems cannot guarantee all three properties simultaneously. |
| 2623 | What does CAP stand for? | Consistency, Availability, Partition tolerance | It describes distributed system trade-offs. |
| 2624 | What is partition tolerance? | Ability to operate despite network failures | Distributed systems must consider it. |
| 2625 | What is distributed transaction? | A transaction spanning multiple systems | It is difficult to coordinate reliably. |
| 2626 | What is two-phase commit? | A distributed transaction coordination protocol | It ensures agreement between participants. |
| 2627 | What is saga pattern? | A sequence of local transactions with compensation | It manages distributed workflows. |
| 2628 | What is compensating transaction? | An operation that reverses a previous action | It handles failures in sagas. |
| 2629 | What is message broker? | A system that routes messages between applications | It enables asynchronous communication. |
| 2630 | What is message queue? | A queue storing messages until processed | It decouples producers and consumers. |
| 2631 | What is publish-subscribe pattern? | A pattern where publishers send messages to subscribers | It supports multiple consumers. |
| 2632 | What is event bus? | A mechanism for publishing and consuming events | It decouples components. |
| 2633 | What is dead letter queue? | A queue storing failed messages | It enables investigation and recovery. |
| 2634 | What is message acknowledgment? | Confirmation that a message was processed | It controls delivery reliability. |
| 2635 | What is at-least-once delivery? | Guarantee that messages may be delivered multiple times | Consumers must handle duplicates. |
| 2636 | What is at-most-once delivery? | Guarantee that messages are delivered zero or one time | Messages may be lost. |
| 2637 | What is exactly-once processing? | Processing each message only once logically | It often requires additional design. |
| 2638 | What is idempotent consumer pattern? | Handling duplicate messages safely | It supports reliable messaging. |
| 2639 | What is outbox pattern? | Storing messages with database changes before publishing | It improves consistency. |
| 2640 | What is inbox pattern? | Tracking processed messages | It prevents duplicate processing. |
| 2641 | What is event-driven architecture? | Architecture based on events between components | It enables loose coupling. |
| 2642 | What is microservice architecture? | Architecture using independently deployable services | Services own specific capabilities. |
| 2643 | What is monolith architecture? | An application deployed as one unit | It is simpler but less independently scalable. |
| 2644 | What is modular monolith? | A monolith organized into independent modules | It combines simplicity with separation. |
| 2645 | What is service boundary? | The separation between independent services | Good boundaries reduce coupling. |
| 2646 | What is bounded service ownership? | Assigning responsibility for a service to a team | It improves accountability. |
| 2647 | What is database per service pattern? | Each service owns its database | It reduces coupling. |
| 2648 | What is shared database anti-pattern? | Multiple services directly using one database | It creates strong dependencies. |
| 2649 | What is backend-for-frontend pattern? | A backend tailored for a specific client type | It simplifies client development. |
| 2650 | What is API composition? | Combining data from multiple services | It creates aggregated responses. |
| 2651 | What is resilience policy? | A defined strategy for handling failures | It controls retries, timeouts, and fallbacks. |
| 2652 | What is Polly in .NET? | A resilience and transient-fault-handling library | It provides retry and circuit breaker patterns. |
| 2653 | What is retry policy? | A rule defining when and how operations retry | It handles temporary failures. |
| 2654 | What is exponential backoff? | Increasing delay between retries | It reduces pressure on failing systems. |
| 2655 | What is jitter in retries? | Random variation added to retry delays | It prevents synchronized retry spikes. |
| 2656 | What is timeout policy? | A rule limiting operation duration | It prevents indefinitely running operations. |
| 2657 | What is circuit breaker pattern? | A pattern that stops calls to failing dependencies | It prevents cascading failures. |
| 2658 | What is circuit breaker closed state? | Normal operation allowing requests | Failures are monitored. |
| 2659 | What is circuit breaker open state? | Blocking requests to a failing dependency | It allows recovery time. |
| 2660 | What is circuit breaker half-open state? | Testing whether a dependency recovered | Limited requests are allowed. |
| 2661 | What is fallback policy? | Returning alternative behavior after failure | It improves availability. |
| 2662 | What is bulkhead pattern? | Isolating resources between workloads | It prevents one failure from affecting everything. |
| 2663 | What is rate limiter? | A component controlling request frequency | It protects resources. |
| 2664 | What is token bucket algorithm? | A rate limiting algorithm using refillable tokens | It allows controlled bursts. |
| 2665 | What is fixed window rate limiting? | Limiting requests within fixed time periods | It is simple but has boundary effects. |
| 2666 | What is sliding window rate limiting? | Rate limiting using moving time intervals | It provides smoother control. |
| 2667 | What is concurrency limiter? | Limiting simultaneous operations | It controls active workload. |
| 2668 | What is queue-based load leveling? | Buffering work through a queue | It smooths traffic spikes. |
| 2669 | What is backpressure? | Slowing producers when consumers cannot keep up | It prevents overload. |
| 2670 | What is graceful timeout handling? | Ending operations cleanly after timeout | It releases resources properly. |
| 2671 | What is cancellation propagation? | Passing cancellation signals through operations | It enables cooperative shutdown. |
| 2672 | What is cooperative cancellation? | Components voluntarily responding to cancellation requests | .NET uses CancellationToken for this. |
| 2673 | What is CancellationTokenSource? | An object creating cancellation signals | It controls cancellation requests. |
| 2674 | What is linked CancellationTokenSource? | Combining multiple cancellation tokens | Any linked cancellation can trigger cancellation. |
| 2675 | What is cancellation callback? | Code executed when cancellation occurs | It allows cleanup actions. |
| 2676 | What is OperationCanceledException purpose? | Indicating an operation was canceled | It represents cooperative cancellation. |
| 2677 | What is ConfigureAwait behavior in ASP.NET Core? | Usually no synchronization context is captured | Continuations run efficiently. |
| 2678 | What is synchronization context? | An abstraction controlling continuation execution location | It affects async behavior. |
| 2679 | What is ExecutionContext? | Ambient context flowing across async operations | It carries security and diagnostic data. |
| 2680 | What is AsyncLocal<T>? | Storage for async-flowing local values | Values flow with ExecutionContext. |
| 2681 | What is Activity.Current? | The current tracing activity | It enables trace context propagation. |
| 2682 | What is ambient context? | Context automatically available throughout execution | It can simplify cross-cutting concerns. |
| 2683 | What is thread affinity? | Requirement that code executes on a specific thread | Some UI frameworks require it. |
| 2684 | What is continuation? | Code executed after an asynchronous operation completes | Await creates continuations. |
| 2685 | What is promise in asynchronous programming? | An object representing a future result | Task represents this concept in .NET. |
| 2686 | What is hot task? | A task that has already started execution | Many async methods return hot tasks. |
| 2687 | What is cold task? | A task representing work that has not started | Task constructors can create these. |
| 2688 | What is async void limitation? | It cannot be awaited or composed | It should mostly be used for event handlers. |
| 2689 | What is TaskCompletionSource? | A mechanism for manually controlling task completion | It bridges callback APIs and tasks. |
| 2690 | What is TaskCompletionSource.SetResult()? | Completing a task successfully | Awaiters receive the result. |
| 2691 | What is TaskCompletionSource.SetException()? | Completing a task with failure | Awaiters receive the exception. |
| 2692 | What is TaskCompletionSource.SetCanceled()? | Completing a task as canceled | Awaiters receive cancellation. |
| 2693 | What is ValueTask limitation? | It should not usually be awaited multiple times | It is optimized for single consumption. |
| 2694 | What is async enumerable? | A sequence producing values asynchronously | It uses IAsyncEnumerable<T>. |
| 2695 | What is yield return? | Returning sequence elements lazily | It creates iterators. |
| 2696 | What is yield break? | Ending iterator execution early | It stops enumeration. |
| 2697 | What is iterator state machine? | Compiler-generated code for iterator methods | It maintains enumeration state. |
| 2698 | What is deferred execution? | Delaying query execution until enumeration | LINQ commonly uses it. |
| 2699 | What is lazy evaluation? | Computing values only when needed | It avoids unnecessary work. |
| 2700 | What is Lazy<T>? | A thread-safe lazy initialization helper | It delays object creation. |
| 2701 | What is eager initialization? | Creating an object immediately instead of delaying creation | It avoids first-use initialization cost. |
| 2702 | What is lazy initialization benefit? | Avoiding unnecessary object creation | It can reduce startup and memory costs. |
| 2703 | What is LazyThreadSafetyMode.ExecutionAndPublication? | A mode ensuring only one value is created | It provides thread-safe initialization. |
| 2704 | What is LazyThreadSafetyMode.PublicationOnly? | A mode allowing multiple creations but publishing one value | It reduces locking overhead. |
| 2705 | What is immutable object? | An object whose state cannot change after creation | It improves thread safety. |
| 2706 | What is record type in C#? | A reference type designed for immutable data models | It provides value-based equality. |
| 2707 | What is record struct? | A value type record | It combines records with value semantics. |
| 2708 | What is positional record? | A record declared using constructor parameters | It generates properties automatically. |
| 2709 | What is with expression? | A syntax for creating modified copies | It is commonly used with records. |
| 2710 | What is init accessor? | A property setter usable only during initialization | It supports immutable objects. |
| 2711 | What is required member in C#? | A member that must be initialized | It improves object initialization safety. |
| 2712 | What is required keyword? | A keyword enforcing initialization requirements | It works with object creation. |
| 2713 | What is nullable reference type? | A compiler feature tracking possible null values | It reduces null reference errors. |
| 2714 | What is nullable annotation context? | Compiler mode controlling nullable analysis | It enables nullability warnings. |
| 2715 | What is null-forgiving operator? | The ! operator suppressing nullable warnings | It tells the compiler a value is not null. |
| 2716 | What is null conditional operator? | The ?. operator performing safe member access | It prevents null reference exceptions. |
| 2717 | What is null coalescing operator? | The ?? operator providing fallback values | It handles null alternatives. |
| 2718 | What is null coalescing assignment? | The ??= operator assigning only when null | It simplifies initialization. |
| 2719 | What is pattern matching declaration? | Creating a variable during a type check | It combines testing and assignment. |
| 2720 | What is property pattern? | Matching object properties in patterns | It enables structured checks. |
| 2721 | What is relational pattern? | Matching values using comparison operators | It supports ranges and comparisons. |
| 2722 | What is logical pattern? | Combining patterns with and, or, and not | It creates complex conditions. |
| 2723 | What is list pattern? | Matching elements of collections or arrays | It was introduced in newer C# versions. |
| 2724 | What is switch expression? | An expression-based form of switch | It returns values directly. |
| 2725 | What is exhaustive switch? | A switch covering all possible inputs | It prevents missing cases. |
| 2726 | What is default interface method? | An interface method with implementation | It allows interface evolution. |
| 2727 | What is interface variance? | Allowing generic interfaces to change type relationships | It improves generic flexibility. |
| 2728 | What is covariance? | Allowing more derived types where base types are expected | It applies to output values. |
| 2729 | What is contravariance? | Allowing base types where derived types are expected | It applies to input values. |
| 2730 | What is invariant generic type? | A generic type without variance conversion | Most generic classes are invariant. |
| 2731 | What is generic type constraint? | A restriction on allowed generic arguments | It improves type safety. |
| 2732 | What is where T : class constraint? | Restricting a type parameter to reference types | It excludes value types. |
| 2733 | What is where T : struct constraint? | Restricting a type parameter to value types | It excludes reference types. |
| 2734 | What is where T : new() constraint? | Requiring a public parameterless constructor | It enables object creation. |
| 2735 | What is generic type inference? | Compiler determining generic type arguments automatically | It reduces explicit type syntax. |
| 2736 | What is generic specialization? | Optimizing generic code for specific types | It can improve performance. |
| 2737 | What is boxing? | Converting a value type into an object reference | It allocates on the heap. |
| 2738 | What is unboxing? | Extracting a value type from an object | It requires the exact compatible type. |
| 2739 | What is constrained call? | A generic optimization avoiding unnecessary boxing | It improves value type performance. |
| 2740 | What is dynamic keyword? | A type resolved at runtime | It bypasses compile-time type checking. |
| 2741 | What is Dynamic Language Runtime (DLR)? | Runtime infrastructure supporting dynamic operations | It enables dynamic binding. |
| 2742 | What is reflection? | Inspecting metadata and types at runtime | It enables dynamic behavior. |
| 2743 | What is Type object? | Runtime representation of a type | It provides metadata access. |
| 2744 | What is Assembly class? | Representation of a loaded .NET assembly | It provides assembly metadata. |
| 2745 | What is AssemblyLoadContext? | A mechanism for loading assemblies into isolation contexts | It supports plugins and unloading. |
| 2746 | What is collectible AssemblyLoadContext? | An unloadable assembly loading context | It enables plugin cleanup. |
| 2747 | What is plugin architecture? | A design allowing extensions to be loaded dynamically | It improves extensibility. |
| 2748 | What is source generator? | A compiler extension generating code during compilation | It reduces runtime work. |
| 2749 | What is incremental source generator? | A source generator optimized for repeated builds | It improves compilation performance. |
| 2750 | What is analyzer in .NET? | A compiler extension detecting code issues | It improves code quality. |
| 2751 | What is Roslyn? | The .NET compiler platform | It provides APIs for code analysis and generation. |
| 2752 | What is syntax tree in Roslyn? | A structured representation of source code | Analyzers inspect syntax trees. |
| 2753 | What is semantic model in Roslyn? | Information about the meaning of code symbols | It provides type and symbol analysis. |
| 2754 | What is symbol in Roslyn? | A representation of code elements such as types and methods | It describes program structure. |
| 2755 | What is code fix provider? | A tool that automatically applies source changes | It works with analyzers. |
| 2756 | What is diagnostic in Roslyn? | A reported code issue or suggestion | Analyzers produce diagnostics. |
| 2757 | What is nullable flow analysis? | Compiler analysis tracking possible null states | It generates nullable warnings. |
| 2758 | What is definite assignment analysis? | Compiler verification that variables are initialized before use | It prevents uninitialized access. |
| 2759 | What is definite assignment? | Guarantee that a variable has a value before reading | The compiler enforces it. |
| 2760 | What is constant expression? | An expression evaluated at compile time | It can be used in constant contexts. |
| 2761 | What is const field? | A compile-time constant value | It is replaced during compilation. |
| 2762 | What is readonly field? | A field assignable only during initialization | It prevents later modification. |
| 2763 | What is static readonly field? | A readonly value shared by all instances | It is initialized once per type. |
| 2764 | What is static constructor? | A constructor that initializes static members | It runs once per type. |
| 2765 | What is type initializer? | The runtime operation executing static initialization | It initializes static state. |
| 2766 | What is partial class? | A class definition split across multiple files | The compiler combines parts. |
| 2767 | What is partial method? | A method declaration that can have a separate implementation | It supports generated code scenarios. |
| 2768 | What is extension method? | A method adding functionality to an existing type | It is syntactic sugar for static methods. |
| 2769 | What is extension block in modern C#? | A syntax for grouping extension members | It organizes extensions more clearly. |
| 2770 | What is operator overloading? | Defining custom behavior for operators | It enables natural syntax for types. |
| 2771 | What is conversion operator? | A custom type conversion definition | It controls implicit and explicit conversions. |
| 2772 | What is implicit conversion? | A conversion performed automatically by the compiler | It should not lose information. |
| 2773 | What is explicit conversion? | A conversion requiring a cast | It may involve data loss. |
| 2774 | What is checked context? | A context detecting arithmetic overflow | It throws on invalid operations. |
| 2775 | What is unchecked context? | A context allowing arithmetic overflow | It ignores overflow exceptions. |
| 2776 | What is arithmetic overflow? | A result exceeding the numeric type range | It can produce incorrect values. |
| 2777 | What is decimal type? | A high-precision decimal numeric type | It is commonly used for financial values. |
| 2778 | What is floating-point precision issue? | Loss of exactness due to binary representation | Decimal may be preferable for exact decimals. |
| 2779 | What is BigInteger? | An integer type supporting arbitrary size values | It avoids fixed integer limits. |
| 2780 | What is Half type? | A 16-bit floating-point type | It reduces storage requirements. |
| 2781 | What is DateOnly? | A date type without time information | It represents calendar dates. |
| 2782 | What is TimeOnly? | A time-of-day type without a date | It represents clock times. |
| 2783 | What is DateTimeKind? | A value describing DateTime time interpretation | It distinguishes local, UTC, and unspecified. |
| 2784 | What is DateTimeOffset? | A date and time with UTC offset | It preserves timezone information. |
| 2785 | What is TimeSpan? | A representation of a duration | It measures time intervals. |
| 2786 | What is CultureInfo? | A type providing culture-specific formatting rules | It controls localization behavior. |
| 2787 | What is invariant culture? | A culture-independent formatting standard | It is used for stable data formats. |
| 2788 | What is globalization? | Supporting different languages and cultures | It enables international applications. |
| 2789 | What is localization? | Adapting applications for specific cultures | It changes resources and formatting. |
| 2790 | What is resource file (.resx)? | A file storing localized resources | It supports multilingual applications. |
| 2791 | What is ResourceManager? | A class retrieving localized resources | It loads resources by culture. |
| 2792 | What is string interning? | Reusing identical string instances | It can reduce memory usage. |
| 2793 | What is StringBuilder? | A mutable string construction type | It avoids repeated string allocations. |
| 2794 | What is UTF-8? | A variable-length Unicode encoding | It is widely used in web systems. |
| 2795 | What is Unicode normalization? | Standardizing equivalent Unicode representations | It improves text comparison. |
| 2796 | What is grapheme cluster? | A user-perceived character unit | It may contain multiple Unicode code points. |
| 2797 | What is Rune in .NET? | A type representing a Unicode scalar value | It handles Unicode characters correctly. |
| 2798 | What is char limitation? | It represents a UTF-16 code unit, not always a full character | Some characters require surrogate pairs. |
| 2799 | What is Regex source generation? | Compile-time generation of regex implementations | It improves performance and trimming support. |
| 2800 | What is RegexOptions.Compiled? | An option compiling regex into optimized code | It improves repeated regex execution. |
| 2801 | What is RegexOptions.NonBacktracking? | A regex mode avoiding traditional backtracking | It improves predictable performance. |
| 2802 | What is catastrophic backtracking? | Excessive regex processing caused by ambiguous patterns | Better patterns or non-backtracking mode prevent it. |
| 2803 | What is regular expression timeout? | A limit on regex execution duration | It prevents denial-of-service scenarios. |
| 2804 | What is FileStream? | A stream for reading and writing files | It provides file-based I/O operations. |
| 2805 | What is Stream abstraction? | A sequence-based abstraction for reading and writing data | It supports many data sources. |
| 2806 | What is MemoryStream? | A stream backed by memory | It avoids physical file storage. |
| 2807 | What is BufferedStream? | A stream adding buffering to another stream | It reduces I/O operations. |
| 2808 | What is StreamReader? | A text reader over a stream | It converts bytes into characters. |
| 2809 | What is StreamWriter? | A text writer over a stream | It converts characters into bytes. |
| 2810 | What is BinaryReader? | A reader for primitive binary values | It reads structured binary data. |
| 2811 | What is BinaryWriter? | A writer for primitive binary values | It writes structured binary data. |
| 2812 | What is FileMode? | An option describing how a file is opened | It controls creation and access behavior. |
| 2813 | What is FileAccess? | An option describing allowed file operations | It specifies read/write permissions. |
| 2814 | What is FileShare? | An option controlling file sharing behavior | It controls access by other processes. |
| 2815 | What is async file I/O? | Non-blocking file operations | It improves scalability. |
| 2816 | What is memory-mapped file? | A file mapped directly into memory space | It enables efficient large-file access. |
| 2817 | What is pipeline in System.IO.Pipelines? | A high-performance streaming abstraction | It reduces copying during I/O processing. |
| 2818 | What is PipeReader? | A component reading from a pipeline | It consumes buffered data. |
| 2819 | What is PipeWriter? | A component writing to a pipeline | It produces buffered data. |
| 2820 | What is backpressure in pipelines? | Controlling producers when consumers are slower | It prevents memory growth. |
| 2821 | What is file watcher? | A component monitoring filesystem changes | It detects file modifications. |
| 2822 | What is FileSystemWatcher? | .NET API for monitoring file system events | It reports changes to files and directories. |
| 2823 | What is directory enumeration? | Listing files and folders | It retrieves filesystem information. |
| 2824 | What is glob pattern? | A wildcard pattern for matching file paths | It simplifies file selection. |
| 2825 | What is path normalization? | Converting paths into a standard format | It improves consistency and security. |
| 2826 | What is path traversal attack? | Accessing files outside intended directories | Input validation prevents it. |
| 2827 | What is temporary file? | A short-lived file used for intermediate data | It should be securely managed. |
| 2828 | What is memory pressure? | Increased demand for available memory | It can trigger garbage collection. |
| 2829 | What is LOH allocation threshold? | The approximate size where objects go to the Large Object Heap | Large objects have different GC behavior. |
| 2830 | What is array covariance? | Allowing arrays of derived types to be assigned to base arrays | It can cause runtime checks. |
| 2831 | What is ArrayTypeMismatchException? | Exception caused by invalid array element assignment | It occurs with array covariance. |
| 2832 | What is IndexOutOfRangeException? | Exception for invalid array or collection indexes | It indicates invalid indexing. |
| 2833 | What is ArgumentException? | Exception for invalid method arguments | It indicates incorrect input values. |
| 2834 | What is ArgumentNullException? | Exception for null arguments where not allowed | It identifies missing required values. |
| 2835 | What is InvalidOperationException? | Exception for an invalid object state | The operation is not valid currently. |
| 2836 | What is ObjectDisposedException? | Exception when using a disposed object | It indicates invalid resource usage. |
| 2837 | What is NotSupportedException? | Exception for unsupported operations | It indicates unavailable functionality. |
| 2838 | What is KeyNotFoundException? | Exception when a dictionary key does not exist | It indicates missing data. |
| 2839 | What is AggregateException? | Exception containing multiple exceptions | It is common with parallel tasks. |
| 2840 | What is exception stack trace? | Information showing where an exception occurred | It helps debugging. |
| 2841 | What is exception inner exception? | The original exception wrapped by another exception | It preserves failure details. |
| 2842 | What is exception rethrow difference between throw and throw ex? | throw preserves the original stack trace | throw ex resets stack information. |
| 2843 | What is custom exception? | A user-defined exception type | It represents specific failure cases. |
| 2844 | What is exception hierarchy? | The inheritance structure of exception types | It determines catch behavior. |
| 2845 | What is catch ordering? | Ordering exception handlers from specific to general | It ensures correct handling. |
| 2846 | What is finally block? | Code that executes after try/catch processing | It performs cleanup. |
| 2847 | What is exception filter advantage? | Avoiding unnecessary catch execution | It allows conditional handling. |
| 2848 | What is first chance exception? | Notification when an exception is initially thrown | Debuggers can observe it. |
| 2849 | What is unhandled exception? | An exception with no matching handler | It can terminate execution. |
| 2850 | What is global exception handler? | A central mechanism for processing unhandled errors | It provides consistent error handling. |
| 2851 | What is application domain? | An isolation boundary for managed code in .NET Framework | .NET Core and modern .NET use AssemblyLoadContext instead. |
| 2852 | What is managed execution? | Running code under CLR control | The runtime manages memory and execution. |
| 2853 | What is Common Language Runtime (CLR)? | The execution engine for .NET applications | It provides garbage collection, JIT compilation, and runtime services. |
| 2854 | What is Common Type System (CTS)? | A specification defining types in .NET | It enables language interoperability. |
| 2855 | What is Common Language Specification (CLS)? | A set of rules for .NET language compatibility | Languages can share public APIs. |
| 2856 | What is Intermediate Language (IL)? | CPU-independent code generated by .NET compilers | The CLR executes it after JIT compilation. |
| 2857 | What is metadata in .NET assemblies? | Information describing types and members | The runtime uses it for reflection and execution. |
| 2858 | What is assembly manifest? | Metadata describing an assembly | It contains identity and referenced assemblies. |
| 2859 | What is strong-named assembly? | An assembly signed with a cryptographic key | It provides identity verification. |
| 2860 | What is assembly version? | A value identifying an assembly release | It helps manage compatibility. |
| 2861 | What is private assembly? | An assembly used by a single application | It is deployed with the application. |
| 2862 | What is shared assembly? | An assembly available to multiple applications | Historically stored in the Global Assembly Cache. |
| 2863 | What is Global Assembly Cache (GAC)? | A machine-wide assembly repository in .NET Framework | Modern .NET generally does not use it. |
| 2864 | What is NuGet package? | A reusable .NET library package | It manages dependencies. |
| 2865 | What is NuGet package restore? | Downloading required packages for a project | It recreates dependencies. |
| 2866 | What is PackageReference? | The modern way to reference NuGet packages | It stores package dependencies in project files. |
| 2867 | What is transitive dependency? | A dependency brought by another dependency | Package managers resolve it automatically. |
| 2868 | What is dependency conflict? | Multiple incompatible versions of a package | Version management resolves conflicts. |
| 2869 | What is assembly binding? | Resolving which assembly version is loaded | It determines runtime dependencies. |
| 2870 | What is trimming? | Removing unused code during publishing | It reduces application size. |
| 2871 | What is ILLinker? | A tool performing assembly trimming | It analyzes reachable code. |
| 2872 | What is trimming warning? | A warning about code incompatible with trimming | Reflection-heavy code may require annotations. |
| 2873 | What is DynamicallyAccessedMembersAttribute? | An attribute preserving members needed by reflection | It helps trimming analysis. |
| 2874 | What is RequiresUnreferencedCodeAttribute? | An attribute marking code unsafe for trimming | It warns callers. |
| 2875 | What is single-file publishing? | Packaging an application into one executable file | It simplifies deployment. |
| 2876 | What is self-contained deployment? | Publishing an application with its runtime included | It does not require .NET installation. |
| 2877 | What is framework-dependent deployment? | Publishing an application requiring installed .NET runtime | It produces smaller output. |
| 2878 | What is runtime identifier (RID)? | Identifier for a target platform | It controls platform-specific assets. |
| 2879 | What is cross-platform .NET? | Running .NET applications on multiple operating systems | Modern .NET supports Windows, Linux, and macOS. |
| 2880 | What is .NET SDK? | Tools used to build and develop .NET applications | It includes compilers and commands. |
| 2881 | What is dotnet CLI? | Command-line interface for .NET development | It manages projects and builds. |
| 2882 | What is dotnet build? | Command compiling a .NET project | It produces build outputs. |
| 2883 | What is dotnet publish? | Command preparing an application for deployment | It creates deployable files. |
| 2884 | What is dotnet test? | Command executing automated tests | It runs test projects. |
| 2885 | What is dotnet restore? | Command restoring dependencies | It downloads required packages. |
| 2886 | What is dotnet tool? | A command-line extension for .NET | It adds developer utilities. |
| 2887 | What is global .NET tool? | A tool installed for the user or machine | It is available across projects. |
| 2888 | What is local .NET tool? | A tool scoped to a project | It provides reproducible tooling. |
| 2889 | What is Directory.Build.props? | A shared MSBuild property file | It applies settings to multiple projects. |
| 2890 | What is Directory.Build.targets? | A shared MSBuild target file | It adds custom build steps. |
| 2891 | What is MSBuild? | The .NET build engine | It executes build tasks and targets. |
| 2892 | What is MSBuild target? | A group of build operations | Targets define build phases. |
| 2893 | What is MSBuild task? | A unit of executable build work | Targets contain tasks. |
| 2894 | What is project file (.csproj)? | An XML file describing a .NET project | It defines dependencies and settings. |
| 2895 | What is SDK-style project? | Modern simplified .NET project format | It reduces project file complexity. |
| 2896 | What is implicit usings? | Automatically included common namespaces | It reduces using statements. |
| 2897 | What is global using? | A using directive applied across files | It centralizes imports. |
| 2898 | What is top-level statement? | C# syntax allowing code without explicit Main method | The compiler generates the entry point. |
| 2899 | What is Main method? | The entry point of a traditional C# application | Execution begins there. |
| 2900 | What is assembly entry point? | The method executed when an application starts | It is usually Main. |
| 2901 | What is Native AOT? | Publishing a .NET application as native machine code | It reduces startup time and runtime dependencies. |
| 2902 | What is ahead-of-time compilation? | Compiling code before execution | It avoids runtime JIT compilation. |
| 2903 | What is ReadyToRun compilation? | Precompiling assemblies with native code | It reduces startup JIT overhead. |
| 2904 | What is tiered compilation? | A JIT strategy that optimizes code over time | It balances startup speed and performance. |
| 2905 | What is tier 0 JIT code? | Quickly generated initial code | It prioritizes fast startup. |
| 2906 | What is tier 1 JIT code? | Optimized JIT compiled code | It improves long-running performance. |
| 2907 | What is profile-guided optimization (PGO)? | Optimization based on runtime execution data | It improves generated machine code. |
| 2908 | What is devirtualization? | Replacing virtual calls with direct calls when possible | It improves performance. |
| 2909 | What is method inlining? | Replacing a method call with its body | It reduces call overhead. |
| 2910 | What is dead code elimination? | Removing unreachable or unused code | It reduces generated code size. |
| 2911 | What is constant folding? | Evaluating constant expressions during compilation | It improves runtime efficiency. |
| 2912 | What is bounds check elimination? | Removing unnecessary array bounds checks | It improves performance in loops. |
| 2913 | What is escape analysis? | Determining whether objects can avoid heap allocation | It enables optimizations. |
| 2914 | What is stack allocation? | Allocating data on the stack instead of heap | It reduces garbage collection pressure. |
| 2915 | What is GC latency mode? | A setting controlling garbage collector behavior | It balances throughput and responsiveness. |
| 2916 | What is GCLatencyMode.LowLatency? | A GC mode minimizing pause times | It is used during sensitive operations. |
| 2917 | What is SustainedLowLatency mode? | A GC mode for long-running low-pause applications | It reduces blocking collections. |
| 2918 | What is NoGCRegion? | A mode temporarily preventing garbage collection | It reserves memory for critical sections. |
| 2919 | What is GC.TryStartNoGCRegion()? | API requesting a no-GC region | It attempts to reserve memory. |
| 2920 | What is GC.EndNoGCRegion()? | API ending a no-GC region | It restores normal GC behavior. |
| 2921 | What is finalizer queue? | A queue containing objects requiring finalization | The GC processes it separately. |
| 2922 | What is finalization? | Cleanup performed before object memory is reclaimed | It is slower than deterministic disposal. |
| 2923 | What is SafeHandle? | A wrapper for unmanaged handles | It provides safer resource cleanup. |
| 2924 | What is CriticalFinalizerObject? | A base class for critical finalizers | It provides stronger cleanup guarantees. |
| 2925 | What is unmanaged resource? | A resource outside CLR memory management | Examples include file handles and native memory. |
| 2926 | What is managed resource? | Memory controlled by the garbage collector | Objects on the managed heap are managed resources. |
| 2927 | What is IDisposable pattern? | A pattern for deterministic resource cleanup | It releases resources explicitly. |
| 2928 | What is dispose pattern with finalizer? | Combining IDisposable with fallback cleanup | It handles missed disposal. |
| 2929 | What is Dispose(bool disposing)? | A common implementation pattern for IDisposable | It separates managed and unmanaged cleanup. |
| 2930 | What is GC.SuppressFinalize()? | Prevents finalization after explicit disposal | It improves performance. |
| 2931 | What is object resurrection? | An object becoming reachable again during finalization | It is rarely recommended. |
| 2932 | What is weak reference? | A reference that does not prevent garbage collection | It allows cache-like behavior. |
| 2933 | What is WeakReference<T>? | Generic weak reference implementation | It provides type-safe weak references. |
| 2934 | What is ConditionalWeakTable? | A table associating data with objects without extending lifetime | It supports metadata scenarios. |
| 2935 | What is memory pressure notification? | Detecting changes in available memory | It helps adaptive applications. |
| 2936 | What is ArrayPool<T>.Shared? | The default shared array pool instance | It enables array reuse. |
| 2937 | What is object pooling? | Reusing objects instead of repeatedly allocating | It reduces allocation overhead. |
| 2938 | What is ObjectPool<T>? | A .NET abstraction for reusable objects | It manages pooled instances. |
| 2939 | What is pooling policy? | Rules controlling object creation and return | It defines pool behavior. |
| 2940 | What is arena allocation? | Allocating objects from a shared memory region | It enables fast bulk cleanup. |
| 2941 | What is memory fragmentation? | Scattered free memory reducing allocation efficiency | It affects memory usage. |
| 2942 | What is compaction? | Moving objects together to reduce fragmentation | The GC performs heap compaction. |
| 2943 | What is pinning? | Preventing an object from being moved by GC | It is required for some native operations. |
| 2944 | What is pinned object heap (POH)? | A heap dedicated to pinned objects | It reduces fragmentation from pinning. |
| 2945 | What is fixed statement? | A C# statement preventing garbage collection movement | It pins managed memory. |
| 2946 | What is GCHandle? | A mechanism for manually controlling object handles | It supports interop scenarios. |
| 2947 | What is unmanaged memory allocation? | Allocating memory outside the managed heap | It requires manual cleanup. |
| 2948 | What is NativeMemory class? | API for unmanaged memory allocation | It provides low-level memory operations. |
| 2949 | What is Marshal class? | API for interoperability services | It converts between managed and unmanaged representations. |
| 2950 | What is P/Invoke? | Calling native functions from managed code | It enables interoperability with native libraries. |
| 2951 | What is DllImportAttribute? | An attribute used to declare external native methods | It enables P/Invoke calls. |
| 2952 | What is LibraryImportAttribute? | A source-generated alternative to DllImport | It improves performance and trimming support. |
| 2953 | What is marshalling? | Converting data between managed and unmanaged formats | It enables interoperability. |
| 2954 | What is blittable type? | A type whose memory representation is identical across managed and unmanaged code | It avoids conversion during interop. |
| 2955 | What is COM interop? | Interoperability between .NET and COM components | It enables use of COM libraries. |
| 2956 | What is COM callable wrapper (CCW)? | A wrapper exposing managed objects to COM | It allows COM clients to call .NET code. |
| 2957 | What is runtime callable wrapper (RCW)? | A wrapper allowing .NET to call COM objects | It manages COM lifetime. |
| 2958 | What is unsafe code? | Code allowing direct memory access | It requires compiler permission. |
| 2959 | What is pointer type in C#? | A variable storing a memory address | It is used in unsafe contexts. |
| 2960 | What is stackalloc? | Allocating memory on the stack | It avoids heap allocation. |
| 2961 | What is Span<T> with stackalloc? | A safe view over stack-allocated memory | It combines performance and safety. |
| 2962 | What is Memory<T>? | A heap-compatible memory abstraction | It works where Span<T> cannot. |
| 2963 | What is ReadOnlySpan<T>? | A read-only view over contiguous memory | It prevents modification. |
| 2964 | What is ReadOnlyMemory<T>? | A read-only heap-compatible memory abstraction | It supports asynchronous scenarios. |
| 2965 | What is IBufferWriter<T>? | An abstraction for writing buffers efficiently | It reduces unnecessary copying. |
| 2966 | What is ReadOnlySequence<T>? | A sequence representing potentially segmented memory | It supports pipelines. |
| 2967 | What is SequenceReader<T>? | A reader optimized for ReadOnlySequence<T> | It parses segmented data efficiently. |
| 2968 | What is MemoryMarshal? | Utility APIs for memory reinterpretation | It enables advanced memory operations. |
| 2969 | What is Unsafe class? | Low-level APIs bypassing safety checks | It enables performance optimizations. |
| 2970 | What is ref return? | A method returning a reference to existing storage | It avoids copying values. |
| 2971 | What is ref local? | A local variable referencing another storage location | It enables direct mutation. |
| 2972 | What is ref readonly? | A read-only reference variable | It avoids copying while preventing modification. |
| 2973 | What is scoped ref? | A reference restricted to a safe lifetime | It prevents escaping stack references. |
| 2974 | What is ref safety? | Compiler rules preventing invalid reference usage | It protects memory safety. |
| 2975 | What is readonly reference? | A reference that cannot modify the target | It reduces copying. |
| 2976 | What is in parameter modifier? | A readonly reference parameter | It avoids copying large structs. |
| 2977 | What is out parameter modifier? | A parameter assigned by the called method | It allows returning additional values. |
| 2978 | What is ref parameter modifier? | A parameter passed by reference | It allows modifying caller variables. |
| 2979 | What is discard variable? | A variable intentionally ignored using underscore | It ignores unused outputs. |
| 2980 | What is deconstruction? | Splitting an object into multiple variables | It uses Deconstruct methods. |
| 2981 | What is tuple type? | A lightweight type grouping multiple values | It supports multiple return values. |
| 2982 | What is ValueTuple? | A struct-based tuple implementation | It avoids some allocations. |
| 2983 | What is named tuple element? | A tuple element with a custom name | It improves readability. |
| 2984 | What is pattern matching with tuples? | Matching multiple values together | It simplifies decision logic. |
| 2985 | What is switch expression guard? | A when condition in pattern matching | It adds extra filtering logic. |
| 2986 | What is discard pattern? | A pattern matching any value without storing it | It ignores unnecessary values. |
| 2987 | What is type pattern? | A pattern checking runtime type | It performs safe type matching. |
| 2988 | What is constant pattern? | A pattern matching a specific constant value | It compares exact values. |
| 2989 | What is var pattern? | A pattern assigning a matched value | It always succeeds. |
| 2990 | What is recursive pattern? | A pattern matching nested object structures | It enables complex matching. |
| 2991 | What is interpolated string handler? | A custom mechanism controlling string interpolation | It can avoid unnecessary formatting work. |
| 2992 | What is FormattableString? | A representation of an interpolated string with format information | It delays formatting. |
| 2993 | What is IFormattable? | Interface supporting custom formatting | It enables culture-aware output. |
| 2994 | What is composite formatting? | Formatting strings using placeholders | It predates interpolation. |
| 2995 | What is DefaultInterpolatedStringHandler? | Built-in handler for optimized interpolation | It reduces allocations. |
| 2996 | What is caller information attribute? | An attribute capturing caller details automatically | It assists diagnostics. |
| 2997 | What is CallerMemberNameAttribute? | Captures the calling member name | It is useful for logging. |
| 2998 | What is CallerFilePathAttribute? | Captures the source file path | It provides source information. |
| 2999 | What is CallerLineNumberAttribute? | Captures the source line number | It assists debugging. |
| 3000 | What is DebuggerDisplayAttribute? | An attribute controlling debugger display text | It improves debugging visibility. |
| 3001 | What is DebuggerTypeProxyAttribute? | An attribute providing a custom debugger view | It simplifies inspection of complex objects. |
| 3002 | What is ConditionalAttribute? | An attribute controlling conditional method compilation | It removes calls when symbols are absent. |
| 3003 | What is ObsoleteAttribute? | An attribute marking APIs as outdated | It warns developers about replacement APIs. |
| 3004 | What is AttributeUsageAttribute? | An attribute defining where custom attributes can be applied | It controls attribute behavior. |
| 3005 | What is custom attribute? | Metadata attached to types or members | It provides additional information. |
| 3006 | What is reflection emit? | Generating assemblies or methods dynamically | It creates code at runtime. |
| 3007 | What is DynamicMethod? | A lightweight runtime-generated method | It avoids creating a full assembly. |
| 3008 | What is expression tree? | A data structure representing code as expressions | It enables runtime query generation. |
| 3009 | What is Expression<TDelegate>? | A strongly typed expression tree | LINQ providers translate it. |
| 3010 | What is expression compilation? | Converting an expression tree into executable code | It creates delegates. |
| 3011 | What is IQueryable<T>? | An interface for query providers | Queries can execute remotely. |
| 3012 | What is IEnumerable<T>? | An interface for in-memory iteration | Queries execute locally. |
| 3013 | What is LINQ provider? | A component translating LINQ expressions | It executes queries against different sources. |
| 3014 | What is query translation? | Converting expressions into another query language | ORMs translate LINQ to SQL. |
| 3015 | What is LINQ deferred execution danger? | Query results can change before enumeration | Execution happens later. |
| 3016 | What is LINQ closure? | Capturing variables from an outer scope | It can affect query behavior. |
| 3017 | What is closure allocation? | Allocation caused by captured variables | It can impact performance. |
| 3018 | What is anonymous function? | A lambda expression or anonymous method | It creates inline behavior. |
| 3019 | What is lambda expression? | A concise syntax for creating delegates | It is common in LINQ. |
| 3020 | What is delegate? | A type-safe reference to a method | It enables callbacks. |
| 3021 | What is multicast delegate? | A delegate containing multiple methods | All methods are invoked sequentially. |
| 3022 | What is delegate covariance? | Allowing compatible return type conversions | It improves delegate flexibility. |
| 3023 | What is delegate contravariance? | Allowing compatible parameter type conversions | It improves delegate assignment. |
| 3024 | What is Action delegate? | A delegate returning void | It represents operations. |
| 3025 | What is Func delegate? | A delegate returning a value | It represents functions. |
| 3026 | What is Predicate delegate? | A delegate returning a Boolean result | It is used for conditions. |
| 3027 | What is event accessor? | Custom add and remove logic for events | It controls event subscriptions. |
| 3028 | What is event invocation restriction? | Only the declaring type can raise an event | It protects event ownership. |
| 3029 | What is weak event pattern? | An event pattern avoiding subscriber lifetime issues | It prevents memory leaks. |
| 3030 | What is observer pattern? | A pattern where objects subscribe to notifications | Events implement this concept. |
| 3031 | What is mediator pattern? | A pattern centralizing communication between objects | It reduces direct dependencies. |
| 3032 | What is strategy pattern? | A pattern selecting interchangeable algorithms | It improves flexibility. |
| 3033 | What is factory pattern? | A pattern creating objects without exposing creation logic | It centralizes construction. |
| 3034 | What is abstract factory pattern? | A factory creating related object families | It supports interchangeable products. |
| 3035 | What is singleton pattern? | A pattern ensuring one instance of a type | It should be used carefully. |
| 3036 | What is dependency inversion principle? | High-level modules should not depend on low-level details | Both should depend on abstractions. |
| 3037 | What is single responsibility principle? | A class should have one reason to change | It improves maintainability. |
| 3038 | What is open-closed principle? | Software entities should be open for extension but closed for modification | It encourages extensible designs. |
| 3039 | What is Liskov substitution principle? | Derived types must be usable where base types are expected | It preserves behavioral correctness. |
| 3040 | What is interface segregation principle? | Clients should not depend on unnecessary members | It encourages smaller interfaces. |
| 3041 | What is SOLID? | A set of object-oriented design principles | It improves software structure. |
| 3042 | What is composition over inheritance? | Building behavior by combining objects instead of extending classes | It reduces coupling. |
| 3043 | What is dependency injection? | Providing dependencies from outside an object | It improves testability. |
| 3044 | What is service lifetime in dependency injection? | The duration a service instance exists | Common lifetimes are transient, scoped, and singleton. |
| 3045 | What is transient service? | A DI service created every time it is requested | It is suitable for lightweight objects. |
| 3046 | What is scoped service? | A DI service created once per scope | HTTP requests commonly define scopes. |
| 3047 | What is singleton service? | A DI service created once for the application lifetime | It must be thread-safe. |
| 3048 | What is captive dependency? | A longer-lived service depending on a shorter-lived service | It can cause lifetime bugs. |
| 3049 | What is IServiceProvider? | The .NET dependency injection service resolver | It creates registered services. |
| 3050 | What is service collection? | A collection used to register dependency injection services | It builds the service provider. |
| 3051 | What is dependency injection scope validation? | A check detecting invalid service lifetime relationships | It catches captive dependencies. |
| 3052 | What is factory registration in DI? | Registering a service using a creation function | It allows custom construction logic. |
| 3053 | What is open generic registration? | Registering a generic service without specifying a type argument | The container closes it when resolving. |
| 3054 | What is keyed service in .NET DI? | A service registered with an identifying key | It allows multiple implementations of the same type. |
| 3055 | What is service locator pattern? | Resolving dependencies manually from a container | It is often considered an anti-pattern. |
| 3056 | What is composition root? | The application location where dependencies are assembled | It centralizes configuration. |
| 3057 | What is inversion of control? | Moving object creation decisions outside the object | DI is one implementation. |
| 3058 | What is test double? | A replacement object used during testing | It isolates dependencies. |
| 3059 | What is mock object? | A test object verifying interactions | It checks expected calls. |
| 3060 | What is stub object? | A test object returning predefined responses | It supplies controlled data. |
| 3061 | What is fake object? | A simplified working implementation used in tests | It behaves realistically but simply. |
| 3062 | What is spy object? | A test double recording interactions | It verifies behavior after execution. |
| 3063 | What is unit test? | A test verifying a small isolated unit of code | It runs quickly. |
| 3064 | What is integration test? | A test verifying multiple components together | It checks real interactions. |
| 3065 | What is end-to-end test? | A test validating complete user workflows | It tests the whole system. |
| 3066 | What is test fixture? | Shared setup and state for tests | It reduces duplication. |
| 3067 | What is test isolation? | Ensuring tests do not affect each other | It improves reliability. |
| 3068 | What is deterministic test? | A test producing the same result every run | It avoids flaky behavior. |
| 3069 | What is flaky test? | A test that sometimes passes and sometimes fails | It reduces confidence in testing. |
| 3070 | What is code coverage? | Measurement of executed code during tests | It indicates tested areas. |
| 3071 | What is mutation testing? | Testing test quality by introducing code changes | It detects weak tests. |
| 3072 | What is property-based testing? | Testing general rules across generated inputs | It finds edge cases. |
| 3073 | What is snapshot testing? | Comparing output against a stored reference | It detects unexpected changes. |
| 3074 | What is approval testing? | Reviewing generated output against approved data | It validates complex results. |
| 3075 | What is xUnit? | A .NET testing framework | It provides test discovery and execution. |
| 3076 | What is NUnit? | A .NET unit testing framework | It supports attribute-based testing. |
| 3077 | What is MSTest? | Microsoft's testing framework for .NET | It integrates with Visual Studio. |
| 3078 | What is test theory in xUnit? | A parameterized test method | It runs with multiple data sets. |
| 3079 | What is fact in xUnit? | A standard test case | It has no parameters. |
| 3080 | What is assertion? | A statement verifying expected behavior | It fails tests when conditions are false. |
| 3081 | What is Arrange-Act-Assert pattern? | A structure for organizing tests | It improves readability. |
| 3082 | What is mocking framework? | A library for creating mock objects | It simplifies unit testing. |
| 3083 | What is Moq? | A .NET mocking library | It creates test doubles. |
| 3084 | What is fake time provider? | A controllable time source for testing | It avoids dependence on real time. |
| 3085 | What is TimeProvider in .NET? | An abstraction for retrieving time | It improves testability. |
| 3086 | What is dependency seam? | A point where behavior can be replaced | It enables testing. |
| 3087 | What is integration boundary test? | A test validating communication between components | It protects contracts. |
| 3088 | What is consumer contract test? | A test ensuring a provider meets consumer expectations | It validates service compatibility. |
| 3089 | What is smoke test? | A basic test verifying major functionality | It detects severe failures quickly. |
| 3090 | What is regression test? | A test ensuring existing functionality still works | It prevents old bugs returning. |
| 3091 | What is acceptance test? | A test verifying business requirements | It validates user expectations. |
| 3092 | What is exploratory testing? | Testing through investigation rather than scripts | It discovers unexpected issues. |
| 3093 | What is load testing? | Testing system behavior under expected traffic | It measures performance. |
| 3094 | What is stress testing? | Testing beyond normal capacity | It finds breaking points. |
| 3095 | What is soak testing? | Long-duration performance testing | It detects leaks and degradation. |
| 3096 | What is spike testing? | Testing sudden traffic increases | It evaluates scalability. |
| 3097 | What is benchmark? | A repeatable performance measurement | It compares implementations. |
| 3098 | What is BenchmarkDotNet? | A .NET benchmarking library | It measures performance accurately. |
| 3099 | What is microbenchmark? | A benchmark measuring a small operation | It isolates performance details. |
| 3100 | What is performance regression? | A decrease in performance after changes | Benchmarks detect it. |
| 3101 | What is BenchmarkDotNet warmup phase? | A phase that runs code before measurement begins | It reduces effects from JIT compilation and startup costs. |
| 3102 | What is BenchmarkDotNet iteration? | A single measured execution cycle | Multiple iterations improve accuracy. |
| 3103 | What is BenchmarkDotNet diagnoser? | A component collecting additional benchmark information | It can measure memory and hardware counters. |
| 3104 | What is allocation benchmark? | A benchmark measuring memory allocations | It identifies allocation overhead. |
| 3105 | What is throughput? | Amount of work completed per unit of time | It measures processing capacity. |
| 3106 | What is latency? | Time required to complete an operation | It measures responsiveness. |
| 3107 | What is tail latency? | Latency experienced by the slowest requests | It reveals worst-case performance. |
| 3108 | What is p50 latency? | The median latency value | Half of requests are faster. |
| 3109 | What is p95 latency? | Latency where 95% of requests are faster | It shows high-percentile behavior. |
| 3110 | What is p99 latency? | Latency where 99% of requests are faster | It highlights extreme slow requests. |
| 3111 | What is throughput bottleneck? | A limitation preventing higher processing rates | It restricts scalability. |
| 3112 | What is CPU-bound operation? | Work limited by processor execution | Parallelism may improve it. |
| 3113 | What is I/O-bound operation? | Work limited by external input/output | Async programming improves scalability. |
| 3114 | What is thread pool starvation? | Too many blocked tasks preventing new work | It reduces application responsiveness. |
| 3115 | What is ThreadPool? | A managed pool of reusable worker threads | It avoids creating threads repeatedly. |
| 3116 | What is worker thread? | A thread executing queued work | ThreadPool uses worker threads. |
| 3117 | What is I/O completion thread? | A thread handling asynchronous I/O callbacks | It supports scalable async operations. |
| 3118 | What is ThreadPool hill climbing algorithm? | An algorithm adjusting thread pool size | It balances throughput and resource usage. |
| 3119 | What is dedicated thread? | A manually created thread with a specific purpose | It provides explicit control. |
| 3120 | What is background thread? | A thread that does not keep the process alive | It terminates when foreground threads finish. |
| 3121 | What is foreground thread? | A thread that keeps the process running | The runtime waits for it to finish. |
| 3122 | What is thread synchronization? | Coordinating access between threads | It prevents race conditions. |
| 3123 | What is lock statement? | A synchronization mechanism using Monitor | It protects critical sections. |
| 3124 | What is Monitor.Enter? | Method acquiring a monitor lock | It provides mutual exclusion. |
| 3125 | What is Monitor.Exit? | Method releasing a monitor lock | It frees the protected resource. |
| 3126 | What is Monitor.Wait? | Method releasing a lock and waiting for a signal | It supports coordination. |
| 3127 | What is Monitor.Pulse? | Method waking a waiting thread | It signals availability. |
| 3128 | What is Mutex? | A synchronization primitive usable across processes | It provides exclusive ownership. |
| 3129 | What is Semaphore? | A synchronization primitive allowing limited concurrent access | It controls resource counts. |
| 3130 | What is SemaphoreSlim? | A lightweight semaphore for managed code | It supports async waiting. |
| 3131 | What is ReaderWriterLockSlim? | A lock allowing concurrent readers | It improves read-heavy performance. |
| 3132 | What is SpinLock? | A lock that waits by spinning | It is useful for very short critical sections. |
| 3133 | What is SpinWait? | A helper for efficient spinning | It balances spinning and yielding. |
| 3134 | What is Interlocked class? | Atomic operation APIs for shared values | It avoids heavier locks. |
| 3135 | What is atomic operation? | An operation that completes indivisibly | Other threads see consistent states. |
| 3136 | What is CompareExchange? | An atomic compare-and-swap operation | It enables lock-free algorithms. |
| 3137 | What is Exchange method? | An atomic value replacement operation | It swaps values safely. |
| 3138 | What is Increment method? | An atomic increment operation | It safely updates counters. |
| 3139 | What is memory barrier? | A mechanism controlling memory operation ordering | It affects visibility between threads. |
| 3140 | What is happens-before relationship? | A guarantee about operation ordering | It defines visibility rules. |
| 3141 | What is data race? | Unsynchronized concurrent access causing unpredictable results | Synchronization prevents it. |
| 3142 | What is race condition? | A bug caused by timing-dependent execution | It occurs in concurrent code. |
| 3143 | What is deadlock? | A state where threads wait indefinitely | Lock ordering can prevent it. |
| 3144 | What is livelock? | Threads remain active but make no progress | It differs from deadlock. |
| 3145 | What is starvation? | A thread waits too long for resources | Fair scheduling can reduce it. |
| 3146 | What is lock contention? | Multiple threads competing for the same lock | It reduces performance. |
| 3147 | What is lock-free algorithm? | An algorithm allowing system progress without locks | It uses atomic operations. |
| 3148 | What is wait-free algorithm? | An algorithm guaranteeing completion in bounded steps | It is stronger than lock-free. |
| 3149 | What is concurrent collection? | A thread-safe collection for parallel access | It avoids manual synchronization. |
| 3150 | What is ConcurrentDictionary<TKey,TValue>? | A thread-safe dictionary implementation | It supports concurrent reads and writes. |
| 3151 | What is ConcurrentQueue<T>? | A thread-safe FIFO collection | It supports multiple producers and consumers. |
| 3152 | What is ConcurrentStack<T>? | A thread-safe LIFO collection | It supports concurrent push and pop operations. |
| 3153 | What is BlockingCollection<T>? | A thread-safe collection supporting blocking operations | It coordinates producer and consumer workflows. |
| 3154 | What is Channel<T>? | A high-performance asynchronous producer-consumer queue | It supports async communication between tasks. |
| 3155 | What is bounded channel? | A channel with a fixed capacity | It provides backpressure. |
| 3156 | What is unbounded channel? | A channel without a fixed capacity limit | It can grow until memory is exhausted. |
| 3157 | What is ChannelWriter<T>? | The producer side of a channel | It writes items into the channel. |
| 3158 | What is ChannelReader<T>? | The consumer side of a channel | It reads items from the channel. |
| 3159 | What is producer-consumer pattern? | A pattern separating work creation and processing | It improves concurrency design. |
| 3160 | What is task parallel library (TPL)? | A .NET framework for parallel programming | It simplifies concurrent execution. |
| 3161 | What is Parallel.For? | A parallel loop construct | It executes iterations concurrently. |
| 3162 | What is Parallel.ForEach? | A parallel collection iteration method | It distributes work across threads. |
| 3163 | What is Parallel.Invoke? | A method executing multiple actions in parallel | It simplifies parallel tasks. |
| 3164 | What is ParallelOptions? | Configuration for parallel operations | It controls parallel behavior. |
| 3165 | What is MaxDegreeOfParallelism? | A limit on concurrent parallel operations | It prevents excessive resource usage. |
| 3166 | What is TaskScheduler? | A component deciding how tasks execute | It controls task scheduling. |
| 3167 | What is TaskScheduler.Current? | The scheduler associated with the current task | It affects task continuation behavior. |
| 3168 | What is TaskScheduler.Default? | The default thread pool scheduler | It runs tasks on ThreadPool threads. |
| 3169 | What is custom TaskScheduler? | A user-defined task scheduling implementation | It provides specialized execution behavior. |
| 3170 | What is Task.Run? | A method scheduling work on the thread pool | It creates a task for CPU-bound work. |
| 3171 | What is Task.Factory.StartNew? | A lower-level task creation API | It provides more configuration options. |
| 3172 | What is DenyChildAttach? | A task creation option preventing child task attachment | It isolates task hierarchies. |
| 3173 | What is AttachedToParent? | A task option linking child tasks to parents | Parent completion waits for children. |
| 3174 | What is Task.WhenAll? | A method awaiting multiple tasks together | It completes when all tasks finish. |
| 3175 | What is Task.WhenAny? | A method awaiting the first completed task | It returns whichever finishes first. |
| 3176 | What is task continuation? | Work scheduled after a task completes | It processes task results. |
| 3177 | What is ContinueWith? | A method creating a continuation task | It provides explicit continuation control. |
| 3178 | What is async coordination primitive? | A primitive designed for asynchronous synchronization | Examples include SemaphoreSlim and AsyncAutoResetEvent. |
| 3179 | What is AsyncLocal<T> usage in web applications? | Storing request-scoped asynchronous context | It can carry correlation information. |
| 3180 | What is ExecutionContext suppression? | Preventing context flow across async boundaries | It reduces overhead in some cases. |
| 3181 | What is ExecutionContext.SuppressFlow()? | API disabling automatic context propagation | It improves performance in special cases. |
| 3182 | What is AsyncMethodBuilder? | A compiler/runtime component building async state machines | It controls async method behavior. |
| 3183 | What is AsyncTaskMethodBuilder? | The builder used for Task-returning async methods | It manages task completion. |
| 3184 | What is AsyncValueTaskMethodBuilder? | The builder used for ValueTask async methods | It reduces allocations. |
| 3185 | What is custom async method builder? | A custom builder controlling async method generation | It enables advanced scenarios. |
| 3186 | What is awaiter pattern? | A pattern allowing types to be awaited | It requires GetAwaiter support. |
| 3187 | What is INotifyCompletion? | Interface defining await continuation support | Awaiters implement it. |
| 3188 | What is ICriticalNotifyCompletion? | Interface allowing unsafe continuation scheduling | It provides advanced awaiter control. |
| 3189 | What is GetAwaiter method? | Method returning an awaiter | It enables await syntax. |
| 3190 | What is IsCompleted property in awaiter? | Indicates whether an async operation finished | The compiler checks it. |
| 3191 | What is OnCompleted method? | Registers continuation logic | It resumes execution after completion. |
| 3192 | What is GetResult method? | Retrieves the awaited result | It can throw exceptions. |
| 3193 | What is async state machine? | Compiler-generated structure managing await execution | It stores continuation state. |
| 3194 | What is state machine boxing? | Allocation caused when async state machines move to the heap | It affects performance. |
| 3195 | What is synchronous completion optimization? | Avoiding allocations when async work finishes immediately | ValueTask can benefit from it. |
| 3196 | What is ValueTask pooling? | Reusing underlying async operation objects | It requires careful implementation. |
| 3197 | What is IValueTaskSource<T>? | Interface providing custom ValueTask backing | It enables allocation-free async operations. |
| 3198 | What is ManualResetValueTaskSourceCore<T>? | Helper implementing IValueTaskSource behavior | It simplifies custom async primitives. |
| 3199 | What is async lock? | A lock designed for awaiting without blocking threads | It coordinates asynchronous access. |
| 3200 | What is AsyncSemaphore? | An asynchronous semaphore implementation | It limits concurrent async operations. |
| 3201 | What is ASP.NET Core middleware? | A component that processes HTTP requests and responses | Middleware forms the request pipeline. |
| 3202 | What is middleware pipeline order importance? | Middleware executes in the order it is registered | Order affects application behavior. |
| 3203 | What is terminal middleware? | Middleware that does not call the next component | It ends request processing. |
| 3204 | What is Use middleware method? | A method adding middleware to the pipeline | It usually calls the next middleware. |
| 3205 | What is Run middleware method? | A method adding terminal middleware | It ends the pipeline. |
| 3206 | What is Map middleware method? | A method branching the pipeline by path | It creates conditional pipelines. |
| 3207 | What is MapWhen middleware method? | A method branching by a custom predicate | It supports flexible routing. |
| 3208 | What is request delegate? | A delegate processing an HTTP request | Middleware uses request delegates. |
| 3209 | What is HttpContext? | An object representing an HTTP request and response | It stores request-specific data. |
| 3210 | What is HttpRequest? | An object containing incoming request data | It provides headers, path, and body access. |
| 3211 | What is HttpResponse? | An object representing outgoing response data | It controls status codes and content. |
| 3212 | What is HttpContext.Items? | A per-request key-value storage collection | It shares data between middleware components. |
| 3213 | What is HttpContext.Features? | A collection of server-specific capabilities | It exposes advanced HTTP features. |
| 3214 | What is endpoint routing? | ASP.NET Core routing system selecting endpoints | It separates matching from execution. |
| 3215 | What is endpoint metadata? | Information attached to an endpoint | It influences filters and middleware. |
| 3216 | What is route constraint? | A rule restricting route parameter values | It validates route matching. |
| 3217 | What is attribute routing? | Routing defined using attributes on controllers or actions | It allows explicit route definitions. |
| 3218 | What is conventional routing? | Routing based on predefined URL patterns | It is common in MVC applications. |
| 3219 | What is route parameter? | A variable segment in a URL pattern | It captures request values. |
| 3220 | What is route value? | A value extracted from matched route data | Controllers can use it. |
| 3221 | What is URL generation? | Creating URLs from route information | It supports navigation. |
| 3222 | What is controller action? | A method handling an HTTP request | It returns an action result. |
| 3223 | What is IActionResult? | An abstraction representing an HTTP response | Controllers return different results. |
| 3224 | What is ActionResult<T>? | A typed action response wrapper | It combines data and HTTP results. |
| 3225 | What is OkObjectResult? | An action result returning HTTP 200 with data | It represents successful responses. |
| 3226 | What is NotFoundResult? | An action result returning HTTP 404 | It indicates missing resources. |
| 3227 | What is BadRequestResult? | An action result returning HTTP 400 | It indicates invalid requests. |
| 3228 | What is UnauthorizedResult? | An action result returning HTTP 401 | It indicates missing authentication. |
| 3229 | What is ForbidResult? | An action result returning HTTP 403 | It indicates insufficient permissions. |
| 3230 | What is CreatedAtActionResult? | An action result returning HTTP 201 with location information | It is used after resource creation. |
| 3231 | What is model binding? | Converting HTTP input into .NET objects | It maps request data to parameters. |
| 3232 | What is model validation? | Checking bound models against validation rules | It detects invalid input. |
| 3233 | What is ModelStateDictionary? | A collection storing binding and validation errors | Controllers use it for validation checks. |
| 3234 | What is validation attribute? | An attribute defining validation rules | Examples include Required and Range. |
| 3235 | What is custom validation attribute? | A user-defined validation rule | It extends validation behavior. |
| 3236 | What is IValidatableObject? | Interface allowing object-level validation | It supports custom validation logic. |
| 3237 | What is automatic model validation? | Framework validation performed during binding | It reduces manual checks. |
| 3238 | What is API controller attribute? | An attribute enabling API-specific behavior | It enables automatic validation and binding rules. |
| 3239 | What is controller filter? | A component running around controller execution | It adds cross-cutting behavior. |
| 3240 | What is authorization filter? | A filter running authorization checks | It executes early in the pipeline. |
| 3241 | What is resource filter? | A filter surrounding model binding and execution | It can short-circuit requests. |
| 3242 | What is action filter? | A filter running before and after action methods | It modifies action execution. |
| 3243 | What is exception filter? | A filter handling controller exceptions | It provides centralized error handling. |
| 3244 | What is result filter? | A filter running before and after action results | It modifies responses. |
| 3245 | What is filter factory? | A mechanism creating filters dynamically | It supports dependency injection. |
| 3246 | What is filter scope? | The level where a filter is applied | It can be global, controller, or action. |
| 3247 | What is global filter? | A filter applied across an application | It affects all matching requests. |
| 3248 | What is action parameter binding source? | The location where parameter data comes from | Examples include body, route, and query. |
| 3249 | What is FromBody attribute? | Attribute binding a parameter from request body | It commonly binds JSON data. |
| 3250 | What is FromQuery attribute? | Attribute binding a parameter from query string | It reads URL parameters. |
| 3251 | What is FromRoute attribute? | Attribute binding a parameter from route values | It reads URL path parameters. |
| 3252 | What is FromHeader attribute? | Attribute binding a parameter from HTTP headers | It extracts header values. |
| 3253 | What is FromServices attribute? | Attribute resolving a parameter from dependency injection | It injects registered services. |
| 3254 | What is model binder provider? | A component creating custom model binders | It extends binding behavior. |
| 3255 | What is custom model binder? | A component converting request data into custom types | It handles specialized input formats. |
| 3256 | What is JSON formatter? | A component converting JSON request and response data | ASP.NET Core uses System.Text.Json by default. |
| 3257 | What is input formatter? | A component reading request body data | It converts HTTP content into objects. |
| 3258 | What is output formatter? | A component writing response data | It converts objects into HTTP content. |
| 3259 | What is content negotiation? | Selecting response format based on client preferences | It uses Accept headers. |
| 3260 | What is Accept header? | An HTTP header specifying preferred response formats | Servers use it during negotiation. |
| 3261 | What is Content-Type header? | An HTTP header describing request or response media type | It identifies data format. |
| 3262 | What is media type? | A format identifier for HTTP content | Examples include application/json. |
| 3263 | What is ProblemDetails? | A standardized HTTP error response format | It improves API error consistency. |
| 3264 | What is IProblemDetailsService? | A service generating standardized problem responses | It centralizes API errors. |
| 3265 | What is OpenAPI? | A specification describing HTTP APIs | It enables API documentation. |
| 3266 | What is Swagger? | A set of tools for OpenAPI documents | It provides interactive API documentation. |
| 3267 | What is Swagger UI? | A web interface for exploring APIs | It sends test requests. |
| 3268 | What is API versioning? | Supporting multiple API versions | It enables backward compatibility. |
| 3269 | What is minimal API? | A lightweight API style using route handlers | It reduces boilerplate. |
| 3270 | What is route handler? | A delegate processing a minimal API endpoint | It handles HTTP requests. |
| 3271 | What is endpoint filter? | A component wrapping minimal API handlers | It provides cross-cutting logic. |
| 3272 | What is endpoint filter factory? | A function creating endpoint filters | It enables dynamic configuration. |
| 3273 | What is typed results? | Strongly typed minimal API responses | They improve compile-time checking. |
| 3274 | What is Results class? | A helper creating minimal API responses | It provides common HTTP results. |
| 3275 | What is WebApplication builder? | A builder configuring an ASP.NET Core app | It creates the application pipeline. |
| 3276 | What is WebApplication? | The main ASP.NET Core application object | It hosts the request pipeline. |
| 3277 | What is WebApplicationFactory? | A testing host for ASP.NET Core applications | It supports integration testing. |
| 3278 | What is TestServer? | An in-memory ASP.NET Core server | It enables fast integration tests. |
| 3279 | What is Kestrel? | The cross-platform ASP.NET Core web server | It handles HTTP requests. |
| 3280 | What is reverse proxy? | A server forwarding requests to an application | Examples include IIS and Nginx. |
| 3281 | What is forwarded headers middleware? | Middleware processing proxy headers | It restores original request information. |
| 3282 | What is hosting environment? | Information about application runtime environment | It controls environment-specific behavior. |
| 3283 | What is IHostEnvironment? | Interface describing hosting environment | It provides environment details. |
| 3284 | What is IWebHostEnvironment? | Web-specific hosting environment information | It adds web root information. |
| 3285 | What is environment name? | A value identifying runtime environment | Common values include Development and Production. |
| 3286 | What is configuration system? | A system combining application settings sources | It supports JSON, environment variables, and more. |
| 3287 | What is IConfiguration? | Interface for reading configuration values | It accesses application settings. |
| 3288 | What is configuration provider? | A source supplying configuration data | Examples include JSON files and environment variables. |
| 3289 | What is appsettings.json? | Default JSON configuration file | It stores application settings. |
| 3290 | What is options pattern? | A way to access strongly typed configuration | It improves configuration management. |
| 3291 | What is IOptions<T>? | A wrapper providing configured options | It provides configuration values. |
| 3292 | What is IOptionsSnapshot<T>? | A scoped options provider supporting reloads | It updates per request. |
| 3293 | What is IOptionsMonitor<T>? | An options provider supporting change notifications | It observes configuration changes. |
| 3294 | What is options validation? | Checking configuration values against rules | It prevents invalid startup settings. |
| 3295 | What is secrets manager? | A tool storing development secrets securely | It avoids hardcoded credentials. |
| 3296 | What is user secrets in .NET? | A development-time secret storage mechanism | It keeps secrets outside source code. |
| 3297 | What is environment variable configuration? | Reading settings from operating system variables | It is common in deployments. |
| 3298 | What is configuration precedence? | The order determining which configuration value wins | Later providers override earlier ones. |
| 3299 | What is logging abstraction? | A common interface for application logging | It separates code from logging providers. |
| 3300 | What is ILogger<T>? | A typed logging interface | It associates logs with a category. |
| 3301 | What is ILoggerFactory? | A factory for creating logger instances | It manages logging providers. |
| 3302 | What is logging provider? | A component that receives and stores log messages | Examples include console and debug providers. |
| 3303 | What is structured logging? | Logging with named properties instead of formatted text only | It improves querying and analysis. |
| 3304 | What is log level? | A severity classification for log messages | Common levels include Debug, Information, Warning, Error, and Critical. |
| 3305 | What is Trace log level? | The most detailed logging level | It is used for fine-grained diagnostics. |
| 3306 | What is Debug log level? | A detailed diagnostic logging level | It is mainly used during development. |
| 3307 | What is Information log level? | A normal operational logging level | It records application flow. |
| 3308 | What is Warning log level? | A log level for potential problems | It indicates unusual conditions. |
| 3309 | What is Error log level? | A log level for failures | It indicates operations that failed. |
| 3310 | What is Critical log level? | A log level for severe failures | It indicates major application problems. |
| 3311 | What is logging scope? | A context attached to multiple log entries | It adds shared diagnostic information. |
| 3312 | What is LoggerMessage pattern? | A high-performance logging approach using predefined delegates | It reduces allocations. |
| 3313 | What is LoggerMessageAttribute? | An attribute generating optimized logging methods | It uses source generation. |
| 3314 | What is distributed tracing? | Tracking requests across multiple services | It follows execution flow. |
| 3315 | What is trace context? | Metadata propagated between services | It connects related operations. |
| 3316 | What is correlation ID? | An identifier linking related requests and logs | It helps diagnose distributed systems. |
| 3317 | What is Activity in .NET? | A representation of an operation for diagnostics | It supports distributed tracing. |
| 3318 | What is ActivitySource? | A factory for creating Activity instances | It integrates with telemetry systems. |
| 3319 | What is OpenTelemetry? | A standard framework for collecting telemetry data | It supports traces, metrics, and logs. |
| 3320 | What is metric? | A numerical measurement of system behavior | It tracks performance and health. |
| 3321 | What is Meter in .NET? | An API for creating application metrics | It produces measurements. |
| 3322 | What is Counter metric? | A metric that only increases | It counts occurrences. |
| 3323 | What is Histogram metric? | A metric recording value distributions | It measures latency and sizes. |
| 3324 | What is Gauge metric? | A metric representing a current value | It tracks changing measurements. |
| 3325 | What is health check? | A mechanism reporting application status | It helps monitoring systems. |
| 3326 | What is IHealthCheck? | Interface implementing custom health checks | It reports component availability. |
| 3327 | What is readiness check? | A check indicating whether an application can receive traffic | Used during deployments. |
| 3328 | What is liveness check? | A check indicating whether an application is running | Detects unhealthy processes. |
| 3329 | What is background service? | A hosted service running background work | It implements IHostedService. |
| 3330 | What is IHostedService? | Interface for application lifetime background tasks | It controls startup and shutdown. |
| 3331 | What is BackgroundService? | Base class simplifying hosted services | It provides ExecuteAsync. |
| 3332 | What is hosted service lifetime? | The period a background service runs | It follows application lifetime. |
| 3333 | What is cancellation token in hosted services? | A signal requesting graceful shutdown | It allows cleanup. |
| 3334 | What is graceful shutdown? | Stopping an application while allowing cleanup | It prevents data loss. |
| 3335 | What is Generic Host? | A framework for hosting .NET applications | It manages configuration, logging, and DI. |
| 3336 | What is HostBuilder? | A builder configuring the generic host | It creates an IHost instance. |
| 3337 | What is IHost? | The generic host abstraction | It manages application lifetime. |
| 3338 | What is host lifetime? | Controls application start and stop events | It coordinates shutdown. |
| 3339 | What is application lifetime event? | Notification when an application starts or stops | It supports initialization and cleanup. |
| 3340 | What is IHostApplicationLifetime? | Interface exposing host lifecycle events | It provides stopping and started tokens. |
| 3341 | What is startup task? | Work performed during application initialization | It prepares services. |
| 3342 | What is hosted singleton? | A singleton service implementing hosted behavior | It runs throughout application lifetime. |
| 3343 | What is graceful cancellation? | Responding to cancellation while finishing safe work | It avoids abrupt termination. |
| 3344 | What is shutdown timeout? | Maximum time allowed for application shutdown | It prevents indefinite stopping. |
| 3345 | What is middleware exception handling? | Handling exceptions in the HTTP pipeline | It provides consistent error responses. |
| 3346 | What is UseExceptionHandler middleware? | Middleware handling unhandled request exceptions | It replaces developer exception pages in production. |
| 3347 | What is DeveloperExceptionPage? | Development middleware showing detailed exceptions | It assists debugging. |
| 3348 | What is exception handler endpoint? | An endpoint receiving processed exceptions | It customizes error responses. |
| 3349 | What is status code pages middleware? | Middleware generating responses for empty error status codes | It improves diagnostics. |
| 3350 | What is request localization middleware? | Middleware applying culture settings to requests | It supports globalization. |
| 3351 | What is authentication? | The process of verifying an identity | It determines who a user is. |
| 3352 | What is authorization? | The process of determining access permissions | It determines what a user can do. |
| 3353 | What is authentication scheme? | A mechanism defining how identities are verified | Examples include cookies and JWT. |
| 3354 | What is IAuthenticationService? | Service responsible for authentication operations | It manages authentication handlers. |
| 3355 | What is authentication handler? | A component processing a specific authentication scheme | It validates credentials. |
| 3356 | What is ClaimsPrincipal? | An object representing an authenticated user | It contains identities and claims. |
| 3357 | What is ClaimsIdentity? | An identity containing authentication information | It stores user claims. |
| 3358 | What is claim? | A piece of information about a user | Examples include name and role. |
| 3359 | What is ClaimTypes? | A collection of standard claim type identifiers | It provides common claim names. |
| 3360 | What is role-based authorization? | Authorization based on assigned roles | It checks user roles. |
| 3361 | What is policy-based authorization? | Authorization based on configurable requirements | It supports complex rules. |
| 3362 | What is authorization policy? | A collection of requirements and handlers | It defines access rules. |
| 3363 | What is authorization requirement? | A condition that must be satisfied | Handlers evaluate requirements. |
| 3364 | What is authorization handler? | A component evaluating authorization requirements | It decides whether access is allowed. |
| 3365 | What is IAuthorizationHandler? | Interface for custom authorization logic | It implements requirement evaluation. |
| 3366 | What is AllowAnonymous attribute? | Attribute bypassing authorization checks | It permits public access. |
| 3367 | What is Authorize attribute? | Attribute requiring authentication or authorization | It restricts access. |
| 3368 | What is cookie authentication? | Authentication storing identity information in cookies | Common for web applications. |
| 3369 | What is JWT authentication? | Authentication using JSON Web Tokens | Common for APIs. |
| 3370 | What is access token? | A credential granting access to resources | It is often short-lived. |
| 3371 | What is refresh token? | A credential used to obtain new access tokens | It extends sessions securely. |
| 3372 | What is bearer token? | A token sent as proof of authorization | Whoever possesses it can use it. |
| 3373 | What is OAuth 2.0? | An authorization framework for delegated access | It enables secure resource access. |
| 3374 | What is OpenID Connect? | An identity layer built on OAuth 2.0 | It provides authentication. |
| 3375 | What is identity provider? | A system authenticating users | It issues identity tokens. |
| 3376 | What is IdentityServer? | An OpenID Connect and OAuth framework | It provides identity services. |
| 3377 | What is ASP.NET Core Identity? | A membership system for managing users and authentication | It provides account features. |
| 3378 | What is UserManager<TUser>? | Service managing user accounts | It handles user operations. |
| 3379 | What is RoleManager<TRole>? | Service managing application roles | It manages role data. |
| 3380 | What is password hashing? | Converting passwords into secure hashes | It avoids storing plain passwords. |
| 3381 | What is password salting? | Adding random data before hashing passwords | It prevents rainbow table attacks. |
| 3382 | What is PBKDF2? | A password-based key derivation algorithm | It is used for secure password hashing. |
| 3383 | What is BCrypt? | A password hashing algorithm | It is designed to resist brute force. |
| 3384 | What is Argon2? | A modern password hashing algorithm | It is memory-hard. |
| 3385 | What is CSRF attack? | An attack causing unwanted authenticated requests | Anti-forgery tokens mitigate it. |
| 3386 | What is anti-forgery token? | A token validating legitimate requests | It protects against CSRF. |
| 3387 | What is CORS? | A browser security mechanism controlling cross-origin requests | It defines allowed origins. |
| 3388 | What is CORS policy? | Rules determining allowed cross-origin access | It controls browser requests. |
| 3389 | What is same-origin policy? | Browser restriction preventing cross-origin access | CORS provides controlled exceptions. |
| 3390 | What is security header? | An HTTP header improving browser security | Examples include CSP and HSTS. |
| 3391 | What is HSTS? | HTTP Strict Transport Security | It forces HTTPS usage. |
| 3392 | What is Content Security Policy? | A browser policy controlling allowed content sources | It reduces XSS risk. |
| 3393 | What is XSS attack? | Injecting malicious scripts into web pages | Output encoding prevents it. |
| 3394 | What is SQL injection? | Injecting SQL commands through input | Parameterized queries prevent it. |
| 3395 | What is parameterized query? | A query using parameters instead of string concatenation | It prevents SQL injection. |
| 3396 | What is ORM? | Object-relational mapping technology | It maps objects to database tables. |
| 3397 | What is Entity Framework Core? | Microsoft's ORM for .NET | It provides database access through objects. |
| 3398 | What is DbContext? | The primary EF Core database interaction class | It manages entities and queries. |
| 3399 | What is DbSet<T>? | A collection representing an entity set | It enables database operations. |
| 3400 | What is EF Core change tracker? | A component tracking entity state changes | It manages updates. |
| 3401 | What is EntityState in EF Core? | The current tracking state of an entity | It determines database operations. |
| 3402 | What is Added entity state? | A state indicating a new entity will be inserted | SaveChanges generates an INSERT statement. |
| 3403 | What is Modified entity state? | A state indicating an entity has changed | SaveChanges generates an UPDATE statement. |
| 3404 | What is Deleted entity state? | A state indicating an entity should be removed | SaveChanges generates a DELETE statement. |
| 3405 | What is Unchanged entity state? | A state indicating no tracked changes exist | No update is generated. |
| 3406 | What is Detached entity state? | A state where EF Core is not tracking an entity | Changes are ignored until attached. |
| 3407 | What is SaveChanges()? | A method persisting tracked changes to the database | It executes generated commands. |
| 3408 | What is SaveChangesAsync()? | An asynchronous version of SaveChanges | It avoids blocking threads. |
| 3409 | What is EF Core migration? | A mechanism for evolving database schemas | It tracks schema changes. |
| 3410 | What is migration snapshot? | A representation of the current model state | It helps generate future migrations. |
| 3411 | What is Add-Migration command? | A command creating a new EF migration | It detects model changes. |
| 3412 | What is Update-Database command? | A command applying migrations to a database | It updates schema. |
| 3413 | What is database-first approach? | Creating models from an existing database | Reverse engineering generates classes. |
| 3414 | What is code-first approach? | Defining models in code and generating schema | EF creates the database structure. |
| 3415 | What is model-first approach? | Designing models before generating database objects | It is less common in modern EF Core. |
| 3416 | What is EF Core convention? | Default behavior inferred from naming and types | It reduces configuration. |
| 3417 | What is EF Core data annotation? | Attributes configuring entity behavior | It provides simple mapping rules. |
| 3418 | What is Fluent API? | Programmatic EF Core model configuration | It supports advanced mappings. |
| 3419 | What is OnModelCreating()? | A method configuring the EF model | It uses Fluent API. |
| 3420 | What is entity relationship? | A connection between database entities | Examples include one-to-many relationships. |
| 3421 | What is one-to-one relationship? | A relationship where each entity has one related entity | It uses unique foreign keys. |
| 3422 | What is one-to-many relationship? | A relationship where one entity relates to many others | It is common in relational databases. |
| 3423 | What is many-to-many relationship? | A relationship where both sides have multiple related entities | EF Core supports automatic join tables. |
| 3424 | What is navigation property? | A property representing related entities | It enables object traversal. |
| 3425 | What is foreign key property? | A property storing related entity identity | It links database rows. |
| 3426 | What is principal entity? | The entity containing the primary key in a relationship | The dependent references it. |
| 3427 | What is dependent entity? | The entity containing the foreign key | It depends on the principal. |
| 3428 | What is cascade delete? | Automatically deleting related entities | It maintains referential integrity. |
| 3429 | What is eager loading? | Loading related data immediately with the query | It uses Include(). |
| 3430 | What is lazy loading? | Loading related data when accessed | It may cause extra queries. |
| 3431 | What is explicit loading? | Loading related data manually | It gives control over queries. |
| 3432 | What is Include method? | EF Core method loading related entities | It performs eager loading. |
| 3433 | What is ThenInclude method? | Loading nested related entities | It extends Include chains. |
| 3434 | What is split query? | Executing multiple queries for related data | It avoids large joins. |
| 3435 | What is single query? | Loading related data through one SQL query | It may create large result sets. |
| 3436 | What is tracking query? | A query where EF tracks returned entities | Changes can be saved. |
| 3437 | What is AsNoTracking()? | Disabling entity tracking for a query | It improves read performance. |
| 3438 | What is identity resolution? | Reusing the same entity instance for the same database row | It maintains object consistency. |
| 3439 | What is query projection? | Selecting only required fields into a new shape | It reduces transferred data. |
| 3440 | What is Select projection in EF Core? | LINQ projection translated into SQL selection | It improves query efficiency. |
| 3441 | What is raw SQL query? | Executing custom SQL through EF Core | It handles complex database operations. |
| 3442 | What is FromSql? | EF Core method executing SQL returning entities | It supports raw queries. |
| 3443 | What is ExecuteSql? | EF Core method executing SQL commands without entities | It runs updates or commands. |
| 3444 | What is concurrency token? | A value used to detect conflicting updates | It supports optimistic concurrency. |
| 3445 | What is optimistic concurrency? | Assuming conflicts are rare and detecting them during update | EF Core commonly uses it. |
| 3446 | What is pessimistic concurrency? | Locking data before modification | It prevents concurrent changes. |
| 3447 | What is RowVersion? | A database-generated concurrency value | SQL Server commonly uses it. |
| 3448 | What is DbUpdateConcurrencyException? | Exception thrown when concurrent changes are detected | It indicates update conflicts. |
| 3449 | What is transaction? | A group of database operations executed atomically | It ensures consistency. |
| 3450 | What is EF Core transaction API? | APIs controlling database transactions | It manages commit and rollback. |
| 3451 | What is transaction commit? | Making transaction changes permanent | Committed changes cannot normally be rolled back. |
| 3452 | What is transaction rollback? | Undoing changes made during a transaction | It restores the previous state. |
| 3453 | What is ambient transaction? | A transaction automatically flowing through operations | System.Transactions provides support. |
| 3454 | What is TransactionScope? | A class creating an ambient transaction scope | It simplifies transaction management. |
| 3455 | What is isolation level? | The degree of separation between concurrent transactions | It controls consistency versus performance. |
| 3456 | What is ReadUncommitted isolation? | An isolation level allowing dirty reads | It provides minimal locking. |
| 3457 | What is ReadCommitted isolation? | An isolation level preventing dirty reads | It is commonly used by default. |
| 3458 | What is RepeatableRead isolation? | An isolation level preventing changed reads within a transaction | It provides stronger consistency. |
| 3459 | What is Serializable isolation? | The strictest standard isolation level | It prevents many concurrency anomalies. |
| 3460 | What is Snapshot isolation? | An isolation model using row versions | It reduces locking. |
| 3461 | What is dirty read? | Reading uncommitted changes from another transaction | It can return invalid data. |
| 3462 | What is non-repeatable read? | Reading different values for the same row in one transaction | Another transaction changed the data. |
| 3463 | What is phantom read? | Seeing new rows appear during a transaction | Another transaction inserted matching rows. |
| 3464 | What is N+1 query problem? | Executing many queries instead of one efficient query | It often occurs with lazy loading. |
| 3465 | What is query batching? | Combining multiple database commands together | It reduces round trips. |
| 3466 | What is database connection pooling? | Reusing database connections | It improves performance. |
| 3467 | What is DbConnection? | An abstraction representing a database connection | Providers implement it. |
| 3468 | What is DbCommand? | An abstraction representing a database command | It executes SQL operations. |
| 3469 | What is DbDataReader? | A forward-only database result reader | It provides efficient reads. |
| 3470 | What is ADO.NET? | The low-level .NET database access framework | EF Core builds on lower-level concepts. |
| 3471 | What is SqlConnection? | SQL Server database connection class | It belongs to ADO.NET provider APIs. |
| 3472 | What is SqlCommand? | SQL Server command execution class | It executes SQL statements. |
| 3473 | What is parameterized SQL? | SQL using parameters instead of string concatenation | It prevents injection attacks. |
| 3474 | What is stored procedure? | A database-side executable routine | It encapsulates SQL logic. |
| 3475 | What is database view? | A virtual table based on a query | It simplifies data access. |
| 3476 | What is database index? | A structure improving query lookup speed | It trades storage for performance. |
| 3477 | What is clustered index? | An index determining physical row ordering | Usually only one exists per table. |
| 3478 | What is nonclustered index? | An index storing references to rows | Multiple can exist. |
| 3479 | What is composite index? | An index containing multiple columns | It supports multi-column queries. |
| 3480 | What is index seek? | Efficient lookup using an index | It is usually faster than scanning. |
| 3481 | What is index scan? | Reading many index entries to find data | It may be slower for large tables. |
| 3482 | What is database normalization? | Organizing data to reduce duplication | It improves consistency. |
| 3483 | What is denormalization? | Intentionally duplicating data for performance | It can improve read speed. |
| 3484 | What is primary key? | A unique identifier for table rows | It enforces uniqueness. |
| 3485 | What is alternate key? | A unique key besides the primary key | It provides additional uniqueness. |
| 3486 | What is composite key? | A key consisting of multiple columns | It identifies rows using combined values. |
| 3487 | What is foreign key constraint? | A rule enforcing valid relationships | It maintains referential integrity. |
| 3488 | What is database migration script? | SQL generated to change schema | It applies controlled changes. |
| 3489 | What is seed data? | Initial data inserted into a database | It supports development and testing. |
| 3490 | What is EF Core data seeding? | Defining initial data through EF configuration | It inserts predefined records. |
| 3491 | What is compiled query in EF Core? | A precompiled LINQ query | It improves repeated query performance. |
| 3492 | What is EF.CompileQuery()? | API creating compiled queries | It reduces query translation overhead. |
| 3493 | What is global query filter? | A filter automatically applied to queries | It is useful for soft delete and multi-tenancy. |
| 3494 | What is soft delete? | Marking data as deleted instead of removing it | It preserves history. |
| 3495 | What is shadow property? | An EF Core property not defined in the CLR class | EF manages it internally. |
| 3496 | What is owned entity type? | An entity type controlled by its owner | It models dependent value objects. |
| 3497 | What is value converter? | A component converting values during persistence | It maps custom types to database types. |
| 3498 | What is value comparer? | A component defining comparison behavior for values | It supports change tracking. |
| 3499 | What is interceptors in EF Core? | Components observing or modifying EF operations | They add cross-cutting behavior. |
| 3500 | What is DbContext pooling? | Reusing DbContext instances | It reduces allocation overhead. |
| 3501 | What is ASP.NET Core Razor Pages? | A page-based web UI framework | It organizes code around pages instead of controllers. |
| 3502 | What is Razor view engine? | A templating engine combining HTML and C# | It generates dynamic web pages. |
| 3503 | What is Razor syntax? | The syntax for embedding C# into markup | It uses the @ symbol. |
| 3504 | What is Razor PageModel? | A class containing page logic | It separates logic from markup. |
| 3505 | What is Razor page handler? | A method handling page requests | Examples include OnGet and OnPost. |
| 3506 | What is MVC pattern? | A pattern separating model, view, and controller responsibilities | It structures web applications. |
| 3507 | What is Model in MVC? | The application data and business logic representation | It represents domain information. |
| 3508 | What is View in MVC? | The presentation layer generating UI | It displays model data. |
| 3509 | What is Controller in MVC? | A component handling requests and coordinating responses | It connects models and views. |
| 3510 | What is ViewData? | A dictionary passing data from controller to view | It stores temporary view data. |
| 3511 | What is ViewBag? | A dynamic wrapper around ViewData | It provides simpler syntax. |
| 3512 | What is TempData? | A storage mechanism surviving one redirect | It uses session or cookies. |
| 3513 | What is strongly typed view? | A view associated with a specific model type | It provides compile-time checking. |
| 3514 | What is partial view? | A reusable view fragment | It reduces duplicated markup. |
| 3515 | What is view component? | A reusable UI component with logic | It is more powerful than partial views. |
| 3516 | What is tag helper? | A server-side component transforming HTML elements | It improves Razor readability. |
| 3517 | What is custom tag helper? | A user-defined HTML transformation component | It extends Razor features. |
| 3518 | What is HTML helper? | A helper generating HTML elements in Razor | It simplifies markup creation. |
| 3519 | What is layout page? | A shared Razor template | It provides common page structure. |
| 3520 | What is section in Razor? | A placeholder filled by child views | It allows customization of layouts. |
| 3521 | What is antiforgery validation? | Checking request tokens against CSRF attacks | It protects form submissions. |
| 3522 | What is Razor encoding? | Automatic HTML escaping of output | It helps prevent XSS. |
| 3523 | What is Html.Raw()? | A method rendering unencoded HTML | It should be used carefully. |
| 3524 | What is ViewComponent invocation? | Calling reusable UI logic from Razor | It renders dynamic components. |
| 3525 | What is MVC area? | A way to organize large applications into sections | It separates features. |
| 3526 | What is action selector? | A component selecting controller actions | It uses routing and metadata. |
| 3527 | What is action constraint? | A rule restricting action selection | It influences routing decisions. |
| 3528 | What is action name selector? | Selecting actions by name | It affects endpoint matching. |
| 3529 | What is controller factory? | A component creating controller instances | It integrates with dependency injection. |
| 3530 | What is controller activator? | A component activating controllers | It manages controller creation. |
| 3531 | What is API explorer? | A service describing API endpoints | It supports documentation generation. |
| 3532 | What is ApiExplorerSettings attribute? | Attribute controlling API explorer visibility | It affects documentation output. |
| 3533 | What is MVC convention? | Default behavior based on naming rules | It reduces configuration. |
| 3534 | What is application model in MVC? | A representation of controllers and actions | It enables customization. |
| 3535 | What is application model convention? | A rule modifying MVC application metadata | It customizes behavior globally. |
| 3536 | What is IActionConstraint? | Interface defining action selection rules | It influences endpoint matching. |
| 3537 | What is IApplicationModelConvention? | Interface modifying MVC application model | It applies conventions. |
| 3538 | What is view discovery? | Process finding Razor views | It follows naming conventions. |
| 3539 | What is Razor compilation? | Compiling Razor files into executable code | It improves runtime performance. |
| 3540 | What is runtime compilation? | Compiling Razor changes while application runs | It helps development scenarios. |
| 3541 | What is Blazor? | A .NET web UI framework using C# | It supports client and server rendering. |
| 3542 | What is Blazor component? | A reusable UI unit in Blazor | It contains markup and logic. |
| 3543 | What is Razor component? | The component model used by Blazor | It uses Razor syntax. |
| 3544 | What is component parameter? | Data passed into a Blazor component | It configures component behavior. |
| 3545 | What is EventCallback? | A mechanism for component event communication | It notifies parent components. |
| 3546 | What is component lifecycle? | The sequence of component initialization and rendering events | It controls component behavior. |
| 3547 | What is OnInitializedAsync()? | A Blazor lifecycle method for initialization | It runs during component setup. |
| 3548 | What is OnParametersSetAsync()? | A lifecycle method called when parameters change | It reacts to updates. |
| 3549 | What is ShouldRender()? | A method controlling component rendering | It can optimize UI updates. |
| 3550 | What is StateHasChanged()? | A method requesting component re-rendering | It updates the UI. |
| 3551 | What is Blazor render tree? | A representation of component UI structure | It is used during rendering. |
| 3552 | What is Blazor diffing algorithm? | A process comparing render trees for changes | It minimizes DOM updates. |
| 3553 | What is Blazor Server? | A Blazor hosting model running components on the server | It communicates through SignalR. |
| 3554 | What is Blazor WebAssembly? | A Blazor hosting model running .NET in the browser | It executes client-side. |
| 3555 | What is Blazor hybrid? | A model hosting Blazor components inside native applications | It combines web and desktop technologies. |
| 3556 | What is SignalR? | A framework for real-time communication | It enables server-to-client updates. |
| 3557 | What is SignalR hub? | A high-level communication endpoint | It manages client connections. |
| 3558 | What is Hub class? | A base class for creating SignalR hubs | It defines client communication methods. |
| 3559 | What is SignalR connection? | A communication link between client and server | It enables real-time messaging. |
| 3560 | What is SignalR group? | A collection of connected clients | Messages can target groups. |
| 3561 | What is SignalR client method? | A method invoked on connected clients | It sends server notifications. |
| 3562 | What is SignalR strongly typed hub? | A hub using interfaces for client methods | It provides compile-time checking. |
| 3563 | What is SignalR backplane? | A mechanism synchronizing messages across servers | It supports scale-out deployments. |
| 3564 | What is WebSocket? | A protocol providing full-duplex communication | SignalR can use it as transport. |
| 3565 | What is Server-Sent Events? | A protocol sending server updates over HTTP | It supports one-way streaming. |
| 3566 | What is long polling? | A technique keeping HTTP requests open for updates | It simulates real-time communication. |
| 3567 | What is gRPC? | A high-performance RPC framework | It uses HTTP/2 and Protocol Buffers. |
| 3568 | What is gRPC service? | A service exposing remote procedures | Clients call methods remotely. |
| 3569 | What is Protocol Buffers? | A binary serialization format | It is used by gRPC. |
| 3570 | What is .proto file? | A file defining gRPC service contracts | It generates client and server code. |
| 3571 | What is gRPC channel? | A connection between client and server | It sends RPC calls. |
| 3572 | What is unary RPC? | A request-response gRPC call | It resembles normal method calls. |
| 3573 | What is server streaming RPC? | An RPC where server sends multiple responses | It supports streaming data. |
| 3574 | What is client streaming RPC? | An RPC where client sends multiple requests | It supports continuous input. |
| 3575 | What is bidirectional streaming RPC? | An RPC allowing both sides to stream messages | It supports real-time communication. |
| 3576 | What is gRPC interceptor? | A component running around RPC calls | It adds cross-cutting behavior. |
| 3577 | What is HTTP/2? | A newer HTTP protocol with multiplexing support | gRPC commonly uses it. |
| 3578 | What is HTTP/3? | A modern HTTP protocol using QUIC | It improves transport performance. |
| 3579 | What is QUIC? | A transport protocol built over UDP | It supports HTTP/3. |
| 3580 | What is reverse proxy load balancing? | Distributing requests among application instances | It improves scalability. |
| 3581 | What is sticky session? | Routing a client repeatedly to the same server | It maintains server state. |
| 3582 | What is stateless application? | An application storing no client session state locally | It scales more easily. |
| 3583 | What is distributed cache? | A cache shared across application instances | It supports scaled deployments. |
| 3584 | What is IDistributedCache? | .NET abstraction for distributed caching | It supports multiple providers. |
| 3585 | What is memory cache? | An in-process cache stored in application memory | It is fast but local. |
| 3586 | What is IMemoryCache? | .NET interface for memory caching | It stores temporary data. |
| 3587 | What is cache expiration? | The process of removing cached data after a period | It controls freshness. |
| 3588 | What is absolute expiration? | Cache expiration at a fixed time | It ignores access frequency. |
| 3589 | What is sliding expiration? | Cache expiration extended when accessed | It keeps active items alive. |
| 3590 | What is cache stampede? | Many requests rebuilding the same expired cache entry | It can overload systems. |
| 3591 | What is cache aside pattern? | A pattern where application manages cache reads and writes | It is commonly used. |
| 3592 | What is write-through cache? | A cache writing data and storage together | It keeps data synchronized. |
| 3593 | What is write-behind cache? | A cache writing to storage asynchronously later | It improves write performance. |
| 3594 | What is Redis? | A distributed in-memory data store | It is often used for caching. |
| 3595 | What is session state? | Temporary user-specific data storage | It can use distributed storage. |
| 3596 | What is cookie storage? | Client-side key-value storage using HTTP cookies | It stores small amounts of data. |
| 3597 | What is distributed session? | Session storage shared across servers | It supports load balancing. |
| 3598 | What is data protection API? | .NET service for protecting sensitive data | It provides encryption and key management. |
| 3599 | What is IDataProtector? | Service creating protected data payloads | It encrypts and decrypts data. |
| 3600 | What is key ring in ASP.NET Core? | Storage containing data protection keys | It enables consistent encryption across instances. |
| 3601 | What is ASP.NET Core rate limiting? | A mechanism controlling request frequency | It protects applications from excessive traffic. |
| 3602 | What is fixed window rate limiter? | A limiter allowing a fixed number of requests per time period | It resets after each window. |
| 3603 | What is sliding window rate limiter? | A limiter using overlapping time windows | It provides smoother request control. |
| 3604 | What is token bucket rate limiter? | A limiter using refillable tokens | It allows controlled bursts. |
| 3605 | What is concurrency limiter? | A limiter restricting simultaneous operations | It controls active workloads. |
| 3606 | What is backpressure? | A mechanism slowing producers when consumers cannot keep up | It prevents overload. |
| 3607 | What is resilience pattern? | A design approach improving system reliability | Examples include retries and circuit breakers. |
| 3608 | What is Polly? | A .NET resilience library | It provides fault-handling policies. |
| 3609 | What is retry policy? | A policy repeating failed operations | It handles transient failures. |
| 3610 | What is exponential backoff? | Increasing delay between retries | It reduces repeated failures. |
| 3611 | What is jitter in retries? | Random delay added to retry timing | It prevents synchronized retries. |
| 3612 | What is circuit breaker pattern? | A pattern stopping calls after repeated failures | It prevents cascading failures. |
| 3613 | What is circuit breaker open state? | A state where calls are blocked | It allows recovery time. |
| 3614 | What is circuit breaker closed state? | A state where calls flow normally | Failures are monitored. |
| 3615 | What is circuit breaker half-open state? | A state testing whether recovery occurred | It allows limited requests. |
| 3616 | What is timeout policy? | A policy limiting operation duration | It prevents indefinite waits. |
| 3617 | What is fallback policy? | A policy providing alternative behavior after failure | It improves resilience. |
| 3618 | What is bulkhead pattern? | A pattern isolating failures between resources | It limits failure spread. |
| 3619 | What is hedging strategy? | Sending parallel requests and using the fastest result | It reduces latency in some cases. |
| 3620 | What is transient fault? | A temporary failure that may recover | Retries can handle it. |
| 3621 | What is idempotent operation? | An operation producing the same result when repeated | It is safer for retries. |
| 3622 | What is distributed transaction? | A transaction spanning multiple systems | It coordinates multiple resources. |
| 3623 | What is saga pattern? | A sequence of local transactions with compensating actions | It replaces distributed transactions. |
| 3624 | What is compensating transaction? | An operation undoing a previous action logically | It restores business consistency. |
| 3625 | What is message queue? | A system storing messages for asynchronous processing | It decouples components. |
| 3626 | What is message broker? | A service routing and storing messages | It enables communication between services. |
| 3627 | What is Azure Service Bus? | A cloud message broker | It supports enterprise messaging. |
| 3628 | What is RabbitMQ? | A message broker implementing AMQP | It supports queues and exchanges. |
| 3629 | What is Apache Kafka? | A distributed event streaming platform | It handles high-throughput messaging. |
| 3630 | What is event-driven architecture? | An architecture based on producing and consuming events | It promotes loose coupling. |
| 3631 | What is domain event? | An event representing something important in a domain | It communicates state changes. |
| 3632 | What is event sourcing? | Storing state changes as events | State is reconstructed from history. |
| 3633 | What is CQRS? | Separating command and query responsibilities | It optimizes read and write models. |
| 3634 | What is command? | A request to change application state | It represents an action. |
| 3635 | What is query? | A request to retrieve data | It does not modify state. |
| 3636 | What is MediatR? | A .NET mediator implementation library | It decouples request handling. |
| 3637 | What is mediator handler? | A component processing mediator requests | It contains operation logic. |
| 3638 | What is pipeline behavior in MediatR? | A component running around handlers | It adds cross-cutting logic. |
| 3639 | What is clean architecture? | An architecture separating business logic from external concerns | It improves maintainability. |
| 3640 | What is hexagonal architecture? | An architecture using ports and adapters | It isolates business logic. |
| 3641 | What is domain-driven design? | An approach modeling software around business domains | It emphasizes domain concepts. |
| 3642 | What is bounded context? | A defined boundary around a domain model | It prevents model conflicts. |
| 3643 | What is aggregate in DDD? | A cluster of domain objects with one root | It maintains consistency boundaries. |
| 3644 | What is aggregate root? | The entry point controlling an aggregate | It protects invariants. |
| 3645 | What is entity in DDD? | An object with a unique identity | Identity remains over time. |
| 3646 | What is value object? | An immutable object defined by its values | It has no identity. |
| 3647 | What is domain service? | A service containing domain logic not belonging to an entity | It represents domain operations. |
| 3648 | What is repository pattern? | An abstraction for data access | It separates persistence concerns. |
| 3649 | What is unit of work pattern? | A pattern coordinating multiple changes as one operation | EF Core DbContext resembles it. |
| 3650 | What is specification pattern? | A pattern encapsulating query rules | It improves reusable business logic. |
| 3651 | What is microservice architecture? | An architecture where applications are split into independent services | Each service owns a specific capability. |
| 3652 | What is monolithic architecture? | An architecture where all functionality exists in one application | It is simpler to deploy initially. |
| 3653 | What is modular monolith? | A monolithic application organized into independent modules | It combines simplicity with separation. |
| 3654 | What is service boundary? | A defined separation between application responsibilities | It prevents excessive coupling. |
| 3655 | What is API gateway? | A service acting as a single entry point for APIs | It handles routing and cross-cutting concerns. |
| 3656 | What is backend-for-frontend pattern? | A dedicated backend tailored for a specific client | It optimizes client communication. |
| 3657 | What is service discovery? | Finding available service instances dynamically | It supports distributed systems. |
| 3658 | What is health-based service discovery? | Discovery using service health information | It avoids unhealthy instances. |
| 3659 | What is containerization? | Packaging applications with their dependencies | It improves deployment consistency. |
| 3660 | What is Docker? | A platform for building and running containers | It isolates applications. |
| 3661 | What is Docker image? | A packaged application template | Containers are created from images. |
| 3662 | What is Docker container? | A running instance of an image | It executes isolated processes. |
| 3663 | What is Dockerfile? | A file describing how to build an image | It automates image creation. |
| 3664 | What is container registry? | A repository storing container images | It distributes images. |
| 3665 | What is Kubernetes? | A platform for orchestrating containers | It manages deployment and scaling. |
| 3666 | What is Kubernetes pod? | The smallest deployable Kubernetes unit | It contains one or more containers. |
| 3667 | What is Kubernetes service? | A networking abstraction exposing pods | It provides stable access. |
| 3668 | What is Kubernetes deployment? | A resource managing application replicas | It maintains desired state. |
| 3669 | What is horizontal scaling? | Increasing application instances | It improves capacity. |
| 3670 | What is vertical scaling? | Increasing resources of an existing instance | It improves individual performance. |
| 3671 | What is autoscaling? | Automatically adjusting resources based on demand | It optimizes resource usage. |
| 3672 | What is cloud-native application? | An application designed for cloud environments | It uses scalable patterns. |
| 3673 | What is twelve-factor app? | A methodology for building cloud applications | It defines operational principles. |
| 3674 | What is configuration as environment? | Storing configuration outside application code | It improves deployment flexibility. |
| 3675 | What is immutable infrastructure? | Infrastructure replaced rather than modified | It reduces configuration drift. |
| 3676 | What is infrastructure as code? | Managing infrastructure through code definitions | It enables automation. |
| 3677 | What is CI/CD? | Continuous integration and continuous delivery/deployment | It automates software delivery. |
| 3678 | What is continuous integration? | Automatically building and testing code changes | It catches problems early. |
| 3679 | What is continuous delivery? | Keeping software ready for release | Deployment is controlled manually. |
| 3680 | What is continuous deployment? | Automatically releasing successful changes | Releases happen without manual approval. |
| 3681 | What is build pipeline? | Automated steps creating software artifacts | It verifies changes. |
| 3682 | What is deployment pipeline? | Automated process moving software through environments | It manages releases. |
| 3683 | What is artifact? | A build output used for deployment | Examples include packages and containers. |
| 3684 | What is semantic versioning? | A versioning scheme using major, minor, and patch numbers | It communicates compatibility. |
| 3685 | What is NuGet package? | A reusable .NET library package | It distributes dependencies. |
| 3686 | What is NuGet package manager? | A tool managing .NET dependencies | It restores and installs packages. |
| 3687 | What is package reference? | A project dependency declaration | It identifies required packages. |
| 3688 | What is transitive dependency? | A dependency brought by another dependency | Package managers resolve it automatically. |
| 3689 | What is assembly binding? | The process of locating referenced assemblies | The runtime performs it. |
| 3690 | What is strong-named assembly? | An assembly with a cryptographic identity | It supports version and identity verification. |
| 3691 | What is assembly version? | A version identifier for assemblies | It tracks releases. |
| 3692 | What is file version? | A version associated with the physical file | It is separate from assembly version. |
| 3693 | What is semantic compatibility? | Maintaining expected behavior across versions | It prevents breaking changes. |
| 3694 | What is breaking change? | A modification requiring consumers to update code | It affects compatibility. |
| 3695 | What is backward compatibility? | Ability of newer versions to work with older clients | It eases upgrades. |
| 3696 | What is forward compatibility? | Ability of older software to handle newer data or features | It supports evolution. |
| 3697 | What is feature flag? | A mechanism enabling or disabling features dynamically | It supports controlled releases. |
| 3698 | What is blue-green deployment? | Deployment strategy switching between two environments | It reduces downtime. |
| 3699 | What is canary deployment? | Releasing changes gradually to selected users | It reduces release risk. |
| 3700 | What is rollback deployment? | Returning to a previous stable version | It recovers from failures. |
| 3701 | What is Git? | A distributed version control system | It tracks source code changes. |
| 3702 | What is repository in Git? | A storage location containing version history | It tracks project files. |
| 3703 | What is commit in Git? | A saved snapshot of changes | It records project history. |
| 3704 | What is branch in Git? | A separate line of development | It enables parallel work. |
| 3705 | What is merge in Git? | Combining changes from different branches | It integrates development work. |
| 3706 | What is rebase in Git? | Moving commits onto another base branch | It creates a cleaner history. |
| 3707 | What is Git conflict? | A situation where Git cannot automatically merge changes | Manual resolution is required. |
| 3708 | What is pull request? | A request to review and merge changes | It supports collaboration. |
| 3709 | What is code review? | Reviewing source code changes before integration | It improves quality. |
| 3710 | What is static code analysis? | Automatically analyzing source code without execution | It detects potential issues. |
| 3711 | What is Roslyn analyzer? | A .NET compiler-based code analysis tool | It detects coding problems. |
| 3712 | What is compiler warning? | A message about possible code issues | It does not prevent compilation by default. |
| 3713 | What is compiler error? | A problem preventing successful compilation | Code cannot build. |
| 3714 | What is nullable reference type? | A C# feature tracking possible null values | It reduces null reference bugs. |
| 3715 | What is nullable annotation context? | The compiler mode controlling nullable analysis | It enables warnings. |
| 3716 | What is null forgiving operator? | The ! operator suppressing nullable warnings | It tells the compiler a value is not null. |
| 3717 | What is null coalescing operator? | The ?? operator providing fallback values | It handles null values. |
| 3718 | What is null conditional operator? | The ?. operator safely accessing members | It avoids null exceptions. |
| 3719 | What is ArgumentNullException? | Exception thrown for null arguments | It validates method inputs. |
| 3720 | What is Guard clause? | An early validation check | It simplifies method logic. |
| 3721 | What is exception filter? | A condition controlling exception handling | It uses when clauses. |
| 3722 | What is custom exception? | A user-defined exception type | It represents specific failures. |
| 3723 | What is exception hierarchy? | The inheritance structure of exception types | All exceptions derive from Exception. |
| 3724 | What is stack trace? | Information showing method call history | It helps diagnose failures. |
| 3725 | What is inner exception? | The original exception causing another exception | It preserves error details. |
| 3726 | What is throw statement? | A statement raising an exception | It transfers control to error handling. |
| 3727 | What is throw expression? | An expression that throws an exception | It can be used inline. |
| 3728 | What is using declaration? | A C# syntax automatically disposing resources | It reduces nesting. |
| 3729 | What is IDisposable? | Interface defining resource cleanup | It provides Dispose(). |
| 3730 | What is IAsyncDisposable? | Interface defining asynchronous cleanup | It provides DisposeAsync(). |
| 3731 | What is await using? | Syntax disposing asynchronous resources | It calls DisposeAsync(). |
| 3732 | What is finalizer? | A method executed before garbage collection cleanup | It releases unmanaged resources. |
| 3733 | What is destructor syntax in C#? | Syntax representing a finalizer | It uses the ~ClassName format. |
| 3734 | What is SafeHandle? | A wrapper for unmanaged handles | It improves resource safety. |
| 3735 | What is unmanaged resource? | A resource outside .NET garbage collection | Examples include file handles. |
| 3736 | What is managed resource? | Memory controlled by the garbage collector | The runtime manages cleanup. |
| 3737 | What is Dispose pattern? | A standard pattern for releasing resources | It combines deterministic and final cleanup. |
| 3738 | What is GC.SuppressFinalize()? | Method preventing finalizer execution | It improves disposal performance. |
| 3739 | What is garbage collection generation? | A grouping of objects by lifetime | It optimizes collection. |
| 3740 | What is Gen 0 collection? | Collection of short-lived objects | It is the most frequent. |
| 3741 | What is Gen 1 collection? | Collection of medium-lived objects | It bridges short and long-lived objects. |
| 3742 | What is Gen 2 collection? | Collection of long-lived objects | It is more expensive. |
| 3743 | What is Large Object Heap? | Heap storing large allocations | It has special collection behavior. |
| 3744 | What is LOH compaction? | Rearranging large object heap memory | It reduces fragmentation. |
| 3745 | What is pinned object? | An object prevented from moving by the GC | It supports unmanaged interoperability. |
| 3746 | What is GC pause? | A period where application threads stop during collection | It affects latency. |
| 3747 | What is workstation GC? | Garbage collector optimized for client applications | It prioritizes responsiveness. |
| 3748 | What is server GC? | Garbage collector optimized for throughput | It uses multiple threads. |
| 3749 | What is background GC? | Concurrent garbage collection of older generations | It reduces pauses. |
| 3750 | What is GC latency mode? | A setting controlling garbage collection behavior | It balances throughput and responsiveness. |
| 3751 | What is SustainedLowLatency GC mode? | A GC mode minimizing pauses during long-running operations | It reduces Gen 2 blocking collections. |
| 3752 | What is NoGCRegion? | A mode temporarily preventing garbage collection | It is used for latency-sensitive sections. |
| 3753 | What is GC.TryStartNoGCRegion()? | A method requesting a no-GC region | It reserves memory for uninterrupted execution. |
| 3754 | What is GC.EndNoGCRegion()? | A method ending a no-GC region | It returns to normal GC behavior. |
| 3755 | What is memory pressure? | A condition indicating high allocation demand | It can trigger more frequent collections. |
| 3756 | What is GC.AddMemoryPressure()? | A method informing GC about unmanaged allocations | It improves collection decisions. |
| 3757 | What is GC.RemoveMemoryPressure()? | A method removing previously reported memory pressure | It updates GC accounting. |
| 3758 | What is object resurrection? | Bringing a finalized object back to reachability | It is rarely recommended. |
| 3759 | What is weak reference? | A reference that does not prevent garbage collection | It allows memory-sensitive caching. |
| 3760 | What is WeakReference<T>? | A generic weak reference implementation | It avoids unsafe casting. |
| 3761 | What is ConditionalWeakTable<TKey,TValue>? | A table associating data with objects without preventing collection | It supports object metadata scenarios. |
| 3762 | What is memory leak in managed code? | Memory retained unintentionally by references | Garbage collection cannot remove reachable objects. |
| 3763 | What is event memory leak? | A leak caused by long-lived publishers holding subscribers | Unsubscribing prevents it. |
| 3764 | What is closure memory leak? | A leak caused by captured variables staying referenced | Closures can extend lifetimes. |
| 3765 | What is allocation? | Reserving memory for an object or value | Allocations affect performance. |
| 3766 | What is stack allocation? | Allocating memory on the call stack | It is automatically reclaimed. |
| 3767 | What is heap allocation? | Allocating memory managed by the GC | Objects usually live there. |
| 3768 | What is escape analysis? | Analysis determining whether values leave a scope | It enables optimizations. |
| 3769 | What is object pooling? | Reusing objects instead of allocating new ones | It reduces GC pressure. |
| 3770 | What is ObjectPool<T>? | A .NET abstraction for reusable objects | It supports pooling patterns. |
| 3771 | What is ArrayPool<T>.Shared? | The shared array pooling instance | It reduces array allocations. |
| 3772 | What is MemoryPool<T>? | A pool for reusable memory blocks | It supports high-performance pipelines. |
| 3773 | What is Memory<T>? | A heap-safe memory view type | It works with async scenarios. |
| 3774 | What is ReadOnlyMemory<T>? | A read-only memory view type | It prevents modifications. |
| 3775 | What is ReadOnlySpan<T>? | A read-only stack-only memory view | It avoids allocations. |
| 3776 | What is MemoryMarshal? | An API for advanced memory operations | It bridges managed and unmanaged memory. |
| 3777 | What is CollectionsMarshal? | An API exposing collection internals safely in limited scenarios | It improves performance. |
| 3778 | What is Unsafe class? | A class providing low-level memory operations | It bypasses safety checks. |
| 3779 | What is stackalloc? | A keyword allocating memory on the stack | It creates stack-based buffers. |
| 3780 | What is fixed statement? | A statement preventing GC movement of variables | It enables pointer access. |
| 3781 | What is pointer type? | A type storing a memory address | It is used in unsafe code. |
| 3782 | What is unsafe context? | A context allowing pointer operations | It requires compiler permission. |
| 3783 | What is interop? | Communication between managed and unmanaged code | It enables native API usage. |
| 3784 | What is P/Invoke? | A mechanism calling native functions from managed code | It uses platform invoke declarations. |
| 3785 | What is DllImportAttribute? | An attribute declaring external native methods | It enables P/Invoke. |
| 3786 | What is LibraryImportAttribute? | A source-generated alternative to DllImport | It improves performance. |
| 3787 | What is COM interop? | Communication with Component Object Model components | It integrates with Windows technologies. |
| 3788 | What is marshalling? | Converting data between managed and unmanaged formats | It enables interop calls. |
| 3789 | What is blittable type? | A type with identical managed and unmanaged memory layout | It avoids copying during interop. |
| 3790 | What is native library loading? | Loading external compiled libraries | The runtime resolves native dependencies. |
| 3791 | What is NativeLibrary class? | API for loading native libraries dynamically | It supports runtime interop. |
| 3792 | What is function pointer in C#? | A low-level reference to a method address | It avoids delegate overhead. |
| 3793 | What is delegate marshalling? | Converting delegates for native callbacks | It enables managed callbacks. |
| 3794 | What is unmanaged callback? | Native code calling managed code | Interop scenarios use it. |
| 3795 | What is source generator? | A compiler feature generating code during compilation | It improves performance and tooling. |
| 3796 | What is incremental source generator? | A source generator processing only changed inputs | It improves build performance. |
| 3797 | What is GeneratorAttribute? | An attribute marking generated-related behavior | It supports generator tooling. |
| 3798 | What is partial class generation? | Adding generated code to existing classes | Source generators commonly use it. |
| 3799 | What is Roslyn? | The .NET compiler platform | It enables code analysis and generation. |
| 3800 | What is syntax tree in Roslyn? | A tree representation of source code | Analyzers inspect it. |
| 3801 | What is semantic model in Roslyn? | A representation of code meaning and symbols | It allows analyzers to understand types and references. |
| 3802 | What is Roslyn symbol? | A representation of a code element such as a type or method | It describes program structure. |
| 3803 | What is syntax node? | A single element in a syntax tree | It represents source code parts. |
| 3804 | What is syntax token? | A lexical element in source code | Examples include keywords and identifiers. |
| 3805 | What is syntax trivia? | Non-code elements like whitespace and comments | Roslyn preserves formatting information. |
| 3806 | What is analyzer in .NET? | A tool inspecting code during compilation | It reports diagnostics. |
| 3807 | What is code fix provider? | A tool providing automatic fixes for diagnostics | It integrates with IDEs. |
| 3808 | What is diagnostic in Roslyn? | A reported code issue or suggestion | It contains severity and location information. |
| 3809 | What is analyzer rule? | A defined check performed by an analyzer | It enforces coding standards. |
| 3810 | What is EditorConfig? | A file configuring coding styles and analyzer rules | It standardizes development settings. |
| 3811 | What is .NET SDK? | A collection of tools for building .NET applications | It includes compilers and CLI tools. |
| 3812 | What is dotnet CLI? | Command-line interface for .NET development | It manages projects and builds. |
| 3813 | What is dotnet build? | A command compiling a .NET project | It produces build output. |
| 3814 | What is dotnet run? | A command building and executing an application | It starts the project. |
| 3815 | What is dotnet test? | A command executing tests | It runs test projects. |
| 3816 | What is dotnet publish? | A command preparing an application for deployment | It creates deployable files. |
| 3817 | What is dotnet restore? | A command downloading project dependencies | It restores NuGet packages. |
| 3818 | What is dotnet pack? | A command creating NuGet packages | It packages libraries. |
| 3819 | What is dotnet clean? | A command removing build outputs | It cleans generated files. |
| 3820 | What is SDK-style project? | Modern .NET project format | It simplifies project files. |
| 3821 | What is project file? | A file describing project configuration | Modern .NET uses .csproj files. |
| 3822 | What is TargetFramework? | The framework version a project targets | It controls available APIs. |
| 3823 | What is TargetFrameworks? | A project setting supporting multiple targets | It enables multi-targeting. |
| 3824 | What is runtime identifier? | An identifier describing target operating system and architecture | It controls platform-specific publishing. |
| 3825 | What is self-contained deployment? | Deployment including the .NET runtime | The target machine does not need .NET installed. |
| 3826 | What is framework-dependent deployment? | Deployment requiring an installed .NET runtime | It produces smaller output. |
| 3827 | What is single-file deployment? | Packaging an application into one executable file | It simplifies distribution. |
| 3828 | What is trimming? | Removing unused assemblies and members during publishing | It reduces application size. |
| 3829 | What is Native AOT? | Ahead-of-time compilation to native code | It improves startup and reduces runtime dependency. |
| 3830 | What is ReadyToRun? | Precompiled assembly code for faster startup | It reduces JIT work. |
| 3831 | What is JIT compilation? | Runtime conversion of IL into native machine code | It executes .NET code. |
| 3832 | What is tiered compilation? | A JIT strategy optimizing code over time | It balances startup and performance. |
| 3833 | What is tier 0 compilation? | Quick initial JIT compilation | It improves startup time. |
| 3834 | What is tier 1 compilation? | Optimized JIT compilation | It improves runtime performance. |
| 3835 | What is profile-guided optimization? | Optimization using runtime execution data | It improves generated code. |
| 3836 | What is IL code? | Intermediate language produced by the compiler | The CLR executes it through JIT. |
| 3837 | What is Common Intermediate Language? | Standard intermediate language for .NET | It enables language interoperability. |
| 3838 | What is metadata table? | Runtime information stored in assemblies | It describes types and members. |
| 3839 | What is manifest in assembly? | Assembly metadata describing identity and references | It defines assembly contents. |
| 3840 | What is module in .NET? | A compiled unit within an assembly | Assemblies can contain modules. |
| 3841 | What is PE file? | Portable Executable format used by .NET assemblies | It contains managed code and metadata. |
| 3842 | What is CLR host? | A component starting and managing the runtime | It loads .NET applications. |
| 3843 | What is CoreCLR? | The open-source .NET runtime implementation | It executes .NET applications. |
| 3844 | What is Mono runtime? | A .NET runtime implementation used historically for cross-platform scenarios | It supports managed execution. |
| 3845 | What is Native runtime? | Runtime environment executing compiled native code | It differs from managed execution. |
| 3846 | What is runtime host? | Software responsible for launching the CLR | It initializes execution. |
| 3847 | What is AssemblyLoadContext? | A mechanism for loading assemblies dynamically | It supports isolation and unloading. |
| 3848 | What is collectible AssemblyLoadContext? | A load context whose assemblies can be unloaded | It enables plugin unloading. |
| 3849 | What is plugin architecture? | A design allowing external extensions | It uses dynamic loading. |
| 3850 | What is MEF? | Managed Extensibility Framework | It supports plugin composition. |
| 3851 | What is reflection? | Inspecting and interacting with types at runtime | It enables dynamic behavior. |
| 3852 | What is Type class? | A representation of a runtime type | It provides reflection information. |
| 3853 | What is Activator class? | A class creating objects dynamically | It uses runtime type information. |
| 3854 | What is Activator.CreateInstance()? | A method creating instances using reflection | It invokes constructors dynamically. |
| 3855 | What is ConstructorInfo? | Reflection representation of a constructor | It allows constructor inspection and invocation. |
| 3856 | What is MethodInfo? | Reflection representation of a method | It provides method metadata. |
| 3857 | What is PropertyInfo? | Reflection representation of a property | It allows property inspection and access. |
| 3858 | What is FieldInfo? | Reflection representation of a field | It describes field metadata. |
| 3859 | What is EventInfo? | Reflection representation of an event | It describes event metadata. |
| 3860 | What is MemberInfo? | Base reflection type for members | Methods, properties, and fields inherit from it. |
| 3861 | What is BindingFlags? | Flags controlling reflection searches | It filters members. |
| 3862 | What is reflection performance cost? | Runtime overhead caused by dynamic inspection | Caching improves performance. |
| 3863 | What is metadata-only loading? | Loading assembly information without executing code | It supports inspection scenarios. |
| 3864 | What is MetadataLoadContext? | An API for inspecting assemblies without loading them for execution | It isolates reflection analysis. |
| 3865 | What is dynamic keyword? | A keyword enabling runtime binding | Type checks happen during execution. |
| 3866 | What is Dynamic Language Runtime? | Runtime infrastructure supporting dynamic languages | It powers dynamic binding. |
| 3867 | What is ExpandoObject? | A dynamic object allowing runtime members | It supports flexible structures. |
| 3868 | What is DynamicObject? | Base class for custom dynamic behavior | It overrides dynamic operations. |
| 3869 | What is IDynamicMetaObjectProvider? | Interface enabling custom dynamic binding | It supports DLR integration. |
| 3870 | What is duck typing? | Treating objects by available behavior rather than declared type | Dynamic languages commonly use it. |
| 3871 | What is generic type? | A type parameterized by one or more types | It enables reusable code. |
| 3872 | What is generic method? | A method using type parameters | It supports type-safe reuse. |
| 3873 | What is generic constraint? | A restriction on allowed generic types | It improves compile-time checking. |
| 3874 | What is where T : class constraint? | Constraint requiring reference types | It restricts generic arguments. |
| 3875 | What is where T : struct constraint? | Constraint requiring value types | It restricts generic arguments. |
| 3876 | What is where T : new() constraint? | Constraint requiring a public parameterless constructor | It allows object creation. |
| 3877 | What is where T : base class constraint? | Constraint requiring inheritance from a base type | It limits valid types. |
| 3878 | What is generic covariance? | Allowing more specific generic types to be used as less specific types | It applies to output types. |
| 3879 | What is generic contravariance? | Allowing less specific types to be used as more specific types | It applies to input types. |
| 3880 | What is invariant generic type? | A generic type without variance conversion | Most generic classes are invariant. |
| 3881 | What is IEnumerable<out T>? | A covariant generic interface | It supports safe output conversion. |
| 3882 | What is IComparer<in T>? | A contravariant generic interface | It supports flexible comparisons. |
| 3883 | What is generic specialization? | Creating a constructed generic type from arguments | The runtime handles closed types. |
| 3884 | What is open generic type? | A generic type without specified arguments | Example: List<T>. |
| 3885 | What is closed generic type? | A generic type with concrete arguments | Example: List<int>. |
| 3886 | What is generic type definition? | The original generic declaration | It defines type parameters. |
| 3887 | What is constructed type? | A type created from a generic definition | It has actual type arguments. |
| 3888 | What is boxing of generic values? | Converting value types in generic contexts to objects | It can create allocations. |
| 3889 | What is generic math? | Numeric operations supported through generic interfaces | Introduced with static abstract members. |
| 3890 | What is INumber<TSelf>? | A generic math interface for numeric types | It enables generic arithmetic. |
| 3891 | What is unmanaged generic constraint? | Constraint allowing only unmanaged types | It enables pointer-related operations. |
| 3892 | What is notnull generic constraint? | Constraint preventing nullable type arguments | It improves null safety. |
| 3893 | What is default literal? | A shorthand for default values | It infers the target type. |
| 3894 | What is target-typed new expression? | Creating objects without repeating the type name | It reduces syntax. |
| 3895 | What is implicit object creation? | Using new() without specifying a type | The compiler infers the type. |
| 3896 | What is collection expression? | A C# syntax for creating collections | It uses square brackets. |
| 3897 | What is spread operator in C# collection expressions? | Syntax expanding another collection into a collection expression | It uses .. |
| 3898 | What is required member? | A member that must be initialized during object creation | It improves initialization safety. |
| 3899 | What is RequiredMemberAttribute? | Metadata marking required members | The compiler uses it. |
| 3900 | What is init accessor? | A property setter usable only during initialization | It supports immutable objects. |
| 3901 | What is record type in C#? | A reference type designed for immutable data models | It provides value-based equality. |
| 3902 | What is record struct? | A value type record | It combines structs with record features. |
| 3903 | What is positional record? | A record using primary constructor parameters | It generates properties automatically. |
| 3904 | What is with expression? | A syntax creating a copy with modified values | It is commonly used with records. |
| 3905 | What is value equality? | Comparing objects based on their contents | Records support it automatically. |
| 3906 | What is reference equality? | Comparing whether two references point to the same object | It uses object identity. |
| 3907 | What is equality contract in records? | A mechanism ensuring compatible record equality | It supports inheritance scenarios. |
| 3908 | What is GetHashCode()? | A method producing a hash value for an object | It supports hash collections. |
| 3909 | What is IEquatable<T>? | An interface defining strongly typed equality comparison | It improves equality performance. |
| 3910 | What is operator overloading? | Defining custom behavior for operators | It enables natural syntax for custom types. |
| 3911 | What is user-defined conversion? | A custom conversion between types | It uses implicit or explicit operators. |
| 3912 | What is implicit conversion? | A conversion performed automatically | It should not lose information. |
| 3913 | What is explicit conversion? | A conversion requiring casting syntax | It may involve data loss. |
| 3914 | What is checked context? | A context detecting arithmetic overflow | It throws exceptions on overflow. |
| 3915 | What is unchecked context? | A context allowing overflow behavior | It ignores overflow exceptions. |
| 3916 | What is checked operator? | An operator enforcing overflow checking | It improves numeric safety. |
| 3917 | What is pattern matching? | A feature for testing and extracting values from objects | It simplifies conditional logic. |
| 3918 | What is type pattern? | A pattern matching based on object type | It checks runtime type. |
| 3919 | What is property pattern? | A pattern matching object properties | It inspects values. |
| 3920 | What is positional pattern? | A pattern matching deconstructed values | It uses Deconstruct methods. |
| 3921 | What is relational pattern? | A pattern comparing values with operators | Examples include > and <. |
| 3922 | What is logical pattern? | A pattern combining patterns using and, or, and not | It creates complex conditions. |
| 3923 | What is list pattern? | A pattern matching collection elements | It works with arrays and lists. |
| 3924 | What is switch expression? | An expression-based switch construct | It returns values directly. |
| 3925 | What is switch statement? | A control structure selecting cases | It executes matching branches. |
| 3926 | What is discard pattern? | A pattern matching any value without storing it | It uses \_. |
| 3927 | What is var pattern? | A pattern capturing a value into a variable | It always matches. |
| 3928 | What is recursive pattern? | A pattern combining nested matching rules | It handles complex objects. |
| 3929 | What is local function? | A method declared inside another method | It improves encapsulation. |
| 3930 | What is static local function? | A local function without captured variables | It avoids closure allocations. |
| 3931 | What is lambda expression? | An anonymous function expression | It creates delegates. |
| 3932 | What is expression lambda? | A lambda with a single expression body | It returns the expression result. |
| 3933 | What is statement lambda? | A lambda containing multiple statements | It uses braces. |
| 3934 | What is lambda capture? | Capturing variables from an outer scope | It creates closures. |
| 3935 | What is closure? | A generated object storing captured variables | It extends variable lifetime. |
| 3936 | What is anonymous method? | A method without a name | It creates delegates inline. |
| 3937 | What is delegate invocation list? | A list of methods attached to a delegate | Multicast delegates use it. |
| 3938 | What is multicast delegate? | A delegate referencing multiple methods | All methods are invoked. |
| 3939 | What is Action delegate? | A delegate returning void | It represents operations. |
| 3940 | What is Func delegate? | A delegate returning a value | It represents functions. |
| 3941 | What is Predicate delegate? | A delegate returning bool | It represents conditions. |
| 3942 | What is method group conversion? | Converting method references into delegates | It simplifies delegate creation. |
| 3943 | What is event accessor? | Custom add and remove logic for events | It controls subscriptions. |
| 3944 | What is custom event? | An event with manually implemented accessors | It provides advanced behavior. |
| 3945 | What is delegate covariance? | Allowing return type compatibility in delegates | It supports flexible assignment. |
| 3946 | What is delegate contravariance? | Allowing parameter type compatibility in delegates | It supports broader handlers. |
| 3947 | What is anonymous object? | A compiler-generated type for temporary data | It is commonly used in LINQ projections. |
| 3948 | What is tuple type? | A lightweight type grouping multiple values | It supports multiple return values. |
| 3949 | What is ValueTuple? | A struct-based tuple implementation | It avoids heap allocation. |
| 3950 | What is tuple deconstruction? | Assigning tuple elements to separate variables | It improves readability. |
| 3951 | What is deconstruction in C#? | A feature extracting values from an object into variables | It uses Deconstruct methods. |
| 3952 | What is Deconstruct method? | A method defining how an object can be split into values | It supports deconstruction syntax. |
| 3953 | What is primary constructor? | A constructor declared directly in a type declaration | It simplifies initialization. |
| 3954 | What is constructor chaining? | Calling one constructor from another constructor | It avoids duplicated initialization code. |
| 3955 | What is static constructor? | A constructor initializing static members | It runs once per type. |
| 3956 | What is instance constructor? | A constructor initializing object instances | It runs when objects are created. |
| 3957 | What is private constructor? | A constructor inaccessible outside the type | It controls object creation. |
| 3958 | What is copy constructor? | A constructor creating an object from another object | It copies state. |
| 3959 | What is default constructor? | A parameterless constructor | The compiler may generate one. |
| 3960 | What is object initializer? | Syntax initializing object properties during creation | It improves readability. |
| 3961 | What is collection initializer? | Syntax initializing collections during creation | It uses Add methods. |
| 3962 | What is index initializer? | Syntax initializing indexed collections | It uses indexer assignments. |
| 3963 | What is field initializer? | Initialization expression assigned to fields | It runs before constructors. |
| 3964 | What is auto-implemented property? | A property with compiler-generated backing storage | It reduces boilerplate. |
| 3965 | What is expression-bodied member? | A member implemented using an expression | It provides concise syntax. |
| 3966 | What is property pattern matching? | Matching objects using their properties | It improves conditional logic. |
| 3967 | What is init-only property? | A property assignable only during initialization | It supports immutability. |
| 3968 | What is required property? | A property that must be initialized | It improves object correctness. |
| 3969 | What is field keyword in C#? | A feature allowing direct access to compiler-generated backing fields | It simplifies property implementation. |
| 3970 | What is indexer? | A member allowing objects to be accessed like arrays | It uses [] syntax. |
| 3971 | What is overloaded indexer? | Multiple indexers with different parameters | It supports flexible access. |
| 3972 | What is operator function member? | A special method implementing an operator | It defines custom operations. |
| 3973 | What is extension method? | A static method adding functionality to existing types | It appears like an instance method. |
| 3974 | What is extension block? | A modern syntax grouping extension members | It organizes extensions. |
| 3975 | What is namespace? | A logical container for types | It prevents naming conflicts. |
| 3976 | What is file-scoped namespace? | A namespace declaration applying to an entire file | It reduces indentation. |
| 3977 | What is global using directive? | A using directive applied across a project | It reduces repeated imports. |
| 3978 | What is using alias? | A name assigned to a namespace or type | It resolves conflicts. |
| 3979 | What is extern alias? | An alias for referencing conflicting assemblies | It resolves duplicate type names. |
| 3980 | What is access modifier? | A keyword controlling member visibility | Examples include public and private. |
| 3981 | What is public access modifier? | An access level allowing access from anywhere | It exposes members broadly. |
| 3982 | What is private access modifier? | An access level limited to the containing type | It hides implementation details. |
| 3983 | What is protected access modifier? | An access level available to derived types | It supports inheritance. |
| 3984 | What is internal access modifier? | An access level limited to the same assembly | It supports assembly boundaries. |
| 3985 | What is protected internal access? | Access from same assembly or derived types | It combines protected and internal rules. |
| 3986 | What is private protected access? | Access from derived types in the same assembly | It is more restrictive. |
| 3987 | What is accessibility inconsistency? | A compiler error caused by exposing less accessible types | It protects type visibility rules. |
| 3988 | What is abstract class? | A class that cannot be instantiated directly | It provides base behavior. |
| 3989 | What is abstract member? | A member without implementation in a base class | Derived classes must implement it. |
| 3990 | What is virtual member? | A member that derived classes can override | It enables polymorphism. |
| 3991 | What is override keyword? | A keyword replacing virtual behavior | It implements derived behavior. |
| 3992 | What is new keyword in inheritance? | A keyword hiding inherited members | It does not override behavior. |
| 3993 | What is sealed class? | A class preventing inheritance | It restricts extension. |
| 3994 | What is sealed override? | An override preventing further overriding | It stops inheritance changes. |
| 3995 | What is interface? | A contract defining required members | Classes implement it. |
| 3996 | What is default interface method? | An interface method with implementation | It allows interface evolution. |
| 3997 | What is explicit interface implementation? | Implementing interface members with qualified names | It hides members from class access. |
| 3998 | What is implicit interface implementation? | Implementing interface members normally | Members are publicly accessible. |
| 3999 | What is marker interface? | An interface without members | It identifies capabilities. |
| 4000 | What is multiple interface inheritance? | Implementing multiple interfaces in one type | C# supports it. |
| 4001 | What is object-oriented programming? | A programming approach based on objects and classes | It uses encapsulation, inheritance, and polymorphism. |
| 4002 | What is encapsulation? | Hiding internal implementation details | It protects object state. |
| 4003 | What is inheritance? | Creating a new type based on an existing type | It promotes code reuse. |
| 4004 | What is polymorphism? | Allowing objects to behave differently through a common interface | It enables flexible designs. |
| 4005 | What is abstraction? | Representing essential behavior while hiding details | It simplifies complexity. |
| 4006 | What is class? | A blueprint defining object structure and behavior | Objects are created from classes. |
| 4007 | What is object? | An instance of a class | It contains state and behavior. |
| 4008 | What is instance member? | A member belonging to an object instance | It requires an object reference. |
| 4009 | What is static member? | A member belonging to the type itself | It is shared across instances. |
| 4010 | What is class modifier? | A keyword controlling class behavior | Examples include abstract and sealed. |
| 4011 | What is partial class? | A class definition split across multiple files | The compiler combines them. |
| 4012 | What is nested class? | A class declared inside another class | It groups related functionality. |
| 4013 | What is immutable object? | An object whose state cannot change after creation | It improves thread safety. |
| 4014 | What is mutable object? | An object whose state can change | It allows modification after creation. |
| 4015 | What is readonly field? | A field assignable only during initialization | It prevents later modification. |
| 4016 | What is const field? | A compile-time constant value | It cannot change. |
| 4017 | What is static readonly field? | A runtime constant value shared by a type | It is initialized once. |
| 4018 | What is constant expression? | An expression evaluated at compile time | It is required for const values. |
| 4019 | What is enum? | A value type containing named constants | It improves readability. |
| 4020 | What is flags enum? | An enum designed for bitwise combinations | It uses the Flags attribute. |
| 4021 | What is bitwise operator? | An operator working on binary representations | It manipulates bits. |
| 4022 | What is bitwise AND operator? | Operator combining bits where both are set | It uses &. |
| 4023 | What is bitwise OR operator? | Operator setting bits from either operand | It uses | . |
| 4024 | What is bitwise XOR operator? | Operator setting bits that differ | It uses ^. |
| 4025 | What is bitwise NOT operator? | Operator reversing bits | It uses ~. |
| 4026 | What is shift operator? | Operator moving bits left or right | It uses << and >>. |
| 4027 | What is nullable value type? | A value type that can represent null | It uses ?. |
| 4028 | What is Nullable<T>? | Generic structure representing nullable values | It wraps value types. |
| 4029 | What is HasValue property? | Property indicating whether nullable has a value | It checks null state. |
| 4030 | What is Value property? | Property retrieving nullable value | It throws if no value exists. |
| 4031 | What is enum underlying type? | The numeric type storing enum values | Default is int. |
| 4032 | What is char type? | A UTF-16 character type | It stores a single character. |
| 4033 | What is string type? | A sequence of characters | It is immutable. |
| 4034 | What is string interning? | Reusing identical string instances | It reduces memory usage. |
| 4035 | What is StringBuilder? | A mutable string construction class | It reduces repeated allocations. |
| 4036 | What is interpolated string? | A string containing embedded expressions | It uses $. |
| 4037 | What is raw string literal? | A string literal preserving formatting and quotes | It uses triple quotes. |
| 4038 | What is verbatim string? | A string literal ignoring escape sequences | It uses @. |
| 4039 | What is escape sequence? | A character representation using backslash notation | Examples include \n and \t. |
| 4040 | What is UTF-8? | A variable-length Unicode encoding | It is common for web data. |
| 4041 | What is UTF-16? | The character encoding used internally by .NET strings | It represents characters with 16-bit code units. |
| 4042 | What is Unicode? | A standard for representing text characters | It supports worldwide languages. |
| 4043 | What is culture? | Information controlling language and formatting rules | It affects dates and numbers. |
| 4044 | What is CultureInfo? | A class representing culture information | It controls formatting behavior. |
| 4045 | What is invariant culture? | A culture-independent formatting standard | It is used for stable data exchange. |
| 4046 | What is globalization? | Supporting multiple languages and cultures | It enables international applications. |
| 4047 | What is localization? | Adapting applications for specific cultures | It changes resources and formatting. |
| 4048 | What is resource file? | A file storing localized application data | It supports translations. |
| 4049 | What is satellite assembly? | An assembly containing localized resources | It supports culture-specific resources. |
| 4050 | What is ResourceManager? | A class retrieving resources at runtime | It supports localization. |
| 4051 | What is globalization in ASP.NET Core? | Supporting multiple languages, cultures, and regional settings | It enables international applications. |
| 4052 | What is localization middleware? | Middleware selecting culture information for requests | It sets request culture. |
| 4053 | What is RequestLocalizationOptions? | Configuration options for localization middleware | It defines supported cultures. |
| 4054 | What is CultureProvider? | A component determining the request culture | Examples include query string and cookies. |
| 4055 | What is QueryStringRequestCultureProvider? | A provider reading culture from query parameters | It supports culture switching. |
| 4056 | What is CookieRequestCultureProvider? | A provider reading culture from cookies | It stores user preferences. |
| 4057 | What is AcceptLanguageHeaderRequestCultureProvider? | A provider reading culture from browser headers | It uses client preferences. |
| 4058 | What is IStringLocalizer? | An ASP.NET Core service for localized strings | It retrieves resources by key. |
| 4059 | What is IHtmlLocalizer? | A localization service for HTML content | It handles encoded HTML resources. |
| 4060 | What is IViewLocalizer? | A localization service for Razor views | It localizes UI text. |
| 4061 | What is data annotation localization? | Localizing validation messages from attributes | It supports multilingual validation. |
| 4062 | What is globalization invariant mode? | A runtime mode without culture-specific data | It reduces application size. |
| 4063 | What is date formatting? | Converting dates into culture-specific strings | Culture controls the output. |
| 4064 | What is number formatting? | Converting numbers according to culture rules | It affects separators and symbols. |
| 4065 | What is currency formatting? | Displaying monetary values using culture rules | It uses currency symbols. |
| 4066 | What is time zone? | A geographic region's time offset rules | It affects date and time calculations. |
| 4067 | What is TimeZoneInfo? | A .NET class representing time zones | It converts between zones. |
| 4068 | What is UTC? | Coordinated Universal Time standard | It avoids local time ambiguity. |
| 4069 | What is DateTime? | A structure representing date and time | It stores calendar values. |
| 4070 | What is DateTimeOffset? | A date and time value with offset information | It preserves timezone offset. |
| 4071 | What is DateOnly? | A type representing only a date | It excludes time information. |
| 4072 | What is TimeOnly? | A type representing only a time | It excludes date information. |
| 4073 | What is Unix timestamp? | A numeric representation of time since Unix epoch | It is common in APIs. |
| 4074 | What is ISO 8601? | An international date and time format standard | It improves interoperability. |
| 4075 | What is calendar system? | A system for measuring dates | Examples include Gregorian calendars. |
| 4076 | What is globalization testing? | Testing applications across cultures | It detects localization issues. |
| 4077 | What is serialization? | Converting objects into a transferable format | It supports storage and communication. |
| 4078 | What is deserialization? | Recreating objects from serialized data | It restores object state. |
| 4079 | What is JSON serialization? | Converting objects to JSON format | It is common for web APIs. |
| 4080 | What is System.Text.Json? | The built-in .NET JSON library | It provides fast JSON processing. |
| 4081 | What is JsonSerializer? | A class serializing and deserializing JSON | It provides JSON APIs. |
| 4082 | What is JsonSerializerOptions? | Configuration options for JSON serialization | It controls naming and behavior. |
| 4083 | What is JsonConverter? | A component customizing JSON conversion | It handles special types. |
| 4084 | What is JsonConverterFactory? | A factory creating JSON converters dynamically | It supports generic conversions. |
| 4085 | What is JsonPropertyName attribute? | Attribute customizing JSON property names | It controls serialized names. |
| 4086 | What is JsonIgnore attribute? | Attribute excluding properties from JSON output | It hides data. |
| 4087 | What is JsonInclude attribute? | Attribute enabling serialization of non-public members | It controls inclusion. |
| 4088 | What is JsonNamingPolicy? | A policy controlling JSON naming conventions | Examples include camelCase. |
| 4089 | What is reference handling in JSON? | Managing object reference cycles during serialization | It prevents errors. |
| 4090 | What is polymorphic JSON serialization? | Serializing derived types through base references | It preserves runtime types. |
| 4091 | What is XML serialization? | Converting objects to XML format | It supports XML-based systems. |
| 4092 | What is XmlSerializer? | A class serializing objects into XML | It uses public members. |
| 4093 | What is DataContractSerializer? | A serializer based on data contracts | It supports service communication. |
| 4094 | What is binary serialization? | Serializing objects into binary format | Modern .NET avoids unsafe binary serialization. |
| 4095 | What is MessagePack? | A compact binary serialization format | It improves performance. |
| 4096 | What is protocol serialization? | Serialization following a defined communication schema | Examples include Protocol Buffers. |
| 4097 | What is schema evolution? | Managing changes to serialized data formats | It maintains compatibility. |
| 4098 | What is version tolerant serialization? | Supporting different versions of serialized objects | It enables upgrades. |
| 4099 | What is DTO? | Data Transfer Object used for communication between layers | It separates external contracts from models. |
| 4100 | What is contract model? | A model defining data exchanged between systems | It controls API boundaries. |
| 4101 | What is API contract? | A definition of how systems communicate | It describes requests and responses. |
| 4102 | What is OpenAPI? | A standard for describing HTTP APIs | It enables documentation and tooling. |
| 4103 | What is Swagger? | A set of tools for OpenAPI APIs | It provides interactive documentation. |
| 4104 | What is Swagger UI? | A web interface for exploring APIs | It allows testing endpoints. |
| 4105 | What is OpenAPI document? | A machine-readable API description | It defines endpoints and schemas. |
| 4106 | What is Swashbuckle? | A .NET library generating Swagger documents | It integrates OpenAPI with ASP.NET Core. |
| 4107 | What is NSwag? | A .NET OpenAPI toolchain | It generates clients and documentation. |
| 4108 | What is API versioning? | Managing multiple versions of an API | It supports backward compatibility. |
| 4109 | What is URL versioning? | API versioning through URL paths | Example: /api/v1/products. |
| 4110 | What is query string versioning? | API versioning using query parameters | Example: ?api-version=1. |
| 4111 | What is header versioning? | API versioning using HTTP headers | It keeps URLs clean. |
| 4112 | What is media type versioning? | Versioning through Accept headers | It uses content negotiation. |
| 4113 | What is API deprecation? | Marking an API version as outdated | It encourages migration. |
| 4114 | What is API sunset policy? | A schedule for retiring APIs | It communicates end-of-life. |
| 4115 | What is REST API? | An API style based on HTTP resources | It uses standard HTTP operations. |
| 4116 | What is resource in REST? | An entity exposed through an API | It is identified by a URI. |
| 4117 | What is URI? | A uniform resource identifier | It identifies resources. |
| 4118 | What is URL? | A locator specifying resource location | It is a type of URI. |
| 4119 | What is HTTP method? | An operation indicating request intent | Examples include GET and POST. |
| 4120 | What is GET method? | HTTP method retrieving data | It should be safe and idempotent. |
| 4121 | What is POST method? | HTTP method creating or processing data | It may not be idempotent. |
| 4122 | What is PUT method? | HTTP method replacing a resource | It is idempotent. |
| 4123 | What is PATCH method? | HTTP method partially updating a resource | It modifies selected fields. |
| 4124 | What is DELETE method? | HTTP method removing a resource | It deletes server-side data. |
| 4125 | What is HEAD method? | HTTP method returning headers without body | It checks resource metadata. |
| 4126 | What is OPTIONS method? | HTTP method describing supported operations | It is used in CORS. |
| 4127 | What is HTTP status code? | A numeric response indicating request result | It communicates outcome. |
| 4128 | What is 200 OK? | Successful HTTP response status | The request completed successfully. |
| 4129 | What is 201 Created? | HTTP status for successful resource creation | It often includes a location header. |
| 4130 | What is 204 No Content? | HTTP status indicating success without response body | Common for delete operations. |
| 4131 | What is 400 Bad Request? | HTTP status for invalid client input | The server cannot process the request. |
| 4132 | What is 401 Unauthorized? | HTTP status indicating missing or invalid authentication | Credentials are required. |
| 4133 | What is 403 Forbidden? | HTTP status indicating insufficient permission | Authentication may exist. |
| 4134 | What is 404 Not Found? | HTTP status indicating missing resource | The resource does not exist. |
| 4135 | What is 405 Method Not Allowed? | HTTP status for unsupported HTTP methods | The endpoint exists. |
| 4136 | What is 409 Conflict? | HTTP status indicating resource conflict | It often represents duplicate data. |
| 4137 | What is 422 Unprocessable Entity? | HTTP status for semantic validation errors | Input format is valid but invalid logically. |
| 4138 | What is 429 Too Many Requests? | HTTP status for rate limiting | The client sent too many requests. |
| 4139 | What is 500 Internal Server Error? | HTTP status for unexpected server failures | It indicates application errors. |
| 4140 | What is 502 Bad Gateway? | HTTP status from an invalid upstream response | It occurs in proxy scenarios. |
| 4141 | What is 503 Service Unavailable? | HTTP status indicating temporary unavailability | The service may recover later. |
| 4142 | What is 504 Gateway Timeout? | HTTP status for upstream timeout | A dependency took too long. |
| 4143 | What is HTTP header? | Metadata sent with HTTP messages | It provides additional information. |
| 4144 | What is Content-Type header? | Header describing request or response format | It indicates media type. |
| 4145 | What is Accept header? | Header indicating desired response formats | It supports content negotiation. |
| 4146 | What is Authorization header? | Header containing authentication credentials | It often carries bearer tokens. |
| 4147 | What is User-Agent header? | Header identifying the client application | It describes the requester. |
| 4148 | What is Cache-Control header? | Header controlling HTTP caching behavior | It manages client and proxy caching. |
| 4149 | What is ETag header? | Header representing a resource version identifier | It supports conditional requests. |
| 4150 | What is If-None-Match header? | Header used for conditional requests with ETags | It enables cache validation. |
| 4151 | What is HTTP content negotiation? | A process selecting the best representation for a response | It uses headers like Accept. |
| 4152 | What is media type? | A format identifier for transmitted data | Examples include application/json and text/html. |
| 4153 | What is MIME type? | A standard identifier describing content format | It is used in HTTP communication. |
| 4154 | What is JSON media type? | application/json content identifier | It represents JSON data. |
| 4155 | What is XML media type? | application/xml content identifier | It represents XML data. |
| 4156 | What is text media type? | A content type representing text data | Examples include text/plain. |
| 4157 | What is HTTP request pipeline? | The sequence of processing stages for an HTTP request | Middleware participates in it. |
| 4158 | What is endpoint routing? | A routing system matching requests to endpoints | It is used in ASP.NET Core. |
| 4159 | What is endpoint? | A destination for handling HTTP requests | It contains metadata and handlers. |
| 4160 | What is endpoint metadata? | Information attached to endpoints | It controls behavior and policies. |
| 4161 | What is endpoint filter? | A component executing around minimal API handlers | It adds cross-cutting logic. |
| 4162 | What is minimal API? | A lightweight way to create HTTP APIs | It reduces controller boilerplate. |
| 4163 | What is RouteHandlerBuilder? | A builder configuring minimal API endpoints | It adds metadata and filters. |
| 4164 | What is WebApplication class? | The main application builder for modern ASP.NET Core apps | It configures hosting and middleware. |
| 4165 | What is WebApplicationBuilder? | A builder configuring an ASP.NET Core application | It creates WebApplication. |
| 4166 | What is WebHostBuilder? | A builder configuring ASP.NET Core hosting | It configures server settings. |
| 4167 | What is Generic Host? | A hosting model managing application lifetime and services | It supports worker and web apps. |
| 4168 | What is IHost? | An abstraction representing a running host | It manages application execution. |
| 4169 | What is IHostBuilder? | A builder configuring a host | It registers services and settings. |
| 4170 | What is HostApplicationBuilder? | A modern host builder API | It simplifies application setup. |
| 4171 | What is BackgroundService? | A base class for long-running hosted tasks | It implements background execution. |
| 4172 | What is IHostedService? | An interface for background services | It controls start and stop behavior. |
| 4173 | What is hosted service lifecycle? | The sequence of starting and stopping background services | It follows host lifetime. |
| 4174 | What is ExecuteAsync()? | A method containing BackgroundService logic | It runs the worker task. |
| 4175 | What is cancellation token in hosted services? | A signal for graceful shutdown | It stops background work safely. |
| 4176 | What is worker service? | A .NET application for background processing | It uses Generic Host. |
| 4177 | What is Windows Service hosting? | Running .NET applications as Windows services | It supports background processes. |
| 4178 | What is Linux systemd hosting? | Running .NET applications as Linux services | It integrates with systemd. |
| 4179 | What is application lifetime? | The period from startup to shutdown | Host controls it. |
| 4180 | What is IHostApplicationLifetime? | Service managing application lifetime events | It provides stopping notifications. |
| 4181 | What is ApplicationStarted event? | Event fired after application startup | It signals readiness. |
| 4182 | What is ApplicationStopping event? | Event fired during application shutdown | It allows cleanup. |
| 4183 | What is ApplicationStopped event? | Event fired after shutdown completes | It confirms termination. |
| 4184 | What is graceful shutdown? | Stopping an application while completing active work | It prevents data loss. |
| 4185 | What is shutdown timeout? | Maximum time allowed for graceful shutdown | It limits stopping duration. |
| 4186 | What is startup task? | Work executed during application startup | It prepares application state. |
| 4187 | What is readiness probe? | A check indicating application can accept traffic | Used in orchestration systems. |
| 4188 | What is liveness probe? | A check indicating application is running | It detects failures. |
| 4189 | What is health check response writer? | Component formatting health check results | It controls output. |
| 4190 | What is HealthCheckService? | Service executing registered health checks | It aggregates health results. |
| 4191 | What is IHealthCheck? | Interface implementing custom health checks | It reports dependency status. |
| 4192 | What is health check tag? | A label grouping health checks | It filters execution. |
| 4193 | What is dependency health check? | A check verifying external services | It monitors dependencies. |
| 4194 | What is liveness versus readiness? | Difference between running and ready states | They serve different purposes. |
| 4195 | What is observability? | Ability to understand system behavior through telemetry | It uses logs, metrics, and traces. |
| 4196 | What is telemetry? | Data collected about application behavior | It supports monitoring. |
| 4197 | What is OpenTelemetry? | An observability standard and framework | It collects traces, metrics, and logs. |
| 4198 | What is distributed tracing? | Tracking requests across multiple services | It identifies performance issues. |
| 4199 | What is trace span? | A single operation within a trace | It represents work performed. |
| 4200 | What is trace context? | Information propagated across service calls | It links distributed operations. |
| 4201 | What is Activity in .NET? | A representation of an operation for diagnostics and tracing | It is used by OpenTelemetry. |
| 4202 | What is ActivitySource? | A factory for creating diagnostic activities | It produces tracing spans. |
| 4203 | What is ActivityListener? | A component listening to activity creation | It controls activity collection. |
| 4204 | What is ActivityContext? | Context information carried across traces | It contains trace and span identifiers. |
| 4205 | What is TraceId? | A unique identifier for a distributed trace | It connects related spans. |
| 4206 | What is SpanId? | An identifier for an individual trace operation | It identifies a span. |
| 4207 | What is baggage in tracing? | Key-value data propagated with a trace | It carries contextual information. |
| 4208 | What is correlation ID? | An identifier linking related operations | It helps track requests. |
| 4209 | What is structured logging? | Logging using named fields instead of plain text | It improves searching and analysis. |
| 4210 | What is ILogger? | The .NET logging abstraction | It supports multiple providers. |
| 4211 | What is ILoggerFactory? | A factory creating logger instances | It manages logging providers. |
| 4212 | What is logging provider? | A component sending logs to a destination | Examples include console and files. |
| 4213 | What is console logger provider? | A provider writing logs to console output | It is commonly used in development. |
| 4214 | What is debug logger provider? | A provider sending logs to debug output | It supports debugging scenarios. |
| 4215 | What is event source logger? | A logger integrating with EventSource diagnostics | It supports system monitoring. |
| 4216 | What is Serilog? | A structured logging library for .NET | It supports advanced log processing. |
| 4217 | What is log level? | A severity category for log messages | Examples include Information and Error. |
| 4218 | What is Trace log level? | The most detailed diagnostic log level | It is used for deep troubleshooting. |
| 4219 | What is Debug log level? | A detailed log level for development diagnostics | It helps developers investigate issues. |
| 4220 | What is Information log level? | A normal operational log level | It records application events. |
| 4221 | What is Warning log level? | A log level indicating potential issues | The application can continue. |
| 4222 | What is Error log level? | A log level indicating failures | Operations may be affected. |
| 4223 | What is Critical log level? | The highest severity log level | It indicates serious failures. |
| 4224 | What is logging scope? | Additional context attached to logs | It groups related messages. |
| 4225 | What is LoggerMessage? | A high-performance logging API | It reduces allocations. |
| 4226 | What is source-generated logging? | Compile-time generated logging code | It improves performance. |
| 4227 | What is event ID in logging? | A numeric identifier for log events | It enables filtering. |
| 4228 | What is log enrichment? | Adding additional information to logs | It improves diagnostics. |
| 4229 | What is log aggregation? | Collecting logs from multiple sources | It centralizes analysis. |
| 4230 | What is metrics? | Numerical measurements of system behavior | They show trends and performance. |
| 4231 | What is counter metric? | A metric that only increases | It tracks totals. |
| 4232 | What is gauge metric? | A metric representing a current value | It tracks changing states. |
| 4233 | What is histogram metric? | A metric recording value distributions | It measures latency and sizes. |
| 4234 | What is Meter in .NET? | An API for creating metrics instruments | It works with OpenTelemetry. |
| 4235 | What is Counter<T>? | A metric instrument recording increasing values | It tracks occurrences. |
| 4236 | What is Histogram<T>? | A metric instrument recording distributions | It measures ranges. |
| 4237 | What is ObservableCounter<T>? | A metric read from a callback | It reports external values. |
| 4238 | What is ObservableGauge<T>? | A metric reporting current measurements | It tracks changing values. |
| 4239 | What is performance counter? | A system measurement of resource usage | It monitors applications and hardware. |
| 4240 | What is BenchmarkDotNet? | A .NET benchmarking framework | It measures code performance. |
| 4241 | What is benchmark? | A performance measurement test | It compares implementations. |
| 4242 | What is warmup iteration? | Benchmark preparation execution | It stabilizes measurements. |
| 4243 | What is throughput? | Amount of work completed over time | It measures capacity. |
| 4244 | What is latency? | Time taken to complete an operation | It measures responsiveness. |
| 4245 | What is tail latency? | Latency of slow requests at high percentiles | It reveals worst-case performance. |
| 4246 | What is percentile latency? | A latency measurement at a percentile level | Examples include p95 and p99. |
| 4247 | What is CPU-bound operation? | Work limited by processor capacity | Parallelism may help. |
| 4248 | What is I/O-bound operation? | Work limited by external input/output | Async programming helps. |
| 4249 | What is performance profiling? | Analyzing application resource usage | It identifies bottlenecks. |
| 4250 | What is dotnet-trace? | A .NET diagnostic tracing tool | It collects runtime events. |
| 4251 | What is dotnet-counters? | A .NET monitoring tool showing performance counters | It displays runtime metrics. |
| 4252 | What is dotnet-dump? | A tool collecting and analyzing memory dumps | It helps diagnose crashes. |
| 4253 | What is dotnet-gcdump? | A tool creating GC heap dumps | It analyzes managed memory usage. |
| 4254 | What is dotnet-monitor? | A tool exposing .NET diagnostics through HTTP APIs | It supports production monitoring. |
| 4255 | What is EventPipe? | A .NET runtime tracing mechanism | It collects diagnostics data. |
| 4256 | What is DiagnosticSource? | A library for producing diagnostic events | It enables instrumentation. |
| 4257 | What is DiagnosticListener? | A listener for DiagnosticSource events | It observes application operations. |
| 4258 | What is runtime event provider? | A source of CLR diagnostic events | It exposes runtime information. |
| 4259 | What is EventSource? | A high-performance event tracing API | It produces structured events. |
| 4260 | What is EventCounter? | A metric emitted through EventSource | It reports runtime statistics. |
| 4261 | What is ActivityListener sampling? | A mechanism deciding which traces to collect | It controls telemetry volume. |
| 4262 | What is head-based sampling? | Sampling decision made at trace start | It reduces trace storage. |
| 4263 | What is tail-based sampling? | Sampling decision made after trace completion | It can select important traces. |
| 4264 | What is observability pipeline? | A process collecting and exporting telemetry | It connects applications to monitoring systems. |
| 4265 | What is exporter in OpenTelemetry? | A component sending telemetry data to a backend | It transfers traces and metrics. |
| 4266 | What is collector in OpenTelemetry? | A service receiving and processing telemetry | It centralizes observability data. |
| 4267 | What is instrumentation library? | A library creating telemetry for a technology | It simplifies monitoring. |
| 4268 | What is automatic instrumentation? | Telemetry generated without code changes | It uses runtime hooks. |
| 4269 | What is manual instrumentation? | Developers adding telemetry explicitly | It provides custom visibility. |
| 4270 | What is service name in tracing? | The identifier of an application service | It groups telemetry. |
| 4271 | What is resource attribute? | Metadata describing telemetry source | It identifies applications. |
| 4272 | What is metric label? | A dimension attached to a metric | It enables filtering. |
| 4273 | What is cardinality in metrics? | Number of unique label combinations | High cardinality affects storage. |
| 4274 | What is SLO? | Service Level Objective defining reliability targets | It measures expected performance. |
| 4275 | What is SLA? | Service Level Agreement between provider and customer | It defines commitments. |
| 4276 | What is SLI? | Service Level Indicator measuring service behavior | It provides reliability data. |
| 4277 | What is error budget? | Allowed failure amount within an SLO | It balances reliability and delivery speed. |
| 4278 | What is incident management? | Process for handling service disruptions | It restores normal operation. |
| 4279 | What is root cause analysis? | Finding the underlying cause of failures | It prevents recurrence. |
| 4280 | What is postmortem? | A review after an incident | It documents lessons learned. |
| 4281 | What is chaos engineering? | Testing resilience through controlled failures | It improves reliability. |
| 4282 | What is fault injection? | Introducing failures intentionally | It tests system behavior. |
| 4283 | What is disaster recovery? | Planning for restoring systems after major failures | It protects business continuity. |
| 4284 | What is backup strategy? | A plan for protecting and restoring data | It reduces data loss. |
| 4285 | What is restore point? | A saved state used for recovery | It enables rollback. |
| 4286 | What is RPO? | Recovery Point Objective defining acceptable data loss | It measures backup requirements. |
| 4287 | What is RTO? | Recovery Time Objective defining recovery duration | It measures restoration speed. |
| 4288 | What is high availability? | Designing systems to minimize downtime | It uses redundancy. |
| 4289 | What is fault tolerance? | Ability to continue operation despite failures | It uses resilient designs. |
| 4290 | What is redundancy? | Duplicating resources for reliability | It prevents single points of failure. |
| 4291 | What is failover? | Switching to a backup system after failure | It maintains availability. |
| 4292 | What is active-passive architecture? | Architecture with primary and standby systems | Standby activates after failure. |
| 4293 | What is active-active architecture? | Architecture where multiple systems serve traffic | It improves availability. |
| 4294 | What is load balancing? | Distributing traffic across servers | It improves scalability. |
| 4295 | What is reverse proxy? | A server forwarding client requests to backend services | It provides routing and security. |
| 4296 | What is YARP? | Yet Another Reverse Proxy for .NET | It builds customizable proxies. |
| 4297 | What is proxy middleware? | Middleware forwarding HTTP requests | It enables proxy behavior. |
| 4298 | What is sticky session? | Routing a client repeatedly to the same server | It preserves session state. |
| 4299 | What is session affinity? | Maintaining client-to-server association | It supports stateful applications. |
| 4300 | What is stateless application? | An application that does not store client state locally | It scales easily. |
| 4301 | What is stateful application? | An application that maintains client or process state | It requires state management. |
| 4302 | What is distributed cache? | A cache shared across multiple application instances | It supports scalable applications. |
| 4303 | What is IMemoryCache? | An in-process memory cache in ASP.NET Core | It stores data locally. |
| 4304 | What is IDistributedCache? | An abstraction for distributed caching | It supports external cache providers. |
| 4305 | What is Redis cache? | A distributed in-memory data store | It is commonly used for caching. |
| 4306 | What is cache-aside pattern? | A pattern where applications manage cache loading | It reduces database load. |
| 4307 | What is cache invalidation? | Removing or updating stale cached data | It maintains data correctness. |
| 4308 | What is cache expiration? | Removing cached data after a period | It controls cache lifetime. |
| 4309 | What is absolute expiration? | Cache expiration at a fixed time | It limits maximum lifetime. |
| 4310 | What is sliding expiration? | Cache expiration extended when accessed | It keeps active data available. |
| 4311 | What is cache stampede? | Many requests rebuilding the same expired cache item | It can overload systems. |
| 4312 | What is cache penetration? | Requests repeatedly bypassing cache for missing data | It increases backend load. |
| 4313 | What is cache avalanche? | Many cache items expiring simultaneously | It causes traffic spikes. |
| 4314 | What is distributed lock? | A lock coordinating processes across machines | It prevents concurrent conflicts. |
| 4315 | What is optimistic concurrency? | Assuming conflicts are rare and checking before update | It improves scalability. |
| 4316 | What is pessimistic concurrency? | Locking data before modification | It prevents conflicts. |
| 4317 | What is concurrency token? | A value used to detect conflicting updates | EF Core supports it. |
| 4318 | What is row version? | A database-generated version value | It supports optimistic concurrency. |
| 4319 | What is timestamp column? | A database column tracking row changes | It detects updates. |
| 4320 | What is EF Core concurrency exception? | Exception thrown when updates conflict | It requires resolution. |
| 4321 | What is transaction isolation level? | A setting controlling transaction visibility | It affects consistency. |
| 4322 | What is ReadUncommitted isolation? | Isolation allowing dirty reads | It provides low consistency. |
| 4323 | What is ReadCommitted isolation? | Isolation preventing dirty reads | It is commonly used. |
| 4324 | What is RepeatableRead isolation? | Isolation ensuring repeated reads return the same data | It prevents changes during transaction. |
| 4325 | What is Serializable isolation? | The strictest isolation level | It prevents most concurrency anomalies. |
| 4326 | What is Snapshot isolation? | Isolation using row versions | It reduces locking. |
| 4327 | What is dirty read? | Reading uncommitted changes | It can return invalid data. |
| 4328 | What is non-repeatable read? | Reading different values within the same transaction | Data changed between reads. |
| 4329 | What is phantom read? | Seeing new rows during repeated queries | Another transaction inserted data. |
| 4330 | What is database transaction? | A unit of work with commit or rollback | It maintains consistency. |
| 4331 | What is atomicity? | Transaction property ensuring all-or-nothing execution | It prevents partial updates. |
| 4332 | What is consistency in transactions? | Transaction property preserving valid data states | It maintains rules. |
| 4333 | What is isolation in transactions? | Transaction property separating concurrent operations | It prevents interference. |
| 4334 | What is durability? | Transaction property preserving committed data | It survives failures. |
| 4335 | What is ACID? | Properties defining reliable transactions | Atomicity, consistency, isolation, durability. |
| 4336 | What is distributed cache invalidation? | Synchronizing cache removal across instances | It maintains consistency. |
| 4337 | What is message-based invalidation? | Updating caches through messages | It supports distributed systems. |
| 4338 | What is event-driven cache update? | Updating cache based on domain events | It keeps data synchronized. |
| 4339 | What is CQRS read model? | A model optimized for querying data | It separates reads from writes. |
| 4340 | What is CQRS write model? | A model handling commands and state changes | It focuses on business rules. |
| 4341 | What is read replica? | A database copy used for read operations | It improves query scalability. |
| 4342 | What is database sharding? | Splitting data across multiple databases | It scales storage. |
| 4343 | What is partitioning? | Dividing data into smaller sections | It improves performance. |
| 4344 | What is horizontal partitioning? | Splitting rows across partitions | It distributes data. |
| 4345 | What is vertical partitioning? | Splitting columns across structures | It separates data access patterns. |
| 4346 | What is database index? | A structure improving query performance | It speeds up searches. |
| 4347 | What is clustered index? | An index determining physical row order | Usually one exists per table. |
| 4348 | What is non-clustered index? | An index storing references to data rows | Multiple can exist. |
| 4349 | What is composite index? | An index using multiple columns | It supports multi-column queries. |
| 4350 | What is covering index? | An index containing all required query columns | It avoids extra lookups. |
| 4351 | What is index seek? | A database operation locating rows using an index | It is usually efficient. |
| 4352 | What is index scan? | A database operation reading many index entries | It may be slower than a seek. |
| 4353 | What is query execution plan? | A plan showing how a database executes a query | It helps optimize performance. |
| 4354 | What is query optimizer? | A database component selecting execution strategies | It improves query performance. |
| 4355 | What is SQL parameterization? | Using parameters instead of string concatenation in SQL | It prevents SQL injection. |
| 4356 | What is SQL injection? | An attack inserting malicious SQL commands | Parameterized queries prevent it. |
| 4357 | What is ORM? | Object Relational Mapper | It maps objects to database tables. |
| 4358 | What is Entity Framework Core? | A modern .NET ORM | It provides database access through objects. |
| 4359 | What is DbContext? | The main EF Core database session class | It tracks entities and executes queries. |
| 4360 | What is DbSet<T>? | A collection representing an entity set | It provides CRUD operations. |
| 4361 | What is EF Core change tracker? | A component tracking entity state changes | It enables updates. |
| 4362 | What is entity state in EF Core? | The current tracking status of an entity | Examples include Added and Modified. |
| 4363 | What is Added entity state? | State indicating a new entity will be inserted | SaveChanges creates a row. |
| 4364 | What is Modified entity state? | State indicating changed entity values | SaveChanges updates the row. |
| 4365 | What is Deleted entity state? | State indicating an entity should be removed | SaveChanges deletes the row. |
| 4366 | What is Unchanged entity state? | State indicating no modifications exist | No update is generated. |
| 4367 | What is Detached entity state? | State where EF Core does not track an entity | Changes are ignored. |
| 4368 | What is SaveChanges()? | EF Core method persisting changes | It executes database commands. |
| 4369 | What is SaveChangesAsync()? | Async version of SaveChanges | It avoids blocking threads. |
| 4370 | What is EF Core migration? | A mechanism for evolving database schema | It tracks schema changes. |
| 4371 | What is migration snapshot? | A model representation used by EF migrations | It compares schema changes. |
| 4372 | What is database-first approach? | Creating models from an existing database | Tools generate classes. |
| 4373 | What is code-first approach? | Creating database schema from C# models | Migrations update the database. |
| 4374 | What is model-first approach? | Designing models before generating database structures | It is less common in EF Core. |
| 4375 | What is EF Core convention? | Default rule used to configure models | It reduces configuration. |
| 4376 | What is Fluent API? | Programmatic EF Core model configuration | It provides advanced mapping. |
| 4377 | What is Data Annotation? | Attributes configuring model behavior | It provides simple configuration. |
| 4378 | What is OnModelCreating()? | Method configuring EF Core models | It uses Fluent API. |
| 4379 | What is entity configuration class? | A class implementing model configuration rules | It organizes mappings. |
| 4380 | What is IEntityTypeConfiguration<T>? | Interface for entity configuration classes | It separates model setup. |
| 4381 | What is navigation property? | Property representing relationships between entities | It enables related data access. |
| 4382 | What is relationship mapping? | Configuring entity relationships | It defines associations. |
| 4383 | What is one-to-one relationship? | A relationship where each entity has one related entity | It uses unique keys. |
| 4384 | What is one-to-many relationship? | A relationship where one entity relates to many entities | It uses foreign keys. |
| 4385 | What is many-to-many relationship? | A relationship where both sides have multiple related entities | EF Core supports join tables. |
| 4386 | What is foreign key? | A column referencing another table's primary key | It defines relationships. |
| 4387 | What is primary key? | A unique identifier for table rows | It identifies records. |
| 4388 | What is alternate key? | A unique key other than the primary key | It provides additional identity. |
| 4389 | What is composite key? | A key made from multiple columns | It identifies rows using combinations. |
| 4390 | What is shadow property? | An EF Core property not defined in the CLR class | EF tracks it internally. |
| 4391 | What is owned entity type? | An entity type controlled by its owner | It shares lifecycle. |
| 4392 | What is table splitting? | Mapping multiple entities to one table | It shares database rows. |
| 4393 | What is entity splitting? | Mapping one entity across multiple tables | It separates storage. |
| 4394 | What is keyless entity type? | An entity without a primary key | It is often used for queries. |
| 4395 | What is raw SQL query in EF Core? | Executing SQL directly through EF Core | It supports advanced scenarios. |
| 4396 | What is FromSql()? | EF Core method executing SQL queries | It returns entities. |
| 4397 | What is ExecuteSql()? | EF Core method executing non-query SQL | It performs commands. |
| 4398 | What is LINQ provider? | A component translating LINQ expressions | EF Core translates queries to SQL. |
| 4399 | What is query translation? | Converting LINQ expressions into database queries | It enables ORM querying. |
| 4400 | What is client evaluation? | Executing part of a query in application memory | It may reduce performance. |
| 4401 | What is LINQ? | Language Integrated Query for querying data | It provides a common query syntax. |
| 4402 | What is LINQ to Objects? | LINQ querying in-memory collections | It uses IEnumerable<T>. |
| 4403 | What is LINQ to SQL? | A LINQ provider translating queries to SQL | It was an early ORM technology. |
| 4404 | What is LINQ to Entities? | LINQ provider used by Entity Framework | It translates expressions to database queries. |
| 4405 | What is IQueryable<T>? | A query representation executed by a provider | EF Core translates it to SQL. |
| 4406 | What is IEnumerable<T>? | An enumerable sequence interface | Queries execute in memory. |
| 4407 | What is deferred execution? | Delaying query execution until enumeration | LINQ queries often use it. |
| 4408 | What is immediate execution? | Executing a query immediately | Methods like ToList() trigger it. |
| 4409 | What is ToList()? | LINQ method converting results into a list | It executes deferred queries. |
| 4410 | What is ToArray()? | LINQ method converting results into an array | It executes a query. |
| 4411 | What is First()? | LINQ method returning the first element | It throws if no element exists. |
| 4412 | What is FirstOrDefault()? | LINQ method returning the first element or default value | It avoids exceptions. |
| 4413 | What is Single()? | LINQ method returning exactly one element | It throws if multiple exist. |
| 4414 | What is SingleOrDefault()? | LINQ method returning one element or default | It validates uniqueness. |
| 4415 | What is Last()? | LINQ method returning the last element | It requires enumeration. |
| 4416 | What is Any()? | LINQ method checking whether elements exist | It returns a boolean. |
| 4417 | What is All()? | LINQ method checking whether all elements match a condition | It returns a boolean. |
| 4418 | What is Count()? | LINQ method counting elements | It may execute a database count. |
| 4419 | What is LongCount()? | LINQ method returning a long count | It supports large sequences. |
| 4420 | What is Where()? | LINQ filtering method | It selects matching elements. |
| 4421 | What is Select()? | LINQ projection method | It transforms elements. |
| 4422 | What is SelectMany()? | LINQ flattening method | It combines nested collections. |
| 4423 | What is OrderBy()? | LINQ ascending sorting method | It sorts by a key. |
| 4424 | What is OrderByDescending()? | LINQ descending sorting method | It sorts in reverse order. |
| 4425 | What is ThenBy()? | Additional ascending sorting method | It provides secondary ordering. |
| 4426 | What is ThenByDescending()? | Additional descending sorting method | It provides secondary reverse ordering. |
| 4427 | What is GroupBy()? | LINQ grouping method | It creates groups by a key. |
| 4428 | What is Join()? | LINQ method combining sequences by matching keys | It performs inner joins. |
| 4429 | What is GroupJoin()? | LINQ method creating grouped joins | It supports one-to-many relationships. |
| 4430 | What is Zip()? | LINQ method combining elements from sequences by position | It creates paired results. |
| 4431 | What is Aggregate()? | LINQ method applying an accumulator function | It reduces sequences. |
| 4432 | What is Distinct()? | LINQ method removing duplicate values | It uses equality comparison. |
| 4433 | What is DistinctBy()? | LINQ method removing duplicates by key | It uses a selector. |
| 4434 | What is Union()? | LINQ method combining sequences without duplicates | It uses set semantics. |
| 4435 | What is Intersect()? | LINQ method returning common elements | It performs set intersection. |
| 4436 | What is Except()? | LINQ method returning elements not in another sequence | It performs set difference. |
| 4437 | What is Contains()? | LINQ method checking membership | It returns true or false. |
| 4438 | What is ElementAt()? | LINQ method accessing an element by index | It may enumerate a sequence. |
| 4439 | What is Skip()? | LINQ method ignoring initial elements | It supports paging. |
| 4440 | What is Take()? | LINQ method selecting a number of elements | It limits results. |
| 4441 | What is SkipWhile()? | LINQ method skipping while a condition is true | It stops skipping after first failure. |
| 4442 | What is TakeWhile()? | LINQ method taking while a condition is true | It stops after first failure. |
| 4443 | What is Chunk()? | LINQ method splitting data into batches | It supports batch processing. |
| 4444 | What is Reverse()? | LINQ method reversing a sequence | It changes enumeration order. |
| 4445 | What is DefaultIfEmpty()? | LINQ method providing a default element for empty sequences | It avoids empty results. |
| 4446 | What is Cast<T>()? | LINQ method casting sequence elements | It throws on invalid casts. |
| 4447 | What is OfType<T>()? | LINQ method filtering by type | It ignores incompatible elements. |
| 4448 | What is AsEnumerable()? | LINQ method treating a sequence as IEnumerable | It switches query context. |
| 4449 | What is AsQueryable()? | LINQ method creating an IQueryable wrapper | It enables provider execution. |
| 4450 | What is Expression Tree? | A data structure representing code as objects | LINQ providers analyze it. |
| 4451 | What is Expression<TDelegate>? | A strongly typed expression tree representation | It enables dynamic query generation. |
| 4452 | What is expression visitor? | A class for traversing and modifying expression trees | It supports query transformations. |
| 4453 | What is IQueryable provider? | A component executing IQueryable expressions | It translates queries. |
| 4454 | What is LINQ query syntax? | SQL-like syntax for LINQ queries | It compiles into method calls. |
| 4455 | What is LINQ method syntax? | Extension method-based LINQ syntax | It uses lambda expressions. |
| 4456 | What is anonymous projection? | Creating unnamed result objects in LINQ | It is common with Select(). |
| 4457 | What is projection? | Transforming objects into another shape | It selects required data. |
| 4458 | What is filtering? | Selecting elements matching conditions | It uses Where(). |
| 4459 | What is aggregation? | Combining multiple values into one result | Examples include Sum and Average. |
| 4460 | What is Sum()? | LINQ method calculating total values | It performs numeric aggregation. |
| 4461 | What is Average()? | LINQ method calculating mean values | It returns an average. |
| 4462 | What is Min()? | LINQ method finding the smallest value | It performs comparison. |
| 4463 | What is Max()? | LINQ method finding the largest value | It performs comparison. |
| 4464 | What is MinBy()? | LINQ method finding minimum element by key | It returns the element. |
| 4465 | What is MaxBy()? | LINQ method finding maximum element by key | It returns the element. |
| 4466 | What is query composition? | Building queries by combining operators | It enables reusable queries. |
| 4467 | What is LINQ performance issue? | Inefficiency caused by expensive query operations | Query optimization is required. |
| 4468 | What is multiple enumeration? | Executing an enumerable sequence more than once | It may repeat expensive work. |
| 4469 | What is materialization? | Converting query results into objects in memory | Methods like ToList() perform it. |
| 4470 | What is tracking query? | EF Core query that tracks returned entities | It enables updates. |
| 4471 | What is no-tracking query? | EF Core query without change tracking | It improves read performance. |
| 4472 | What is AsNoTracking()? | EF Core method disabling tracking | It is useful for read-only data. |
| 4473 | What is identity resolution? | Reusing the same entity instance for duplicate results | It maintains object consistency. |
| 4474 | What is AsNoTrackingWithIdentityResolution()? | No-tracking query with identity resolution | It balances performance and consistency. |
| 4475 | What is eager loading? | Loading related data with the main query | It uses Include(). |
| 4476 | What is lazy loading? | Loading related data when accessed | It can cause extra queries. |
| 4477 | What is explicit loading? | Loading related data manually | It uses EF Core APIs. |
| 4478 | What is Include()? | EF Core method loading related entities | It performs eager loading. |
| 4479 | What is ThenInclude()? | EF Core method loading nested relationships | It extends Include(). |
| 4480 | What is filtered Include()? | Loading related data with filtering | It reduces loaded data. |
| 4481 | What is N+1 query problem? | Excessive queries caused by repeated related data loading | Lazy loading can cause it. |
| 4482 | What is split query? | EF Core query executing multiple SQL statements for related data | It avoids huge joins. |
| 4483 | What is single query? | EF Core query loading related data with one SQL statement | It uses joins. |
| 4484 | What is Cartesian explosion? | Duplicate data caused by large joins | Split queries can help. |
| 4485 | What is compiled query? | A precompiled EF Core query | It improves repeated query performance. |
| 4486 | What is EF.CompileQuery()? | Method creating compiled EF Core queries | It reduces translation overhead. |
| 4487 | What is bulk operation? | Processing many database records efficiently | It avoids individual commands. |
| 4488 | What is ExecuteUpdate()? | EF Core method updating records directly in database | It avoids loading entities. |
| 4489 | What is ExecuteDelete()? | EF Core method deleting records directly in database | It avoids loading entities. |
| 4490 | What is database provider? | EF Core component connecting to a database | Examples include SQL Server and PostgreSQL. |
| 4491 | What is SQL Server provider? | EF Core provider for Microsoft SQL Server | It translates queries to T-SQL. |
| 4492 | What is PostgreSQL provider? | EF Core provider for PostgreSQL databases | It supports PostgreSQL features. |
| 4493 | What is SQLite provider? | EF Core provider for SQLite databases | It supports lightweight databases. |
| 4494 | What is Cosmos DB provider? | EF Core provider for Azure Cosmos DB | It supports NoSQL storage. |
| 4495 | What is database connection string? | Configuration describing database connection details | It includes server and credentials. |
| 4496 | What is DbConnection? | ADO.NET abstraction for database connections | It manages database communication. |
| 4497 | What is DbCommand? | ADO.NET abstraction for database commands | It executes SQL statements. |
| 4498 | What is DbDataReader? | ADO.NET forward-only data reader | It reads query results efficiently. |
| 4499 | What is ADO.NET? | The .NET data access technology | It provides low-level database access. |
| 4500 | What is connection pooling? | Reusing database connections instead of creating new ones | It improves performance. |
| 4501 | What is database connection pool? | A collection of reusable database connections | It reduces connection creation overhead. |
| 4502 | What is DbProviderFactory? | A factory creating database provider objects | It supports provider-independent code. |
| 4503 | What is DataReader? | A forward-only mechanism for reading database results | It provides fast data access. |
| 4504 | What is DataSet? | An in-memory collection of relational data | It supports disconnected data access. |
| 4505 | What is DataTable? | An in-memory representation of a database table | It stores rows and columns. |
| 4506 | What is DataAdapter? | A component transferring data between database and DataSet | It supports disconnected models. |
| 4507 | What is parameterized command? | A database command using parameters | It improves security and performance. |
| 4508 | What is stored procedure? | A database-side executable routine | It contains SQL logic. |
| 4509 | What is view in database? | A virtual table based on a query | It simplifies data access. |
| 4510 | What is database trigger? | A database action executed automatically on events | It enforces database logic. |
| 4511 | What is foreign key constraint? | A rule maintaining relationships between tables | It enforces referential integrity. |
| 4512 | What is unique constraint? | A rule preventing duplicate values | It ensures uniqueness. |
| 4513 | What is check constraint? | A rule validating column values | It enforces data rules. |
| 4514 | What is NOT NULL constraint? | A rule requiring a value | It prevents missing data. |
| 4515 | What is normalization? | Organizing database data to reduce redundancy | It improves consistency. |
| 4516 | What is first normal form? | A normalization rule requiring atomic values | It removes repeating groups. |
| 4517 | What is second normal form? | A normalization rule removing partial dependencies | It applies to composite keys. |
| 4518 | What is third normal form? | A normalization rule removing transitive dependencies | It reduces duplication. |
| 4519 | What is denormalization? | Adding redundancy for performance reasons | It can speed up reads. |
| 4520 | What is data integrity? | Accuracy and consistency of stored data | Constraints help maintain it. |
| 4521 | What is referential integrity? | Ensuring relationships between tables remain valid | Foreign keys enforce it. |
| 4522 | What is migration rollback? | Reverting a database migration | It restores a previous schema. |
| 4523 | What is EF Core EnsureCreated()? | Method creating a database without migrations | It is useful for testing. |
| 4524 | What is EF Core EnsureDeleted()? | Method deleting a database | It is used in development scenarios. |
| 4525 | What is database seeding? | Adding initial data automatically | It prepares application data. |
| 4526 | What is model seeding in EF Core? | Defining initial data through the model | It uses HasData(). |
| 4527 | What is custom seeding? | Writing application code to insert initial data | It supports complex scenarios. |
| 4528 | What is repository pattern? | An abstraction over data access operations | It separates persistence logic. |
| 4529 | What is unit of work pattern? | A pattern coordinating multiple changes as one transaction | EF Core DbContext acts similarly. |
| 4530 | What is specification pattern? | A pattern encapsulating query rules | It improves query reuse. |
| 4531 | What is domain model? | A model representing business concepts | It contains business logic. |
| 4532 | What is persistence model? | A model designed for database storage | It focuses on data access. |
| 4533 | What is aggregate root? | The main entity controlling a group of objects | It enforces consistency. |
| 4534 | What is domain-driven design? | An approach focusing on business domain modeling | It aligns software with business needs. |
| 4535 | What is bounded context? | A boundary defining a domain model scope | It avoids model conflicts. |
| 4536 | What is entity in DDD? | An object with identity over time | It represents domain concepts. |
| 4537 | What is value object? | An object defined by its values rather than identity | It is usually immutable. |
| 4538 | What is domain service? | A service containing domain logic not belonging to an entity | It supports complex rules. |
| 4539 | What is application service? | A service coordinating application workflows | It connects use cases. |
| 4540 | What is domain event? | An event representing an important business occurrence | It communicates changes. |
| 4541 | What is integration event? | An event shared between systems | It supports distributed communication. |
| 4542 | What is event sourcing? | Storing state changes as events | It enables history reconstruction. |
| 4543 | What is event store? | A database storing domain events | It supports event sourcing. |
| 4544 | What is projection in event sourcing? | A read model created from events | It supports queries. |
| 4545 | What is eventual consistency? | A model where data becomes consistent over time | It is common in distributed systems. |
| 4546 | What is strong consistency? | Immediate consistency after changes | It provides strict correctness. |
| 4547 | What is Saga pattern? | A pattern managing distributed transactions | It uses compensating actions. |
| 4548 | What is compensating transaction? | An operation reversing a previous action | It handles failures. |
| 4549 | What is message broker? | A system routing messages between applications | It enables asynchronous communication. |
| 4550 | What is RabbitMQ? | A message broker using queues and exchanges | It supports messaging patterns. |
| 4551 | What is Apache Kafka? | A distributed event streaming platform | It handles high-volume message streams. |
| 4552 | What is message queue? | A queue storing messages for later processing | It decouples systems. |
| 4553 | What is publish-subscribe pattern? | A messaging pattern where publishers send events to subscribers | It enables loose coupling. |
| 4554 | What is producer in messaging? | A component creating messages | It sends data to a broker. |
| 4555 | What is consumer in messaging? | A component receiving messages | It processes events. |
| 4556 | What is consumer group? | A group of consumers sharing message processing | It enables parallel processing. |
| 4557 | What is message acknowledgment? | Confirmation that a message was processed | It controls reliability. |
| 4558 | What is message retry? | Attempting message processing again after failure | It handles transient errors. |
| 4559 | What is dead-letter queue? | A queue storing messages that cannot be processed | It supports failure analysis. |
| 4560 | What is poison message? | A message that repeatedly fails processing | It may require manual handling. |
| 4561 | What is idempotent message processing? | Processing a message multiple times with the same result | It prevents duplicate effects. |
| 4562 | What is message ordering? | Maintaining message sequence during processing | It is important for some workflows. |
| 4563 | What is outbox pattern? | A pattern storing messages with database changes | It improves consistency. |
| 4564 | What is inbox pattern? | A pattern tracking processed messages | It prevents duplicate handling. |
| 4565 | What is distributed transaction? | A transaction spanning multiple systems | It is difficult to manage. |
| 4566 | What is two-phase commit? | A distributed transaction coordination protocol | It ensures atomic commits. |
| 4567 | What is CAP theorem? | A principle describing distributed system trade-offs | It involves consistency, availability, and partition tolerance. |
| 4568 | What is consistency in CAP theorem? | All nodes see the same data at the same time | It is one CAP property. |
| 4569 | What is availability in CAP theorem? | Every request receives a response | It is one CAP property. |
| 4570 | What is partition tolerance in CAP theorem? | System operation despite network failures | It is one CAP property. |
| 4571 | What is microservices architecture? | An architecture using independently deployable services | It improves scalability and autonomy. |
| 4572 | What is monolithic architecture? | An application built as one deployable unit | It is simpler initially. |
| 4573 | What is modular monolith? | A monolith organized into independent modules | It combines simplicity with structure. |
| 4574 | What is service boundary? | A separation defining service responsibilities | It supports maintainability. |
| 4575 | What is API gateway? | A gateway routing requests to services | It provides centralized concerns. |
| 4576 | What is backend-for-frontend? | A backend designed for a specific client type | It optimizes client communication. |
| 4577 | What is service discovery? | Finding available services dynamically | It supports distributed systems. |
| 4578 | What is configuration service? | A service managing application configuration | It centralizes settings. |
| 4579 | What is containerization? | Packaging applications with dependencies | It improves portability. |
| 4580 | What is Docker? | A platform for building and running containers | It packages applications. |
| 4581 | What is Docker image? | A template used to create containers | It contains application layers. |
| 4582 | What is Docker container? | A running instance of an image | It isolates applications. |
| 4583 | What is Dockerfile? | A file describing how to build an image | It defines container steps. |
| 4584 | What is container registry? | A repository storing container images | It distributes images. |
| 4585 | What is Kubernetes? | A container orchestration platform | It manages container workloads. |
| 4586 | What is Kubernetes pod? | The smallest deployable Kubernetes unit | It contains one or more containers. |
| 4587 | What is Kubernetes deployment? | A resource managing application replicas | It controls rollout. |
| 4588 | What is Kubernetes service? | A network abstraction exposing pods | It provides connectivity. |
| 4589 | What is Kubernetes ingress? | A resource routing external HTTP traffic | It manages external access. |
| 4590 | What is container health probe? | A Kubernetes check for application health | It controls traffic and restarts. |
| 4591 | What is scaling? | Increasing or decreasing application capacity | It handles demand changes. |
| 4592 | What is horizontal scaling? | Adding more application instances | It improves throughput. |
| 4593 | What is vertical scaling? | Increasing resources of an existing instance | It improves individual capacity. |
| 4594 | What is auto scaling? | Automatically adjusting resources based on demand | It optimizes cost and performance. |
| 4595 | What is load test? | Testing system behavior under expected traffic | It measures capacity. |
| 4596 | What is stress test? | Testing beyond normal capacity | It identifies breaking points. |
| 4597 | What is spike test? | Testing sudden traffic increases | It evaluates elasticity. |
| 4598 | What is soak test? | Long-duration performance testing | It finds memory leaks. |
| 4599 | What is scalability? | Ability to handle increasing workload | It supports growth. |
| 4600 | What is elasticity? | Ability to automatically adjust resources | It supports changing demand. |
| 4601 | What is software architecture? | The high-level structure of a software system | It defines components and interactions. |
| 4602 | What is architectural pattern? | A reusable solution for common system structures | It guides design decisions. |
| 4603 | What is design pattern? | A reusable solution to common programming problems | It improves code organization. |
| 4604 | What is Gang of Four pattern? | A collection of classic object-oriented design patterns | It includes creational, structural, and behavioral patterns. |
| 4605 | What is Singleton pattern? | A pattern ensuring one instance of a class | It provides shared access. |
| 4606 | What is Factory pattern? | A pattern creating objects without exposing creation logic | It separates construction from usage. |
| 4607 | What is Abstract Factory pattern? | A pattern creating related object families | It supports interchangeable products. |
| 4608 | What is Builder pattern? | A pattern constructing complex objects step by step | It separates construction from representation. |
| 4609 | What is Prototype pattern? | A pattern creating objects by copying existing objects | It avoids expensive creation. |
| 4610 | What is Adapter pattern? | A pattern converting one interface into another | It enables compatibility. |
| 4611 | What is Decorator pattern? | A pattern adding behavior dynamically | It avoids subclass explosion. |
| 4612 | What is Facade pattern? | A pattern providing a simplified interface | It hides complexity. |
| 4613 | What is Proxy pattern? | A pattern controlling access to another object | It adds behavior around access. |
| 4614 | What is Composite pattern? | A pattern representing objects as tree structures | It treats groups and objects uniformly. |
| 4615 | What is Bridge pattern? | A pattern separating abstraction from implementation | It improves flexibility. |
| 4616 | What is Flyweight pattern? | A pattern sharing common object data | It reduces memory usage. |
| 4617 | What is Strategy pattern? | A pattern encapsulating interchangeable algorithms | It enables runtime selection. |
| 4618 | What is Observer pattern? | A pattern notifying dependent objects of changes | It supports event-based communication. |
| 4619 | What is Command pattern? | A pattern representing actions as objects | It supports undo and queuing. |
| 4620 | What is Mediator pattern? | A pattern centralizing object communication | It reduces dependencies. |
| 4621 | What is Template Method pattern? | A pattern defining algorithm structure in a base class | Derived classes customize steps. |
| 4622 | What is State pattern? | A pattern changing behavior based on state | It avoids complex conditions. |
| 4623 | What is Chain of Responsibility pattern? | A pattern passing requests through handlers | It creates flexible pipelines. |
| 4624 | What is Iterator pattern? | A pattern providing sequential access to elements | IEnumerable uses this concept. |
| 4625 | What is Dependency Injection pattern? | A pattern providing dependencies externally | It improves testability. |
| 4626 | What is Inversion of Control? | A principle where control flow is managed by a framework | DI is an example. |
| 4627 | What is SOLID principle? | A set of object-oriented design principles | It improves maintainability. |
| 4628 | What is Single Responsibility Principle? | A class should have one reason to change | It improves separation. |
| 4629 | What is Open/Closed Principle? | Software entities should be open for extension and closed for modification | It encourages flexible design. |
| 4630 | What is Liskov Substitution Principle? | Derived types should replace base types safely | It preserves correctness. |
| 4631 | What is Interface Segregation Principle? | Clients should not depend on unused members | It promotes focused interfaces. |
| 4632 | What is Dependency Inversion Principle? | High-level modules should depend on abstractions | It reduces coupling. |
| 4633 | What is DRY principle? | Avoiding duplicated code | It improves maintainability. |
| 4634 | What is KISS principle? | Keeping solutions simple | It reduces complexity. |
| 4635 | What is YAGNI principle? | Avoiding unnecessary features | It prevents overengineering. |
| 4636 | What is separation of concerns? | Dividing software into distinct responsibilities | It improves organization. |
| 4637 | What is cohesion? | Degree to which related responsibilities belong together | High cohesion is desirable. |
| 4638 | What is coupling? | Degree of dependency between components | Low coupling is preferred. |
| 4639 | What is tight coupling? | Strong dependency between components | It reduces flexibility. |
| 4640 | What is loose coupling? | Minimal dependency between components | It improves maintainability. |
| 4641 | What is clean architecture? | Architecture separating business rules from external concerns | It improves testability. |
| 4642 | What is hexagonal architecture? | Architecture isolating application logic through ports and adapters | It supports flexibility. |
| 4643 | What is onion architecture? | Architecture placing domain logic at the center | It emphasizes dependency direction. |
| 4644 | What is layered architecture? | Architecture dividing application into layers | It organizes responsibilities. |
| 4645 | What is presentation layer? | Layer handling user interaction | It communicates with users. |
| 4646 | What is application layer? | Layer coordinating use cases | It contains workflow logic. |
| 4647 | What is domain layer? | Layer containing business rules | It represents core logic. |
| 4648 | What is infrastructure layer? | Layer handling external systems | It contains technical implementations. |
| 4649 | What is persistence layer? | Layer managing data storage | It communicates with databases. |
| 4650 | What is anti-corruption layer? | A boundary protecting one domain from another model | It prevents unwanted dependencies. |
| 4651 | What is application architecture? | The organization of an application's major components | It defines system structure. |
| 4652 | What is monolithic application? | An application where all features are deployed together | It has a single deployment unit. |
| 4653 | What is modular architecture? | Architecture dividing an application into independent modules | It improves maintainability. |
| 4654 | What is module? | A self-contained unit of functionality | It groups related code. |
| 4655 | What is bounded module? | A module with clear responsibility and boundaries | It reduces dependencies. |
| 4656 | What is feature-based architecture? | Organizing code by business features | It improves discoverability. |
| 4657 | What is vertical slice architecture? | Organizing code around complete features | It reduces layer coupling. |
| 4658 | What is Clean Architecture dependency rule? | Dependencies point toward business logic | Inner layers remain independent. |
| 4659 | What is dependency direction? | The direction in which components depend on each other | It affects maintainability. |
| 4660 | What is architecture decision record? | A document capturing important design decisions | It preserves reasoning. |
| 4661 | What is technical debt? | Future cost caused by quick or poor design choices | It increases maintenance effort. |
| 4662 | What is refactoring? | Improving internal code structure without changing behavior | It reduces technical debt. |
| 4663 | What is code smell? | A sign of possible design problems | It suggests refactoring opportunities. |
| 4664 | What is duplicated code smell? | Repeated logic across code | It violates DRY. |
| 4665 | What is long method smell? | A method containing too much logic | It reduces readability. |
| 4666 | What is large class smell? | A class with too many responsibilities | It violates SRP. |
| 4667 | What is feature envy smell? | A method depending heavily on another class | It suggests poor placement. |
| 4668 | What is primitive obsession? | Excessive use of primitive types for domain concepts | It reduces expressiveness. |
| 4669 | What is magic number? | An unexplained constant value in code | It reduces readability. |
| 4670 | What is dead code? | Code that is never executed or used | It increases maintenance cost. |
| 4671 | What is code review? | A process of examining code changes | It improves quality. |
| 4672 | What is pull request? | A request to merge code changes | It enables review workflows. |
| 4673 | What is branch strategy? | A method for organizing source control branches | It supports collaboration. |
| 4674 | What is Git? | A distributed version control system | It tracks source changes. |
| 4675 | What is repository in Git? | A storage location containing version history | It tracks project files. |
| 4676 | What is commit? | A saved set of source changes | It records history. |
| 4677 | What is branch? | A separate line of development | It enables parallel work. |
| 4678 | What is merge? | Combining changes from branches | It integrates development work. |
| 4679 | What is merge conflict? | A conflict when Git cannot automatically combine changes | It requires manual resolution. |
| 4680 | What is rebase? | Moving commits onto another base branch | It creates cleaner history. |
| 4681 | What is tag in Git? | A named reference to a specific commit | It marks releases. |
| 4682 | What is Git stash? | A temporary storage for uncommitted changes | It preserves work in progress. |
| 4683 | What is cherry-pick? | Applying selected commits to another branch | It transfers specific changes. |
| 4684 | What is continuous integration? | Automatically building and testing code changes | It detects issues early. |
| 4685 | What is continuous delivery? | Preparing software for release automatically | It improves deployment reliability. |
| 4686 | What is continuous deployment? | Automatically releasing tested changes | It removes manual release steps. |
| 4687 | What is CI/CD pipeline? | An automated software delivery workflow | It manages build, test, and deployment. |
| 4688 | What is build pipeline? | A sequence of steps compiling and validating code | It produces artifacts. |
| 4689 | What is deployment pipeline? | A workflow delivering applications to environments | It automates releases. |
| 4690 | What is build artifact? | A generated output from a build process | It is deployed later. |
| 4691 | What is artifact repository? | Storage for build outputs | It manages package versions. |
| 4692 | What is package manager? | A tool managing software dependencies | It installs and updates packages. |
| 4693 | What is NuGet? | The .NET package manager | It distributes libraries. |
| 4694 | What is NuGet package? | A reusable .NET library package | It contains compiled code and metadata. |
| 4695 | What is PackageReference? | A project file reference to a NuGet package | It manages dependencies. |
| 4696 | What is semantic versioning? | A versioning scheme using major, minor, and patch numbers | It communicates compatibility. |
| 4697 | What is breaking change? | A change that breaks existing consumers | It requires migration. |
| 4698 | What is backward compatibility? | Ability to work with previous versions | It protects consumers. |
| 4699 | What is forward compatibility? | Ability to work with future versions | It supports evolution. |
| 4700 | What is dependency management? | Managing external libraries and versions | It controls application dependencies. |
| 4701 | What is software testing? | The process of verifying software behavior | It improves reliability. |
| 4702 | What is unit testing? | Testing individual components in isolation | It validates small pieces of code. |
| 4703 | What is integration testing? | Testing interactions between components | It validates system connections. |
| 4704 | What is system testing? | Testing the complete application | It validates end-to-end behavior. |
| 4705 | What is acceptance testing? | Testing whether software meets business requirements | It validates user expectations. |
| 4706 | What is regression testing? | Re-running tests after changes | It prevents new defects. |
| 4707 | What is smoke testing? | Basic testing confirming essential functionality | It detects major failures quickly. |
| 4708 | What is sanity testing? | Testing specific changes after fixes | It verifies targeted functionality. |
| 4709 | What is exploratory testing? | Testing through investigation without predefined scripts | It discovers unexpected issues. |
| 4710 | What is test case? | A documented scenario for testing behavior | It defines inputs and expected results. |
| 4711 | What is test suite? | A collection of test cases | It groups related tests. |
| 4712 | What is test fixture? | Setup required for running tests | It prepares test conditions. |
| 4713 | What is test runner? | A tool executing tests | It reports results. |
| 4714 | What is assertion? | A statement verifying expected behavior | It determines test success. |
| 4715 | What is xUnit? | A .NET testing framework | It supports unit testing. |
| 4716 | What is NUnit? | A .NET unit testing framework | It provides test attributes and assertions. |
| 4717 | What is MSTest? | Microsoft's testing framework for .NET | It integrates with Visual Studio. |
| 4718 | What is Moq? | A mocking framework for .NET | It creates test doubles. |
| 4719 | What is mocking? | Replacing dependencies with simulated objects | It isolates unit tests. |
| 4720 | What is stub? | A simple test replacement returning predefined results | It controls test input. |
| 4721 | What is fake object? | A working lightweight implementation for testing | It replaces real dependencies. |
| 4722 | What is spy object? | A test object recording interactions | It verifies calls. |
| 4723 | What is test double? | A generic term for test replacements | It includes mocks and stubs. |
| 4724 | What is dependency isolation? | Separating code under test from external systems | It improves unit testing. |
| 4725 | What is test-driven development? | Writing tests before implementation code | It guides design. |
| 4726 | What is behavior-driven development? | Testing based on business behavior descriptions | It improves communication. |
| 4727 | What is Arrange-Act-Assert pattern? | A structure for organizing unit tests | It separates setup, execution, and verification. |
| 4728 | What is code coverage? | A measure of tested code execution | It indicates test completeness. |
| 4729 | What is branch coverage? | Coverage measuring executed decision paths | It tests conditions. |
| 4730 | What is line coverage? | Coverage measuring executed code lines | It measures execution. |
| 4731 | What is mutation testing? | Testing test quality by introducing code changes | It detects weak tests. |
| 4732 | What is performance testing? | Testing speed and resource usage | It evaluates scalability. |
| 4733 | What is security testing? | Testing protection against vulnerabilities | It improves application safety. |
| 4734 | What is penetration testing? | Simulated attack testing | It discovers security weaknesses. |
| 4735 | What is vulnerability scanning? | Automated detection of security issues | It identifies risks. |
| 4736 | What is static analysis? | Analyzing code without execution | It detects problems early. |
| 4737 | What is dynamic analysis? | Analyzing software during execution | It observes runtime behavior. |
| 4738 | What is code analyzer? | A tool checking source code quality | It detects issues and suggestions. |
| 4739 | What is Roslyn analyzer? | A C# compiler-based code analysis tool | It provides diagnostics. |
| 4740 | What is compiler warning? | A message about possible code problems | It does not always stop compilation. |
| 4741 | What is compiler error? | A problem preventing compilation | Code must be fixed. |
| 4742 | What is nullable reference type warning? | A warning about possible null usage | It improves null safety. |
| 4743 | What is SonarQube? | A code quality analysis platform | It detects bugs and smells. |
| 4744 | What is security vulnerability? | A weakness that can be exploited | It threatens system protection. |
| 4745 | What is OWASP? | An organization providing application security guidance | It publishes security standards. |
| 4746 | What is OWASP Top 10? | A list of common web application security risks | It guides security practices. |
| 4747 | What is authentication? | Verifying user identity | It confirms who a user is. |
| 4748 | What is authorization? | Determining permitted actions | It controls access. |
| 4749 | What is identity? | Information representing a user or principal | It supports security decisions. |
| 4750 | What is principal? | An entity requesting access | It can be a user or service. |
| 4751 | What is claims-based authentication? | Authentication using claims about a user | It carries identity information. |
| 4752 | What is claim? | A piece of information about a user or entity | It represents identity attributes. |
| 4753 | What is ClaimsPrincipal? | A .NET object representing the current user | It contains identities and claims. |
| 4754 | What is ClaimsIdentity? | An object representing an authenticated identity | It stores claims and authentication type. |
| 4755 | What is role-based authorization? | Authorization based on user roles | It controls access by groups. |
| 4756 | What is policy-based authorization? | Authorization based on configurable policies | It supports flexible rules. |
| 4757 | What is authorization policy? | A set of requirements for access | It determines permissions. |
| 4758 | What is authorization requirement? | A rule that must be satisfied for access | It is used in policies. |
| 4759 | What is authorization handler? | A component evaluating authorization requirements | It decides access. |
| 4760 | What is IAuthorizationService? | A service checking authorization policies | It supports custom authorization. |
| 4761 | What is resource-based authorization? | Authorization based on the object being accessed | It checks resource ownership or rules. |
| 4762 | What is ASP.NET Core Identity? | A framework for managing users and authentication | It provides identity features. |
| 4763 | What is UserManager? | A service managing user accounts | It handles user operations. |
| 4764 | What is SignInManager? | A service managing user sign-in operations | It handles authentication workflows. |
| 4765 | What is RoleManager? | A service managing application roles | It manages role data. |
| 4766 | What is IdentityUser? | The default user entity in ASP.NET Core Identity | It stores user information. |
| 4767 | What is IdentityRole? | The default role entity in ASP.NET Core Identity | It stores role information. |
| 4768 | What is password hashing? | Converting passwords into secure stored values | It protects credentials. |
| 4769 | What is password salt? | Random data added before hashing passwords | It prevents identical hashes. |
| 4770 | What is password policy? | Rules controlling password requirements | It improves account security. |
| 4771 | What is account lockout? | Temporarily blocking accounts after failures | It prevents brute force attacks. |
| 4772 | What is two-factor authentication? | Authentication requiring two verification methods | It improves security. |
| 4773 | What is MFA? | Multi-factor authentication using multiple factors | It strengthens identity protection. |
| 4774 | What is authenticator app? | An application generating verification codes | It supports MFA. |
| 4775 | What is one-time password? | A temporary authentication code | It is valid for limited use. |
| 4776 | What is JWT? | JSON Web Token used for authentication and information exchange | It is common in APIs. |
| 4777 | What is JWT header? | Token section describing metadata | It contains algorithm information. |
| 4778 | What is JWT payload? | Token section containing claims | It stores identity data. |
| 4779 | What is JWT signature? | Token section verifying integrity | It prevents tampering. |
| 4780 | What is bearer token? | A token presented to access protected resources | It is sent in Authorization headers. |
| 4781 | What is access token? | A token granting API access | It has limited lifetime. |
| 4782 | What is refresh token? | A token used to obtain new access tokens | It supports long sessions. |
| 4783 | What is token expiration? | Time after which a token becomes invalid | It limits exposure. |
| 4784 | What is token validation? | Checking token authenticity and claims | It ensures secure access. |
| 4785 | What is OAuth 2.0? | An authorization framework for delegated access | It enables secure API access. |
| 4786 | What is OpenID Connect? | An identity layer built on OAuth 2.0 | It provides authentication. |
| 4787 | What is identity provider? | A system authenticating users | It issues identity tokens. |
| 4788 | What is authorization server? | A server issuing access tokens | It manages OAuth flows. |
| 4789 | What is resource server? | A server hosting protected resources | It validates access tokens. |
| 4790 | What is client application? | An application requesting access to resources | It uses OAuth flows. |
| 4791 | What is OAuth client credentials flow? | A flow for service-to-service authentication | It uses application identity. |
| 4792 | What is authorization code flow? | OAuth flow for user authentication | It uses a temporary code. |
| 4793 | What is PKCE? | Proof Key for Code Exchange | It protects authorization code flow. |
| 4794 | What is CORS? | Cross-Origin Resource Sharing mechanism | It controls browser cross-origin requests. |
| 4795 | What is CSRF? | Cross-Site Request Forgery attack | It tricks users into unwanted actions. |
| 4796 | What is XSS? | Cross-Site Scripting attack | It injects malicious scripts. |
| 4797 | What is SQL injection prevention? | Techniques preventing malicious SQL execution | Parameterization is a common method. |
| 4798 | What is HTTPS? | HTTP over TLS encryption | It protects data in transit. |
| 4799 | What is TLS? | Transport Layer Security protocol | It encrypts communication. |
| 4800 | What is certificate? | A digital document proving identity | It enables secure communication. |
| 4801 | What is digital signature? | A cryptographic mechanism verifying authenticity and integrity | It proves data origin. |
| 4802 | What is encryption? | Converting data into an unreadable format | It protects confidentiality. |
| 4803 | What is decryption? | Converting encrypted data back to readable form | It requires a key. |
| 4804 | What is symmetric encryption? | Encryption using the same key for encryption and decryption | It is fast for large data. |
| 4805 | What is asymmetric encryption? | Encryption using public and private keys | It supports secure key exchange. |
| 4806 | What is public key? | A key shared openly in asymmetric cryptography | It encrypts or verifies data. |
| 4807 | What is private key? | A secret key in asymmetric cryptography | It decrypts or signs data. |
| 4808 | What is hashing? | Converting data into a fixed-size value | It is one-way. |
| 4809 | What is cryptographic hash? | A secure hash function used for integrity | Examples include SHA-256. |
| 4810 | What is SHA-256? | A secure hashing algorithm | It produces a 256-bit hash. |
| 4811 | What is HMAC? | Hash-based message authentication code | It verifies message integrity. |
| 4812 | What is nonce? | A value used once in cryptographic operations | It prevents replay attacks. |
| 4813 | What is replay attack? | An attack reusing captured communication | Nonces and timestamps prevent it. |
| 4814 | What is brute force attack? | Trying many possible credentials or keys | Rate limiting helps prevent it. |
| 4815 | What is rate limiting? | Controlling the number of requests allowed | It protects resources. |
| 4816 | What is throttling? | Restricting request processing speed | It manages load. |
| 4817 | What is API key? | A token identifying an application | It controls API access. |
| 4818 | What is secret management? | Secure handling of sensitive values | It protects credentials. |
| 4819 | What is Azure Key Vault? | A service storing secrets, keys, and certificates | It secures application secrets. |
| 4820 | What is environment variable? | A value supplied by the operating environment | It stores configuration settings. |
| 4821 | What is secret rotation? | Replacing secrets periodically | It reduces security risk. |
| 4822 | What is least privilege principle? | Giving only required permissions | It reduces attack surface. |
| 4823 | What is defense in depth? | Using multiple security layers | It improves protection. |
| 4824 | What is secure coding? | Writing software resistant to vulnerabilities | It follows security practices. |
| 4825 | What is input validation? | Checking user input before processing | It prevents invalid data. |
| 4826 | What is output encoding? | Escaping output before displaying it | It prevents injection attacks. |
| 4827 | What is secure headers? | HTTP headers improving browser security | They reduce attacks. |
| 4828 | What is Content Security Policy? | A browser security policy controlling resource loading | It mitigates XSS. |
| 4829 | What is HSTS? | HTTP Strict Transport Security | It forces HTTPS usage. |
| 4830 | What is SameSite cookie? | A cookie attribute controlling cross-site sending | It helps prevent CSRF. |
| 4831 | What is HttpOnly cookie? | A cookie inaccessible to JavaScript | It reduces theft risk. |
| 4832 | What is Secure cookie? | A cookie sent only over HTTPS | It protects transmission. |
| 4833 | What is session authentication? | Authentication using server-managed sessions | It stores user state. |
| 4834 | What is cookie authentication? | Authentication using encrypted cookies | It maintains login sessions. |
| 4835 | What is authentication middleware? | Middleware handling user authentication | It sets user identity. |
| 4836 | What is authorization middleware? | Middleware enforcing access rules | It checks permissions. |
| 4837 | What is UseAuthentication()? | ASP.NET Core middleware enabling authentication | It populates user identity. |
| 4838 | What is UseAuthorization()? | ASP.NET Core middleware enforcing authorization | It applies policies. |
| 4839 | What is authentication scheme? | A method used to authenticate users | Examples include cookies and JWT. |
| 4840 | What is authentication handler? | Component processing an authentication scheme | It creates identities. |
| 4841 | What is JWT bearer authentication? | Authentication using JWT tokens | It is common for APIs. |
| 4842 | What is cookie handler? | Authentication handler using cookies | It manages login cookies. |
| 4843 | What is policy scheme? | A scheme selecting another authentication scheme | It enables dynamic selection. |
| 4844 | What is authorization filter? | A filter executing authorization logic | It protects actions. |
| 4845 | What is security audit? | Reviewing security controls and events | It identifies weaknesses. |
| 4846 | What is audit logging? | Recording security-related activities | It supports investigation. |
| 4847 | What is compliance? | Meeting required standards and regulations | It guides security practices. |
| 4848 | What is GDPR? | European data protection regulation | It protects personal data. |
| 4849 | What is privacy by design? | Building privacy into systems from the beginning | It reduces privacy risks. |
| 4850 | What is data protection? | Protecting information from unauthorized access or loss | It ensures confidentiality and integrity. |
| 4851 | What is personal data? | Information relating to an identifiable person | GDPR protects it. |
| 4852 | What is data minimization? | Collecting only necessary personal data | It reduces privacy risks. |
| 4853 | What is data retention? | Controlling how long data is stored | It supports compliance. |
| 4854 | What is data anonymization? | Removing identifying information from data | It protects privacy. |
| 4855 | What is data pseudonymization? | Replacing identifiers with artificial values | It reduces identification risk. |
| 4856 | What is privacy impact assessment? | An analysis of privacy risks | It supports GDPR compliance. |
| 4857 | What is security incident? | An event compromising security | It requires investigation. |
| 4858 | What is breach notification? | Reporting a security breach | It informs affected parties. |
| 4859 | What is threat modeling? | Identifying and analyzing security threats | It improves system security. |
| 4860 | What is STRIDE model? | A threat modeling framework | It categorizes security threats. |
| 4861 | What is spoofing? | Pretending to be another identity | It threatens authentication. |
| 4862 | What is tampering? | Unauthorized modification of data | It threatens integrity. |
| 4863 | What is repudiation? | Denying performed actions | Logging helps prevent it. |
| 4864 | What is information disclosure? | Exposing sensitive information | Encryption helps prevent it. |
| 4865 | What is denial of service? | Making a service unavailable | Rate limiting helps mitigate it. |
| 4866 | What is elevation of privilege? | Gaining unauthorized permissions | Access controls prevent it. |
| 4867 | What is secure software lifecycle? | Integrating security throughout development | It reduces vulnerabilities. |
| 4868 | What is DevSecOps? | Integrating security into DevOps practices | It automates security checks. |
| 4869 | What is security scanning? | Automated analysis for vulnerabilities | It finds security issues. |
| 4870 | What is dependency scanning? | Checking libraries for known vulnerabilities | It protects supply chains. |
| 4871 | What is software bill of materials? | A list of software components and dependencies | It improves transparency. |
| 4872 | What is SBOM? | Software Bill of Materials abbreviation | It tracks components. |
| 4873 | What is supply chain attack? | An attack through trusted dependencies or vendors | It targets software ecosystems. |
| 4874 | What is vulnerability management? | Process of identifying and fixing vulnerabilities | It reduces security exposure. |
| 4875 | What is patch management? | Process of applying software updates | It fixes known issues. |
| 4876 | What is security patch? | An update fixing security problems | It improves protection. |
| 4877 | What is zero-day vulnerability? | A vulnerability unknown to defenders | It is difficult to mitigate. |
| 4878 | What is exploit? | Code or technique taking advantage of a vulnerability | It causes unintended behavior. |
| 4879 | What is malware? | Malicious software designed to harm systems | It includes viruses and trojans. |
| 4880 | What is ransomware? | Malware encrypting data for payment demands | It disrupts operations. |
| 4881 | What is phishing? | A social engineering attack using deception | It targets users. |
| 4882 | What is social engineering? | Manipulating people to reveal information | It exploits human behavior. |
| 4883 | What is insider threat? | Risk caused by authorized users | It requires monitoring. |
| 4884 | What is endpoint security? | Protecting user devices and endpoints | It reduces attack risks. |
| 4885 | What is network security? | Protecting network communication and infrastructure | It prevents unauthorized access. |
| 4886 | What is firewall? | A system controlling network traffic | It filters connections. |
| 4887 | What is Web Application Firewall? | A firewall protecting web applications | It blocks web attacks. |
| 4888 | What is WAF rule? | A rule controlling web traffic behavior | It detects malicious requests. |
| 4889 | What is VPN? | Virtual Private Network providing secure connections | It encrypts network traffic. |
| 4890 | What is proxy server? | A server forwarding requests on behalf of clients | It controls communication. |
| 4891 | What is reverse proxy security? | Protection provided by a reverse proxy | It includes filtering and TLS handling. |
| 4892 | What is DDoS attack? | Distributed Denial of Service attack | It floods services with traffic. |
| 4893 | What is DDoS protection? | Measures preventing large traffic attacks | It improves availability. |
| 4894 | What is bot detection? | Identifying automated malicious traffic | It protects applications. |
| 4895 | What is CAPTCHA? | A challenge distinguishing humans from bots | It reduces automated abuse. |
| 4896 | What is API security? | Protecting application programming interfaces | It controls access and usage. |
| 4897 | What is API gateway security? | Security controls at an API gateway | It manages authentication and filtering. |
| 4898 | What is API rate limiting? | Restricting API request frequency | It prevents abuse. |
| 4899 | What is API versioning? | Managing different API versions | It supports evolution. |
| 4900 | What is API deprecation? | Removing or retiring an old API version | It encourages migration. |
| 4901 | What is REST API? | An API style based on HTTP resources and operations | It is widely used for web services. |
| 4902 | What is REST resource? | An entity exposed through an API endpoint | It represents application data. |
| 4903 | What is REST endpoint? | A URL representing an API operation or resource | Clients use it for communication. |
| 4904 | What is HTTP GET? | An HTTP method used to retrieve data | It should be safe and idempotent. |
| 4905 | What is HTTP POST? | An HTTP method used to create resources or process data | It usually changes server state. |
| 4906 | What is HTTP PUT? | An HTTP method used to replace a resource | It is generally idempotent. |
| 4907 | What is HTTP PATCH? | An HTTP method used for partial updates | It modifies selected fields. |
| 4908 | What is HTTP DELETE? | An HTTP method used to remove resources | It deletes server data. |
| 4909 | What is HTTP HEAD? | An HTTP method returning headers without a body | It checks resource metadata. |
| 4910 | What is HTTP OPTIONS? | An HTTP method describing supported operations | It is used in CORS. |
| 4911 | What is HTTP status code? | A numeric response indicating request result | It communicates outcome. |
| 4912 | What is 200 OK? | HTTP success status for completed requests | It indicates successful processing. |
| 4913 | What is 201 Created? | HTTP status indicating a resource was created | It is common after POST. |
| 4914 | What is 202 Accepted? | HTTP status indicating processing was accepted | Work may complete later. |
| 4915 | What is 204 No Content? | HTTP success status with no response body | It is used for empty responses. |
| 4916 | What is 400 Bad Request? | HTTP status for invalid client input | The request cannot be processed. |
| 4917 | What is 401 Unauthorized? | HTTP status indicating missing or invalid authentication | Credentials are required. |
| 4918 | What is 403 Forbidden? | HTTP status indicating insufficient permission | Access is denied. |
| 4919 | What is 404 Not Found? | HTTP status indicating missing resource | The resource does not exist. |
| 4920 | What is 409 Conflict? | HTTP status indicating a resource conflict | It handles duplicate or conflicting operations. |
| 4921 | What is 422 Unprocessable Entity? | HTTP status indicating validation failure | Data format is understood but invalid. |
| 4922 | What is 429 Too Many Requests? | HTTP status indicating rate limit exceeded | The client should retry later. |
| 4923 | What is 500 Internal Server Error? | HTTP status for server-side failures | It indicates unexpected errors. |
| 4924 | What is 502 Bad Gateway? | HTTP status indicating invalid upstream response | It often occurs with proxies. |
| 4925 | What is 503 Service Unavailable? | HTTP status indicating temporary unavailability | It may indicate overload or maintenance. |
| 4926 | What is 504 Gateway Timeout? | HTTP status indicating upstream timeout | A dependency did not respond. |
| 4927 | What is content negotiation? | Selecting response format based on client request | It uses headers like Accept. |
| 4928 | What is Accept header? | HTTP header specifying desired response formats | It supports negotiation. |
| 4929 | What is Content-Type header? | HTTP header describing message body format | It identifies payload type. |
| 4930 | What is media type? | A format identifier for transmitted data | Examples include JSON and XML. |
| 4931 | What is application/json? | JSON media type used in HTTP APIs | It is common for REST APIs. |
| 4932 | What is XML? | Extensible Markup Language for structured data | It is another API format. |
| 4933 | What is JSON? | JavaScript Object Notation data format | It is lightweight and common. |
| 4934 | What is serialization? | Converting objects into transferable formats | It enables communication. |
| 4935 | What is deserialization? | Converting data back into objects | It restores application models. |
| 4936 | What is System.Text.Json? | Built-in .NET JSON serialization library | It provides high-performance JSON support. |
| 4937 | What is JsonSerializer? | .NET class for JSON conversion | It serializes and deserializes objects. |
| 4938 | What is JSON converter? | A component customizing JSON serialization | It handles special types. |
| 4939 | What is Newtonsoft.Json? | A popular .NET JSON library | It provides advanced JSON features. |
| 4940 | What is DTO? | Data Transfer Object used for communication | It separates API models from domain models. |
| 4941 | What is API contract? | A definition of API inputs and outputs | It guides consumers. |
| 4942 | What is OpenAPI? | A specification describing HTTP APIs | It enables documentation and tooling. |
| 4943 | What is Swagger? | A toolset for OpenAPI documentation | It provides interactive API UI. |
| 4944 | What is Swagger UI? | A web interface for testing APIs | It displays API operations. |
| 4945 | What is Swagger document? | A machine-readable API description | It describes endpoints and schemas. |
| 4946 | What is API documentation? | Documentation explaining API usage | It helps developers integrate. |
| 4947 | What is API client? | An application consuming an API | It sends requests and processes responses. |
| 4948 | What is typed API client? | A client generated with strongly typed models | It improves developer experience. |
| 4949 | What is Refit? | A .NET library for generating REST clients | It simplifies API consumption. |
| 4950 | What is HttpClient? | .NET class for sending HTTP requests | It communicates with web services. |
| 4951 | What is HttpClientFactory? | A .NET service for creating and managing HttpClient instances | It handles lifetime and configuration. |
| 4952 | What is named HttpClient? | A configured HttpClient identified by name | It supports multiple API configurations. |
| 4953 | What is typed HttpClient? | A strongly typed wrapper around HttpClient | It improves maintainability. |
| 4954 | What is delegating handler? | A middleware component for HttpClient requests | It adds cross-cutting behavior. |
| 4955 | What is HttpMessageHandler? | A component processing HTTP requests and responses | It powers HttpClient communication. |
| 4956 | What is Polly? | A .NET resilience library | It handles retries and failures. |
| 4957 | What is retry policy? | A rule defining repeated attempts after failures | It handles transient errors. |
| 4958 | What is exponential backoff? | Increasing delay between retry attempts | It reduces system pressure. |
| 4959 | What is circuit breaker pattern? | A pattern stopping calls after repeated failures | It prevents cascading failures. |
| 4960 | What is timeout policy? | A rule limiting operation duration | It prevents hanging requests. |
| 4961 | What is bulkhead pattern? | A pattern isolating resources between operations | It prevents failures spreading. |
| 4962 | What is fallback policy? | A policy providing alternative behavior after failure | It improves resilience. |
| 4963 | What is resilience? | Ability of a system to handle failures | It improves reliability. |
| 4964 | What is fault tolerance? | Ability to continue operating despite failures | It supports availability. |
| 4965 | What is availability? | Percentage of time a system is operational | It measures uptime. |
| 4966 | What is reliability? | Ability to perform correctly over time | It measures dependability. |
| 4967 | What is observability? | Ability to understand system behavior through outputs | It uses logs, metrics, and traces. |
| 4968 | What is monitoring? | Tracking system health and performance | It detects issues. |
| 4969 | What is logging? | Recording application events and information | It supports troubleshooting. |
| 4970 | What is structured logging? | Logging with searchable fields instead of plain text | It improves analysis. |
| 4971 | What is Serilog? | A structured logging library for .NET | It supports rich log events. |
| 4972 | What is ILogger? | .NET logging abstraction | It provides application logging. |
| 4973 | What is log level? | A severity classification for log messages | Examples include Information and Error. |
| 4974 | What is Trace log level? | Detailed diagnostic logging level | It is used for deep debugging. |
| 4975 | What is Debug log level? | Logging for developer diagnostics | It helps troubleshooting. |
| 4976 | What is Information log level? | Normal operational logging level | It records application events. |
| 4977 | What is Warning log level? | Logging for potential issues | It indicates attention may be needed. |
| 4978 | What is Error log level? | Logging for failures and exceptions | It indicates problems. |
| 4979 | What is Critical log level? | Logging for severe failures | It indicates major system impact. |
| 4980 | What is log aggregation? | Collecting logs from multiple systems | It enables centralized analysis. |
| 4981 | What is centralized logging? | Storing logs in a common location | It simplifies troubleshooting. |
| 4982 | What is Elasticsearch? | A search and analytics engine | It stores and searches logs. |
| 4983 | What is Kibana? | A visualization tool for Elasticsearch data | It displays dashboards. |
| 4984 | What is ELK stack? | Elasticsearch, Logstash, and Kibana stack | It supports log analysis. |
| 4985 | What is Application Insights? | Azure monitoring service for applications | It collects telemetry. |
| 4986 | What is telemetry? | Data describing system operation | It supports observability. |
| 4987 | What is metric? | A numerical measurement of system behavior | It tracks performance. |
| 4988 | What is trace? | A record of request execution flow | It supports distributed debugging. |
| 4989 | What is distributed tracing? | Tracking requests across multiple services | It identifies bottlenecks. |
| 4990 | What is OpenTelemetry? | An observability standard for telemetry collection | It supports logs, metrics, and traces. |
| 4991 | What is health check? | A mechanism verifying application availability | It detects failures. |
| 4992 | What is liveness check? | A check confirming an application is running | It triggers restarts when unhealthy. |
| 4993 | What is readiness check? | A check confirming an application can receive traffic | It controls routing. |
| 4994 | What is ASP.NET Core Health Checks? | A framework feature for health monitoring | It exposes health endpoints. |
| 4995 | What is /health endpoint? | An endpoint reporting application health | It is used by monitoring systems. |
| 4996 | What is uptime monitoring? | Monitoring whether a service is available | It tracks availability. |
| 4997 | What is alerting? | Notifying teams about important events | It enables quick response. |
| 4998 | What is incident response? | Process of handling system incidents | It restores service. |
| 4999 | What is root cause analysis? | Finding the underlying reason for a problem | It prevents recurrence. |
| 5000 | What is postmortem? | A review after an incident | It identifies improvements. |
