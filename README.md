# squicons - Icons for Favicon Testing

Favicons in 25 sizes, numerically named to easily identify which get used.

Trying to figure out exactly which sizes are needed for favicons is a confusing mass of information. Sites list a variety of sizes with notes on when and where the icons suposedly getused. There are a variety of "essential sizes" listed, but not any consistent real-world list. In order to find out for myself what sizes get used, I created 25 crude, numerically named icons for easy identification.

## <abbr title="Too long, didn't read">TL/DR</abbr>

You only need 2 favicons: 32px, 180px.

## Short Resuts

I tested a variety of browsers to see which icons got used in the browser tab and bookmark (bar, sidebar, etc). Also tested was the new tab (aka Start page) screen which lists either recent sites or a selection from bookmark/favorites. Additional tests include saving to the homescreen on mobile (both Apple and Android), and pinning to the Taskbar and Start bar in Windows 10.

| Icon | Browser tab | Bookmark | New Tab | Reading List | Homescreen | TaskBar | Startbar |
|------|-------------|----------|---------|--------------|------------| ------- | -------- |
|  16  | F, E(18)    | F, E(18) |         |              |            ||
|  32  | S,C,F,E,B,V,O|S,C,F,E,B,V,O| C,E | ||||
|  48  |             |          | O       | ||||
|  70  |||||||Small|
|  120 |||||iPhone|x||
|  150 |||||||Large|
|  152 ||||||iPad||
|  180 |||Sm,F|Sm,Si| Si*||
|  192 |(C,E,V,B)**| Android | || Andoroid ||
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

## Sources

There are a lot of favicon resources out there. Just Google it. But the two I found most helpful:

- https://realfavicongenerator.net/favicon_compatibility#.X5pMM1NKjUJ
- https://github.com/audreyfeldroy/favicon-cheat-sheet
