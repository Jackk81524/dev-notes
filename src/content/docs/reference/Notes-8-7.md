---

title: 8/7 Notes

---

# Notes
Software Dev Types
    • Clear
        ○ We have best practices for that
        ○ It's "another one of these things"
        ○ Good work for newer devs
        ○ You can basically write unit test, get them to pass, and be done
        ○ Not much design work
        ○ Almost all system tests
    • Complicated
        ○ "Governing Constraints" - we know context of what we need, but not exactly how to do it
        ○ "Good practices" not best practices
        ○ Probably more unit tests than system tests
    • Complex
        ○ "Enabling Constrains"
            § "Enabling Practices"
        ○ Almost all user interface stuff
        ○ Testing is weirdly not automated too much
            § Manual testing
            § Observability
    • Chaotic
        ○ Site reliability engineering / Chaos engineering

Orchestration
    • Competing Concerns
        ○ You need a bunch of software running in production reliably
        ○ The software will be put into production at different rates
        ○ You have finite resources on which to run that software
        ○ No software installed on a machine should break any other software on that machine

Angular
    • Pick and Emit are ways to inherit certain vars from an object
    • Partial is similar, but it inherits all items, but makes them all optional

Service Relationships (Domain Driven Design)
    • "Entities" are based on an id
    • "values" are objects compared on value
        ○ -Records
    • "Services" are  like Utilities
        ○ An object or class that provides a service
    • Open Host: A service that is authoritarian, but it knows how to do stuff
    • Shared Language: follows a standard
    • Customer- Supplier: Supplier designs a service, and customer conforms to use that service
