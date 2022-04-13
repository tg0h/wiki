# Cookbook

# Ansi

use sed to search for a string and colour it
provide the ansi colour code
the ending code is the ansi reset colour code

```bash
use the standard s/<pattern>/<replaceWith>/
note that & refers to the matched pattern

# searches for comments (beginning with #) and colours it cyan
gsed -E "s/#.*/"$'\e[36m'"&"$'\e[m'"/"
```
