# lto-cuse-stub

## Description 
implements a [cuse](https://github.com/libfuse/libfuse/blob/master/example/cuse.c) chardev /dev/nst0stub that handles most I/O as real /dev/nst0 would. Can be utilized for testing tape backup software.

## Dependencies

[fuse](https://github.com/libfuse/libfuse)

## Building

```
meson setup build
cd build
meson build
```
## Running

 Mount the file system with:
 ```
 ./lto-cuse-stub
 ```
 
 You should now have a new /dev/nst0stub character device. To "unmount" it,
 kill the "lto-cuse-stub" process.