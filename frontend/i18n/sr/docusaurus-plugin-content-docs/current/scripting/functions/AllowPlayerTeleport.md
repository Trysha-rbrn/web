---
title: AllowPlayerTeleport
sidebar_label: AllowPlayerTeleport
description: Омогућава или онемогућава могућност телепортације играча десним кликом на мапу.
tags: ["player"]
---

:::warning

Ова функција је, почев од верзије 0.3d, застарела. Погледај [OnPlayerClickMap](../callbacks/OnPlayerClickMap).

:::

## Опис

Омогућава или онемогућава могућност телепортације играча десним кликом на мапу.

## Параметри

| Назив       | Опис                              |
| ---------- | ---------------------------------------- |
| playerid   | 	ID играча коме се дозвољава телепортација.  |
| bool:allow | **false** – онемогућава, **true** – омогућава. |

## Враћа

Ова функција не враћа никакве специфичне вредности.

## Примери

```c
public OnPlayerConnect(playerid)
{
    // Allows the Player to teleport by right-clicking on the map
    // since this is in OnPlayerConnect, this will be done for EACH player
    AllowPlayerTeleport(playerid, true);
    return 1;
}
```

## Белешке

:::warning

Ова функција ради само ако је [AllowAdminTeleport](AllowAdminTeleport) омогућен, и морате бити администратор.

:::

## Повезане функције

- [IsPlayerTeleportAllowed](IsPlayerTeleportAllowed): Да ли играч може да се телепортује десним кликом на мапу?
- [AllowAdminTeleport](AllowAdminTeleport): Омогућава телепортацију администраторима путем мапе.
