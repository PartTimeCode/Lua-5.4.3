# Lua-5.4.3
Visual Studio 2015 solution for compiling Lua 5.4.3 lib and dll from source for dynamic linking.

## Usage:

Open the solution in Visual Studio, from the menu select "Build" >> "Batch Build"

In the dialog click "Select All" and then "Build"

### Files are generated in the solution dir

Release\Win32\lua.dll<br />
Release\Win32\lua.lib<br />
Release\x64\lua.dll<br />
Release\x64\lua.lib<br />

Debug\Win32\lua.dll<br />
Debug\Win32\lua.lib<br />
Debug\x64\lua.dll<br />
Debug\x64\lua.lib<br />

## Start a new Console project:

Add Headers to your project:<br />
src\lua.h<br />
src\luaconf.h<br />
src\lauxlib.h<br />
src\lualib.h<br />

Load them in your code<br />
extern "C" {<br />
	#include "lua\lua.h"<br />
	#include "lua\lauxlib.h"<br />
	#include "lua\lualib.h"<br />
}

// Create a new Lua state<br />
lua_State * L = luaL_newstate();<br />
luaL_openlibs(L);<br />
  
And have fun coding in Lua







