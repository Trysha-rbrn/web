---
title: TogglePlayerGhostMode
sidebar_label: TogglePlayerGhostMode
description: Постављање "ghost mode" за играча.
tags: ["player"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Омогућите ghost mode за играча.
Ghost mode онемогућава колизију између играчких модела.

## Парамтери

| назив        | Опис                                    |
| ----------- | ---------------------------------------------- |
| playerid    | ID играча за којег се активира ghost mode. |
| bool:toggle | **true** за укључивање и **false** за искључивање.         |

## Враћа

Ова функција увек враћа **true**.

## Примери

```c
public OnPlayerCommandText(playerid, cmdtext[])
{
    if (!strcmp(cmdtext, "/ghostmode", true))
    {
        TogglePlayerGhostMode(playerid, true);
        SendClientMessage(playerid, -1, "SERVER: You enabled the ghost mode!");
        return 1;
    }
    return 0;
}
```

## Повезане функције

- [GetPlayerGhostMode](GetPlayerGhostMode): Добијање тренутног стања ghost mode-a за играча.
