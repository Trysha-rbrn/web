---
title: AllowPlayerWeapons
sidebar_label: AllowPlayerWeapons
description: Омогућава или онемогућава оружје за одређеног играча.
tags: ["player"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Омогућава или онемогућава оружје за одређеног играча.

## Параметри

| Назив       | Опис                            |
| ---------- | -------------------------------------- |
| playerid   | ID играча коме се оружје омогућава/забрањује.  |
| bool:allow | **true** за омогућавање, **false** за забрану. |

## Враћа

Ова функција увек враћа **true**.

## Примери

```c
public OnPlayerConnect(playerid)
{
    AllowPlayerWeapons(playerid, true);
    return 1;
}
```

## Повезане функције

- [ArePlayerWeaponsAllowed](ArePlayerWeaponsAllowed): Да ли играч може да користи оружје?
