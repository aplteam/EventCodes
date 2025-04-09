# EventCodes

## Overview

Dyalog uses numbers to represent errors. Those errors are accessible via `⎕EN`. However, when one wants to specify an error with a `:Trap` or a `⎕TRAP` statement then one must use integers.

Although a seasoned programmer will over time memorize the most important error numbers, the unusual ones will escape her, not to mention newbies.

There is a better solution to this: using symbolic names which are effectively constants (strictly speaking read-only variables) carrying the integer. That's what the `EventCode` class is for: it offers symbolic names for all trappable events.

Examples:

```
      EventCodes.DEADLOCK
1008
      EventCodes.GetName 1008
DEADLOCK
      EventCodes.List'T'
 TIMEOUT            1006
 TRANSLATION_ERROR    92
 TRAP_ERROR           84
      ⍴EventCodes.List''
53 2      
```
