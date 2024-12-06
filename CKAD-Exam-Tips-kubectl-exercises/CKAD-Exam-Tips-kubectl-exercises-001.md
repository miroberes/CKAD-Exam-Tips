## Getting Started with kubectl for CKAD exam

## kubectl for CKAD - exercise 1

### First things first
Put your mouse away, forget you have a touchpad and **keep your hands on the keyboard**.

###  Start your terminal, the adventure begins... 

The situation with the CKAD and other CK* exams is that we need to be ***fast***.
To key be fast when editing yaml files and applying them with kubectl apply is - ***don't leave Vim***.
Yes, we can do kubectl apply, even kubectl replace right from inside Vim!

### A possible CKAD exam scenario
Run a pod testpod, name the container nginx-container

### Open a free kubernetes cluster playground or use your own
https://killercoda.com/playgrounds/scenario/kubernetes

### Open a new yaml file directly in Vim
```bash
kubectl run testpod --image nginx:alpine --dry-run=client -o yaml | vim -
```

### Look up the container name (testpod), then jump right to it by searching in Vim starting at the bottom
```bash
G         // jump down to the last line
?testpod  // search upwards from the bottom to top
Enter
N         // 'N'ew search - repeat search upwards as needed
```

### Replace the container name with nginx-container - type it or copy & paste it from the task description
```bash
C          // 'C'lear (delete) everything from the cursor to the end of this line and start writing
nginx-container
```

### ***w***rite (save) the document
```bash
ESC              // 'ESC'ape from INSERT mode 
:w testpod.yaml  // 'w'rite (save) the document
```

## Watch the magic...
### run kubectl apply directly from inside Vim
```bash
:!kubectl apply -f %   // % references the file name
```

If everything is fine with the yaml file, testpod.yaml gets applied, pod is created.

### Scenario continued
If there is an error and **the pod has not been created**, read the error, then simply press Enter to edit the yaml file and correct the error.

### ***w***rite (save) the document
```bash
ESC         // 'ESC'ape from INSERT mode 
:w          // 'w'rite (save) the document
```

### Repeat running kubectl apply directly from Vim using the previous command
```bash
:up arrow    // repeat to find the command :!kubectl apply -f %
Enter
```
If the error is fixed in the yaml file, testpod.yaml gets applied, pod is created.

### Scenario
kubectl edit and replace an existing pod

A pod testpod is running in the cluster. We want to edit it, change something like for example the label value 'testpod' to 'nginx', replace the pod - and do it ***fast***.

### Start editing pod testpod in Vim
```bash
kubectl edit po testpod
```

### Look up the label value (testpod), then jump right to it by searching in Vim from the top
```bash
/testp     // search down from the top, no need to write the whole word
Enter
n          // repeat search downwards as needed
```

### Replace the label value name - type it or copy & paste it from the task description
```bash
C          // 'C'lear (delete) everything from the cursor to the end of this line and start writing
nginx
```

### ***w***rite (save) the document to persist changes
```bash
ESC         // 'ESC'ape from INSERT mode 
:w          // 'w'rite (save) the document, file name is provided by kubectl edit
```

## Watch the magic... again
### run kubectl replace directly from inside Vim - delete the pod and create a new one
```bash
:!kubectl replace -f % --force --grace-period 0
```

### Scenario continued
If there is an error and **the pod has not been replaced**, read the error, then simply press Enter to edit the yaml file and correct the error.

### ***w***rite (save) the document
```bash
ESC         // 'ESC'ape from INSERT mode 
:w          // 'w'rite (save) the document
```

### Repeat replacing the pod directly from Vim using the previous command
```bash
:up arrow    // repeat to find the command :!kubectl replace -f % --force --grace-period 0
Enter
```

If everything is fine with the edited pod file, pod is deleted and a new pod is created.

### Close the document / ***q***uit Vim
```bash
:q
```
Vim ***q***uits, closing the edited pod manifest.

### Congratulations!
Practice these steps to make applying yaml files and replacing running pods with kubectl directly from Vim second nature.
