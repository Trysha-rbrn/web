---
title: AddPlayerClass
sidebar_label: AddPlayerClass
description: Додаје класу у избор класа.
tags: ["player", "class"]
---

## Опис

Додаје класу у избор класа. Класе се користе како би играчи могли да се појаве са скином по свом избору.

| Назив           | Опис                                                      |
| -------------- | ---------------------------------------------------------------- |
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
    // Players can spawn with either the CJ skin (0) or The Truth skin (1).
    AddPlayerClass(0, 1958.33, 1343.12, 15.36, 269.15, WEAPON_SAWEDOFF, 36, WEAPON_UZI, 150, WEAPON_BRASSKNUCKLE, 1); // CJ
    AddPlayerClass(1, 1958.33, 1343.12, 15.36, 269.15, WEAPON_SAWEDOFF, 36, WEAPON_UZI, 150, WEAPON_BRASSKNUCKLE, 1); // The Truth
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
- [SetPlayerSkin](SetPlayerSkin): Поставља скин играчу.

## Повезани ресурси

- [ID-еви скинова](../resources/skins)
- [ID-еви оружја](../resources/weaponids)
