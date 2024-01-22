# The Romak Keyboard Layout

**Romak** is a keyboard layout built for Portuguese and English users, with a goal to enhance hand alternation, minimize finger movement, reduce single-finger bigrams, and decrease reliance on the pinky and central columns.

Romak is inspired mostly by [BEAKL](https://deskthority.net/wiki/BEAKL) and [Engram](https://engram.dev/), but resembles some modern keyboard layouts, like [Gallium](https://github.com/GalileoBlues/Gallium), [Graphite](https://github.com/rdavison/graphite-layout), [Apt](https://github.com/Apsu/apt), [Sturdy](https://oxey.dev/sturdy/), [Semimak](https://semilin.github.io/blog/2021/semimak.html), [Canary](https://github.com/Apsu/Canary) and [Recurva](https://github.com/GalileoBlues/Recurva), but was not inspired by any of them (I did not know about them when Romak was designed).

## Romak 34

This is a variation of Romak that can be used by anyone with a 34 keys columnar staggered keyboard, in the common format 3x5+2.

```
  Q  B  M  G  K    X  L  O  U  Y
  D  N  S  T  W    Z  R  A  E  I
  /  F  C  P  V    J  H  ,  .  ;
```

## Romak 30

This is a variation of Romak that can be used with 30 keys, in the format 23332+2, with boards like the Hummingbird and Rommana.
In this variation, all alphas remain in the base layer, and common symbols like comma and dot are moved to combos, like HK for comma and KX for dot.

```
  Q  B  M  G  W    Z  L  O  U  Y
  D  N  S  T  V    J  R  A  E  I
     F  C  P          H  K  X  
```

## Romak 24

This is the default Romak layout, designed for the uncommon format 1333+2, in which there are no center columns and only one key per pinky. A secondary alpha layer is necessary to place the missing alphas. Common accented letters, in Portuguese, are also available in this secondary alpha layer.

Alpha 1 layer:

```
     B  M  G          L  O  U   
  D  N  S  T          R  A  E  I 
     F  C  P          H  ,  .   
           ®  Sp   A2 Sf
```

Alpha 2 layer:

```
     Q  Qu K          Ô  Ó  Ú
  Y  Z  X  W          Ã  Á  É  Í
     J  Ç  V          Õ  Â  Ê
           '  _    _  _
```
```
® = Repeat Last Key
Sp = Space
Sf = One Shot Shift
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

### Mid Word Detection

Along with Enter, Tab, Esc, Backspace and Navigation keys, Space will signal to the keyboard that a new word will be starting and clear the repeat key state. 300ms of inactivity will also clear this state. In both cases, One Shot Shift will be triggered instead when the Magic Key or Repeat Key is tapped.

### Smart Shift / Repeat Key

Usually the Repeat Key, when not acting like One Shot Shift, will simply repeat the last character, but in some cases, an alternate repeat can be used, most of the time to complete a word.

This is how the Smart Shift / Repeat Key behaves:

| Combination  | Output  | Example | Reason |
|---|---|---|---|
| Space, Tab, Enter, Esc, Backspace, Navigation ® | One Shot Shift | | new word
| 300ms of inactivity ® | One Shot Shift | | inactivity 
| h®  | One Shot Shift |  | `h` is used to replace a char in my remapped VIM
| o®  | One Shot Shift |  | `o` is used to enter a new line in VIM
| y®  | One Shot Shift |  | `y` is used to yank in VIM
| a®  | and | and | word completion
| i®  | ng | doing | word completion
| j®  | just | just | word completion
| k®  | key | keyboard | word completion
| v®  | ver | version | word completion
| w®  | which | which | word completion
| ã®  | ão | não | word completion
| õ®  | ões | anões | word completion
| ç®  | ção | ação | word completion 
| .®  | .com | .com | word completion
| á®  | áv | agradável | reduce activation of Alpha 2
| é®  | év | prévia | reduce activation of Alpha 2 
| í®  | ív | possível | reduce activation of Alpha 2 
| ó®  | óv | imóvel | reduce activation of Alpha 2 
| ú®  | úv | dúvida | reduce activation of Alpha 2 
| anything else ®  | repeat| follow | reduce SFBs 

### Smart Shift / Magic Key

And this is how this Smart Shift / Magic Key behaves:

| Combination  | Output  | Example | Reason |
|---|---|---|---|
| Space, Tab, Enter, Esc, Backspace, Navigation * | One Shot Shift | |  new word
| 300ms inactivity * | One Shot Shift | | inactivity 
| h*  | One Shot Shift |  | `h` is used to replace a char in my remapped VIM
| o*  | One Shot Shift |  | `o` is used to enter a new line in VIM
| y*  | One Shot Shift |  | `y` is used to yank in VIM
| a*  | ao | xiao | reduce SFBs
| c*  | cs | physics | reduce SFBs
| d*  | dy | dye | reduce SFBs
| e*  | eu | meu | reduce SFBs
| k*  | kw | awkward | reduce SFBs
| l*  | lh | coelho | reduce SFBs
| m*  | ms | synonyms | reduce SFBs
| n*  | nf | info | reduce SFBs
| r*  | rh | rhythm | reduce SFBs
| s*  | sm | smile | reduce SFBs
| t*  | tw | two | reduce SFBs
| u*  | ue | blue | reduce SFBs
| w*  | wk | awkward | reduce SFBs
| x*  | xc | exceed | reduce SFBs
| b*  | by | bye | avoid uncomfortable movements
| f*  | fy | certify | avoid uncomfortable movements
| g*  | gu | ambíguo | avoid uncomfortable movements
| ã*  | ão | não | avoid uncomfortable movements
| õ*  | õe | põe | avoid uncomfortable movements
| .*  | ./ | ./ | avoid uncomfortable movements 
| -*  | -> | -> | avoid uncomfortable movements
| qu*  | quê | sequência | reduce activation of Alpha 2 
| j*  | já | já | reduce activation of Alpha 2 
| p*  | pq | pq | reduce activation of Alpha 2 
| v*  | vá | várias | reduce activation of Alpha 2 
| á*  | áv | agradável | reduce activation of Alpha 2
| é*  | év | prévia | reduce activation of Alpha 2 
| í*  | ív | possível | reduce activation of Alpha 2 
| ó*  | óv | imóvel | reduce activation of Alpha 2 
| ú*  | úv | dúvida | reduce activation of Alpha 2 
| ç*  | çõ | ações | reduce activation of Alpha 2 
| i*  | backspace I' | I'm | smart apostrophe
| anything else *  | repeat / ignore |  | reduce SFBs 

## Performance Analysis

A quick comparison between these 3 variations of Romak and some popular modern layouts can be seen below. These tests included both Portuguese and English in the text corpus.

![img](img/perf3romaks.png)
![img](img/heatmaps3romaks.png)

A more detailed performance analysis for the Romak 34 and other modern layouts can be found [here](analysis.md).

## Use Case

If you want to see this layout in use, check my [Keyboards](https://github.com/rafaelromao/keyboards) repository.
