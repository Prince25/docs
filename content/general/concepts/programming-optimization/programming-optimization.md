---
Title: 'Programming Optimization'
Description: 'Optimization in programming is the process of modifying a software system to execute faster and become more efficient by minimizing the use of available computing resources.'
Subject:
- 'Web Development'
Tags:
- 'Optimization in Programing'
- 'Programming Optimization'
CatalogContent:
- 'paths/computer-science'
- 'web-development'
---
***Programming Optimization*** is the process of modifying a software system to amplify its functionality, making the application execute faster and more efficiently by minimizing the use of computing resources. In other words, a computer program may be optimized to reduce execution time, memory usage, disk space, bandwidth, and even draw less power. This usually requires a trade-off, where one aspect is implemented at the expense of others (eg. increasing the size of cache improves run-time performance but also increases memory consumption).

It has become an important focal point since today’s users appreciate a highly performant experience and have significantly higher expectations. It has become a deciding factor of the success of modern business in today’s digital market. Optimization in programming is a key element in the improvement of such performance.

## Programming Optimization
Optimization in programming is an extensive topic, it relies on many different metrics, focuses and areas within the application depending on specific situations.

Although consideration and awareness of performance issues of design and implementation should be factored into every part of the development cycle, it should not be the primary concern within the first iteration. These can potentially complicate the design and/or implementation, hence should be left until the final iteration of the application. 

Techniques used can be broken up among various scopes which can affect anything from a single statement to the entire program. Generally speaking, locally scoped techniques are easier to implement than global ones, though they may result in smaller gains. 

These are important points to target for optimization in programming:

- reducing code complexity
- avoiding unnecessary for-loops
- using data structures similar to like sorting, string concatenation
- avoiding unnecessary functions
- avoiding dots
- initializing dictionary elements
- import statement overhead
- data aggregation
- re-map functions at runtime
- profiling code   

## Levels of Optimization
Every application, generally, is composed of 2 areas where programming optimizations can be applied within levels of development:

***Client Side***, which is the side seen on the web browser by the user, includes: 
- JavaScript that runs in the browser
- load times for pages
- images
- videos
- downloading of any resources required by the application, etc.

A few of the techniques that can be applied optimize the programming on the client side could be: 
- caching and content delivery networks
- bundle and minification
- image usage
- removing duplicate JavaScript and CSS code
- using minimalist styling frameworks, etc.

***Server Side***, this second side relates to any computations done behind the scenes, tends to involve:
- database queries and processing
- application configuration and dependencies, etc.        

Although not restricted to only these, typical strategies that help with this include:
- using an appropriate server application instead of the default
- enable caching(opcode, memory, http and application)
- de-fragmentation of database tables
- database settings
- virtualization
- dns query response time
- and again, this list can go on depending how deep requirements are needed. 

These programming optimizations can occur at different levels within the cycle of the application's creation. Consideration tends to be given to efficiency throughout a project, though this varies significantly, but major optimization in the programming is often considered a refinement to be done later, if ever. 

Typically the higher levels have greater impact and are harder to change later on in a project, requiring significant changes or even a complete rewrite. On longer-running projects there are typically cycles of optimization, where improving one area reveals limitations in another, and these are typically curtailed when performance is acceptable and gains become too small or costly.

### Design
The architecture design of a system plays a major role, its optimization can overwhelmingly affect the system's performance by making the best use of the available resources and expected load (e.g. network latency can be optimized to minimize requests, ideally making a single request rather than multiple requests to the network).

Ultimately the choice of design depends on the goals of the project: If speed of the output is a key priority in the compilation when designing the compiler, taking into account the same level of work, a one-pass compiler is faster than a multi-pass compiler and although a multi-pass is slower, it may fulfill the overall objective just fine. The platform and programming source code language to be used will also be decided at this level.

Changing any of these will most definitely require extensive rewrites, which is always a practice to avoid, regardless if a modular system may allow rewrites of some components. (eg. a Python program may rewrite performance-critical sections in C). In a distributed system, choice of design (e.g. client-server, peer-to-peer, etc.) occurs at this level and may be extremely challenging to modify later on, particularly if all components cannot be replaced in sync (e.g. old clients).

### Algorithms and Database Structures
After the design solution, an efficient implementation for the algorithms and data structure should be decided on, and will play a key role to the system’s performance.
  
Generally data structures are more difficult to change than algorithms since a data structure and its performance assumptions are used throughout the program. Changing a data structure after implementing it is an uphill battle, it’s crucial to think wisely before implementing an algorithmic solution for any optimization. This can be minimized by the use of abstract data types in function definitions, keeping the concrete data structure definitions restricted to a few places.

Optimized systems tend to have algorithms that are constant O(1), logarithmic O(log n), linear O(n) or log-linear O(n log n). For example, a linear search is asymptotically slower than a binary search, but a linear search is faster for small inputs and a binary search is faster for large inputs. Quadratic complexity algorithms O(n2) fail to scale and even linear algorithms cause problems if repeatedly called and are typically replaced with constant or logarithmic whenever it is possible to do so.

Beyond asymptotic order of growth, the constant factors matter: An asymptotically slower algorithm may be faster or smaller because it is simpler than an asymptotically faster algorithm when they are both faced with a small input, which may be the reality for most cases. 

Memoization is also an important dynamic programming caching technique to optimize the code, preventing redundant computations. Because of the importance of caching, there are often many levels of caching in a system because of possible problems from memory use and correctness issues from stale caches.

### Source Code
Beyond algorithm implementation, source code level choices can make a significant impact in programming optimization performance. 

For example,
- control flow statements like while loops are slower than for loops for an unconditional loop. 
- On early C compilers, for loops had an unconditional jump, however, while loops have a conditional jump.
- a language that is dynamically typed may be slower than a statically typed language, but it may be easier to write and maintain.

In the most general terms, source code optimization tends to substitute generic high-level programming structures with lower-level source code, thus enhancing performance and/or reducing resource consumption (e.g. CPU, memory, etc.).

Such aforementioned programming optimizations can now be performed by compilers. Although compilers can optimize source code at a lower level, they are often limited to general purpose optimization, thus making manual optimization still necessary, allowing talented and experienced programmers to be creative with their solutions.  

Important source code optimizing objectives to focus on would be: 
- Rewrite or remove redundant code. 
- Reduce execution speed. 
- Reduce available resources, whenever possible.

Also important key points to keep in mind before optimizing the source code: 
- Time based optimization can execute faster output, but it can also lead to a bigger code base, which can create conflict with memory and consumption.
- Performance optimization is a never-ending process. There will always be improvement opportunities for faster source code, especially as technology keeps moving ahead.
- Certain optimization methods in programming to execute faster outputs may not follow best coding standards and practices. Avoiding such methods will render better results long term. 
- Let's not forget that temptation to use certain optimization methods in programming to execute faster outputs and can result in best coding standards and practices not be followed. Avoiding such methods will render better results long term.

The following are some examples of different types of source coding optimizations: 
#### Loop Optimization
A majority of system programs, if not all, operate in loops. It is vital to optimize these to save CPU cycles and memory, avoiding loop-invariants and performing induction analysis will have a positive impact on optimization.

Example:

```javascript
do { i = 10;  v = v + i; } 
while (v<100);
```

The code above repeats the assignment of the identifier i for every iteration.

```javascript
i = 10;
do { v = v + i; } 
while (v<100);
```

Written as above should not only save the CPU cycles but can also be used on any processor.

#### Strength Reduction
Some expressions use more CPU cycles, time, and memory than others. These expressions should be replaced with less expensive expressions without sacrificing the output (e.g. multiplication (x * 2) uses more CPU cycles than (x 1) but producing the same output).

#### Partially Dead Code
This type of source code refers to statements that include value calculations that are used only in particular and irregular conditions.

#### Unreachable Code Elimination
Before implementing this type of source code optimization, ideally a control flow graph should be created first. Only after determining that a particular inaccessible code block does not have an incoming edge, these branches can then be deleted after continual propagation and folding.

#### Function Inlining  
The body of the function takes the place of a function call. This saves a lot of time by eliminating the need to copy all parameters, store the return address, and so on.

#### Function Cloning
For different calling arguments, specialized source codes functions are implemented (e.g. overloading a function is an example of this).

#### Partial Redundancy
In a parallel route, redundant expressions are calculated many times without changing the operands and partial-redundant, on the other hand, are calculated several times along a path without changing the operands. A code-motion approach, loop-invariant can possibly result in a largely redundant render.

### Builds
This level lands in between the source code and compiler level. Using preprocessor defines to disable unneeded software features can be done to optimize for specific processor models, hardware capabilities and/or predicting branching. These types of directives and build flags can facilitate improvement within the source code and compiler, also source-based software distribution systems can take advantage of this form of optimization.

Towards the end of the development stage will be an optimal time to perform any deep programming optimizations since these tend to reduce readability and also the source codes and/or technologies to achieve this may complicate the maintenance and any debugging that may be needed.

### Compilers
What is a compiler used for?
A compiler is a specific piece of software that converts the source code of a computer language into machine code, byte code, or another programming language. 

Typically, the source code is written in a high-level, human-readable language and these structures are replaced with highly efficient low-level programming codes to the extent of the compiler's program. The compiler can improve loops and address computations after completing intermediate code and leverage memory hierarchy and CPU registers while generating the target machine code.

We can categorize the programming optimization at this level, broadly, into 2 types:
- Machine Independent
This step of source code optimization compiling aims to improve intermediate code to produce a better target. No CPU registers or absolute memory addresses are involved to be translated.

- Machine Dependent
After the target code has been created and converted to fit the machine architecture, machine-dependent optimization is performed. It may use absolute memory references rather than relative memory accesses and also requires CPU registers. Machine-dependent optimizers make a concerted attempt to maximize the memory hierarchy's benefits.

### Run Time
By dynamically adjusting parameters in response to the actual input or other factors, adaptive optimization may be able to perform run-time optimization beyond the capability of static compilers. At the cost of overhead and based on runtime data, customized machine code can be done by Just-in-Time Compilers and can also have self modifying code which is adaptable depending on the runtime conditions. 

Optimizing based on run-time profiles is an ahead-of-time (AOT) compilation technique similar to an "average case" analogy to adaptive optimization. It's common for assembly language programs to use self-modifying code to optimize themselves, depending on runtime conditions.

Through instruction scheduling, compilers can support programs to take advantage of CPU design features (e.g. like out-of-order execution, speculative execution, instruction pipelines and branch predictors), that perform programming optimizations at runtime. Thus, other versions of the code may be required to be utilized across different platforms and/or processors.  

### Platform Dependence and Independence
Programming optimization techniques can also be openly categorized as platform dependent or independent.
 
Independent developments are effective across most, if not all, platforms, while dependent techniques use determined properties and/or rely on parameters from the single platform in question or even single processor. 

Let's take the case of compile-level optimization in programming: platform-independent techniques are generic techniques,  

- loop unrolling
- reduction in function calls
- memory efficient routines
- reduction in conditions

that will impact most CPU architectures in a similar way.

An example, which we mentioned above earlier in the source code level, can apply to a platform-independent optimization: the inner for loop, where it was observed that a loop with an inner for loop performs more computations per unit time than a loop without it or one with an inner while loop. 

These can typically lower the overall length of instruction paths needed to finish the program and/or the amount of memory used overall. 

Contrarily, when it comes to platform-dependent techniques, these use instruction scheduling, instruction-level parallelism, data-level parallelism, cache optimization techniques (i.e., parameters that vary across different platforms), and the best time to schedule instructions may vary even between processors with the same architecture.