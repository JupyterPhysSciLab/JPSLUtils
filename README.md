## JPSLUtils
(aka Jupyter Physical Science Lab Utilities)

#### Introduction
These are utilities used by multiple packages within the [Jupyter Physical
Science Lab project](https://github.com/JupyterPhysSciLab). It is unlikely 
that anyone but a developer would
have reason to install these independently. They are installed when
required by other packages/modules.

#### Contents
* This package mostly provides tools for running javascript operations that
impact the notebook. This includes things such as selecting a certain cell,
inserting text into an existing cell, or running python code and using the
result from javascript. Some custom dialogs for user interaction are also
included.
* `JPSL Tools` menu is installed as well. This provides menu access to some
of the javascript operations:
    * __Hide cells__ that are marked as `hide_on_print` in the cell metadata.
    This metadata can be set from a menu provided by the 
      [jupyter-instructortools](https://github.com/JupyterPhysSciLab/jupyter-instructortools)
      package. The meta-data can also be set manually, by editing it in the
      notebook.
    * __De-hide cells__ marked as `hide_on_print` in the cell metadata.

#### Change Log
  * 0.5.5 added `JPSL Tools` menu to access cell hiding.
  * 0.5.4 added cell hiding toggle, which cells to hide chosen with instructor 
    tools.
  * 0.5.3 add `select_containing_cell` and 
    `insert_text_at_beginning_of_current_cell` to JS routines. Add python calls
    `havenp()` to check for `numpy as np` and `havepd()`
    to check for `pandas as pd`  in user name space.
  * 0.5.2 Minor bug fixes and updates to README.
  * 0.5.1 Introduced "one time Javascript" (`OTJS(...)`) alternative to 
    `display(JS(...))`. This allows javascript calls from python that will 
    not be run the next time the notebook is opened and trusted.
  * 0.5.0 Initial release.

##### [This software is distributed under the GNU V3 license](https://gnu.org/licenses)
This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.
    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

Copyright - Jonathan Gutow, 2021.