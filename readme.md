# Xellum QMK keyboard layout

## Inspiration

- [Callum](https://github.com/callum-oakley/qmk_firmware/tree/master/users/callum)
- [Wellum](https://github.com/braindefender/wellum)
- [Miryoku](https://github.com/manna-harbour/miryoku)
- [Dreymar's Extend layer](https://dreymar.colemak.org/layers-extend.html)
- [Engram 3x5 mod](https://github.com/shnarazk/engram/tree/extensions/mod-3x5)
- [Раскладка Ильи Шепрута](https://optozorax.github.io/p/my-keyboard-layout/)
- [Pascal Getreuer's layout](https://github.com/getreuer/qmk-keymap) and his ["Designing Symbol Layer"](https://getreuer.info/posts/keyboards/symbol-layer/index.html)
- [T-34 keyboard layout](https://www.jonashietala.se/blog/2021/06/03/the-t-34-keyboard-layout/)
- [Ergohaven default layouts](https://ergohaven.xyz)
- [Beakl proposed layers](http://ieants.cc/beakl/?i=3)
- [Beakl z](http://thedarnedestthing.com/beakl%20zi%20revisited)

Also, I use two layouts: [Colemak-dh](https://colemakmods.github.io/mod-dh/) for English and national (Russian), and it leads to the following challenges:

- Language switching button should also toggle layers (implemented [here](https://github.com/xelorr/xellum/blob/vial/keyboards/ergohaven/ergohaven_ruen.c#L20-L38) as layer_invert(1))
- Ctrl-xcv are differently placed for different layouts (solved by placing ^x ^c ^v on mouse layer)
- As there are 33 letters and one special symbol (№) in russian, totalling 34 buttons required for symbols only and without punctuation (decided to have ёхъ,. in symbol layer and э to replace russian dot)

## Layers

<details>

<summary>Key voc</summary>

| abbr     | key symbol | key name                                         |
| -------- | ---------- | ------------------------------------------------ |
| ◇        |            | Holding to keep layer activated                  |
| S        | ⇧          | OSM or OSSM Shift                                |
| C        | ⌃          | OSM or OSSM Control                              |
| A        | ⌥          | OSM or OSSM Alt                                  |
| G        | ⌘          | OSM or OSSM Gui                                  |
| LS       | ⇧          | Regular (non-sticky) Left Shift                  |
| LC       | ⌃          | Regular (non-sticky) Left Control                |
| LA       | ⌥          | Regular (non-sticky) Left Alt/Option             |
| LG       | ⌘          | Regular (non-sticky) Left Gui/Super/Win/Command  |
| RS       | ⇧          | Regular (non-sticky) Right Shift                 |
| RC       | ⌃          | Regular (non-sticky) Right Control               |
| RA       | ⌥          | Regular (non-sticky) AltGr                       |
| RG       | ⌘          | Regular (non-sticky) Right Gui/Super/Win/Command |
| __       |            | nothing/transition to previous layer             |
| E        | ⎋          | Escape                                           |
| N        | ↵          | Enter                                            |
| T        | ⇥          | Tab                                              |
| P        |            | Print Screen                                     |
| sp       | ␣          | Space                                            |
| bs       | ⌫          | Backspace                                        |
| dl       | ⌦          | Delete                                           |
| ap       |            | App/Menu                                         |
| U        | ↑          | Up                                               |
| D        | ↓          | Down                                             |
| L        | ←          | Left                                             |
| R        | →          | Right                                            |
| ed       | ↘          | End                                              |
| hm       | ↖          | Home                                             |
| pd       | ⇟          | Page Down                                        |
| pu       | ⇞          | Page Up                                          |
| lb       |            | Left mouse button / button 1                     |
| rb       |            | Right mouse button / button 2                    |
| mb       |            | Miggle mouse button / button 3                   |
| mu       |            | Mouse cursor up                                  |
| md       |            | Mouse cursor down                                |
| ml       |            | Mouse cursor left                                |
| mr       |            | Mouse cursor right                               |
| wu       |            | Mouse wheel up                                   |
| wd       |            | Mouse wheel down                                 |
| wl       |            | Mouse wheel left                                 |
| wr       |            | Mouse wheel right                                |
| Wu       |            | Focus up window                                  |
| Wd       |            | Focus down window                                |
| Wl       |            | Focus left window                                |
| Wr       |            | Focus right window                               |
| Wc       |            | Vim window close                                 |
| Wh       |            | Window split horisontally                        |
| Wv       |            | Window split vertcally                           |
| nl       |            | Num Lock                                         |
| sl       |            | Scroll Lock                                      |
| cl       | ⇪          | Caps Lock                                        |
| cw       | ⇪          | Caps Word                                        |
| lw       |            | RuEn Word                                        |
| lg       |            | Language toggle                                  |
| en       |            | Language set English                             |
| ru       |            | Language set Russian                             |
| pa       |            | Pause/Break                                      |
| rm       |            | Record macro                                     |
| pm       |            | Play recorded macro                              |
| sm       |            | Stop recording macro                             |
| st       |            | Switch Tab (sticky Ctrl-tab)                     |
| sw       |            | Switch Window (sticky Alt-tab or Command-tab)    |
| pt       |            | Previous tab                                     |
| nt       |            | Next tab                                         |
| ns       |            | Next space                                       |
| ps       |            | Prev space                                       |
| qt       |            | Close tab                                        |
| qw       |            | Close window                                     |
| pl       |            | Media play                                       |
| tp       |            | Media stop                                       |
| mp       |            | Media prev                                       |
| mn       |            | Media next                                       |
| vu       |            | Volume up                                        |
| vd       |            | Volume down                                      |
| mt       |            | Mute                                             |
| ^c       |            | Copy                                             |
| ^v       |            | Paste                                            |
| ^x       |            | Cut                                              |
| ^z       |            | Undo                                             |
|  EN      |            | English alphas layer                             |
|  RU      |            | Russian alphas layer                             |
|  NV      |            | navigation layer                                 |
|  MS      |            | mouse/cursor layer                               |
|  SY      |            | symbol later                                     |
|  MC      |            | macro/launcher layer                             |
|  BU      |            | button layer                                     |
|  NU      |            | numbers layer                                    |
|  ME      |            | media layer                                      |
|  FN      |            | F-row/function layer                             |
|  GM      |            | Gaming layer                                     |
|  GF      |            | Function layer for Gaming layer                  |
|  AL      |            | Alt symbol layer                                 |

</details>

<details>

<summary>Effort grids</summary>

[Ergohaven](https://ergohaven.xyz/) [K03](https://ergohaven.xyz/k03)
```
 5  5  4  3  4  6          6  4  3  4  5  5
 4  3  3  2  2  4          4  2  2  3  3  4
 2  1  0  0  0  2          2  0  0  0  1  2
 3  3  2  2  1  4  6    6  4  1  2  2  3  3
       4  4  3  0  1    1  0  3  4  4
```

</details>

It is mostly [Miryoku](https://github.com/manna-harbour/miryoku/tree/master/docs/reference), but with following additions:

- separate RU layer with corresponding symbol layer
- separate gaming layer
- extra russian letters and punctuation placrment on Sym and Num layers
- unicode symbol layer
- macro layer
- active use of [RuEn](https://github.com/ergohaven/vial-qmk/blob/vial/keyboards/ergohaven/docs/ruen.md) functionality
- i prefer inverted t in most cases

EN (LTs: E/ME, sp/NV, T/MS, N/SY, bs/NY, dl/FN, Mod-taps: GACS on home row)
```
q  w  f  p  b          j  l  u  y  '
a  r  s  t  g          m  n  e  i  o
z  x  c  d  v          k  h  ,  .  /
         E sp  T    N bs dl
```

RU (LTs: E/ME, sp/NV, T/MS, N/SY, bs/NY, dl/FN, Mod-taps: GACS on home row)
```
й  ц  у  к  е          н  г  ш  щ  з
ф  ы  в  а  п          р  о  л  д  ж
я  ч  с  м  и          т  ь  б  ю  э
         E sp  T    N bs dl
```

NU
```
[  7  8  9  ]                  AL   
;  4  5  6  =            LS LC LA LG
`  1  2  3  \            MC GM RA   
         .  0  -       ◇   
```

SY (EN)
```
{  &  *  ?  }                  AL   
:  $  %  ^  +            LS LC LA LG
~  !  @  #  |            MC GM RA   
         (  )  _    ◇       
```

SY (RU)
```
Х  .  *  ?  Ъ                  AL   
:  $  %  ,  +            LS LC LA LG
Ё  !  "  #  |            MC GM RA   
         (  )  _    ◇       
```

FN
```
F12 F7 F8 F9  P                  AL   
F11 F4 F5 F6 sl            LS LC LA LG
F10 F1 F2 F3               MC GM RA   
          ap sp  T          ◇
```

NV
```
   AL                     hm  U ed pu
LG LA LC LS            cl  L  D  R pd
   RA GM MC               cw lw      
                ◇   FN lb RA
```

MS
```
   AL                    wl mu wr wu
LG LA LC LS              ml md mr wd
   RA GM MC           ^y ^v ^c ^x ^z 
                   rb lb mb
```

GM (LTs: P/FN)
```
T  q  w  e  r                U     T
S  a  s  d  f             L  D  R  S
C  z  x  c  v                      C
        LA sp GF   EN sp  P
```

GF (LTs: bs/NU)
```
E  7  8  9  j         mr   
cl 4  5  6  i         ms   
g  1  2  3  m         mp   
        ME  N  ◇      bs
```

ME
```
   AL                       vu      
LG LA LC LS              mp vd mn   
   RA GM MC                          
                   tp pl mt
```

BU
```
^z ^x ^c ^v ^y        ^y ^v ^c ^x ^z
LG LA LC LS              RS RC RA RG
^z ^x ^c ^v ^y        ^y ^v ^c ^x ^z 
         mb lb rb  rb lb mb
```

MC
```
M0 M1 M2 M3 M4         M5 M6 M7 M8 M9 
10 11 12 13 14         15 16 17 18 10 
20 21 22 23 24         25 26 27 28 20 
```

AL
```
 ⎋  ₹  φ  §  ₿          ≈  λ  ∞  ¥  ⌘
 α  ₽  Σ  ±  ❖          μ  №  €  ➔  ⌥
 •  ×  ©  °  ✓          ⌨  ⌗  «  »  ⇧
```

There are no language togglers here.
Just set `LG_TOGGLE` or `LG_SET_EN`/`LG_SET_RU` as combo. It will also toggle layers on language switch.

## Current version

- [Ergohaven](https://ergohaven.xyz/) [K03](https://ergohaven.xyz/k03): [keymap](./keyboards/ergohaven/k03/keymaps/miryoku/keymap.c), precompiled [firmware](https://github.com/XelorR/xellum/releases/download/latest/ergohaven_k03_rev1_miryoku.uf2)

<details>

<summary>Experimental layers</summary>

```
q  w  f  p  b          j  l  u  y  '
a  r  s  t  g          m  n  e  i  o
z  x  c  d  v          k  h  ,  .  /
         E sp  T    N bs dl
```

NU
```
!  7  8  9  %                  AL   
,  4  5  6  .            LS LC LA LG
?  1  2  3  ^            MC GM RA   
         .  0  \       ◇   
```

SY (EN)
```
@  <  =  >  `                  AL   
:  (  -  )  *            LS LC LA LG
~  [  ;  ]  #            MC GM RA   
         &  $  /    ◇       
```

</details>
