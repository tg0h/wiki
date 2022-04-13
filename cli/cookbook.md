# Cookbook

# Ansi

use sed to search for a string and colour it

```bash
use the standard s/<pattern>/<replaceWith>/
note that & refers to the matched pattern

gsed -E "s/#.*/"$'\e[36m'"&"$'\e[m'"/"
```
