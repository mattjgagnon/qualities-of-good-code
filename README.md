# Qualities of good code

## Good code
- Does what it is supposed to
- Is easily readable and maintainable
- Has few bugs
- Is efficient from a user and code speed perspective
- Has automated tests for all the critical parts

## More detail
- Does the code work and perform its intended function?
- Is the code broken out into single responsibility functions/methods/classes?
- Is each function short and not complex? (For example, 20 LOC or fewer and CC of less than 6. This aids understanding and maintainability.)
- (optional if the function is named properly, and type hints are used for params and function returns) Is there at least a minimal docblock or comment for the function, explaining what it does, what each parameter is, and what it returns?
- If it's a critical function, does it have at least one unit test for each code branch? And if it is critical, does it log some useful information?
- Can the function's purpose be easily derived from its name? (Also methods, classes, interfaces)
- Logs useful information consistently across the software
- Are variables/properties named in a manner that they are clear what they store?
- Are classes in their own files? Likewise, are groups of related functions in their own file?
- Are all debugging lines (dpm, var_dump, print_r, etc) removed before commit?
- Are all uncommented lines of code (zombie code) deleted?
- Is unnecessary code refactored/deleted?
- Does the code pass the team style/formatting guide?
- Does the code not generate PHP errors, warnings, or notices?
- Is the code under inspection at the same level of abstraction?
- If the code is not yet production-ready, is there a @todo comment in the docblock stating this, and what needs to be done?
- Is the code under version control?
- Are duplicate blocks of code extracted into their own functions and re-used?
- Are global variables in use? Can they be replaced with local, or passed into the function?
- Do loops have a termination condition?
- Can any functions be replaced with ones that already exist elsewhere?
- Is the interface/class/method called or used anywhere? (Be careful of “magic” or dynamically called code)
- Likewise, is there a good library that can be substituted for some parts, instead of custom code?
- Are all variables used in the function? Parameters also?
- Are try/catch/throw or other error catching means employed with critical logic? (If the function fails, does it do so gracefully? Does it actually handle the exception/error?)
- Can variables passed by reference instead be returned?
- Are guard clauses used to fail fast?
