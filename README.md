This is a copy of a C++ implementation of a FORTH interpreter for COMP 310 (Operating Systems). It will be used in the live demo to demonstrate the functionality of FORTH in addition to gnu forth on the command line. Since gnu forth is free-form input with an immediate return stack, it is difficult to show written code. Here, you can see how forth functions with minimal structure and commands at the base of the language.

Project objective:
To use C++ to reconstruct our foundational construction of forth interpretation in C. 


How to run with C-11 compiler:
cmake -DCMAKE_BUILD_TYPE=Debug -DCMAKE_CXX_STANDARD=11 -S . -B build
		cmake --build build
./build/r-forth



Functionality:  
-- testing with main() in token.cpp (don't worry, this will be removed in the final submission, i just made it easier
to test input instead of compiling the user interface every time)
-- added a mapping from token to function
    --done by token type
-- added a mapping from token to token type
    -- planning on controlling input by checking first if token is a : or ; -> if so, push everything onto a stack and handle
    in custom function (to be built by Nick/Luke)
-- take input as string stack, convert to queue (so that you can see the front/back of input at all times)
-- added compatability for variables and constants
-- re-added interactivity on command line
-- loops are working independently of the rest of the codebase
-- ability to print out the number of each iteration, values, and strings
-- arrays
    -- array numbers -> to delcare array
    -- 3 cells allot numbers -> declare array size
    -- 10 0 numbers +! -> assigns value 10 to index 0 of array numbers
    

Completed:
-- basic operations (+, -, dup, swap, etc.)
-- variable declaration, constants, and operation (!, @, +!)
-- add booleans (<, >, and, etc.)
--interactive feature
-- word definitions (functions)
-- do loops
-- arrays
-- if else then

