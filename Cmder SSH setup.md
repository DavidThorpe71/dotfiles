# Setup Cmder to ssh into servers

Info from (https://medium.com/@erinus/cmder-setup-tasks-e5109bbb742b)

1. Open Cmder - settings menu
1. Select `Startup` / `tasks`
1. Add new tasks by clicking `+`
1. In top left box type `ssh::` followed by the name you want to appear in the menu eg `root@my_website`
1. In task parameters type `/icon"%CMDER_ROOT\icons\cmder.ico"` - this is to select the icon that shows in Cmder (can select a different icon if you like!)
1. In main box type:
   
```
cmd /c "%ConEmuDir%\..\git-for-windows\usr\bin\ssh [username]@[hostname] -i [sshkey]" -new_console:d:%USERPROFILE% "-new_console:t:[display]"
```
  * [username] is `root`
  * [hostname] is the IP address e.g. `12.345.67.89`
  * [sshkey] is the path of the ssh key on your computer e.g. `C:\Documents\Keys\mykey`
    * N.B. ssh key must be converted to open SSH file in putty-gen in order for it to work in Cmder - does not load .ppk files
  * [display] is the name you want to appear in the Cmder window
7. Click `Save settings`
