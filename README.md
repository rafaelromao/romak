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
| a®  | and | and | word completion
| h®  | hões | milhões | word completion 
| i®  | ing | doing | word completion
| j®  | já | já | word completion 
| k®  | key | keyboard | word completion
| w®  | which | which | word completion
| x®  | xá | hexágono | word completion
| y®  | you | you | word completion
| v®  | vá | várias | word completion
| ã®  | ão | não | word completion
| õ®  | ões | limões | word completion
| ç®  | ção | ação | word completion 
| .®  | .com | .com | word completion
| á®  | áv | agradável | word completion
| é®  | év | prévia | word completion
| í®  | ív | possível | word completion
| ó®  | óv | imóvel | word completion
| ú®  | úv | dúvida | word completion
| anything else ®  | repeat| follow | reduce SFBs 

### Smart Shift / Magic Key

The main problem with this double duty in these thumb keys, behaving either as One Shot Shift or as Repeat / Magic keys, is that false positives can happen, with a Repeat or Magic being triggered when a One Shot Shift is expected.

I usually use only the key on the right side as One Shot Shift, so false positives with the Repeat Key are not common, but for the Magic Key they could be quite common.

For that reason I included the inactivity timeout, since Repeat and Magic Key will usually be required only when fast typing a word. But when working with VIM, moving from the normal to the insert mode and then typing an upper case letter would easily trigger a false positive for the Magic Key. This is why you can see some keys excluded from the Magic.

And this is how the Smart Shift / Magic Key behaves:

| Combination  | Output  | Example | Reason |
|---|---|---|---|
| Space, Tab, Enter, Esc, Backspace, Navigation * | One Shot Shift | |  new word
| 300ms inactivity * | One Shot Shift | | inactivity 
| h*  | One Shot Shift |  | `h` is used to replace a char in my remapped VIM
| o*  | One Shot Shift |  | `o` is used to enter a new line in VIM
| y*  | One Shot Shift |  | `y` is used to copy in VIM, and following paste before the cursor is performed with `P`;
| z*  | One Shot Shift |  | `z` is used to insert in my remapped VIM
| j*  | One Shot Shift |  | `j` is used to append in my remapped VIM
| a*  | ao | xiao | reduce SFBs
| c*  | cs | physics | reduce SFBs
| d*  | dy | dye | reduce SFBs
| e*  | eu | meu | reduce SFBs
| k*  | kw | backward | reduce SFBs
| l*  | lh | coelho | reduce SFBs
| m*  | ms | synonyms | reduce SFBs
| n*  | nf | info | reduce SFBs
| p*  | pt | accept | reduce SFBs
| r*  | rl | early | reduce SFBs
| s*  | sm | smile | reduce SFBs
| t*  | tw | two | reduce SFBs
| u*  | ue | blue | reduce SFBs
| w*  | wk | awkward | reduce SFBs
| b*  | by | bye | avoid uncomfortable movements
| f*  | fy | certify | avoid uncomfortable movements
| g*  | gu | ambíguo | avoid uncomfortable movements
| ã*  | ão | não | avoid uncomfortable movements
| õ*  | õe | põe | avoid uncomfortable movements
| .*  | ./ | ./ | avoid uncomfortable movements 
| -*  | -> | -> | avoid uncomfortable movements
| qu* | quê | sequência | reduce activation of Alpha 2 
| v*  | ví | vídeo | reduce activation of Alpha 2
| x*  | xí | exímio | reduce activation of Alpha 2 
| á*  | áv | agradável | reduce activation of Alpha 2
| é*  | év | prévia | reduce activation of Alpha 2 
| í*  | ív | possível | reduce activation of Alpha 2 
| ó*  | óv | imóvel | reduce activation of Alpha 2 
| ú*  | úv | dúvida | reduce activation of Alpha 2 
| ç*  | çõe | ações | reduce activation of Alpha 2 
| i*  | backspace I' | I'm | smart apostrophe
| anything else *  | repeat / ignore |  | reduce SFBs 

## Performance Analysis

A quick comparison between the 3 main variations of Romak and some popular modern layouts can be seen below. These tests included both Portuguese and English in the text corpus.

![img](img/perf3romaks.png)
![img](img/heatmaps3romaks.png)

A more detailed performance analysis for the Romak 34 and other modern layouts can be found [here](analysis.md).

## Use Case

If you want to see this layout in use, check my [Keyboards](https://github.com/rafaelromao/keyboards) repository.
