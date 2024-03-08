# Exit Codes

Below is a list of exit codes and explanations for each code. An exit code hightights the state of the code once it has completed its task. This is used to highlight if the proccess completed, failed or somwhere inbetween.

to see the exit code you can activate developer mode.

```text
./gameserver developer
```

## Pass

* **Code:** 0
* **Description:** This code is returned when all is well.
* **On Screen Automated:** \[ OK \]
* **On Screen Interactive:** Complete!
* **Logfile:** PASS

## Fatal

* **Code:** 1
* **Description:** Fatal errors occur when LinuxGSM is prevented from completing its task. e.g it was unable to start a server.
* **On Screen Automated:** \[ FAIL \]
* **On Screen Interactive:** Failure!
* **Logfile:** FATAL

## Error

* **Code:** 2
* **Description:** An error occurs when LinuxGSM can complete its task however something went wrong. In many cases LinuxGSM will attempt to resolve errors itself.
* **On Screen Automated:** \[ ERROR \]
* **On Screen Interactive:** Error!
* **Logfile:** ERROR

## Warning

* **Code:** 3
* **Description:** Warnings happen when there is something mis-configured or not setup correctly. LinuxGSM may still work but not do as expected.
* **On Screen:** \[ WARN \]
* **On Screen Automated:** \[ WARN \]
* **On Screen Interactive:** Warning!
* **Logfile:** WARN

## Info

* **Code:** N/A
* **Description:** Useful information about what LinuxGSM is currently doing.
* **On Screen:**
* **On Screen Automated:** \[ INFO \]
* **On Screen Interactive:** Information!
* **Logfile:** INFO

## How to use exit codes in code

An exit code is set when you use a log message like `fn_script_log_fatal`. To properly exit the script and specify the exit code, you should use `core_exit.sh` instead of just the `exit` command. `core_exit.sh` will handle the exit and set the last known exit code. For example, if the most recent command was `fn_script_log_fatal`, the exit code will be 1.

### Example - Exit Code 1

```text
fn_script_log_fatal "RCON password is not set"
core_exit.sh
```

### Example - Exit Code 2

```text
fn_script_log_error "RCON password is not set"
core_exit.sh
```

### Example - Exit Code 0

```text
fn_script_log_error "SteamCMD is missing"
LinuxGSM installs SteamCMD
fn_script_log_pass "SteamCMD has been installed"
core_exit.sh
```
