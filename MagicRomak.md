# The Romak Keyboard Layout

**Romak** is a keyboard layout built for Portuguese and English users, with a goal to enhance hand alternation, minimize finger movement, reduce single-finger bigrams, and decrease reliance on the pinky and central columns.

For the regular versions of Romak, including performance analysis, check [this other page](README.md) instead.

## Magic Romak

This is a version of Romak 24 that uses [Magic Keys](https://github.com/Ikcelaks/keyboard_layouts/blob/main/magic_sturdy/magic_sturdy.md) to improve the typing experience, reducing SFBs and consecutive activations of the secondary alpha layer.

This Magic Key replaces the regular H key from the standard Romak 24. It will still type H by default, but will also produce V or Y in some cases where H is not the most useful output. For consonants in the secondary alpha layer, this Magic Key will simply reactivate the secondary alpha layer for a second shot.

To cope with the cases where an H is required but the Magic Key would produce something else, H also appears in the secondary alpha layer, in the outer left thumb key.

Alpha 1 layer:

```
     B  M  G          L  O  U   
  D  N  S  T          R  A  E  I 
     F  C  P          *  ,  .   
           ®  Sp   A2 Sf
```

Alpha 2 layer:

```
     Q  Qu K          Ô  Ê  Â
  Y  Z  X  W          Ã  É  Á  Í
     J  Ç  V          Õ  Ó  Ú
           H  _    _  '
```
```
® = Repeat Key
* = Magic Key
Sp = Space
A2 = One Shot Alpha 2
Sf = One Shot Shift
```

### Magic Key

The Magic Key will produce H after most consonants, V after vowels and Y after consonants that are not usually followed by H. For consonants in the secondary alpha layer, except for W, it will reactivate the secondary alpha layer.

This is how the **Magic Key** behaves:

| Previous Keys | Output  | 
|---|---|
| Vowels | V
| BMDF | Y |
| YQZJQuXÇKVH | OS Alpha 2 |
| . | / |
| &blank; | H |
| OS &#8679; | H |
| Anything Else | H |

### Repeat Key

Usually the Repeat Key will simply repeat the last character, but in some cases an alternate repeat can be used.

This is how the **Repeat Key** behaves:

| Previous Key | Output  |
|---|---|
| H | A |
| A | H |
| Qu | Ê |
| Ç | OS Alpha 2 |  
| ' | V |
| &#8679; I | ' |
| Anything Else | Repeat | 

### Reversed Magic Key

The Reversed Magic Key is a simpler adaptive key that replaces the dedicated key for V.
- This adaptive key will type V by default and H after vowels. It will make typing words like `behave` and `behind` much easier, although increasing the cognitive load a bit more.
- There is no dedicated key for V in this case, but it can always be typed with either the Reversed Magic Key or the regular Magic Key.
- Since there are some cases for which neither the Magic Key or the Reversed Magic Key will produce an H, the dedicated key for H in the thumb is still present, although rarely necessary.

Alpha 1 layer:

```
     B  M  G          L  O  U   
  D  N  S  T          R  A  E  I 
     F  C  P          *  ,  .   
           ®  Sp   A2 Sf
```

Alpha 2 layer:

```
     Q  Qu K          Ô  Ê  Â
  Y  Z  X  W          Ã  É  Á  Í
     J  Ç  √          Õ  Ó  Ú
           H  _    _  '
```
```
® = Repeat Key
* = Magic Key
√ = Reversed Magic Key
Sp = Space
A2 = One Shot Alpha 2
Sf = One Shot Shift
```
This is how the **Reversed Magic Key** behaves:

| Previous Keys | Output  | 
|---|---|
| Consonants | H |
| &blank; | V |
| OS &#8679; | V |
| Anything Else | V |

## Implementation

A complete implementation for Magic Romak can be found [here](https://github.com/rafaelromao/keyboards).
