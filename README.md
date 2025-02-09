# SAO_Pin

This is where all the files for SAO_Pin will be stored.

This includes code and art and cad and fab files.  All the things.

## File Structure

This is the file structure of this repository

* [/](/README.md) - YOU ARE HERE
* [/art/](./art/) - Artwork and other graphics created by this project
  * [/art/inspiration/](./art/inspiration/) - Art and graphics pulled from other sources used as inspiration for this project
  * [/art/fonts/](./art/fonts/) - Fonts used in art and graphics
* [/code/](./code/) - All project related Code / Firmware
* [/docs/](./docs/) - Documentation created by this project including web pages
* [/eda/](./eda/) - Electronic Design Automation files (i.e. KiCad)
  * [/eda/SAO_Pin/](./eda/SAO_Pin/) - KiCad 7.x project folder for the SAO_Pin PCB
* [/reference_parts/](./reference_parts/) - Submodule of Third Party Documentation related to components
* [./README.md](/README.md) - This File
* [./LICENSE](/LICENSE) - Currently set to MIT

Note: the reference_parts directory is a link to a submodule repository.
To add it use the following cmd after cloning this:
```
git submodule add https://github.com/gowenrw/reference_parts reference_parts
```
This will make a link to the current commit of that repo.
To update it to a newer commit after its been added use this cmd:
```
git submodule update --init --recursive
```

## PCB_Project_Template

Notes on use: 

* First replace all references to SAO_Pin in this document to whatever your project name is.

* Next fix up the KiCad project folder which references a name TEMPLATEPCB to replace both its filename references as well as references inside those files using sed like so (linux/windows-bash):
```bash
mv eda/TEMPLATEPCB eda/SAO_Pin
cat eda/SAO_Pin/TEMPLATEPCB.kicad_pro | sed s/TEMPLATEPCB/SAO_Pin/g >eda/SAO_Pin/SAO_Pin.kicad_pro
rm eda/SAO_Pin/TEMPLATEPCB.kicad_pro
cat eda/SAO_Pin/TEMPLATEPCB.kicad_pcb | sed s/TEMPLATEPCB/SAO_Pin/g >eda/SAO_Pin/SAO_Pin.kicad_pcb
rm eda/SAO_Pin/TEMPLATEPCB.kicad_pcb
cat eda/SAO_Pin/TEMPLATEPCB.kicad_sch | sed s/TEMPLATEPCB/SAO_Pin/g >eda/SAO_Pin/SAO_Pin.kicad_sch
rm eda/SAO_Pin/TEMPLATEPCB.kicad_sch
```

* Next fix up the docs folder which references a name TEMPLATEDOC to replace both its filename references as well as references inside those files using sed like so (linux/windows-bash):
```bash
cat docs/TEMPLATEDOC-_config.yml | sed s/TEMPLATEDOC/SAO_Pin/g >docs/_config.yml
rm docs/TEMPLATEDOC-_config.yml
cat docs/TEMPLATEDOC-CNAME | sed s/TEMPLATEDOC/SAO_Pin/g >docs/CNAME
rm docs/TEMPLATEDOC-CNAME
cat docs/TEMPLATEDOC-index.md | sed s/TEMPLATEDOC/SAO_Pin/g >docs/index.md
rm docs/TEMPLATEDOC-index.md
```

* Finally remove this section from this document.
