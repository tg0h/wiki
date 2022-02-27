# zsh

- load order
- completion
- param expansion

## Autoload

### fpath

add the current directory (.) to fpath with

```zsh
fpath=(. $fpath)
```

### autoload

autoload tells zsh to lazy load the function. This is better than sourcing (which eagerly loads ) the function. If you source many functions in your zshrc, it slows down your zsh startup time.

three kinds of functions

```zsh
# file named 0f
# calling 0f the first time calls 0f

echo this is 0f
```

```zsh
# file named f
# calling f the first time calls f

f(){
  echo this is f with $1 arg
}
```

```zsh
# file named fa with initialization code
# calling fa the first time runs the initialization code (but does not call fa)
# calling fa the second time calls the fa function

fa(){
  echo this is fa with $1 arg
}
echo this is f2's initialization code
```

### extras

which, autoload -X, setopt KSH_AUTOLOAD

call which to see if your function is defined
after autoloading your function the function body is shown as

```zsh
f () {
	# undefined
	builtin autoload -X
}
```

autoload with the -X flag tells zsh to call your function after loading it. However, if your file also contains initialization code, the function is not called? see `man zshbuiltins` to learn more about the autoload function

from `man zshmisc` see section AUTOLOADING FUNCTIONS
if KSH_AUTOLOAD is set or the file contains only a simple definition of the function, the file's contents will be executed
setting the opt KSH_AUTOLOAD will run both the initialization code and the function
