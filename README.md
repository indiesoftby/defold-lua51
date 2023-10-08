# Lua 5.1 for Defold

A quick way to replace LuaJIT with Lua 5.1 (PUC Rio version, i.e. interpreted) on desktop platforms to run the game as on the Defold HTML5 platform.

## Explanation

Defold aims to keep Lua the same across all platforms, but it currently has a few minor discrepancies in Lua language version between platforms:

| Platform        | Lua version         | JIT Enabled |
|-----------------|---------------------|-------------|
| Windows         | LuaJIT 2.1.0-beta3  | Yes         |
| macOS           | LuaJIT 2.1.0-beta3  | Yes         |
| Linux           | LuaJIT 2.1.0-beta3  | Yes         |
| Android         | LuaJIT 2.1.0-beta3  | Yes         |
| iOS             | LuaJIT 2.1.0-beta3  | No          |
| Nintendo Switch | LuaJIT 2.1.0-beta3  | No          |
| **HTML5**       | **Lua 5.1.4**       | N/A         |

There is a HUGE performance gap between Lua and LuaJIT. If your primary target development platform is HTML5, it's important to see the actual performance of Lua as if it were running on HTML5 while developing on a PC/Mac/Linux computer.

## Usage

Add this project as a [Defold library dependency](http://www.defold.com/manuals/libraries/). Open your `game.project` file and in the dependencies field under project add:

https://github.com/indiesoftby/defold-lua51/archive/main.zip

Check:

```lua
if jit then
    -- LuaJIT!
else
    -- Lua 5.1!
end
```

## Credits

This project is licensed under the terms of the MIT license. The implementation is extracted from the [lmprof](https://github.com/defold/extension-lmprof) extension.
