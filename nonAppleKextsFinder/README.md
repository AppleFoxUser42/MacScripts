#Non-Apple Kernel Extension (.kext) finder
This script utilises Apples ``kextfind`` Command to list .kext's.

Although it's called with ``kextfind -not -b -is com.apple.`` the command as-is would still show 10 items belonging to OSX. 
For this reason the script also utilises the following filterlist
* /Library/Extensions/ACS6x.kext
* /Library/Extensions/ArcMSR.kext
* /Library/Extensions/ATTOCelerityFC8.kext
* /Library/Extensions/ATTOExpressSASHBA2.kext
* /Library/Extensions/ATTOExpressSASRAID2.kext
* /Library/Extensions/CalDigitHDProDrv.kext
* /Library/Extensions/HighPointIOP.kext
* /Library/Extensions/HighPointRR.kext
* /Library/Extensions/PromiseSTEX.kext
* /Library/Extensions/SoftRAID.kext

Additional calling it with -nl executes ``kextfind -nl -or -w  -not -b -is com.apple.`` which shows all non-Apple .kext's which are not loaded.

This script is commandline only. call it from terminal with ``./nonAppleKextFinder`` or ``./nonAppleKextFinder -nl``
