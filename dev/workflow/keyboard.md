# keyboard

- do not switch ctrl keys for related actions

  - eg switch monitor, switch stack
  - hyper r, hyper /

- vim
  - https://github.com/drmikehenry/vim-fixkey/blob/main/doc/fixkey.txt
  - https://sw.kovidgoyal.net/kitty/keyboard-protocol/
  - https://erwin.co/getting-ctrltab-to-work-in-neovim/

## problems

- terminals ignore shift key when ctrl key is pressed
- terminals respect the c0 control codes - ctrl m and enter are the same

## ansi

- control characters

  - non-printing characters
  - started first because of technical limitations (only 32 instructions)
  - then escape sequences were introduced to send hundreds of device instructions ...

- C0 control codes

  - 32
  -

- control codes can be represented with caret notation. keyboards use this mnemonic device for users to send control codes with the terminal

  - caret notation
    - ^[ - introduces an escape sequence
      - 0x1b, decimal 27

- C1 control codes
  - CSI
    - control sequence introducer
    - ESC [
    - ansi code for esc is (decimal) 27 or (hex) 0x1b
    - ansi code for [ is (decimal) 91 or (hex) 0x5b
    - in other words, CSI can also be sent as 0x1b 0x5b

## kitty keyboard-protocol

- CSI <unicode key>:<shifted unicode key>:<base layout unicode key> ; <modifiers> ; <text as codepoints> u
  - optionality
    - only unicode key is mandatory, everything else is optional. see progressive enhancement.
  - parameters
    - unicode key
      - can be a foreign letter
    - shifted unicode key
      - shifted foreign letter
    - base layout unicode key
      - which key is pressed in a standard english keyboard
    - text as code point
      - eg if opt-a is pressed, it can represent å. the unicode key of å can be sent
  - <xxx> parameters are decimal numbers (unicode key points)
  - u character 0x75 terminates

```
Shift+ㅅ REPEAT
CSI 12613 : 12614 : 116 ; 2 : 2 u
Shifted key: ㅆ Alternate key: t
```

- modifiers

  - bit mask,
  - shift is 0b1
  - alt is 0b10
  - etc ...

- event types
  - press
  - repeat
  - release

## scancodes

## references

- https://sw.kovidgoyal.net/kitty/keyboard-protocol/
- https://erwin.co/getting-ctrltab-to-work-in-neovim/
- https://gist.github.com/fnky/458719343aabd01cfb17a3a4f7296797
- https://en.wikipedia.org/wiki/ANSI_escape_code
