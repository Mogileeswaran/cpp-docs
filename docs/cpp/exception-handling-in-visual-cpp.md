---
title: "Exception handling in MSVC"
ms.date: "11/19/2019"
helpviewer_keywords: ["try-catch keyword [C++], exception handling"]
ms.assetid: a6aa08de-669d-4ce8-9ec3-ec20d1354fcf
---
# Exception handling in MSVC

An exception is an error condition, possibly outside the program's control, that prevents the program from continuing along its regular execution path. Certain operations, including object creation, file input/output, and function calls made from other modules, are all potential sources of exceptions even when your program is running correctly. Robust code anticipates and handles exceptions. To detect logic errors, use assertions rather than exceptions (see [Using Assertions](/visualstudio/debugger/c-cpp-assertions)).

## Kinds of exceptions

The Microsoft C++ compiler (MSVC) supports three kinds of exception handling:

- [C++ exception handling](errors-and-exception-handling-modern-cpp.md)

   For most C++ programs, you should use C++ exception handling, which is type-safe and ensures that object destructors are invoked during stack unwinding.

- [Structured exception handling](structured-exception-handling-c-cpp.md)

   Windows supplies its own exception mechanism, called SEH. It is not recommended for C++ or MFC programming. Use SEH only in non-MFC C programs.

- [MFC exceptions](../mfc/exception-handling-in-mfc.md)

Use the [/EH](../build/reference/eh-exception-handling-model.md) compiler option to specify the type of exception handling to use in a project; C++ exception handling is the default. Do not mix the error handling mechanisms; for example, do not use C++ exceptions with structured exception handling. Using C++ exception handling makes your code more portable, and it allows you to handle exceptions of any type. For more information about the drawbacks of structured exception handling, see [Structured Exception Handling](structured-exception-handling-c-cpp.md). For advice about mixing MFC macros and C++ exceptions, see [Exceptions: Using MFC Macros and C++ Exceptions](../mfc/exceptions-using-mfc-macros-and-cpp-exceptions.md).

## In this section

- [Modern C++ best practices for exceptions and error handling](errors-and-exception-handling-modern-cpp.md)

- [How to design for exception safety](how-to-design-for-exception-safety.md)

- [How to interface between exceptional and non-exceptional code](how-to-interface-between-exceptional-and-non-exceptional-code.md)

- [The try, catch, and throw Statements](try-throw-and-catch-statements-cpp.md)

- [How Catch Blocks are Evaluated](how-catch-blocks-are-evaluated-cpp.md)

- [Exceptions and Stack Unwinding](exceptions-and-stack-unwinding-in-cpp.md)

- [Exception Specifications](exception-specifications-throw-cpp.md)

- [noexcept](noexcept-cpp.md)

- [Unhandled C++ Exceptions](unhandled-cpp-exceptions.md)

- [Mixing C (Structured) and C++ Exceptions](mixing-c-structured-and-cpp-exceptions.md)

- [Structured Exception Handling (SEH) (C/C++)](structured-exception-handling-c-cpp.md)

## See also

[C++ Language Reference](cpp-language-reference.md)</br>
[x64 exception handling](../build/exception-handling-x64.md)</br>
[Exception Handling (C++/CLI and C++/CX)](../extensions/exception-handling-cpp-component-extensions.md)
