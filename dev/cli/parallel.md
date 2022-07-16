# parallel

## how to run things in parallel

zargs

```zsh
# run a zsh function
# autoload zargs
-P with 10 cores

-t with verbose output

-- supply the input args

-- supply the zsh function to run

zargs -P 10 -t -i{} -- $(seq 100) -- csci -c 4213 -i {}
```

gnu parallel
