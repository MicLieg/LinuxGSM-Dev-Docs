# Semantic Versioning

LinuxGSM has now moved from a rolling release to [Semantic Versioning](https://semver.org/). This is due to the size of the project and the requirement to better manage features and bug fixes.

## Core Concept

The core concept of Semantic Versioning is to provide a clear and concise way to communicate the impact of changes to a project. This is done by using a version number that is made up of three numbers separated by a dot.

```text
v24.1.5
  ║ ║ ║
  ║ ║ ╚══ Patch
  ║ ╚════ Minor
  ╚══════ Major
```

### Major

The first number in the version number is the `major` version. This is incremented when there are `breaking changes`. This could be a change in the way a command is used or a change in the way a module is called.

### Minor

The second number in the version number is the `minor` version. This is incremented when `new features` are added. This could be a new game, a new command or a new module.

### Patch

The third number in the version number is the `patch` version. This is incremented when a `bug fix` is added. This could be a fix to a command, a fix to a module or a fix to a game.
