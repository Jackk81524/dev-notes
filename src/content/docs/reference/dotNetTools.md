---

title: .NET Syntax

---

# Notes
    • [Fact(Skip = "Have a question about this")] 
        ○ If you want to leave something failing while you inquire
    • .Contains(',') checks if string contains character
    • Int.Parse(sampleString) converts string to int
    • Use ref int x to make the variable x a reference to the original
        □ This means its value can be changed directly in function/method
        □ Compared to int * x in C.
    • When passing, must also do  ref x
        □ Compared to &x in C
    • Nulls
        □ Can declare certain types as nullable with ?
            - Ex: string?
        □ To check if null, can use ??
            - Ex: S ?? "No string"
        □ Can check on function call as well using ?
            - Ex: S?.ToUpper() ?? "No String"
    • Var { get; set; } allows you to customize the retrieving and setting of a type
    • C# Record: 
        ○ Two records with the same content will be able to read equal to one another
        ○ Two classes with the same content will read different, because it is referring to location in memory
            - Will need to compare specific values.
                □ Ex. Class1.id == Class2.id, Class1.Name == Class2.Name
                □ Instead of Class1 == Class2 for a record
    • Instead of { get; set; }. {get; init; } allows you to initialize a class with your values, but you cannot adjust it.
        -Required key word means you must initialize it
    
