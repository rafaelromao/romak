# The Romak Keyboard Layout

**Romak** is a keyboard layout built for Portuguese and English users, with a goal to enhance hand alternation, minimize finger movement, reduce single-finger bigrams, and decrease reliance on the pinky and central columns.

Romak is inspired mostly by [BEAKL](https://deskthority.net/wiki/BEAKL) and [Engram](https://engram.dev/), but resembles some modern keyboard layouts, like [Gallium](https://github.com/GalileoBlues/Gallium), [Graphite](https://github.com/rdavison/graphite-layout), [Apt](https://github.com/Apsu/apt), [Sturdy](https://oxey.dev/sturdy/), [Semimak](https://semilin.github.io/blog/2021/semimak.html), [Canary](https://github.com/Apsu/Canary) and [Recurva](https://github.com/GalileoBlues/Recurva), but was not inspired by any of them (I did not know about them when Romak was designed).

## Magic Romak

The most relevant version of the layout is Magic Romak. It contains only 24 keys and uses [Magic Keys](https://github.com/Ikcelaks/keyboard_layouts/blob/main/magic_sturdy/magic_sturdy.md) to improve the typing experience. To see more about that, check the [Magic Romak](MagicRomak.md) page.

## Romak 34

This is the standard version of Romak, that can be used by anyone with a 34 keys columnar staggered keyboard, in the common format 3x5+2.

```
  Q  B  M  G  K    X  L  O  U  Y
  D  N  S  T  W    Z  R  A  E  I
  Qu F  C  P  V    J  H  ,  .  ;
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

This is the smallest version of the Romak layout, designed for the uncommon format 1333+2, in which there are no center columns and only one key per pinky. A secondary alpha layer is necessary to place the missing alphas. Common accented letters, in Portuguese, are also available in this secondary alpha layer.

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
           '  _    _  '
```
```
® = Repeat Last Key
Sp = Space
Sf = One Shot Shift
A2 = One Shot Alpha 2
```

## Combos:

Base layer combos are optional. They are available as a convenient alternative to the secondary alpha layer.

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
Secondary alpha layer combos complement its funcionalities.

Alpha 2 combos:
```
ZX  = dead ^
JÇ  = dead ~
QuK = dead "
XW  = dead '
ÇV  = dead `
ÃÁ  = ?
ÕÂ  = ! 
ÁÉ  = À
ÂÊ  = _
```

## Ç Extension

There is an extension to the secondary alpha layer, which I call *Ç Extension*. It activates an one-shot layer just after `ç` is typed, to allow easy access to `ã`, `õ` and macros for `ão` and `ões`.

Ç Extension layer:

```
     _  _  _          _  _  _
  _  _  _  ÃO         Ã  _  _  _
     _  _  ÕES        Õ  _  _
           _  _    _  _
```

## Performance Analysis

A quick comparison between the 3 main variations of Romak and some popular modern layouts can be seen below. These tests included both Portuguese and English in the text corpus.

![img](img/perf3romaks.png)
![img](img/heatmaps3romaks.png)

A more detailed performance analysis for the Romak 34 and other modern layouts can be found [here](analysis.md).

## Implementation

If you want to see this layout in use, check my [Keyboards](https://github.com/rafaelromao/keyboards) repository.
