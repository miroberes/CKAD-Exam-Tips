Vim is great if we invest time to learn to use it. Editing Kubernetes YAML files in Vim should be as natural as breathing.

## Getting Started with Vim for CKAD exam

## Vim for CKAD - exercise 2

### First things first
Put your mouse away, forget you have a touchpad and **keep your hands on the keyboard**.

### Open an existing file in Vim
```bash
vim vimisawesome.yaml
```

### The text reads something like this
```bash
Vim is awesome.
```

### Keep the existing text and ***A***ppend some more text to the end aka start writing at the end of this line
```bash
A
```
***A*** moves cursor to the end of this line and switches to INSERT mode allowing us to ***A***ppend text.

### Start writing at the current cursor position
```bash
 Because it really is!
```
### ESCape from INSERT mode and ***w***rite (save) the document
```bash
ESC
:w
```

### Alternatively, use ***saveas*** to save the document under a new name
```bash
:saveas newfilename.yaml
```
Vim saves the current document as a new file and opens the copy for editing, closing the original document.

### Close the document / ***q***uit Vim
```bash
:q
```
Vim ***q***uits, closing the edited document.

### Congratulations!
Practice these steps to make creating, editing, saving, and closing YAML files in Vim second nature.