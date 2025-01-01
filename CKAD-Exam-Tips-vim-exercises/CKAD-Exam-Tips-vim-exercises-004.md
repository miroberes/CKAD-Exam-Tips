Vim is great if we invest time to learn to use it. Editing Kubernetes YAML files in Vim should be as natural as breathing.

## Getting Started with Vim for CKAD exam

## Vim for CKAD - exercise 4

### First things first
Put your mouse away, forget you have a touchpad and **keep your hands on the keyboard**.

### Open a new file in Vim
```bash
vim vimisawesome.yaml
```
If the file vimisawesome.yaml does not exist, Vim opens a new file.

### Send vim to background
Put vim to sleep, ***z***zzz...
If you viewed some resource in the terminal and need to see the output again, but now you are in vim editing a pod, don't leave Vim, just hide it.

```bash
control z
```

The output in the terminal shows that Vim is stopped:
```bash
[1]+  Stopped                 vim vimisawesome.yaml
```
### Bring vim to ***f***ore***g***round

```bash
fg
```

Now you can continue to edit the file in Vim.

### Congratulations!
Practice these steps to make using Vim second nature, hiding it and bringing it back instead of closing it and opening again.
