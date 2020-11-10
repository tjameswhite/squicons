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

First a note about the webmanifest. Include it if you want. Most browser will read it and you can include other site info. Interestingly, most of the Chromium-based browsers will download the manifest and the 192px icon referenced, but they never used the icon in my tests. Seems a waste of bandwidth. The only place the 192px icon in the manifest gets used is on Android for the home screen icon. However, if you don't include it, Android will use the 180px icon.

For the rest of the icons, we'll start from the far right of our table with the Win10 Start bar. From what I can tell, with the new Chromium-based Edge on Windows 10, it is no longer possible to pin a regular website to the Start bar. So we can elliminate the 70px and 150px icons, as well as the browserconfig.xml file. (If you plan on supporting Edge 18 and really want users to be able to pin to the start bar, then keep the browserconfig and the 70px and 150px icons. But feel free to trim browserconfig down to just those sizes. Lots of sites put 4 sizes in the browserconfig; in my tests there was an option for "small" and "large" (70 and 150) but no options for the larger or rectangular icons.)

Next on the chopping block: Win10 pin to taskbar. Edge 18 will only pin the 32px icon. Chromium-Edge will use 192px if available, but falls back to 120 or 32px. I'm happy to just use 32px on the off chance someone wants to pin the site to their Win10 taskbar. 

As for Apple homescreen icons, iOS prefers the 120px icon and iPadOS prefers the 152px. However, oddly, conviently, both will upsize to the 180px icon if the smaller sizes are missing. This is handy because both devices use the 180px icon for the Reading List and new tab screen (iPad). (Note: tests were done with iOS 13 and 14.) Neither iPhones or iPads show favicons in the favorites/bookmark screen, but when viewing all open tabs, they'll use the 32px. Two more down. An important note: you'll need to use `rel="apple-touch-icon-precomposed"` instead of the standard `rel="icon'` in order to get the homescreen icon to show up. Luckily the other browsers aren't picky and will use `apple-touch-icon-precomposed`. 

Opera Speed dial (new tab screen) was the only place the 48px icon was used. Without it, Opera resorts to a screen shot. A sacrifice I can live with.

As for the crop of Chromium-based browsers, they stick with the 32px icon for everything -- tab, bookmark, new tab screen. 

Firefox will use the 32px for tabs and bookmarks, but if a 16px is available it will use it. For the new tab screen, Firefox prefers the 228px icon, but if that is missing, falls back to the 180px. 

That just leaves Safari desktop. Like Chrome, Safari uses the 32px for tabs and bookmark icons, and like its mobile versions, uses 180px for Reading List and new tab page. Confusingly, in testing an SVG icon, Safari desktop used it for the browser tab, but nowhere else. 

## TL/DR

For a normal website, 32px favicon will get used for the most common use-case: brower tab and favorites. For Firefox new tab and mobile home screens, 180px is the answer.

## Sources

There are a lot of favicon resources out there. Just Google it. But the two I found most helpful:

- https://realfavicongenerator.net/favicon_compatibility#.X5pMM1NKjUJ
- https://github.com/audreyfeldroy/favicon-cheat-sheet
