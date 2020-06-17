# Change log


------
## Version 0.9.1
June 21, 2020

#### New/Changed Features
- ...

#### Bugs Fixed
- ...


------
## Version 0.9
June 9, 2020

#### New/Changed Features
- Added a `CHECK SYNTAX` button on right panel, isolated that process from the `RUN` button.
- Added a simple `PROGRAM NAME` field. Automatically takes this text and makes the file for that name. `PROGRAM file_name` & `END PROGRAM file_name` must equal this text value.
- Added LaTex formatting in `ABOUT` menu; now allows font change, hyperlinking, and equation writing, but nothing done with this yet.
- Changed `prism.js` & `prism.css` -> `fortran.js` & `fortran.css` respectively, in anticipation of added programming languages.
- Added `output.html` & `output.css` to format the output of the compile process. Also added `def_output.html` & `def_syntax.html` which are basic start-up menus for output/syntax panes.
- Now records and displays a output history in the output pane. Stores all previous outputs until relaunch and displays above the most recent (with timestamps).
- Updated `LAYOUT.md` and add the arbitrary positioning data used to design the GUI. Added information regarding the re-zeroing of coordinates on each respective pane.

#### Bugs Fixed
- N/A


------
## Version 0.8
June 1, 2020

#### New/Changed Features
- Added a working editor and output window.
- Compiles and outputs on push of RUN button.

#### Bugs Fixed
- N/A
