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
* `JPSL Tools` menu can be installed as well. The command to activate it 
  from python is `JPSL_Tools_Menu():`; from javascript 
 `JPSLUtils.createJPSLToolsMenu(); JPSLUtils.init();`. This provides menu 
  access to some of the javascript operations:
    * __Hide cells__ that are marked as `JPSL.hide_on_print=true` in the cell 
      metadata.
    This metadata can be set from a menu provided by the 
      [jupyter-instructortools](https://github.com/JupyterPhysSciLab/jupyter-instructortools)
      package. The meta-data can also be set manually, by editing it in the
      notebook.
    * __De-hide cells__ marked as `hide_on_print` in the cell metadata.
    * __Hide/Show__ input table creation code.
    * __Hide/Show__ code marked as hidden. Set using
    [jupyter-instructortools](https://github.com/JupyterPhysSciLab/jupyter-instructortools).
    * __Snippets for initializing some JPSL components and links to their
      documentation__ (JupyterPiDAQ, Jupyter Pandas GUI and Algebra with Sympy)
* __NOTE__: if you wish input table creation code and selected code cells 
  hidden without the menu being available, then you need to issue the command 
  `OTJS('JPSLUtils.init();')` in python or just `JPSLUtils.init();` in 
  javascript.

#### Change Log
  * 0.6.0rc
    * Python cell actions no longer run when a trusted notebook is opened 
      (using `OTJS
      ()`).
    * Reformatted the user name and partner information saved on each 
      initialization.
  * 0.5.9
    * Switch to using hierarchical menus.
    * Now requires JPSLMenus package.
  * 0.5.8
    * additional insert text and selection utilities
  * 0.5.7
    * __Breaking change__: JPSL Tools menu is not automatically activated when
      this package is imported. It now must be activated by an explicit call to
      `JPSLUtils.JPSL_Tools_Menu()`.
    * Can now have package hide table creation code and selected code cells 
      without the menu showing. The call is `OTJS('JPSLUtils.init();')`
  * 0.5.6
    * added `hide/show` input table creation code.
    * added `hide/show` hidden code.
    * initialization now hides input table creation code.
    * initialization now hides code marked for hiding.
  * 0.5.5 
    * added `JPSL Tools` menu to access cell hiding.
    * record name dialog cannot be cancelled.
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

Copyright - Jonathan Gutow, 2021, 2022.