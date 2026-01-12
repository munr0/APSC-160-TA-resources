# Instructions for Using VS Code in This Course

## Setup/Installation

### 1. Open a Terminal
Hit the Windows Key on your keyboard, type <kbd>wt</kbd>, and press Enter.

### 2. Install VS Code and the Compiler
Run these two commands to install the environment:


```powershell
winget install -e --id Microsoft.VisualStudioCode
```

```powershell
winget install -e --id BrechtSanders.WinLibs.MCF.UCRT
```

### 3. Restart your Terminal
Close the current terminal and repeat step 1. This should add `gcc` and `code` to your system path.

In the new terminal, verify this by running:

```powershell
code --version; gcc --version
```

If this doesn't throw an error, you're good to go!

### 4. Install VS Code Extensions
Install the following VS Code extensions to make it easier to develop and run files:

```powershell
code --install-extension ms-vscode.cpptools
```
```powershell
code --install-extension danielpinto8zz6.c-cpp-compile-run
```

## Testing

### 5. Open VS Code
You can launch the editor like any other Windows app, or by simply typing in terminal:

```powershell
code
```

### 6. Create a File to Test
In VS Code, create a new file and save it as `hello.c`. Paste the following code:

```c
#include <stdio.h>

int main(void) {
    printf("Hello World\n");
    return 0;
}
```

### 7. Run the Code
You can now run the file in one of two ways:

- Click the Play Icon (▷) in the top right corner of the screen.
- Pressing <kbd>F6</kbd>.

A terminal should pop up inside VS Code, and you should see:

```
Hello World
```
