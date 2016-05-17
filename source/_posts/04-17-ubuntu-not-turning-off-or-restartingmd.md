---
title: ubuntu not restarting or turning off 
date: 2016-05-17 21:15:00
tags: daily, learn
---
Lately I have been getting tired of my operating system just not wanting to reboot or sometimes not turning off. This happens in my version off ubuntu due a problem with the energy management. 
The way to solve this is changing the boot parameters for the operating system. So you will need to follow the next steps:
1. Edit the grub settings file (if you use nano as at the end do CTRL+O to save CTRL+X to close)
```
sudo nano /etc/default/grub
```
2.

4. 3. Call the command line to update the grub (os selector for operating system)
```
sudo update-grub
```
first reboot this 
