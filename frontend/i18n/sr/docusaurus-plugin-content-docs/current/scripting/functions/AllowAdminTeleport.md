---
title: AllowAdminTeleport
sidebar_label: AllowAdminTeleport
description: Ова функција одређује да ли ће RCON админи бити телепортовани до своје ознаке (waypoint) када је поставе.
tags: []
---

:::warning

Ова функција је, почев од верзије 0.3d, застарела. Погледај [OnPlayerClickMap](../callbacks/OnPlayerClickMap).

:::

## Опис

Ова функција одређује да ли ће RCON админи бити телепортовани на свој waypoint када га поставе.

## Параметри

| Назив       | Опис                              |
| ---------- | ---------------------------------------- |
| bool:allow | **false** за онемогућавање, **true** за омогућавање. |

## Враћа

Ова функција не враћа никакве специфичне вредности.

## Примери

```c
public OnGameModeInit()
{
    AllowAdminTeleport(true);
    // Other stuff
    return 1;
}
```

## Повезане функције

- [IsAdminTeleportAllowed](IsAdminTeleportAllowed): Проверава да ли је омогућен teleport за RCON администраторе кликом на мапу.
- [IsPlayerAdmin](IsPlayerAdmin): Проверава да ли је играч пријављен као RCON админ.
- [AllowPlayerTeleport](AllowPlayerTeleport): Омогућава или онемогућава teleport путем waypoint-а за играче.
