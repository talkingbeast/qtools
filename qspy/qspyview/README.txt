About this Directory====================This directory contains the Tcl/Tk scripts that implement the "QSPYview"
front-end to the QSPY software tracing "back-end" utility.


Usage 
=====
The scripts require Tcl/Tk 8.4 with the UDP extension, which is available
in the Qtools collection for Windows (version 5.5.0 and newer).

To launch the "QSPYview", you need to first run the QSPY utility (5.5.0+)
with the -u option. Once QSPY is running, you open the QSPYview script by
running the wish interpreter on the qspyview.tcl script:

wish qspyview.tcl

When executed without additional parameters, the script uses the default.tcl
extension that provides empty placeholders for all QS trace records and
commands that you can receive from and send to the QS Target component.


Customizing QSPYview
====================
The qspyview.tcl script provides also a basic mechanism to customize the
behavior for specific projects. To customize the behavior you need to copy
and modify the default.tcl script. The modified script should be renamed
to the specific project and used as an additional command parameter to the
qspyview.tcl script. For example, the directory

<qpc>\examples\arm-cm\dpp_ek-tm4c123gxl\qspy

contains the customization dpp.tcl, which handles specific QS records
generated by the dpp example application for the EK-TM4C123GXL board.
To launch this example, change to the directory just mentioned and type

wish qspyview.tcl dpp.tcl


Headless QSPY Front-Ends
========================
The provided Tcl scripts allow you also to develop "headless" scripts
(no GUI) to drive testing of the Target. The script qspy.tcl encapsulates
the basic communication protocol with the QSPY back-end. Based on this
functionality, you can write your own Tcl scripts to exercise the Target.


More Information
================
More information about the QS/QSPY software tracing system is available
online at:

http://www.state-machine.com/qspy/
