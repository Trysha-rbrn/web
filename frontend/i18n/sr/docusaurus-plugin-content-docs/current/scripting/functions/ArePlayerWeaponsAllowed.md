---
title: ArePlayerWeaponsAllowed
sidebar_label: ArePlayerWeaponsAllowed
description: Да ли играч може да користи оружје?
tags: ["player"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Да ли играч може да користи оружје?

## Параметри

| Име     | Опис                    |
| -------- | ------------------------------ |
| playerid | ID играча којем се проверава дозвола. |

## Враћа

**true** - Играч има дозволу.

**false** - Играч нема дозволу.

## Примери

```c
public OnPlayerSpawn(playerid)
{
    if (ArePlayerWeaponsAllowed(playerid))
    {
        // уради нешто овде..
    }

    return 1;
}
```

## Повезане функције

- [AllowPlayerWeapons](AllowPlayerWeapons): Омогућава или онемогућава оружје за играча.
