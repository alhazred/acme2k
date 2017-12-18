# [acme](http://acme.cat-v.org/)


**_Q:_** so what's an acme?

**_A:_** and if thou gaze long into an abyss, the abyss will also gaze into thee.

**_Q:_** let me act as a mediator between me, the actual riddler here and thee.

**_A:_** thy will be done or w/e... ...

**_Q:_** what he is saying that acme is in fact an anvil just like from roadrunner and et cetera.

**_Q:_** oh let me get this one.

**_Q:_** so am i supposed to edit text with an anvil?

**_A:_** you bet your ass it is, but unlike `emacs` in this allegory of sorts, it's not heavy. it is, though,

### ACME INTERNATIONAL COMPILED EDITORS

#### THEY EDIT LIKE HELL.
```
   No editor made, pretty much anywhere,

surpasses our Acme in shape, material or finish.
```
solid forged of unsigned int pieces of best wrought C, linked at the binary; tag line is made of one

piece of code, compiled with -funroll-loops to the the rest of the window column and warranted 

with a [permissive license](https://raw.githubusercontent.com/9fans/plan9port/master/LICENSE). text window has sufficient refactoring done to insure stability and 

prevent SEGFAULTing; has ug, but perfectly written shell: [rc](http://doc.cat-v.org/plan_9/4th_edition/papers/rc); acme is linted and debugged by a 

special compiler so that there are no functions that return structures or integer and floating 

numbers in object code not converted to known formats and byte orders; [config.h](https://github.com/karahobny/acmecolors/blob/master/acme/config.h) should be perfectly 

tempered by the user or it will fuck up. mkfiles are straight and true, so you will have no trouble 

on account of acme returning zero or not compiling.

# brass tacks (the serious business)

**acme2k** depends on `plan9port` which can be found [here on github](https://github.com/9fans/plan9port) or on your local repository. i know debian has stripped plan9 userpace called `9base` but i wouldn't roll my dice with this working wth it. don't know haven't a clue, now's yer chance to feel useful.


after following the instructions in your `$PLAN9`-folder to run `./INSTALL` and `mk`'ing every goddamn plan9 userspace application there happens to be ported, you can move right on to mangle it with this godawfulness:


just copy `acme`-folder to your `$PLAN9/src/cmd` replacing the existing `acme`-folder. ie.:

```bash
      cp -r acme /usr/lib64/plan9/src/cmd/
```

you may need to build from the `INSTALL`-file located in the `$PLAN9`-root, but usually its enough to build from

```bash
      cd $PLAN9/src/cmd/acme; mk install
```


## config.h
`config.h` includes all the neccesary color and font modifications you just need to `mk install` it after every time you modify it, suckless style. `fontsrv -p .` to list all the available fonts and then use them like `"/mnt/font/*listed font*/*font size**a or no a depending if you want antialiasing or not*/font"` ie.
    `"/mnt/font/Monaco/9a/font"`
would stand for Monaco size 9 antialised.

## colors
colors need to be in the format of `0x*rgb hex color code*FF` without the prefixed hashtag. i'd suggest just to experiment what all the #defines mean but to start you with something `c_tagbg` means tag window background color. `c_txtbg` means text window backgorund color. `...hlbg/fg` means highlighted text background and foreground color etc.

## example looks

![configuration nro1](https://raw.githubusercontent.com/karahobny/acmecolors/master/acme1.png)

![configuration nro2](https://raw.githubusercontent.com/karahobny/acmecolors/master/acme3.png)
