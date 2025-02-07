# snappy

This is [snappy](https://github.com/google/snappy) packaged for [Zig](https://ziglang.org)

# Installation

Use `zig fetch`:

```
zig fetch --save git+https://github.com/vrischmann/snappy#master
```

You can then import `snappy` in your `build.zig`:
```zig
const snappy = b.dependency("snappy", .{
    .target = target,
    .optimize = optimize,
});

your_exe.addIncludePath(snappy.path("."));
your_exe.linkLibrary(snappy.artifact("snappy"));
```
