---
layout: post
category : tech
---

    PS> function d {$true;}
    PS> d
    True
    PS> $result = d
    PS> $result -eq $true
    True
    PS> $result -eq $false
    False

So far so good.

    PS> d -eq $true
    True

Still so far so good.

    PS> d -eq $false
    True

Wut.

The solution is [here](http://stackoverflow.com/questions/149191/powershell-functions-return-behavior).