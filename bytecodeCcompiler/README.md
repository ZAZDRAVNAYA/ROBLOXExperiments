# C compiler experiment
Albeit not directly ROBLOX-related, this experiment seeks to create a C compiler that compiles to Lua bytecode. This could be useful for porting real applications to a Lua VM within ROBLOX. Ideally, this will be able to compile itself, essentially creating a C compiler in and for Lua bytecode.

# Purpose
Lua's dofile, loadfile, and loadstring functions allow for the direct input of Lua bytecode files, which allows us to bypass Lua's compiler and interface directly with the VM. While there isn't much purpose to this besides obfuscating source code, there are some interesting things we can do by controlling the VM directly. What I seek to do is to create a rudimentary C interpreter that compiles bytecode for the Lua VM.
Lua can interface with external libraries, but there's an issue when it comes to portability. The library being called must be in the host computer's machine code or it won't run. At the sacrifice of speed and optimization, compiling libraries to Lua bytecode should eliminate the issue of incompatibility between platforms.

# Issues
Come another major release, the compiler may need to be updated or succeeded to accomodate the changes in the next version. Additionally, versions of the compiler may need to be created for prior Lua releases. Currently, this project's scope is Lua 5.3, so I'm not presently concerned with cross-compatibility (or the lack thereof).

# Vision
Hopefully, the many open-source tools that are written in C will be made available to use natively in Lua. Unfortunately, I don't think I'll ever get to the point of writing something GCC-esque, but perhaps this will set the stage for more complex compilers in the future.
I really want to see some advanced libraries interfacing with Lua through my (future) compiler.
Imagine compiling the entirety of libavcodec in Lua bytecode!
(You bet I'll post a release if I actually manage to do this.)
