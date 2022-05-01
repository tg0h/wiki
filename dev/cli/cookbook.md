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

- TODO: combine with jq colour module

# Colour

```bash
ansi supports truecolour (8 bits per colour)
specify the RGB 256bit triple with the escape sequence below
the triple below is 82,96,255

echo "\x1b[38;2;82;96;255m colourful text"
```

# get directory from filepath

```bash
# /dir/to/file becomes /dir/to
[[ -f $target ]] && target=${target%/*} # zsh variable expansion - min match pattern /* and remove from tail
```

# tail

```bash
tail -n +2 # print everything but the first line
tail -n +3 # print everything but the first 2 lines
```
