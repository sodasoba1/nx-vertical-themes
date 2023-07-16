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


How to extract & patch controller.szs & common.szs
--------------------------------------------------

[1] Goldleaf : Manage console contents > NAND SYSTEM > 0100000000001003 > Export > YES

NSP Located in SDMC:/switch/Goldleaf/export/title

[2] move nsp into same folder as nstool or hactool on PC
                  ----           ------    -------

open cmd and extract via the commans

nstool.exe -x pfs0 0100000000001003.nsp
the above command extracts the NCA

then use nstool again to extract the SZS

nstool.exe -x romfs pfs0/477aa65a2473e44e9adc968bd02d9759.nca
the SZS will be located in romfs/1/lyt


Now apply the json 'theme' Controller.szs & common.szs
------------------------------------------------------

Open Controller.szs in SwitchLayoutEditor click Tools > Load JSON patch
load controller.json save the .szs

Open common.szs in SwitchLayoutEditor click Tools > Load JSON patch
load common.json save the .szs

COPY both patched szs to : SDMC:/atmosphere/contents/0100000000001003/romfs/lyt

if the patched SZS don't load make a empty file called: fsmitm.flag and place it in atmosphere/contents/0100000000001003/