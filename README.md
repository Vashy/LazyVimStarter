# 💤 LazyVim

A starter template for [LazyVim](https://github.com/LazyVim/LazyVim).
Refer to the [documentation](https://lazyvim.github.io/installation) to get started.

## Troubleshooting

> libbfd-2.38-system.so: cannot open shared object file: No such file or directory

Fixed by creating a symlink to the older version:

```shell
# find the shared library installed version
ldconfig -p | grep libbfd

# symlink the existing version to the version required by mason
sudo ln -s /lib/x86_64-linux-gnu/libbfd-2.45-system.so /lib/x86_64-linux-gnu/libbfd-2.38-system.so
```
