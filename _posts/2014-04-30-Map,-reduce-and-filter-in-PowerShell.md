---
layout: post
category : tech
---

*Map* (Select in LINQ)

    PS> $double = { $_ * 2 }     # a scriptblock is like a lambda
    PS> 1..5 | % $double         # % is an alias for ForEach-Object
    2
    4
    6
    8
    10

*Filter* (Filter in LINQ)

    PS> $equals3 =  { $_ -eq 3 }
    PS> 1..5 | ? $equals3        # ? is an alias for Where-Object
    3

Composing the two

    PS> 1..5 | ? $equals3 | % $double
    6

*Reduce* (Aggregate in LINQ)

There's no reduce (aggregate) built into PowerShell. The closest seems to be to use a function with a begin and end block.

    function Reduce($initial, $sb)
    {
      begin
      {
        $result = $initial
      }

      process
      {
        $result = & $sb $result $_
      }

      end
      {
        $result
      }
    }

    $sb = { param($x, $y) $x + $y }

    1..5 | Reduce 0 $sb

Update 9/9/2014: Although, conveniently, the ForEach-Object takes a Begin and End block.

    PS> 1..5 | % { $result = 0 } { $result += $_ } { $result } # % is an alias for ForEach-Object
    15
