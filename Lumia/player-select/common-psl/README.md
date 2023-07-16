Guide for manual patching
-------------------------
https://layoutdocs.themezer.net/guide/manualszs/


info on pfs0
------------
https://switchbrew.org/wiki/NCA#PFS0


SwitchLayoutEditor
------------------
https://github.com/FuryBaguette/SwitchLayoutEditor

Golfleaf for switch
-------------------
https://github.com/XorTroll/Goldleaf


nstool
------
https://github.com/jakcron/nstool

with nstool or hactool (console keys maybe required)


How to extract & patch psl common.szs
--------------------------------------------------

[1] Goldleaf : Manage console contents > NAND SYSTEM > 0100000000001007 > Export > YES

NSP Located in SDMC:/switch/Goldleaf/export/title

[2] move nsp into same folder as nstool or hactool on PC
                  ----           ------    -------

open cmd and extract via the commans

nstool.exe -x pfs0 0100000000001007.nsp
the above command extracts the NCA stringoflettersandnumbers.NCA

then use nstool again to extract the SZS

nstool.exe -x romfs pfs0/stringoflettersandnumbers.NCA
the SZS will be located in romfs/1/lyt


Now apply the json 'theme' common.szs
------------------------------------------------------

Open common.szs in SwitchLayoutEditor click Tools > Load JSON patch
load common.json save the .szs

COPY patched szs to : SDMC:/atmosphere/contents/0100000000001007/romfs/lyt

if the patched SZS don't load make just delete romfs_metadata.bin from atmosphere/contents/0100000000001007/
and reboot