# Rich Presence U - Database

Title database for https://github.com/ninstar/Rich-Presence-U.

## How to contribute

Here is the list of currently supported platforms:

- Wii U - [wup.csv](titles/wup.csv)
- Nintendo Switch - [hac.csv](titles/hac.csv)
- Nintendo 3DS - [ctr.csv](titles/ctr.csv)
- Nintendo Switch 2 - [bee.csv](titles/bee.csv)

> [!Important]
>  Cells are separated by commas ``,`` and delimited by double quotation marks ``"``.

### Titles

Each line is for a different software, regions are separated by columns with the following prefixes:

- **US** for America
- **EU** for Europe
- **JP** for Japan

You must fill out at least one of the cells in one of the `TITLE` columns. You don't have to fill the other cells if the title localization is the same for other regions (unless that region has an [unique icon](#icons)).

**Example**

| ... | US TITLE | EU TITLE | JP TITLE |
| --- | --- | --- | --- |
| ... | Super Mario |     | スーパーマリオ |

### Icons

The first column is used to define a unique ID to the icon associated with the software. The icon filename should be the same, but with a region suffix appended.

**Example**

For a software entry like this:

| ID | US | EU | JP | US TITLE | EU TITLE | JP TITLE |
| --- | --- | --- | --- | --- | --- | --- |
| smario | ✓ |  | ✓ | Super Mario |     | スーパーマリオ |

The filename of the icons should be like this:

- ``smario.us.jpg``
- ``smario.jp.jpg``

> [!Warning]
> ``default`` and ``id`` are reserved internally, therefore you should not use them as the filename of an icon or IDs.

The cells in columns 2, 3, and 4 (from left to right) are used to indicate whether a corresponding icon file is present when they are populated with a character. It can be any character, but I recommend using a check mark (``✓``).

To avoid duplicates, when a software has a different title in one region but has exactly the same icon in all of them, it is necessary to provide the icon for only one region, that being the region with the highest priority. The order of priority is as follows:

- **US ➜ EU ➜ JP**

Applying this to the example above, only ``smario.us.png`` would be required.

**Icon requirements**

- You need an icon for at least one region.
- The filename of the icon should be the same as the `ID` with a region suffix added to the left of the file extension.
- The file extensions needs to be **.jpg**.
- The minimum accepted size is **512x512** pixels.
- If an icon is smaller than the minimum accepted size but evenly divisible by it, you should always enlarge it using nearest neighbor scaling, otherwise it is preferable to upscale it using bilinear or lanczos interpolation or other super-resolution methods.

## Credits

All resources provided here were made possible thanks to the contribution of the following people:

- NinStar
- Majesty
- Sneethan
- Lakelimbo
- Luxen
- CodeBarre
- issey
- AbBrittus
- gilramot
- K1rbYat1Na
- Kcroyals3
- Peach774
- Sup3r-M4rio
- ShadowzI
- Schitzel9000
- squihb
- teemerae
- yurisasc
- Zushi11
- Zyliqx
- catfxngs