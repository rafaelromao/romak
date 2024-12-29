# The Romak Keyboard Layout

**Romak** is a keyboard layout built for Portuguese and English users, with a goal to enhance hand alternation, minimize finger movement, reduce single-finger bigrams, and decrease reliance on the pinky and central columns.

For the regular versions of Romak, including performance analysis, check [this other page](README.md) instead.

## Magic Romak

This is a version of Romak 24 that uses [Magic Keys](https://github.com/Ikcelaks/keyboard_layouts/blob/main/magic_sturdy/magic_sturdy.md) to improve the typing experience.

Alpha 1 layer:

```
     B  M  G          L  O  U   
  D  N  S  T          R  A  E  I 
     F  C  P          *  ,  .   
           ®  Sp   A2 Sf
```

Alpha 2 layer:

```
     Q  Qu K          Ô  Ó  Ú
  Y  Z  X  W          Ã  Á  É  Í
     J  Ç  ^          Õ  Â  Ê
           '  _    _  '
```
```
® = Repeat Key
* = Magic Key
^ = Reversed Magic Key
Sp = Space
A2 = One Shot Alpha 2
Sf = One Shot Shift
```

### Magic Key

The Magic Key will produce H after consonants and V after vowels.

This is how the **Magic Key** behaves:

| Previous Keys | Output  | 
|---|---|
| Consonants | V |
| &blank; | H |
| OS &#8679; | H |
| Anything Else | H |

### Reversed Magic Key

The Reversed Magic Key does the opposite as the Magic Key, producing V after consonants and H after vowels..

This is how the **Reversed Magic Key** behaves:

| Previous Keys | Output  | 
|---|---|
| Consonants | H |
| &blank; | V |
| OS &#8679; | V |
| Anything Else | V |

### Repeat Key

Usually the Repeat Key will simply repeat the last character, but in some cases an alternate repeat can be used.

This is how the **Repeat Key** behaves:

| Previous Key | Output  |
|---|---|
| H | A |
| A | H |
| Y | D |
| X | Y |
| J | Á |
| QU | Ê |
| ÁÉÓ | X |
| ÍÚ | V |
| Ê | . |
| Ô | L |
| Ã | O |
| Õ | E |
| Ç | OS Alpha 2 |  
| ' | V |
| &#8679; I | ' |
| Anything Else | Repeat |

## Implementation

A complete implementation for Magic Romak can be found [here](https://github.com/rafaelromao/keyboards).
