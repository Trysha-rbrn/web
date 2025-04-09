---
title: TogglePlayerWidescreen
sidebar_label: TogglePlayerWidescreen
description: Промените статус широког екрана за играча.
tags: ["player"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Промените статус широког екрана за играча.

| Назив      | Опис                                      |
|-----------|--------------------------------------------------|
| playerid  | ID играча за кога се мења статус широког екрана.   |
| bool:wide | **true** за укључивање и **false** за искључивање. |

## Враћа

**true** - Функција је успешно извршена.

**false** - Функција није успела. Ово значи да играч са наведеним ID-ом не постоји.

## Примери

```c
public OnPlayerCommandText(playerid, cmdtext[])
{
    if (!strcmp(cmdtext, "/widescreen", true))
    {
        TogglePlayerWidescreen(playerid, true);
        SendClientMessage(playerid, -1, "SERVER: You turned on the widescreen!");
        return 1;
    }
    return 0;
}
```

<hr />

**Widescreen on:**

![](https://i.ibb.co/Zcc2qmD/widescreen-on.png)

**Widescreen off:**

![](https://i.ibb.co/jb1YcQS/widescreen-off.png)

## Повезане функције

- [IsPlayerWidescreenToggled](IsPlayerWidescreenToggled): Провера да ли је широки екран укључен или искључен за играча.
