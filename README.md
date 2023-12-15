# The Romak Keyboard Layout

**Romak** is a keyboard layout built for Portuguese and English users, with a goal to enhance hand alternation, minimize finger movement, reduce single-finger bigrams, and decrease reliance on the pinky and central columns.

Romak is inspired mostly by [BEAKL](https://deskthority.net/wiki/BEAKL) and [Engram](https://engram.dev/), but resembles some modern keyboard layouts, like [Apt](https://github.com/Apsu/apt), [Sturdy](https://oxey.dev/sturdy/), [Semimak](https://semilin.github.io/blog/2021/semimak.html), [Canary](https://github.com/Apsu/Canary) and [Recuva](https://github.com/GalileoBlues/Recurva), but was not inspired by any of them (I did not know about them when Romak was designed).

## Romak 34

This is a variation of Romak that can be used by anyone with a 34 keys columnar staggered keyboard, in the common 3x5+2 format.

```
  Q  B  M  G  K    X  L  O  U  Y
  D  N  S  T  W    Z  R  A  E  I
  /  F  C  P  V    J  H  ,  .  ;
```

## Romak 24

This is the default Romak layout, designed for the uncommon format 1333+2, in which there are no center columns and only one key per pinky. A secondary alpha layer is necessary to place the missing alpha. Common accented letters, in Portuguese, are also available in this secondary alpha layer, along with some combos for common n-grams like `ão`, `õe`, `ção` and `ções`.

Alpha 1 layer:

```
     B  M  G          L  O  U   
  D  N  S  T          R  A  E  I 
     F  C  P          H  ,  .   
           Rp Sp   A2 SF
```
```
Rp = Repeat Last Key
Sp = Space
Sf = One Shot Shift
A2 = One Shot Alpha 2 layer
```

Alpha 2 layer:

```
     Q  Qu K          À  Ó  Ú
  Y  Z  X  W          Ã  Á  É  Í
     J  Ç  V          Â  Ô  Ê
           '  Sp   A2 SF
```

## Combos for alphas and common symbols and n-grams:


Alpha 1 combos:
```
DN = Q, MG = K, ST = W, CP = V,

LO = X, RA = Z, H = J, AE = Y
```

Alpha 2 combos:
```
ZX = (, JÇ = _, QuK = #, XW = ), ÇV = ?

ÀÓ = :, ÃÁ = -, ÂÔ = !, ÁÉ = ão, ÔÊ = õe,

ÃÁÉ = ção, ÂÔÊ = ções
```

## Performance Analysis

A simple performance analysis for the Romak layout can be found [here](analysis.md).

## Use Case

If you want to see this layout in use, check my [Keyboards](https://github.com/rafaelromao/keyboards) repository.
