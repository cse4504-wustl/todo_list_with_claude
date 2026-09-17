# Agent instructions
## Project overview
Simple todo-list application, to keep track of tasks that need to be done. 
User can create new tasks with an optional due date, mark tasks off as completed, and give tasks a priority order
User should be able to short tasks by priority, due date, and alphabetically
## Tech stack
- Core application logic is in Python
- User interface is in HTML/javascript
- In-memory stoarge

## Project architecture
- Decompose modules into layers with specific responsibilities
  - data transfer objects - simple data only classes for carrying requests to use cases and sending responses back to the caller
  - use cases: orchestrate the logic, retrieving data from storage, processing request objects(dto), creating response objects (dto)
  - abstractions: use cases communicate with data storage and presentation layer via an abstraction, never directly depending on concrete implementation
    - use an abstraction for data storage
    - use an abstraction for the use case to communicate the response object to the presenter
  - entities: core objects of the application, business rules are encoded here
  - exception handling: throw exceptions on bad requests. On failed lookups, communicate the failure response object

## Coding style
- use docstrings for all functions
- use camel case for naming functions
- use camel case for class names
- class names start with an upper-case letter
- fine names start with lower-case letter
- keep one class per file

