# libluv-cygwin

This a recipe to build and package [libuv bindings for luajit][1] on
[Cygwin][2]. The recipe is based on the [recipe in cascent's old neovim
port][3].

Dependencies:
- [luajit{,-devel}][4]

To build the package install the dependencies and run the following command:
```sh
cygport libluv-cygwin.cygport download prepare compile install package
```

To install the package you can extract it into the root directory:
```sh
eval "$(cygport libluv.cygport vars PVR)"
tar -C / -xjvf libluv-$PVR.x86_64/dist/libluv/libluv1-$PVR.tar.xz
```

[1]: https://github.com/luvit/luv
[2]: http://www.cygwin.com/
[3]: https://github.com/cascent/neovim-cygwin/blob/09277e3f76981189a2f15d1dbc2f5a4ab4b6c86f/libuv/libuv.cygport
[4]: https://github.com/kgraefe/luajit-cygwin
