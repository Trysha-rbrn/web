---
title: AddPlayerClassEx
sidebar_label: AddPlayerClassEx
description:  Ова функција је потпуно иста као функција AddPlayerClass, с тим што има додатни параметар за тим.
tags: ["player", "class"]
---

## Опис

Ова функција је потпуно иста као функција `AddPlayerClass`, али са додатим параметром за тим.


| Назив           | Опис                                                      |
| -------------- | ---------------------------------------------------------------- |
| team           | The team you want the player to spawn in.                        |
| skin           | [Skin](../resources/skins) са којим ће се играч појавити. |
| Float:spawnX   | X координата тачке појављивања за ову класу.                |
| Float:spawnY   | Y координата тачке појављивања за ову класу.                |
| Float:spawnZ   | Z координата тачке појављивања за ову класу.                |
| Float:angle    | Правац у ком играч треба да гледа након појављивања.    |
| WEAPON:weapon1 | Прво оружје које играч добија по појављивању.                           |
| ammo1          | Количина муниције за прво оружје.           |
| WEAPON:weapon2 | Друго оружје које играч добија по појављивању.                          |
| ammo2          | Количина муниције за друго оружје.            |
| WEAPON:weapon3 | Треће оружје које играч добија по појављивању.                           |
| ammo3          | Количина муниције за треће оружје.             |

## Враћа

ID класе која је управо додата.

319 ако је достигнут лимит класа (320). Највећи могући ID класе је 319.

## Пример

```c
public OnGameModeInit()
{
    // Players can spawn as either:
    // CJ Skin (ID 0) in team 1.
    // The Truth skin (ID 1) in team 2.
    AddPlayerClassEx(1, 0, 1958.33, 1343.12, 15.36, 269.15, WEAPON_SAWEDOFF, 36, WEAPON_UZI, 150, WEAPON_FIST, 0); // CJ
    AddPlayerClassEx(2, 1, 1958.33, 1343.12, 15.36, 269.15, WEAPON_SAWEDOFF, 36, WEAPON_UZI, 150, WEAPON_FIST, 0); // The Truth
    return 1;
}
```

## Белешке

:::tip

Максималан ID класе је 319 (почевши од 0, што значи укупно 320 класа). Када се достигне тај лимит, све додатне класе замењују класу са ID-јем 319.

:::

## Повезане функције

- [AddPlayerClassEx](AddPlayerClassEx): Додаје класу са подразумеваним тимом.
- [GetAvailableClasses](GetAvailableClasses): Враћа број дефинисаних класа.
- [EditPlayerClass](EditPlayerClass): Уређује податке о класи.
- [SetSpawnInfo](SetSpawnInfo): Поставља подешавања појављивања за играча.
- [SetPlayerTeam](SetPlayerTeam): Постави играчев тим.
- [SetPlayerSkin](SetPlayerSkin): Поставља скин играчу.

## Повезани ресурси

- [ID-еви скинова](../resources/skins)
- [ID-еви оружја](../resources/weaponids)
