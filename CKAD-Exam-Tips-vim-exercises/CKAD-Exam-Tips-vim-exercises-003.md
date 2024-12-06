Vim is great if we invest time to learn to use it. Editing Kubernetes YAML files in Vim should be as natural as breathing.

## Getting Started with Vim for CKAD exam

## Vim for CKAD - exercise 3

### First things first
Put your mouse away, forget you have a touchpad and **keep your hands on the keyboard**.

### Open an existing file in Vim
```bash
vim vimisawesome.yaml
```

### The text reads something like this
```bash
Vim is awesome. Because it really is!
```

### Keep the existing text and ***o***pen a new line below the current line - aka start writing below this line
```bash
o
```
***o*** ***o***pens a new line l***o***wer (as in l***o***wercase ***o***) than the current one and switches to INSERT mode, allowing us to start writing

### Start writing at the current cursor position
```bash
A new line has opened low below the current line.
```

### ESCape from INSERT mode and return to NORMAL mode before proceeding to the next step.
```bash
ESC
```

### Keeping the existing text ***O***pen a new line above the current line - aka start writing above this line

```bash
O
```

***O*** ***O***pens a new line up (as in uppercase ***O***) ab***O***ve the current one and switches to INSERT mode, allowing us to start writing.

### Start writing at the current cursor position
```bash
A new line has opened up abOve the current line.
```

### ESCape from INSERT mode and return to NORMAL mode before proceeding to the next step.
```bash
ESC
```
### Now that the exercise pattern is clear, practice these most commonly used INSERT mode commands

### Start writing – remember to ESCape from INSERT mode after each write.

r***i***ght where you are
```bash
i
```

before the first non-blank character on this line (***I***nitial)
```bash
I
```

move to position ***0*** and start writing r***i***ght there aka before the first character on this line
```bash
0i
```

***A***ppend after the last character on this line
```bash
A
```

***a***fter this character aka one character to the right
```bash
a
```

on a new line up ab***O***ve the current line
```bash
O
```

on a new line l***o***w below this line
```bash
o
```

from the ***S***tart of this line but delete all the text
```bash
S
```

right where you are but delete the ***s***elected character
```bash
s
```

 ***C***lear (delete) everything from the cursor to the end of this line and start writing (enter INSERT mode)
```bash
C
```

### Combining INSERT mode commands with movements up ***k*** and down ***j***

***A***ppend to the end of the existing line above
```bash
kA
```

at the beginning of the existing line above (***I***nitial)
```bash
kI
```

***A***ppend to the end of the existing line below
```bash
jA
```
at the beginning of the existing line below (***I***nitial)
```bash
jI
```

### ESCape from INSERT mode 
```bash
ESC
```

### ***w***rite (save) the document if you want to
```bash
:w
```

### Alternatively, if you don't want to write the document, close it without saving aka - ***q***uit forcefully (!)
```bash
:q!
```
Vim ***q***uits, closing the edited document, discarding all changes.

### Congratulations!
Practice these steps to make editing YAML files in Vim second nature.
