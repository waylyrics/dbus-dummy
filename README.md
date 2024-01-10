# dbus-dummy

Dummy package.

## Why?

cargo does not support [Platform target-specific features](https://github.com/rust-lang/cargo/issues/1197),

in other words,

```toml
[target.'cfg(not(target_os = "windows"))'.features]
default = ["general_feature"]

[target.'cfg(target_os = "windows")'.features]
default = ["winonly_replacement"]
```

these statements will **not** work.

