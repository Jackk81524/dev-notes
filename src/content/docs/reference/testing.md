---

title: Software Testing

---
 
# About Unit Testing
 
Language Types

    - Object Oriented Programming

        - Support encapsulation, polymorphism, inheritance, sometimes reflection
        - Has objects as the "first class citizen"
        - Objects are a combination of data and the code that uses that data
    - Functional Languages
        - Have functions of "first class citizens"
        - You construct solutions by combining functions
        - Data is immutable, so there are no "variables"
            - You cannot have a string later become an int
        - You cannot have a variable set equal to a function.

.NET History
    ○ 2002: .NET 1.0 was released
        § Prior to this, C++ and Visual Basic were standard for Windows programmers
        § There was a need for a bridge between the two, as C++ was too complex and Visual Basic was too simple (Obviously more complex than this, but simple way to put it).
        § C# was born from this, as it attempts to achieve this. (# is ++ stacked on top of each other)
    ○ 2003: .NET 1.1
    ○ 2005: .NET 2.0
        § Caught up to Java and began to surpass. Introducing Generics helped 
    ○ 2008: .NET 3.0
        § Homoiconicity: Code and data are represented the same in data structures
            □ .NET 3 introduces some of this with expressions and LINQ
    ○ ~2013: .NET 4.0
        § Prior to this, .NET would only run on windows
        § Then, Cloud Computing exploded
    ○ Shortly After: .NET Core, takes advantage of cloud sevicing
    ○ .NET Framework is the older .NET. Moving to .NET Core

.NET Core
    ○ Not associated with any one provider. Can be on Microsoft, Linux, OS
    ○ Compared to .NET Framework, which is only on Microsoft
        § The goal is to move away from this, and to move all to Core
    ○ .NET typically uses PascalCase and not CamelCase

.NET Coding
    ○ Class Labels
        § Public: Anything with reference can see it
        § Private: Not used much in .NET
        Internal: Only other code with project can see it
    ○ Solution: Text file with information and config info about the project
        § Can have multiple projects within the same solution

Test Driven Development
    ○ Recommended to write tests as you go
    ○ Red, Green, Refactor
        § Red: Always start with a meaningfully failing test.
            □ Fail on assert
            □ Start by hardcoding.
        § Green: Write ridiculous (bad) code to get the test to pass.
            □ Do not worry about good conventions at all just yet, just get green
            □ If it takes longer than 2-3 minutes, then go back and rewrite test
        § Refactor: Start worrying about making it good.
    ○ Goal of code in order
        § #1: Passes the code
        § #2: Reveals intention
        § #3: No duplication
        § #4: Fewest number of elements
    ○ Test one thing at a time, or do best to do so

Keyboard Shortcuts
    ○ Ctrl . In Visual Studio Provides error solutions
    ○ F12 will take you to highlighted func
    ○ Ctrl - takes you back
 
# API Testing with Alba
 
```csharp
 
using Alba;
 
namespace HelpDesk.Tests.Software;

public class GettingSoftware

{

    // Test that we can make an HTTP GET requests to /api/software
 
    [Fact]

    public async Task CanGetSoftware()

    {

        var host = await AlbaHost.For<Program>();
 
        await host.Scenario(api =>

        {

            api.Get.Url("/api/software");

            api.StatusCodeShouldBeOk();

        });
 
 
    }

}

```
 
Write what you understand about this code. What is Alba? Where did that come from? What is `Program`?
 