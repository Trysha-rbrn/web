---
title: AllowInteriorWeapons
sidebar_label: AllowInteriorWeapons
description: Омогућава или онемогућава употребу оружја у interior-има.
tags: []
---

## Опис

Омогућава или онемогућава употребу оружја у interior-има.

| Назив       | Опис                                                                                          |
| ---------- | ---------------------------------------------------------------------------------------------------- |
| bool:allow | **true** – омогућава оружје у interior-има (подразумевано укључено), **false** – онемогућава га. |

## Враћа

Ова функција не враћа никакве специфичне вредности.

## Примери

```c
public OnGameModeInit()
{
    // Ово ће омогућити употребу оружја у interior-има.
    AllowInteriorWeapons(true);
    return 1;
}
```

## Белешке

:::warning

Ова функција тренутно не ради у актуелној верзији SA:MP-а!

:::

:::tip

Могуће је укључити или искључити оружје у interior-има и преко фајла [config.json](../../server/config.json)

```json
"allow_interior_weapons": true,
```

:::

## Повезане функције

- [AreInteriorWeaponsAllowed](AreInteriorWeaponsAllowed): Да ли је дозвољено користити оружје у interior-има?
- [SetPlayerInterior](SetPlayerInterior): Поставља interior за играча.
- [GetPlayerInterior](GetPlayerInterior): Враћа тренутни interior играча.

## Повезане повратне функције

- [OnPlayerInteriorChange](../callbacks/OnPlayerInteriorChange): Позива се када играч промени interior.
