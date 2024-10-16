# Raylib Zig Build Bug

Follow the commit log for a step-by-step walkthrough to reproduce the problem.

With the current state this project is in, if you run `zig build`, it will fail and you will get 2 errors. The main error is that, when building raylib, the build script is looking for the raylib source files in the wrong directory.

```console
$ zig build # fails
```

If you revert raylib to an earlier commit, the project builds without any issues.

```console
$ cd raylib
$ git checkout 74ce90ce671fbcd0d31e26d7b13d142b8425de60
$ cd ..
$ zig build # ok
```
