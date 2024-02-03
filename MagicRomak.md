# The Romak Keyboard Layout

**Romak** is a keyboard layout built for Portuguese and English users, with a goal to enhance hand alternation, minimize finger movement, reduce single-finger bigrams, and decrease reliance on the pinky and central columns.

For the regular versions of Romak, including performance analysis, check [this other page](README.md) instead.

## Magic Romak

This is a version of Romak 24 that uses a [Magic Key](https://github.com/Ikcelaks/keyboard_layouts/blob/main/magic_sturdy/magic_sturdy.md) to improve the typing experience, reducing SFBs and consecutive activations of the secondary alpha layer.

### Smart Shift

In this version, another new feature is introduced, the Smart Shift behavior. With this feature, the One Shot Shift key will not act as shift when typed mid word, but as something else instead. In this case, it can be either a Repeat Key or a Magic Key.

Alpha 1 layer:

```
     B  M  G          L  O  U   
  D  N  S  T          R  A  E  I 
     F  C  P          H  ,  .   
           ®  Sp   A2 *
```

Alpha 2 layer:

```
     Q  Qu K          Ô  Ó  Ú
  Y  Z  X  W          Ã  Á  É  Í
     J  Ç  V          Õ  Â  Ê
           '  _    _  _
```
```
® = One Shot Shift / Repeat Key
Sp = Space
* = One Shot Shift / Magic Key
A2 = One Shot Alpha 2
```
## Combos:

Alpha 1 combos:
```
NS = Q
MG = K
ST = W
CP = V
LO = X
RA = Z
H, = J
AE = Y
```

Alpha 2 combos:
```
ZX = (
JÇ = _
QuK = "
XW = '
ÇV = ?
ÔÓ = :
ÃÁ = -
ÕÂ = !
ÁÉ = )
ÂÊ = À
```


### Mid Word Detection

Along with Enter, Tab, Esc, Backspace and Navigation keys, Space will signal to the keyboard that a new word will be starting and clear the repeat key state. 300ms of inactivity will also clear this state. In both cases, One Shot Shift will be triggered instead when the Magic Key or Repeat Key is tapped.

### Smart Shift / Repeat Key

Usually the Repeat Key, when not acting like One Shot Shift, will simply repeat the last character, but in some cases, an alternate repeat can be used, most of the time to complete a word. Alternate repeats must be simple to memorize, anything more complex should go to the Magic Key.

This is how the **Smart Shift / Repeat Key** behaves:

| Previous Key | Output  | Example | Alternate Repeat |
|---|---|---|---|
| a | nd | and | *
| á | v | agradável | *
| ã | o | não | *
| â | n | ângulo | 
| à | qu  | àquela | *
| b | b | rabbit | 
| c | c | accept | 
| ç | ão | ação | *
| d | d | add | 
| e | e | seed | 
| é | v | prévia | *
| ê | e | vêem | *
| f | f | off | 
| g | g | hugging | 
| h | ões | milhões | *
| i | ng | doing | *
| í | v | possível | *
| j | á | já | *
| k | ey | keyboard | *
| l | l | follow | 
| m | m | common | 
| n | n | announce | 
| o | o | door | 
| ó | v | imóvel | *
| õ | es | limões | *
| ô | o | vôo | *
| p | p | flopping | 
| q | q | qq (short for qualquer) | 
| qu | ê | sequência | *
| r | r | carry | 
| s | s | less | 
| t | t | flutter | 
| u | y | buy | *
| ú | v | dúvida  | *
| v | á | várias | *
| w | hy | why | *
| x | á | hexágono | *
| y | ou | you | *
| z | z | buzzword | 
| . | com | .com | *
| - | --- | markdown horizontal separator | *

### Smart Shift / Magic Key

The main problem with this double duty in these keys is that false positives can happen, with a Repeat or Magic being triggered when a One Shot Shift is expected.

I usually use only the key on the right side as One Shot Shift, so false positives with the Repeat Key are not frequent, but for the Magic Key they could be quite common.

There is a inactivity timeout, since Repeat and Magic Key will usually be required only when fast typing a word, but when working with VIM, moving from the normal to the insert mode and then typing an upper case letter would easily trigger a false positive. This is why some keys must be excluded:

| Previous Key | Output  | Reason |
|---|---|---|
| c | OS &#8679; | `c` is used to change text in VIM
| s | OS &#8679; | `s` is used to substitute text in VIM
| o | OS &#8679; | `o` is used to enter a new line in VIM
| z | OS &#8679; | `z` is used to insert in my remapped VIM
| j | OS &#8679; | `j` is used to append in my remapped VIM
| h | OS &#8679; | `h` is used to replace text in my remapped VIM
| y | OS &#8679; | `y` is used to copy in VIM, and following paste before the cursor is performed with `P`

And this is how the **Smart Shift / Magic Key** behaves for the remaining keys:

| Previous Key | Output  | Example | 
|---|---|---|
| a | o | caos
| á | x | máximo 
| ã | o | não 
| â | m | câmbio | *
| à | qu  | àquilo | 
| b | y | bye 
| c | | 
| ç | ões | ações 
| d | y | dye
| e | u | meu
| é | u | céu 
| ê | x | êxito 
| f | y | certify 
| g | u | ambíguo
| h | | 
| i | backspace I' | I'm
| í | z | juízo 
| j | | 
| k | w | backward
| l | h | coelho
| m | s | synonyms
| n | f | info
| o | | 
| ó | x | próximo 
| õ | e | põe 
| ô | v | côvado | 
| p | t | accept
| q | q | qq (short for qualquer)
| qu | ê | sequência 
| r | l | early
| s | | 
| t | w | two 
| u | e | blue 
| ú | z | dúzia 
| v | í | vídeo 
| w | k | awkward 
| x | í | exímio 
| y | | 
| z | | 
| . | ./ | ./ 
| - | -> | ->

## Implementation

A complete implementation for QMK and ZMK can be found [here](https://github.com/rafaelromao/keyboards).
