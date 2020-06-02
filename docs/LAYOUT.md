# Design layout

```
  ________________________________
 |              tb                |    Macbook Screen Size
 |  rbr                           |     [1, 1, 1440, 900]
 |                                |
 |                                |
 |                                |
 |    ew                  ow      | h = 900
 |                                |
 |                                |
 |                                |
 |________________________________|
 ^             w = 1440
(x=1,y=1)
```

```matlab
screen_size = get(groot, "ScreenSize");
```
 gathers the information regarding the screen size, in the form of a 1-by-4 array, `[x y width height]`.
`x` & `y` are equal to `1` and are related to the position.

Element positions:
-----------------

| Element Name       | Nickname |  Position                        |
| ------------------ | -------- | -------------------------------- |
| Toolbar            | (`tb`)   | [`tb1`  `tb2`  `tb3`  `tb4`]     |
| Run button ribbon  | (`rbr`)  | [`rbr1` `rbr2` `rbr3` `rbr4`]    |
| Editor window      | (`ew`)   | [`ew1`  `ew2`  `ew3`  `ew4`]     |
| Output window      | (`ow`)   | [`ow1`  `ow2`  `ow3`  `ow4`]     |
