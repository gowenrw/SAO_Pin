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
  * [/eda/SAO_Pin/](./eda/SAO_Pin/) - KiCad 9.x project folder for the SAO_Pin PCB
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

## Project Details

The SAO_Pin is a simple adapter that will allow you to wear any badge Shitty Add On (SAO) as a broach pin instead of being attached to a badge or a totem.

The PCB is small at 25mm x 40mm, just large enough to hold its few components and hopefully small enough to be hidden behind any attached SAO.

The Gerber files have been made available [HERE](./eda/SAO_Pin/gerber/2025-06-03.zip) for anyone to use to order thier own PCBs.
Simply download the [ZIP file](./eda/SAO_Pin/gerber/2025-06-03.zip) and then choose your PCB manufacture to upload it to for ordering.

The design is simple, requiring only four components:
* SAO 2x3 keyed socket header, the type used on badges not the type used on SAO's.
* CR2032 Battery Holder with THT pins
* 20mm Brooch clip pin clasp with M2 sized screw holes for attachment
* M2 screws and nuts for attaching the pin.

Here are some links for ordering the components:

* SAO 2x3 keyed socket header, the type used on badges not the type used on SAO's.
  * https://www.aliexpress.us/item/2251832874579437.html
  * https://www.ebay.com/itm/173960769032

* CR2032 Battery Holder with THT pins
  * https://www.aliexpress.us/item/3256806213778380.html
  * https://www.amazon.com/dp/B07T3WP9T4

* 20mm Brooch clip pin clasp with M2 sized screw holes for attachment
  * https://www.aliexpress.us/item/2255800106050402.html - Choose the 2cm option
  * https://www.amazon.com/dp/B0BJJ4L94L - Choose the 20mm option

* M2 screws and nuts for attaching the pin.
  * https://www.aliexpress.us/item/3256808318392916.html - Choose M2 Screw 5mm Length
  * https://www.amazon.com/dp/B082XXXRV6 - Choose M2 Screw 5mm Length
  * https://www.aliexpress.us/item/3256806543218419.html - Choose M2 Nut
  * https://www.amazon.com/dp/B0CMG7Q27P - Choose M2 Nut

