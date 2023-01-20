# C++/C# Interop Via CLI Wrapper Code  
Working Example of a CLI wrapper for C++ Integration into C#/.NET 6.0 Code  

This project was written by following the how-to guide at [red-gate.com](https://www.red-gate.com/simple-talk/development/dotnet-development/creating-ccli-wrapper/)  

Also, see [Microsoft's docs on migrating from C++/CLI to .NET](https://learn.microsoft.com/en-us/dotnet/core/porting/cpp-cli)

NOTES:
- All CLI wrapper classes must have a .cpp source file to be exported for use in a C# project
- As of this time of writing (Jan 20, 2023), there is no CLI support for C++ editions beyond C++17 
- Class destructors (denoted by a tilde like '~Class()') are not the same as finalizers (denoted with an exclaimation point like '!Class()'). Destructors in a reference type perform deterministic clean up of your resources. Finalizers clean up unmanaged resources and can be called deterministically by the destructor or non-deterministically by the garbage collector. See: [Microsoft's Documentation](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms177197(v=vs.100)?redirectedfrom=MSDN)
- Importing .lib files to the CppCLIWrapperLayer project from remote folders may be unsuccessful unless .lib files are moved locally into the local bin folder (eg. './x64/Debug/libFileToLink.lib')
