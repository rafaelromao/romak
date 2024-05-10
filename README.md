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

## Ç Extension

There is an optional extension to the secondary layer, which I call *Ç Extension*. It activates an one-shot layer just after `ç` is typed, to allow easy access to the vowels and accentuated vowels that are commonly seem after ç, in Portuguese, so that typing common bigrams like `çã` and `çõ` will not require two consecutive activations of the secondary alpha layer.

Ç Extension layer:

```
     _  _  _          Ô  O  U
  _  _  _  _          Ã  A  E  Ú
     _  _  _          Õ  Á  Ó
           _  _    _  _
```

## Magic Romak

There is a version of Romak 24 that uses a [Magic Key](https://github.com/Ikcelaks/keyboard_layouts/blob/main/magic_sturdy/magic_sturdy.md) to improve the typing experience, reducing SFBs and consecutive activations of the secondary alpha layer. To see more about that check the [Magic Romak](MagicRomak.md) page.

## Performance Analysis

A quick comparison between the 3 main variations of Romak and some popular modern layouts can be seen below. These tests included both Portuguese and English in the text corpus.

![img](img/perf3romaks.png)
![img](img/heatmaps3romaks.png)

A more detailed performance analysis for the Romak 34 and other modern layouts can be found [here](analysis.md).

## Implementation

If you want to see this layout in use, check my [Keyboards](https://github.com/rafaelromao/keyboards) repository.
