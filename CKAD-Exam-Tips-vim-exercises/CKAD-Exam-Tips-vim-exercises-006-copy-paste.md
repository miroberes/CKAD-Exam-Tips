---
title: Vim for CKAD - exercise 6 - copy from browser, paste into Vim
date: 2025-01-11
---
Vim is great if we invest time to learn to use it. Editing Kubernetes YAML files in Vim should be as natural as breathing.

## Getting Started with Vim for CKAD exam

## Vim for CKAD - exercise 6 - copy from browser, paste into Vim

### First things first
Put your mouse away, forget you have a touchpad and **keep your hands on the keyboard**.

### Open a new file in Vim
```bash
vim vimisawesome.yaml
```

To keep the yaml properly formatted after pasting it into Vim, we need to set Vim up:
```bash
:set paste
```

For proper yaml formatting, the indentation needs to be done with spaces. To see if yaml is not accidentally indented using tabulators, make tabulators visible :
```bash
:set list
```
### Copy a yaml from kubernetes.io - paste it into a Vim document

Open the networkpolicy.yaml file from:
https://kubernetes.io/docs/concepts/services-networking/network-policies/#networkpolicy-resource

Practice using the Firefox browser in Linux: select the yaml text with the mouse and copy it.
```bash
control c
```

Paste the yaml into the Vim document:
```bash
i  // switch to insert mode
shift control v
```

If the yaml looks good - which means, that indentation is done with empty spaces (NOT with multiple ```^I``` characters, which would now be visible), the last but very important step - reset the **paste** mode back to **nopaste**, otherwise the tab expansion will not work. We need Vim to expand tabulators into two spaces when we press Tab, instead of inserting the ```^I```character.
```bash
:set nopaste 
```

### Congratulations!
Practice these steps to make editing documents in Vim second nature, copying yaml text from a browser and pasting it into Vim documents without loosing the proper indentation.
