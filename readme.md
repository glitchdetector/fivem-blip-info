# FiveM Blip Info Utility
by [**glitchdetector**](https://github.com/glitchdetector)

This resource aims to help implement the pop-up information window that appears when hovering over blips in GTA Online. It also serves as an example use of the newly discovered tech it's built upon.

This popup is only visible while in the pause menu map, and while hovering over a blip that has information attached to it.

All rendering and logic is handled by the resource.

This resource is a standalone utility, meaning:

 * It does not rely on a framework
 * It does nothing by itself
 * You as a developer need to utilize its exports
 * **If you are not a resource developer, this is not for you**

## Screenshots

![](https://i.imgur.com/f8RKdqJ.png)

## Setup
Set `blip_info` as a depencendy in your resource

## Usage
*All functions are available via exports*

Info is set per blip (handle) and only need to be set once.

**`ResetBlipInfo(blip)`**

Removes all blip info and no longer shows info popup when selected

**`SetBlipInfoTitle(blip, title, rockstarVerified)`**

Sets the info popup title and the state of the R* verified icon

**`SetBlipInfoImage(blip, dict, tex)`**

Sets the header image for the info popup

**`SetBlipInfoEconomy(blip, rp, money)`**

Changes the visual representation for RP and Money in the popup, empty strings disable the respective icon

**`AddBlipInfoText(blip, leftText, rightText)`**

Adds a line to the info popup

**`AddBlipInfoName(blip, leftText, rightText)`**

Adds a line to the info popup, `rightText` appearing in bold

**`AddBlipInfoHeader(blip, leftText, rightText)`**

Adds a line to the info popup, including a separator between this and the previous line

**`AddBlipInfoIcon(blip, leftText, rightText, iconId, iconColor, checked)`**

Adds a line to the info popup, including a blip icon.

`iconId` can range from 0 to 25. `iconColor` appears to match with blip colors.

**`SetBlipInfo(blip, infoData)`**

Sets the raw info data, for advanced use

## Example
*This example code is what produced the result in the screenshot earlier*

```lua
exports['blip_info']:SetBlipInfoTitle(blip, "Sample Title", true)
exports['blip_info']:SetBlipInfoEconomy(blip, "1 200", "12.85M")
exports['blip_info']:AddBlipInfoText(blip, "Info Text", "Sample Text")
exports['blip_info']:AddBlipInfoName(blip, "Info Name", "glitchdetector")
exports['blip_info']:AddBlipInfoHeader(blip, "Info Header", "Look a line")
exports['blip_info']:AddBlipInfoIcon(blip, "Info Blip", "wew", 16, 0, true)
```

## License
Do what you want, except:

 - Re-distribute a non-remixed version of this resource outside of the target platform
