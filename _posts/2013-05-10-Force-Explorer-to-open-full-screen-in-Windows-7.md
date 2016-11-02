---
layout: post
category : tech
---
To force Windows Explorer to always open maximised, add

    "MaximizeApps"=dword:00000001

to

    [HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer]

I got this from Phantom010 [here](http://forums.techguy.org/windows-7/1023278-windows-explorer-my-computer-doesnt.html) but putting it here for my own reference.
