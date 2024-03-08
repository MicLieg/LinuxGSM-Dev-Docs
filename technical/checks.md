# Checks

The `check.sh` script is a requirement for any script file. It allows you to choose which checks to run for a specific function. To specify the functions that require this check, you need to populate the `allowed_commands_array` variable within `check.sh` with the scripts `commandname`.

There are several checks available:

| Check File                     | Description                                                              |
|--------------------------------|--------------------------------------------------------------------------|
| `check_config.sh`              | Checks for a missing config file or a wrong parameter.                   |
| `check_deps.sh`                | Checks and installs missing dependencies.                                |
| `check_executable.sh`          | Checks if server executable exists.                                      |
| `check_gamedig.sh`             | Installs nodejs and gamedig if not installed.                            |
| `check_glibs.sh`               | Checks if the server has the correct Glibc version.                      |
| `check_ip.sh`                  | Automatically identifies the server interface IP.                        |
| `check_last_update.sh`         | Checks Lockfile to see when last update happened.                        |
| `check_logs.sh`                | Checks if log files exist.                                               |
| `check_permissions.sh`         | Checks ownership & permissions of scripts, files and directories.        |
| `check_root.sh`                | Checks if the user tried to run the script as root.                      |
| `check_status.sh`              | Checks the process status of the server. Either online or offline.       |
| `check_steamcmd.sh`            | Checks if SteamCMD is installed correctly.                               |
| `check_system_dir.sh`          | Checks if systemdir/serverfiles is accessible.                           |
| `check_system_requirements.sh` | Checks RAM requirements. (maybe more into the future)                    |
| `check_tmuxception.sh`         | Checks if run from tmux or screen.                                       |
| `check_version.sh`             | Will run update-lgsm if gameserver.sh and modules version does not match |
