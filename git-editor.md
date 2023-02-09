# Set up git editor

The main command is:

```bash
$git config --global core.editor "path to your editor with params"
```

Set up an editor and check it by making a commit:

```bash
$git commit --allow-empty
```

Your favourite editor should open. Write commit message, save and close file. See `git log` to look for a commit. Is it there? If yes, you’re awesome.

## Windows, VS Code

Make sure you selected ‘Add to PATH’ during the installation.

```bash
$git config --global core.editor "code --wait"
```

## Windows, Atom

```bash
$git config --global core.editor "atom --new-window --foreground --wait"
```

## Windows, Sublime Text 3

```bash
 $git config --global core.editor "'c:/program files/sublime text 3/subl.exe' -w"
```

## Windows, Notepad++

```bash
$git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"
```

## macOS, VS Code

Select Shell Command: Install 'Code' command in path from the Command Palette. Then run:

```bash
$git config --global core.editor "code --wait"
```

## macOS, TextEdit

```bash
$git config --global core.editor "open -W -n"
```

## macOS, Atom

```bash
$git config --global core.editor "atom --wait"
```

## macOS, Sublime Text 3

```bash
$ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" ~/bin/subl
$git config --global core.editor "subl -n -w"
```

or

```bash
$git config --global core.editor '"/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" -n -w'
```
