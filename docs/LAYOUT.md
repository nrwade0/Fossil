# UI Design layout

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

Startup function initializes the UI to the full screen using,

```matlab
screen_size = get(groot, "ScreenSize"); % a.k.a. 'ss'
```
in the form of a 1-by-4 array, `[x y width height]`.
`x` & `y` are equal to `1` and are related to the *position*.

-----------------

## Element positions:


### Main elements:

| Element Name       | Nickname |  Position (`[x y width height]`)   |
| ------------------ | -------- | ---------------------------------- |
| Toolbar            | (`TB`)   | `TB position set automatically`    |
| Left Panel         | (`LP`)   | `[1  1  ss(3)/2  ss(4)-118]`       |
| Right Panel        | (`RP`)   | `[ss(3)/2  1  ss(3)/2  ss(4)-118]` |


### Panel elements:


Panels act as containers for multiple UI objects. In that way, panel element coordinates (x, y) are centered on the bottom left of the panels, not the entire UI. For instance, the Editor panes coordinates (x<sub>EP</sub> = 10, y<sub>EP</sub> = 10) are in relation to the left panels coordinates (x<sub>LP</sub>, y<sub>LP</sub>). A simple translation can be used to determine the objects coordinates in relation to the UI (x<sub>UI</sub> = x<sub>EP</sub> + x<sub>LP</sub>, y<sub>UI</sub> = y<sub>EP</sub> + y<sub>LP</sub>).

As of version 0.9, most positional values are arbitrary to the leading computer. Will be update later will variable values.

#### Left:

| Element Name       | Nickname |  Position (`[x y width height]`)   |
| ------------------ | -------- | ---------------------------------- |
| Editor Pane        | (`EP`)   | `[10 10 ss(3)/2-20, ss(4)-170]`    |


#### Right:

| Element Name        | Nickname |  Position (`[x y width height]`)  |
| ------------------- | -------- | --------------------------------- |
| Tab Group (2 total) | (`TG`)   | `[10 10 ss(3)/2-20 ss(4)-170]`    |
| Tab 1 (T1)- RUN btn | (`RB`)   | `[20 ss(4)-200 80 30]`            |
| T1 - Output Pane    | (`OP`)   | `[20 20 ss(3)/2-60 ss(4)-230]`    |
| T1 - Program Name   | (`PN`)   | `[240 ss(4)-200 120 30]`          |
| T1 - Prgrm Name Txt | (`PNt`)  | `[110 ss(4)-200 120 30]`          |
| T2 - Syntax Pane    | (`SP`)   | `[20 20 ss(3)/2-60 ss(4)-230]`    |
| T2 - CHECKSYNTAX btn| (`CSB`)  | `[20 ss(4)-200 160 30]`           |

<sup> Note that Tab # -> T# </sup>
