## RESHADE UNLOCKED - NO DEPTH BUFFER DETECTION   
   
   I have edited a file to disable that annoying depth buffer lock when you are online. You do have to be wary though, I personally have not been banned from any game because of my use of this, but I know one thing for sure, you CAN NOT use reshade or any .dll modification on battle eye anticheat game. You will get banned almost right away if it does not disable it.
   
   Go to the releases tab to download the installers, I'm not gonna keep the source code up to date lol

   Anyways, I'm keeping all of the text below available if anyone would like to view it to do whatever.
The file I have changed is ~

source \ runtime.cpp

If you want to build your own version, use the original repo by crosire, I haven't updated mine for a while

All credit to u/TheGuyMadeOfCheese and u/Shamsiel_ on reddit, they taught me how to make these installers.

I AM NOT RESPONSIBLE FOR ANY GAME BANS YOU GET USING THIS MODIFIED VERSION OF RESHADE, YOU SHOULD USE COMMON SENSE, AND NOT USE THIS ON GAMES BANNED ON THIS LIST
https://www.pcgamingwiki.com/wiki/ReShade#Online_games_to_avoid

## Video Tutorial
https://vimeo.com/787218714

(IN THE VIDEO I FUCKED SOMETHING UP LMAO - THE INSTALLER DIDNT WORK, IT SHOULD WORK FINE FOR YOU THOUGH...)

## Building

You'll need Visual Studio 2017 or higher to build ReShade and Python for the `gl3w` dependency.

1. Clone this repository including all Git submodules\
```git clone --recurse-submodules https://github.com/crosire/reshade```
2. Open the Visual Studio solution
3. Select either the `32-bit` or `64-bit` target platform and build the solution.\
   This will build ReShade and all dependencies. To build the setup tool, first build the `Release` configuration for both `32-bit` and `64-bit` targets and only afterwards build the `Release Setup` configuration (does not matter which target is selected then).

A quick overview of what some of the source code files contain:

|File                                                                  |Description                                                            |
|----------------------------------------------------------------------|-----------------------------------------------------------------------|
|[dll_log.cpp](source/dll_log.cpp)                                     |Simple file logger implementation                                      |
|[dll_main.cpp](source/dll_main.cpp)                                   |Main entry point (and optional test application)                       |
|[dll_resources.cpp](source/dll_resources.cpp)                         |Access to DLL resource data (e.g. built-in shaders)                    |
|[effect_lexer.cpp](source/effect_lexer.cpp)                           |Lexical analyzer for C-like languages                                  |
|[effect_parser.cpp](source/effect_parser.cpp)                         |Parser for the ReShade FX shader language                              |
|[effect_preprocessor.cpp](source/effect_preprocessor.cpp)             |C-like preprocessor implementation                                     |
|[hook.cpp](source/hook.cpp)                                           |Wrapper around MinHook which tracks associated function pointers       |
|[hook_manager.cpp](source/hook_manager.cpp)                           |Automatic hook installation based on DLL exports                       |
|[input.cpp](source/input.cpp)                                         |Keyboard and mouse input management and window message queue hooks     |
|[runtime.cpp](source/runtime.cpp)                                     |Core ReShade runtime including effect and preset management            |
|[runtime_gui.cpp](source/runtime_gui.cpp)                             |Overlay rendering and everything user interface related                |

## Contributing

Any contributions to the project are welcomed, it's recommended to use GitHub [pull requests](https://help.github.com/articles/using-pull-requests/).

## Feedback and Support

See the [ReShade Forum](https://reshade.me/forum) and [Discord](https://discord.gg/PrwndfH) server for feedback and support.

## License

ReShade is licensed under the terms of the [BSD 3-clause license](LICENSE.md).\
Some source code files are dual-licensed and are also available under the terms of the MIT license, when stated as such at the top of those files.
