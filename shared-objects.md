
- Files shared by executable or other shared object files, typically denoted with an `.so`, `.dylib`, or `.dll` suffix. These can also be referred to as dynamic(ally) (linked) libraries 
- These files contain code / functionality that can be linked at "load" or "runtime", to prevent needing to incorporate these modules in the executable file.
- Shared objects can be output in a common format, mostly ELF or Mach-o, which define a header that indicates where code and data are in the file.

```
Linking is the process of collecting and combining various pieces of code and data into a single file that can be loaded (copied) into memory and executed. Linking can be performed at compile time, when the source code is translated into machine code, at load time, when the program is loaded into memory and executed by the loader, and even at run time, by application programs. On early computer systems, linking was performed manually. On modern systems, linking is performed automatically by programs called linkers.
```

- Three types of object files: relocatable, executable, and shared.
  - Relocatable: binary code and data that can be combined with other relocatable object files at compile time to produce an executable object file.
  - Executable: binary code and data that can be loaded into memory and executed.
  - Shared: relocatable object that can be loaded and linked dynamically at load (copied into memory) or run (executing code) time.
- Object files contain binary data (machine code).

- `.a` are static libraries, which are like a collection of shared objects. A linker will only pick out the stuff from this static library that is actually used in a program (by matching symbols, I guess?). So for stuff in the C standard library, you'd link `libc.a` and then the linker would only pick out the stuff you're using.



