The Ramses ecosystem consists of multiple projects. You can use some of them or all, depending on your needs.

# The Ramses core library

The Ramses libraries are the cornerstone of the Ramses ecosystem. All other libraries and tools
are build around these libs.

Here are links for more detailed information:

* [Source code repository](https://github.com/GENIVI/ramses)
* [API docs](https://genivi.github.io/ramses/)
* [Wiki pages](https://github.com/GENIVI/ramses/wiki)

You can find more info on how to build the libs, which are the individual components and APIs,
how to use them, which are the supported compilers and OS-es, how to debug among other things in
the API docs.

# The Ramses logic library

The Ramses core libraries provide a thin layer over OpenGL, but offer no way to script dynamic behavior
or animation. If you don't need such functionality or have your own - you don't need more than
just Ramses. If you do - the Ramses Logic runtime provides this additional scripting and animation
runtime on top of Ramses, based on the Lua syntax.

Here are links for more detailed information:

* [Source code repository](https://github.com/GENIVI/ramses-logic)
* [API docs](https://ramses-logic.readthedocs.io/en/latest/)
* [Lua Syntax](https://ramses-logic.readthedocs.io/en/latest/lua_syntax.html)
* [Example projects](https://github.com/GENIVI/ramses-composer-docs/blob/master/manual.md) as part of the Ramses Composer user manual

# The Ramses Composer

The Ramses Composer is a GUI application (with a powerful headless mode) which allows the import of external data
to compose, optimize, version and share complex projects in a modular yet visual way. The Ramses Composer complements your DCC
tool of choice by allowing writing custom shaders, adding scripts and packaging content optimally for Ramses. It also provides
a powerful concept for reusing content across larger projects and teams. The Composer is designed to
be the medium of exchange between artists and software developers so that both can contribute to
a well-managed, strictly versioned, performance-optimized and documented 3D project.

Using the headless mode, the Ramses Composer is designed to be also used in automated builds where quality, performance and regressions can
be tracked in ways familiar to software engineers, without compromising on ease of access for artists and non-technical staff.

Here are links for more detailed information:

* [Source code repository](https://github.com/GENIVI/ramses-composer)
* [User manual](https://github.com/GENIVI/ramses-composer-docs/blob/master/manual.md)
* Example projects are part of the [User Manual Repository](https://github.com/GENIVI/ramses-composer-docs/) - clone it to try them out locally!

# Demo

You can find a [demo using Ramses and a detailed map of the Helsinki city model](https://github.com/GENIVI/ramses-citymodel-demo)
which shows the level of detail possible with Ramses on embedded devices. We demonstrated the demo on the Genivi All-hands summit in 2018 using
an Intel NUC and a 25Mbs Ethernet connection. You can also find a video on [Youtube](https://youtu.be/tyzvEI25BMg?t=198)!

```{warning} This repository is not using the latest version of Ramses! We keep it as a reference since it's a great demo of what is possible with modern OpenGL and Ramses
```

```{warning} The demo runs well only on devices with ASTC texture compression support! Desktop devices usually don't support this type of compression, and the demo does not run fluently there.
```

# Archive

As part of the Google Summer of Code 2019, we evaluated options to integrate Ramses with Blender so that a Blender user can directly
export Ramses content out of Blender. Even though we loved Blender and its Python interface, we figured it's better to support a wider range
of DCC tools, and don't want to have to write exporters for each of them. This understanding led us to develop [the Ramses Logic runtime](#the-ramses-logic-library) and
[the Ramses Composer](#the-ramses-composer) which still support a Blender workflow, but also other tools which can export [glTF data](https://github.com/KhronosGroup/glTF).

We left the source code and the Python bindings for Ramses on Github in case someone else is interested in the code:

* [Ramses Python bindings](https://github.com/GENIVI/ramses-python)
* [Ramses Blender Plugin](https://github.com/GENIVI/ramses-blender)