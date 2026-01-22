Aside from the offline editors listed [on canvas](https://canvas.ubc.ca/courses/185376/pages/other-code-editors-and-compilers?module_item_id=8813463), one of the other popular options in this course, and upper year courses, is **Visual Studio Code** (different from Visual Studio, see @46). A difficulty with this editor can frequently be getting a compiler set up, but Microsoft actually has a package manager (WinGet) that can simplify installation by reducing a long process into a few commands you can paste into a terminal.

> **If you are happy using an online editor (like https://www.onlinegdb.com), already have/will set something set up, or aren't on Windows, don't bother with this.**
---

## Setup/Installation
---

#### 1. Open a Terminal
Hit the Windows Key on your keyboard, type <kbd>wt</kbd>, and press Enter.

#### 2. Install VS Code and the Compiler
Run these two commands to install the editor and GCC (the GNU Compiler Collection):


```powershell
winget install -e --id Microsoft.VisualStudioCode
```
<br>

```powershell
winget install -e --id BrechtSanders.WinLibs.MCF.UCRT
```

#### 3. Restart your Terminal
Close the current terminal and repeat step 1. This should add `gcc` and `code` to your system path.

In the new terminal, verify this by running:

```powershell
code --version; gcc --version
```

If this doesn't throw an error, you're good to go! If it does, try restarting your device and try again.

#### 4. Install VS Code Extensions
Install the following VS Code extensions to make it easier to develop and run C files:

```powershell
code --install-extension ms-vscode.cpptools
```
<br>

```powershell
code --install-extension danielpinto8zz6.c-cpp-compile-run
```

---
## Testing
---

#### 5. Open VS Code
You can launch the editor like any other Windows app, or by simply typing in terminal:

```powershell
code
```
VS Code will likely open to a walkthrough _"Get started with VS Code"_ tab. You don't need to click anything on this screen.

#### 6. Create a File to Test
In VS Code, create a new file with <kbd>ctrl</kbd><kbd>n</kbd> and paste in the following code. Save the file (<kbd>ctrl</kbd><kbd>s</kbd>) as `hello.c`.

```c
#include <stdio.h>

int main(void) {
    printf("You're all set up!\n");
    return 0;
}
```

#### 7. Run the Code
You can now run the file in one of two ways:

- Click the Play Icon (▷) in the top right corner of the screen.
- Pressing <kbd>F6</kbd>.

A terminal should pop up inside VS Code, and you should see:

```
You're all set up!
```

If this is what you see, you're all set!

---

> If VS Code prompts you to install other extensions or set up anything else (GitHub Copilot, etc.) throughout this process, you can click `x`. These aren't necessary for this course.
