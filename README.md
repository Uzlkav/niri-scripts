# niri Scripts

Collection of simple scripts I use with niri

## niri dynamics
Easily toggle the inclusion of a file in your `config.kdl`. This can be used to dynamically change your configuration at runtime, for example to change whether new windows are focused, change default opening size, etc.

### Setup:
This script assumes your config is located in `~/.config/niri`, though this is easily changed.
Create a directory named `dynamic` in `~/.config/niri` and place the configuration you want to toggle dynamically in that folder. In your main `config.kdl`, make that file an optional include:
```kdl
include optional=true "./dynamic/your_file.kdl"
```

### Usage:
```bash
./niri-dyanmics your_file.kdl
```

This will toggle the inclusion of the file by renaming it, prefixing, or removing, `no-` at the start by default. You can override this by changing the value of the `prefix` variable at the top of the script.
