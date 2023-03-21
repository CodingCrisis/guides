# Software Development Best Practices by @CodingCrisis

## Goal
Ensure unified and successful completion of software component construction by providing a shared understanding of best practices 

## Disclaimer
It is impossible to gather and upkeep a list of universal best practices related to software development. There are many conflicting views on how to write code. The optimal practices may depend on the purpose of developed software, used technologies, involved individuals and other factors. 
This document is based on experiences gathered during my career in software engineering. It is limited to general practices, which should be applicable to most coding tasks. 
Specific practices should be gathered and shared on team level, as they are relatively short-lived (technology updates) and often related to type and construction of the software itself.

## Best Practices
* Consider if SOLID, GRASP or CUPID principles are well aligned with your project – apply them deliberately, not by default. 
* Do not overengineer. KISS – most systems work best if they are kept simple rather than made complicated
* Do not add unnecessary features. YAGNI – do not add functionality until deemed necessary. Rarely architecting for future requirements / applications turns out net-positive. External-facing APIs are somewhat of an exception, as breaking changes affect users and often slow you down. 
* Consider code duplication carefully. DRY (Don’t Repeat Yourself) might be less important in Microservices than independent development and deployability. Also, duplication in Test Automation can be perceived as less important than in production code (readability in tests is key). 
* Delete unused code. Dead code is dangerous – it can cause issues, it needs maintenance. 
* Keep code readable. Code is for people; unreadable code eventually becomes technical debt. 
* Keep consistent (and publicly available) code formatting rules throughout a project. 
* Agree and enforce common coding guidelines (naming conventions, indentation, error/exception handling conventions, etc.). Make sure the rules are easy to understand and apply (e.g., using tools). 
* Prefer code readability over comments. Two descriptions of intent sooner or later diverge. 
* Fail fast. Check input and fail as early as possible, providing clear error response to your caller. 
* Try to keep logic stateless and side-effect free, to make it easily unit testable. Break out logic into separate functions. 
* Keep functions/methods short 30-50 lines maximum. Keep modules manageable – 500 lines maximum.
* Keep code complexity in check – observe Cyclomatic Complexity and Cognitive Complexity metrics. Agree upon lowest manageable levels.
* Do not be afraid of refactoring. If tests are done right, refactoring should be relatively safe.
* Consider using design patterns to facilitate understandability, reusability and testing. 
* Siloed knowledge is bad – do not limit access to your code to other programmers and teams. 
* Ensure Unit Tests apply to the unit of behavior, not the unit of implementation.  
* Do not test “other people’s code” e.g., external libraries, 3rd party products. Use mocks.
* Use QA tooling to ensure code quality does not decline over time and test coverage is in-line with the agreed levels. 
* Get feedback fast – attempt to validate the code with peers and end users as soon as possible. This limits waist. 
* Look at the big picture – allow exceptions to any of the above practices. Do it only when absolutely necessary.
