---

title: Testing

---
    # July 31
    
    Testing Levels
        • Types of Software Processes
            ○ Waterfall
                 Requirements -> Design -> Coders -> Testers -> Stabilization -> Done!
                - Is completely linear, no going backwards
            ○ eXtreme Processing (90s)
            ○ Agile
            ○ Lean
        • Chart to Right: Could be due to number of reasons: larger codebase, leaving hard things to end, 
        Small changes become harder
            ○ The goal is to have the blue line
        • Testing
            ○ End to End (System Integration Tests)
                - Black box test: Test what happens, not how it happens
            ○ Integration Tests (System Tests)
                - We are testing the API of our service, not the Angular app
            ○ Unit Tests
                - Testing the individual units of functionality within our system
                - White box tests: They break encapsulation. They test how your code does things, not what it does
                - Why do change implementation in our code:
                    □ We find better ways to do something: Better design, better performance, we identify "abstractions"
                    □ Upgrading the dependencies
                - This lead to limitations, as when we change our code, the end to end tests may still work, which is the most important, unit tests may fail in large amounts
                    □ This is because even though implementation changes, the outcome stays the same
                    □ They need to be properly used in order to be efficient 
            ○ What order to test:
                - Start with Integration tests, then proceed to unit tests as needed
            ○ When dealing with a bug, it is often helpful to write a unit test to demonstrate the bad behavior
            ○ You can only test your understanding of the code, which is why developers writing and testing their own code is a bad idea

    .NET Notes
        • Using uint instead of int means unsigned int, cannot have negatives
        • Static allows you to call method on the class
    Internal means that it can only be accessed within project