# ⚠️ UPDATE: Nov 4 2024
If you are the person who just purchased [the Mac N Touch from ebay](https://www.ebay.com/itm/116370628547) on Nov 4, 2024, please reach out to me on here or [68kmla](https://68kmla.org/bb/index.php?members/nickpunt.2094/). I'd love to hear more about your experience getting it working, if we have the same version of ROMs, etc.

# MicroTouchMac
This is a resource for people interested in the MicroTouch Mac 'n Touch touchscreen for ADB-based Compact Macintosh computers (SE, SE/30, Classic, Classic II), as well as for later Mac-based Microtouch products (external monitors and iMacs).

# Mac 'n Touch
The Mac 'n Touch is a 9" glass touchscreen with a controller board made in the late 80s for ADB-based Compact Macs. It is a capacitive touchscreen with 1024x1024 resolution at 60hz.

Example images and video can be seen in the **Images** folder. The video is by vintagecomputer.ca, originally [posted to youtube](https://www.youtube.com/watch?v=DF-Je337sFo).

# Community
Discussion is happening on [this 68kmla thread](https://68kmla.org/forums/topic/55457-mac-se30-with-microtouch-touchscreen/). There are two, possibly three units that have been seen in the wild.

* [vintagecomputer.ca](http://vintagecomputer.ca/) has a unit (c 1989), ebay item # 112373352145
* [nickpunt](https://nickpunt.com) (me) has a unit (c 1987), ebay item # 333911485496
* A Mac Classic with a touchscreen was seen in the wild in 2015 in this [thread](https://68kmla.org/forums/topic/24522-ebay-not-me-a-touch-screen-classic/?tab=comments#comment-257093), ebay item # 251793191988

# Products & Drivers
See the **Drivers** folder.

Touchware 2 and 3 drivers are from [vintagecomputer.ca](http://vintagecomputer.ca/files/MicroTouch/). Touchware 3 and 5 are from reverse engineering 3M's legacy download URLs (http://www.3m.com/us/electronics_mfg/touch_systems/downloads/drivers/ via [this copy of their 90s website html](http://www.3m.com/us/electronics_mfg/touch_systems/downloads/legacy.jhtml). You can see this in original form [on archive.org's version of MicroTouch's 90s website](https://web.archive.org/web/20001202084100/http://www.microtouch.com/mthtml/05a1_drivers.htm). Some drivers are also available at [TouchWindow](https://www.touchwindow.com/c/3Mmicrotouch.html) (a touchscreen vendor). Including all copies acquired here, in case there are problems.

## Touchware 2 (68k)
Versions: 2.4, 2.5

Use **Mac+n+Touch+2.4.sea** or **MacnTouch 2.5.sea**

Presumably this is for ADB-based 68k Macs, and possibly exclusively the Mac 'n Touch line. In the user guide, mention is made of needing a newer ROM to support multiple touchscreen monitors. This could be external CRTs.

Another source of early TouchWare drivers may be MicroTouch's Unmouse trackpad product, which seems to have come out around 1990. Getting an original floppy from one of these (often available on eBay) may have more. The Unmouse is mentioned in the Mac 'n Touch User Guide PDF.


## Touchware 3 (PPC ADB)
Versions: 3.3

Use **TouchWare for Macintosh 3.3.sea**, **twmac33.hqx**, **twmac33.exe**, or **3MmacBelow8-51Driver.exe** (guessing exe is self-extracting)

This is for ADB-based PPC Macs. This line was discontinued on Jan 3, 2000 [source](https://web.archive.org/web/20000817023955/http://www.microtouch.com/mtmedia/images/CustLtr_102599.jpg).

From the website: *TouchWare 3.3 for Macintosh Power PC, System 7.x. (up to OS 8.51) [262KB] Updated 3/3/98 -- You can also download or view the TouchWare for Macintosh User's Guide PDF.*

In the Touchware 3.3 User Guide there is mention of "Microcal for the Macintosh version 3.3", which may be included, as Microcal seems to be a cross-platform calibration app.

## Touchware 5 (PPC USB)
Versions: 5.3.2

Use **TW532Mac.sit** or **3MMacOS8-9Driver.sit**

From the website: *TouchWare 5.32 Mac [TW532Mac.sit, 72 KB] Updated 10/19/00 -- This driver is designed for MicroTouch USB ClearTek 3000 and TouchTek controllers. The operating systems supported are Mac OS 8.5, 8.5.1, 8.6, and 9.0 on iMac, G3 and G4 systems with USB firmware 1.1 or 1.2. The following options are accessed through the control panel: calibration, configuration options and multiple monitors support for up to 4 USB touchscreens. The installation is manual. You can download the following file TW532Mac.sit. To extract it you will need a third party software called StuffIt Expander available from http://www.aladdinsys.com/expander/index.html. You can also view or download the TouchWare 5.3 Mac User's Guide in PDF format.*

Available at this url: http://www.3m.com/us/electronics_mfg/touch_systems/downloads/legacy.jhtml
which itself is from the 90s-00s website:
https://web.archive.org/web/20001202084100/http://www.microtouch.com/mthtml/05a1_drivers.htm
Replace the names in the directory, e.g. ‘drivers/TW532Mac.sit’ is at: http://www.3m.com/us/electronics_mfg/touch_systems/downloads/drivers/TW532Mac.sit

# Mac Guides
See **Mac Guides** folder.

**Mac 'n Touch Brochure.pdf** - overview of Mac 'n Touch products, including other screen sizes.

**Mac 'n Touch TouchWare 2.4 User Guide.pdf** - nickpunt's scan of original, explains calibration and troubleshooting.

**TouchWare 3.3 User Guide.pdf** - from 3M

**TouchWare 5.3 User Guide.pdf** - from 3M

# Other Guides
See **Other** folder. Contains lots of PDFs that may be of interest for reverse engineering. These two are especially interesting:

**MicroTouch CRT OEM Install Guide.pdf** - shows how to install curved MicroTouch screens to CRTs. MicroTouch offered kits for OEMs to install touchscreens, in addition to making their own touchscreen CRT line.

**Touch Controllers Reference Guide.pdf** - explains how touch controllers work


# Reverse Engineering

## Screens
**ClearTek** are MicroTouch's capacitive screens, which they made in sizes from 8.5"-28". [source](https://web.archive.org/web/20000302005950/http://www.microtouch.com/mthtml/03a1a_sensors-controllers.htm). Mentions are made elsewhere in MicroTouch documentation about '5 pin' style touchscreens. The Mac 'n Touch capacitive screens use a DB9 connector with 5 pins active, which suggests these may be compatible. Mentions are made of the same 1024x1024 resolution, suggesting the touchscreen hardware may be interchangeable.

## Controllers
It seems like MicroTouch tried to standardize their controllers to make them compatible with a wide variety of systems even early on. nickpunt's 1987 unit has pads for two DB25 connectors, for instance. Later touchscreen controllers can be configured for ADB and PC Serial, and possibly others. There's a chance they may be compatible with TouchWare 2 Macs (Mac n Touch). See "Overview of Touchscreen Controllers" in the Touch Controllers Reference Guide.

# Mentions
A few places I've found the Mac 'n Touch mentioned:

**Touch Screen Technology, 15 Years Ago**, Riccardo Mori (2008) - [article](https://systemfolder.wordpress.com/2008/10/01/touch-screen-15yrs-ago/), which quotes MacUser's review of it from August 6, 1993.

**Macintosh Desktop Presentations** (1990) (PDF in Mentions) - Microtouch Touchscreens are mentioned as costing $395-$995, depending on configuration. "Low-cost, user-installable touchscreen system for interactive presentations."

**UM Computing News, Volume 4** (1989) p13 [source](https://books.google.ca/books?id=cZXvAAAAMAAJ&pg=PA69&lpg=PA69&dq=microtouch+systems+macintosh&source=bl&ots=fOfHx-Ne1P&sig=-ip7Cb71CUlEbeFE3vGqCIGZQKg&hl=en&sa=X&ei=qW29VMvrN82nyAT6woCgCg&ved=0CEUQ6AEwCA#v=onepage&q=microtouch&f=false) - Discuses an external 'Snap-on Kit' as well as an internal 'Add-in Kit' (aka 'Standard Kit' from Brochure pdf), and talks about using it with Hypercard.

**History of Pen and Gesture Computing** (1996-1998) [source](http://ruetersward.com/biblio.html) [alt](http://users.rcn.com/rwservices/pens/biblio93.html) [alt](http://users.erols.com/rwservices/pens/biblio03.html) [alt](https://www.researchgate.net/publication/258219935_History_of_Pen_and_Gesture_Computing_Annotated_Bibliography_in_On-line_Character_Recognition_Pen_Computing_Gesture_User_Interfaces_and_Tablet_and_Touch_Computers_References_from_the_approximate_years_) - very thorough list of various touch computing products over the years

# Notes
* Early 90s - MicroTouch also made something called the UnMouse, an early trackpad (see PDF in Other).
* 1993 - Microtouch also announced a monitor for the Amiga called the TruePoint CA-42. [source: AmigaReport](https://www.amigareport.com/ar124/p1-5.html)
* 2001 - MicroTouch was acquired by 3M.
