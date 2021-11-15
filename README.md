# Lua-5.4.3
Visual Studio 2015 solution for compiling Lua 5.4.3 lib and dll from source for dynamic linking.

Usage:

Open the solution in Visual Studio, from the menu select "Build" >> "Batch Build"

In the dialog click "Select All" and then "Build"

Files are generated in the solution dir

Release\Win32\lua.dll
Release\Win32\lua.lib
Release\x64\lua.dll
Release\x64\lua.lib

Debug\Win32\lua.dll
Debug\Win32\lua.lib
Debug\x64\lua.dll
Debug\x64\lua.lib

Start a new Console project:

Add Headers to your project:
src\lua.h
src\luaconf.h
src\lauxlib.h
src\lualib.h

Load them in your code
extern "C" {
	#include "lua\lua.h"
	#include "lua\lauxlib.h"
	#include "lua\lualib.h"
}

// Create a new Lua state
lua_State * L = luaL_newstate();
luaL_openlibs(L);
  
And have fun coding in Lua







