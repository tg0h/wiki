# jq Cookery

## Export as CSV

Does not work with nested json

The secret sauce is to dereference the object passed to map with an array `map ( .[ "key1", "key2" ... ] )`

:::caution escape the $ with a \ in a shell script HEREDOC
:::

```jq
      (.[0] | keys_unsorted) as $keys
      |
        $keys,
        # object dereferencing in jq accepts an array
        # eg  obj | jq .["key1", "key2
        map( [ .[ $keys[] ] ] )[]
      | @csv
```

## Modules

```jq
  local jqQuery=$(cat <<-EOF
                      include "pad";
                      .[] |
                      "\(.key | rpad(8;" "))
EOF
)

  jq --raw-output -L "~/.config/jq" $jqQuery <<< $json
```

## Inline Functions

```jq
    local jqQuery=$(cat <<-EOF
                               def rpad(\$len; \$fill): tostring | (\$len - length) as \$l | . + (\$fill * \$l)[:\$l];
                               def lpad(\$len; \$fill): tostring | (\$len - length) as \$l | (\$fill * \$l)[:\$l] + .;
                               include "pad"
                               .keymaps |
                               map( "\(.bindkey) \(.dir)")
                               | .[]
EOF
)
  jq $jqQuery <<< $json
```
