# The Romak Keyboard Layout

**Romak** is a keyboard layout built for Portuguese and English users, with a goal to enhance hand alternation, minimize finger movement, reduce single-finger bigrams, and decrease reliance on the pinky and central columns.

For the regular versions of Romak, including performance analysis, check [this other page](README.md) instead.

## Magic Romak

This is a version of Romak 24 that uses a [Magic Key](https://github.com/Ikcelaks/keyboard_layouts/blob/main/magic_sturdy/magic_sturdy.md) to improve the typing experience, reducing SFBs and consecutive activations of the secondary alpha layer.

This Magic Key replaces the comma from the standard Romak 24.

The standard Repeat Key is also replaced by a Smart Repeat Key, which outputs an alternate result for keys that do not worth repeating.

Alpha 1 layer:

```
     B  M  G          L  O  U   
  D  N  S  T          R  A  E  I 
     F  C  P          H  *  .   
           ®  Sp  A2  Sf
```

Alpha 2 layer:

```
     Q  Qu K          Ô  Ê  Â
  Y  Z  X  W          Ã  É  Á  Í
     J  Ç  V          Õ  Ó  Ú
           '  _    _  '
```
```
 ® = Repeat Key
Sp = Space
A2 = One-Shot Alpha 2
Sf = One-Shot Shift
 * = Magic Key
```

### Comma-Shift

But since comma is replaced by this Magic Key, how can we type comma?

The best way to use comma in Magic Romak is simply tapping Space after tapping One-Shot Shift. In this case it will send `, ` (comma followed by space), which is quite smart, since comma will almost always be followed by space.
In practice, it can also give the impression that the One-Shot Shift key is actually behaving like a comma when followed by Space, thus the Comma-Shift nickname.

Another way to type comma is tapping One-Shot Shift before tapping the Magic Key. It will make the Magic Key behave as a regular comma.
On the other hand, simple shifting (holding shift while tapping) the Magic Key will type `<`, to preserve the angle brackets pair usually found in the shifted versions of `,` and `.`.

### Repeat Key

Usually the Repeat Key will simply repeat the last character, but in some cases, an alternate repeat can be used. Alternate repeats must be simple to memorize, anything more complex should go to the Magic Key.

This is how the **Repeat Key** behaves:

| Previous Key | Output  | Example | Alternate Repeat |
|---|---|---|---|
| a | v | através | *
| á | v | agradável | *
| ã | o | não | *
| â | n | ângulo | *
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
| ' | v | I've | *

### Magic Key

The Magic Key is available in the same physical key as the repeat key, but in the secondary alpha layer.

This is how the **Magic Key** behaves:

| Previous Key | Output  | Example | 
|---|---|---|
| a | o | caos
| á | x | máximo 
| ã | o | não 
| â | m | câmbio
| à | qu  | àquilo | 
| b | y | bye 
| c | s | docs
| ç | ões | ações
| d | y | dye
| e | u | meu
| é | u | céu 
| ê | x | êxito 
| f | y | certify 
| g | g | 
| h | r | chrome
| i | backspace I' | I'm
| í | z | juízo 
| j | ã | feijão 
| k | w | backward
| l | h | coelho
| m | s | synonyms
| n | f | info
| o | o | 
| ó | x | próximo 
| õ | e | põe 
| ô | v | côvado 
| p | t | accept
| qu | í | química 
| r | ly | early
| s | c | school
| t | w | two 
| u | e | blue 
| ú | z | dúzia 
| v | í | vídeo 
| w | k | awkward 
| x | í | exímio 
| y | y | 
| z | á | 
| . | ./ | ./ 

## Implementation

A complete implementation for QMK and ZMK can be found [here](https://github.com/rafaelromao/keyboards).
