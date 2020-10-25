# using Git as Portable version

1. Выбрать *portable* версию <span style="color:red"> (♦ открывая страницу начнется авто-загрузка стандартной версии - **отказаться**)</span>
[Download Git for Windows](https://git-scm.com/download/win)

2. скаченый файл `PortableGit-2.28.0-64-bit.7z.exe` с расширением `*.7z.exe` - самораспаковывющийся архив; запустить там где будет находиться **данная программа**; пусть распакуется сам, иначе потребуется донастраивать. Папку он создаст сам.

## Sources

- README.portable (in folder of *portableGit*)
- Integrated Terminal [official](https://code.visualstudio.com/docs/editor/integrated-terminal)
- https://fofxacademy.com/how-to-setup-git-on-your-pc-for-multiple-github-accounts/
  - chapter:
What Happens When Git is not Configured for Multiple Accounts
- [using ConEmu](https://medium.com/fierce-punch-studios/portable-bash-cli-for-windows-13f52eb013c3)
  - 2nd place on [What are the best terminal emulators for Windows?](https://www.slant.co/topics/1552/~terminal-emulators-for-windows)
- [mingw](http://www.mingw.org/wiki/getting_started)
- [r-a-y notes](https://gist.github.com/r-a-y/da6c3b1b99aafcb3e97e311280aa9434)
- [youtube from JavaScript.ru](https://youtu.be/ePcY5dRdnPo?list=PLDyvV36pndZHkDRik6kKF6gSb0N0W995h&t=129)
- [Nov.2018 - Create a Portable IDE with Visual Studio Code](https://medium.com/@fawwazyusran/create-a-portable-ide-with-visual-studio-code-fb0c6bc198ef)
- PATH for the processes on a per session basis
- Git Bush command:
  - MinGW64
    - `q` - for *quit* from big listing and at the end

- [Integrated Terminal](https://code.visualstudio.com/docs/editor/integrated-terminal#_configuration) - config terminal of portable VS Code
  - path of config .json "C:\soft\prgrm\N.VSCode-1.50.0\data\user-data\User\settings.json"
  - shell cnfig
    - `terminal.integrated.shell.*`
    - `terminal.integrated.shellArgs.*`
    > !! if do it on workspace level needs whitelist the workspace to allow setting your shell, shell args and it's environment using the `Terminal: Manage Workspace Shell Permissions` command.
  - set the exact executable used in your settings file

    ```json
    // Command Prompt
    "terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe"
    // PowerShell
    "terminal.integrated.shell.windows": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe"
    // Git Bash
    "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe"
    ```

## ToDo

- ? new ver.: https://github.com/git-for-windows/git/releases/
- ? Windows Credential Manager
- set --global env in my path
- VS Code
  - Terminal
    - use several tools in terminal
      - how to add portable terminal to VS Code?
    - what command can be used when starting Git
    - ? use and config cmd from *portableGit*
    - ? [Cmder](https://cmder.net/)
    - ? [PowerShell Core 6.0](https://docs.microsoft.com/en-us/powershell/scripting/whats-new/what-s-new-in-powershell-core-60?view=powershell-7)
      - VS Code + Power Shell [official](https://code.visualstudio.com/docs/languages/powershell)
  - set path to Git

## some notes

>Git configuration variables can be stored at three different levels. Each level overrides values at the previous level

1. System level (applied to every user on the system and all their repositories)

- to view, `git config --list --system` (may need sudo)
- to set, `git config --system color.ui true`
- to edit system config file, `git config --edit --system`

2. Global level (values specific personally to you, the user).

- to view, `git config --list --global`
- to set, `git config --global user.name xyz`
- to edit global config file, `git config --edit --global`

3. Repository level (specific to that single repository)

- to view, `git config --list --local`
- to set, `git config --local core.ignorecase true` (--local optional)
- to edit repository config file, `git config --edit --local` (--local optional)

>How do I view all settings?

- Run `git config --list`, showing system, global, and (if inside a repository) local configs
- Run `git config --list --show-origin`, also shows the origin file of each config item

> How do I read one particular configuration?

- Run `git config user.name "Mr-Niko"` to get user.name, for example.
- You may also specify options `--system`, `--global`, `--local` to read that value at a particular level.

> ? set configuration (--system, --global, --local)
`git config user.name "Mr-Niko"`
`git config user.email "47379249+Mr-Niko@users.noreply.github.com"`

## Configuration

### add portable [PowerShell Core](https://github.com/PowerShell/PowerShell)
- under *...download the PowerShell binary archives...* → Downloads (stable) → 64-bit


#### ? or [ZIP package](https://github.com/PowerShell/PowerShell/releases)

- you may need to unblock the file using the Unblock-File cmdlet
- unzip the contents to the location of your choice and run pwsh.exe from there
- for remoting over WSMan to work properly, ensure that you've met the [prerequisites](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-7#prerequisites)

### Git Components

#### [mingw](http://www.mingw.org/wiki/getting_started)
- `q` - after big listing to *quit*

#### Git Credential Manager Core (**GCM Core**)

- default credential helper since *"Git for Windows 2.29"* ver. and is included as an optional component of *"Git for Windows 2.28"*
- old ver. was [Git-Credential-Manager-for-Windows](https://github.com/microsoft/Git-Credential-Manager-for-Windows)