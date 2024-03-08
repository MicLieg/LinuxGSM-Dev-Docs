---
description: '[WIP] discuss using LF and white space remover etc.'
---

# Text Editor Settings

## Editorconfig

Using editorconfig allows the editor to automatically apply the settings recommended by LinuxGSM. Most modern IDE's have an extension or plugin available or even built-in support for `.editorconfig` files.

## Required Settings

Below is some information on requirements needed when using a text editor to work on LinuxGSM code. All the recommended text editors can be set up to take into account the requirements.

Note: Using editorconfig will automatically apply all of these settings.

### Indentation

LinuxGSM uses `tabs` instead of spaces, it is possible to specify tabs and convert spaces to tabs if required.

### Line Ending

All files must be saved using `LF` (Line Feed) line endings which is the default line ending used by UNIX based systems. Please ensure that your text editor is saving in `LF` format as failure to do so will cause BASH scripts to stop functioning.

For more info about line endings check out the article "[The Great Newline Schism](https://blog.codinghorror.com/the-great-newline-schism/)".

### Trailing White Spaces

When developing code sometimes it can be easy to end up with trailing white spaces as shown below.

```bash
fn_example_func(){
    # The line below has two spaces after its final character
    code••
}
```

All code must have trailing whitespaces removed to keep code tidy. Many text editors have a feature that will automatically remove trailing whitespaces when a file is saved. It is highly recommended this feature is turned on.
