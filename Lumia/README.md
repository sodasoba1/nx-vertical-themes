Lumia-Vertical-Theme
Made for HOS14+

![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/home.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/allapps.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/groups.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/lock.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/pls.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/psl-archadearchives.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/settings.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/news.jpg>)


Extra screen shots
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/add-remove.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/close-app.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/Controller00.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/Controller01.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/Controller02.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/Controller03.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/Controller04.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/Controller05.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/remap-joy.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/remap-joy2.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/remap-joy3.jpg>)

![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/lock.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/lock2.jpg>)

![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/MyPage-comm-set-patched.jpg>)

![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/psl-common-patch.jpg>)



![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/settings-extra.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/settings-internet.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/sortandfilter.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/sort-groups.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/sortsoftware.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/ser.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/data.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/data2.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/data3.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/data-select.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/data-select2.jpg>)
![csv1](<https://github.com/sodasoba1/nx-vertical-themes/raw/master/Lumia/Preview/extra/test-touch.jpg>)



EXTRAS (advanced themeing) :


[how to & OptionPatch json](https://sodasoba1.github.io/layouteditor-patch/)

[Guide for extracting szs](<https://layoutdocs.themezer.net/guide/manualszs/>)

[SwitchLayoutEditor](<https://github.com/FuryBaguette/SwitchLayoutEditor/>)

[Golfleaf for switch](<https://github.com/XorTroll/Goldleaf>)

[nstool](<https://github.com/jakcron/nstool/>)

using nstool or hactool (console keys maybe required)


How to extract & patch controller.szs & common.szs
--------------------------------------------------

[1] Goldleaf : Manage console contents > NAND SYSTEM > 0100000000001003 > Export > YES

NSP Located in SDMC:/switch/Goldleaf/export/title

[2] move nsp into same folder as nstool or hactool on PC


open cmd and extract via the commans

`nstool.exe -x pfs0 0100000000001003.nsp`

the above command extracts the NCA

then use nstool again to extract the SZS

`nstool.exe -x romfs pfs0/477aa65a2473e44e9adc968bd02d9759.nca`

the SZS will be located in `romfs/1/lyt`


How to apply the json 'theme' Controller.szs & common.szs
------------------------------------------------------

Open Controller.szs in *SwitchLayoutEditor* click **Tools** > **Load JSON patch**
load `controller.json` **save** the .szs

Open common.szs in *SwitchLayoutEditor* click **Tools** > **Load JSON patch**
load `common.json` save the .szs

COPY both patched szs to : `SDMC:/atmosphere/contents/0100000000001003/romfs/lyt`

if the patched SZS *don't load* make a *empty file* called: `fsmitm.flag` and place it in atmosphere/contents/0100000000001003/