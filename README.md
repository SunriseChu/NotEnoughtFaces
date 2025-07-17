# NotEnoughtFaces v1.0.1 (Release)
# FiveM MP Freemode Additional Faces Instructions

## Overview

This readme provides instructions on how to install and configure NotEnoughtFaces on your FiveM server. This mod expands the number of freemode face options available for character creation in FiveM, increasing the limit from 45 to 100.

## Requirements

- A working FiveM server using QBCore, ESX, or a custom framework.

- qb-clothing or illenium-appearance installed (if applicable to your server).

- If you are using a custom framework or vRP, support is available via Discord.

- You must adjust your client-side clothing/appearance scripts to recognize the new face slots.

- Discord support is available for questions, bug reports, and to request new face additions.

- Feel free to reach out in discord if you have questions or suggestions. There are specific chanells for you to use to submit for new faces to be added!

![alt text][logo]

[logo]: https://r2.fivemanage.com/xEb6bHmDhTgwVdhHMh47w/notenoughtfacesguide.jpg "NotEnoughtFaces Forum in Discord"

# Installation

## QBCore / ESX

### qb-clothing
1. Open client/main.lua,
2. Find this block: 

```if v.type == "face" then
    maxModelValues[k].item = 45
    maxModelValues[k].texture = 15
end

if v.type == "face2" then
    maxModelValues[k].item = 45
    maxModelValues[k].texture = 15
end
```

3. Replace it with:

```if v.type == "face" then
    maxModelValues[k].item = 100
    maxModelValues[k].texture = 15
end

if v.type == "face2" then
    maxModelValues[k].item = 100
    maxModelValues[k].texture = 15
end
```

### illenium-appearance

1. Open game/customization.lua,
2. Find this block: 

```shapeFirst = {
    min = 0,
    max = 45
},
shapeSecond = {
    min = 0,
    max = 45
},
shapeThird = {
    min = 0,
    max = 45
},
```

3. Replace it with:

```shapeFirst = {
    min = 0,
    max = 100
},
shapeSecond = {
    min = 0,
    max = 100
},
shapeThird = {
    min = 0,
    max = 100
},
```

### QBox crm

1. Open crm-appearance/crm-config.lua,
2. Find this block: 

```crm_config.crm_faces_max = 45 -- Default: 45
```

3. Replace it with:

```crm_config.crm_faces_max = 100 -- Default: 45
```

## vRP/Custom

### For vRP or other custom frameworks, please reach out via Discord for assistance. Custom implementation support is provided based on your system's structure and my own knowledge, but ultimately you are the one who knows your framework best.

## Notes

- Be sure your server had started the resource and that you had adjusted the required scripts.
- Some older scripts may not respect the new values without additional tweaking.
- Always test character creation thoroughly after modifying appearance scripts.

---

## Support & Community

Join our [Discord Server](https://discord.gg/zH9fsKkBUP) to get support, submit bug reports, or suggest new face types to add.
All Updates will now be visiblein #NotEnoughtFaces chanell!

---

**Created by:** sunr1sechu\
**Version:** 1.0.0\
**Last Updated:** 13th July 2025
