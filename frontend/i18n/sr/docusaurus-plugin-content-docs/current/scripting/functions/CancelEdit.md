---
title: CancelEdit
sidebar_label: CancelEdit
description: Отказује режим уређивања објекта за играча.
tags: []
---

## Опис

Отказује режим уређивања објекта за играча.

| Назив   | Опис                                |
| -------- | ------------------------------------------ |
| playerid | 	ID играча за кога се отказује режим уређивања. |

## Враћа

Ова функција не враћа никакве специфичне вредности.

## Examples

```c
public OnPlayerCommandText(playerid, cmdtext[])
{
    if (!strcmp(cmdtext, "/stopedit", true))
    {
        CancelEdit(playerid);
        SendClientMessage(playerid, 0xFFFFFFFF, "SERVER: You stopped editing the object!");
        return 1;
    }
    return 0;
}
```

## Повезане функције

- [SelectObject](SelectObject): Избор објекта.
- [EditObject](EditObject): Уређивање објекта.
- [EditPlayerObject](EditPlayerObject): Уређивање објекта.
- [EditAttachedObject](EditAttachedObject): Уређивање прикљученог објекта. 
- [CreateObject](CreateObject): Креирање објекта.
- [DestroyObject](DestroyObject): Уништавање објекта.
- [MoveObject](MoveObject): Померање објекта.
