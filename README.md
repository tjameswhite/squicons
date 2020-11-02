# squicons - Icons for Favicon Testing

Favicons in 25 sizes, numerically named to easily identify which get used.

Trying to figure out exactly which sizes are needed for favicons is a confusing mass of information. Sites list a variety of sizes with notes on when and where they allegedly get used. There are a variety of "essential sizes" listed, but no consistent real-world list. In order to find out for myself what sizes are getting used, I created 25 crude, numerically named icons for easy identification. 

## The Winners

32px and 180px.

Out of 25 icons, only 10 were used. But you really only need two sizes: 32px, 180px.

## Tests and Results

I tested a variety of browsers to see which icons got used in the browser tab and bookmark (bar, sidebar, etc). Also tested was the new tab (aka Start page) screen which lists either recent sites or a selection from bookmark/favorites. Additional tests include saving to the homescreen on mobile (both Apple and Android), and pinning to the Taskbar and Start bar in Windows 10.

In addition to the 25 icons, there are also two files: browserconfig.xml and site.webmanifest.

| Icon | Browser tab | Bookmark | New Tab | Reading List | Homescreen | TaskBar (Win10) | Startbar (Win10) |
|------|-------------|----------|---------|--------------|------------| ------- | -------- |
|  16  | Si, F, E(18)| F, E(18) |         |              |            ||
|  32  | Sm,C,F,E,B,V,O|Sm,C,F,E,B,V,O| C,E | ||E(18)||
|  48  |             |          | O       | ||||
|  70  |||||||Small|
|  120 |||||iPhone|E||
|  150 |||||||Large|
|  152 ||||||iPad||
|  180 |||Sm,F|Sm,Si| Si*||
|  192 |(C,E,V,B)**| Android | || Andoroid | E | |
|  228 |||F***||||
|  SVG |Sm ||||||

Key:

- F: Firefox
- C: Chrome
- B: Brave
- V: Vivaldi
- O: Opera
- Sm: Safari macOS
- Si: Sarari iOS/iPadOS
- E: Edge (Chromium)
- E(18): Edge 18

First a note about the webmanifest. Include it if you want. Most browser will read it; you can include other site info, <!--***does android use it for home screen??**-->
Let's start whinning this down starting on the right. From what I can tell, with the new Chromium-based Edge on Windows 10, it is no longer possible to pin a regular website to the Start bar. Right off we can elliminate the 70px and 150px icons, as well as the browserconfig.xml file. 

## Sources

There are a lot of favicon resources out there. Just Google it. But the two I found most helpful:

- https://realfavicongenerator.net/favicon_compatibility#.X5pMM1NKjUJ
- https://github.com/audreyfeldroy/favicon-cheat-sheet
