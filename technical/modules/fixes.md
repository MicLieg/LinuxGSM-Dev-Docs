# Fixes

Fixes are managed in `fix.sh`. This file is run by several modules: `command_debug.sh`, `command_install.sh` and `command_start.sh`.

If the given server requires a fix, then create a `fix_gameserver.sh` file and add it to either the `apply_pre_start_fix` array or the `apply_post_install_fix` array in `fix.sh`.
