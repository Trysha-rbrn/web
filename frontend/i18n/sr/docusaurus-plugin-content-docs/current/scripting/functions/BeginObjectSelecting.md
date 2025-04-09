---
title: BeginObjectSelecting
sidebar_label: BeginObjectSelecting
description: Приказује курсор и омогућава играчу да изабере објекат.
tags: ["object"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Приказује курсор и омогућава играчу да изабере објекат. OnPlayerSelectObject се позива када играч изабере објекат.

| Име     | Опис                                                   |
| -------- | ------------------------------------------------------------- |
| playerid | 	ID играча који треба да буде у могућности да изабере објекат. |

## Враћа

Ова функција не враћа никакве специфичне вредности.

## Примери

```c
public OnPlayerCommandText(playerid, cmdtext[])
{
    if (!strcmp(cmdtext, "/select", true))
    {
        BeginObjectSelecting(playerid);
        SendClientMessage(playerid, 0xFFFFFFFF, "SERVER: Please select the object you'd like to edit!");
        return 1;
    }
    return 0;
}
```

## Повезане функције

- [CreateObject](CreateObject): Креира објекат.
- [DestroyObject](DestroyObject): Уништава објекат.
- [MoveObject](MoveObject): Помера објекат.
- [BeginObjectEditing](BeginObjectEditing): Уреди објекат.
- [BeginPlayerObjectEditing](BeginPlayerObjectEditing): Уреди објекат.
- [EditAttachedObject](EditAttachedObject): Уреди прикачени објекат.
- [EndObjectEditing](EndObjectEditing): Откажи уређивање објекта.

## Повезане повратне функције

- [OnPlayerSelectObject](../callbacks/OnPlayerSelectObject): Позива се када играч изабере објекат.
