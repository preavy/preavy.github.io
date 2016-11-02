---
layout: post
category : tech
tags : [ssh]
---

Every time I edit ~/.ssh/config I get an error afterwards

    Bad owner or permissions on .ssh/config

I never remember, but the error message is exactly right. You just need to set the [owner](http://serverfault.com/questions/253313/ssh-hostname-returns-bad-owner-or-permissions-on-ssh-config) and [permissions](http://superuser.com/questions/348694/bad-owner-or-permissions-error-using-cygwins-ssh-exe).
