---

title: Software Testing

---
 
# About Unit Testing
    Test Driven Development
        ○ Recommended to write tests as you go
        ○ Red, Green, Refactor
            - Red: Always start with a meaningfully failing test.
                □ Fail on assert
                □ Start by hardcoding.
            - Green: Write imperfect code to get the test to pass.
                □ Do not worry about good conventions at all just yet, just get green
                □ If it takes longer than 2-3 minutes, then go back and rewrite test
            - Refactor: Start worrying about making it good.
    Goal of Your Code, in order (Not just Unit Testing)
        - #1: Passes the code
        - #2: Reveals intention
        - #3: No duplication
        - #4: Fewest number of elements
    ○ Test one thing at a time
    
    Unit Tests
        - Testing the individual units of functionality within our system
        - White box tests: They break encapsulation. They test how your code does things, not what it does
        - Why do change implementation in our code:
            □ We find better ways to do something: Better design, better performance, we identify "abstractions"
            □ Upgrading the dependencies
        - This lead to limitations, as when we change our code, the end to end tests may still work, which is the most important, unit tests may fail in large amounts
            □ This is because even though implementation changes, the outcome stays the same
            □ They need to be properly used in order to be efficient 

        - Unit tests at the minimum cannot access the :
            ○ File system
            ○ Database
            ○ Network
            ○ The Clock
        - These things are external, and failures may be because of external factors, which defeats the purpose of unit testing
        - They also change: Defeats the purpose of unit tests if what you are testing continuously changes.
        
    


    

# Other Notes
    Language Types
        ○ Object Oriented Programming
            - Support encapsulation, polymorphism, inheritance, sometimes reflection
            - Has objects as the "first class citizen"
            - Objects are a combination of data and the code that uses that data
        ○ Functional Languages
            - You construct solutions by combining functions
            - Data is immutable, so there are no "variables"
                □ You cannot have a string later become an int
            - You cannot have a variable set equal to a function.
        
    .NET History
        ○ 2002: .NET 1.0 was released
            - Prior to this, C++ and Visual Basic were standard for Windows programmers
            - There was a need for a bridge between the two, as C++ was too complex and Visual Basic was too simple (Obviously more complex than this, but simple way to put it).
            - C# was born from this, as it attempts to achieve this. (# is ++ stacked on top of each other)
        ○ 2003: .NET 1.1
        ○ 2005: .NET 2.0
            - Caught up to Java and began to surpass. Introducing Generics helped 
        ○ 2008: .NET 3.0
            - Homoiconicity: Code and data are represented the same in data structures
                □ .NET 3 introduces some of this with expressions and LINQ
        ○ ~2013: .NET 4.0
            - Prior to this, .NET would only run on windows
            - Then, Cloud Computing exploded
        ○ Shortly After: .NET Core, takes advantage of cloud sevicing
        ○ .NET Framework is the older .NET. The goal is for everything to move to .NET Core

    .NET Core
        ○ Not associated with any one provider. Can be on Microsoft, Linux, macOS
        ○ Compared to .NET Framework, which is only on Microsoft
            - The goal is to move away from this, and to move all to Core
        ○ .NET typically uses PascalCase and not CamelCase

    .NET Syntax and Other General Info
        ○ Class Labels
            - Public: Anything with reference can see it
            - Private: Not used much in .NET
            -Internal: Only other code with project can see it
        ○ Solution: Text file with information and config info about the project
            - Can have multiple projects within the same solution


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

This code appears to be an asynchronous integration test that tests the functionality of the /api/software API endpoint. It is attempting to confirm that the Api returns a status code of 200 (Ok). It seems that Alba is a way for the system to actually test the functionality of the API, in conjunction with xUnit, rather than just mocking it. Program appears to be a method for the system to retrieve and actually run the API that you are attempting to test.