# ahud nut variation

A customised version of ahud for Team Fortress 2. 

## Customisations Made
* Made the font bigger in the lobby and in-game chat.
* Disabled the spy disguise animation

## Installation

1. Download ahud nut variation by clicking `Download ZIP` from the green `Code` button on the ahud-nut-variation GitHub repo.
2. Navigate to  `..\Steam\steamapps\common\Team Fortress 2\tf\custom`.
3. Extract `ahud-nut-variation` from the ZIP file to the `custom` folder.
4. Verify `materials`, `resource`, `scripts`, and `info.vdf` is inside the `ahud-nut-variation` folder.
5. Run Team Fortress 2.

**Windows**: Yes
* 4:3 - 1024×768 and above  
* 16:9 - 1280x720 and above  
* 16:10 -  1280x800 and above  

**Linux**: Yes, with minor issues with the tickboxes in the options and advanced options menus. 
**Mac**: Idk, I suspect that it will probably work but haven't tested it. 

nokk did the testing for ahud on his Windows PC using a 16:9 monitor primarily on resolutions 1280x720 and above. ahud also works on 16:10 and 4:3. 

In addition, I have run ahud on my Linux machine with no problems at 16.9 on the resolution 1920x1080. 

## Re-Enable The Spy Disguise Animation
1. Go to `ahud-nut-variation\scripts\hudanimations_ahud.txt`
2. Remove the following lines of code
```ReScript
//HudSpyDisguiseChanged refers to the outline being at its largest point
//HudSpyDisguiseHide refers to it at its smallest point
//Alpha changes the opacity of the outline
//Position changes position. Feel free to remove the c, but your numbers will be wildly different.
//Size changes size.
//Remember to paste over the already existing commands (and back them up!)

event HudSpyDisguiseChanged
{
Animate PlayerStatusSpyOutlineImage Alpha "255" Linear 0.0 0.2

Animate PlayerStatusSpyOutlineImage Position "c-100 c50" Linear 0.0 0.2
Animate PlayerStatusSpyOutlineImage Size "0" Linear 0.0 0.2

RunEvent HudSpyDisguiseHide 0.7
}

event HudSpyDisguiseHide
{
Animate PlayerStatusSpyOutlineImage Position "c-50 c105" Linear 0.0 0.2
Animate PlayerStatusSpyOutlineImage Size "0" Linear 0.0 0.2

Animate PlayerStatusSpyOutlineImage Alpha "0" Linear 0.2 0.1
}
```
3. Save the hudanimations_ahud.txt file
4. Run TF2

## Original Credit / References
Thanks to [nokk](https://github.com/n0kk) for creating ahud.

<br>

In addition, I would also like to thank the creators of [ToonHud](https://toonhud.com/) for giving me the custom font size scripts.

