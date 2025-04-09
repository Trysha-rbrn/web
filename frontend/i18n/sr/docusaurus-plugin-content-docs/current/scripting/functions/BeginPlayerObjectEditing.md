---
title: BeginPlayerObjectEditing
sidebar_label: BeginPlayerObjectEditing
description: Омогућава играчима да уређују играчко-објекат (положај и ротацију) са GUI интерфејсом и њиховим мишем.
tags: ["player", "object", "playerobject"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис 

Омогућава играчима да уређују играчко-објекат (положај и ротацију) са GUI интерфејсом и њиховим мишем.

| Име     | Опис                                      |
| -------- | ------------------------------------------------ |
| playerid | ID играча који треба да уређује објекат |
| objectid | Објекат који треба да уреди играч            |

## Враћа

**true** - Функција је успешно извршена.

**false** - Функција није успела да се изврши. Играч или објекат нису важећи.

## Примери

```c
new gPlayerObject[MAX_PLAYERS];

public OnPlayerSpawn(playerid)
{
    gPlayerObject[playerid] = CreatePlayerObject(playerid, 1337, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0);
}

public OnPlayerCommandText(playerid, cmdtext[])
{
    if (!strcmp(cmdtext, "/edit", true))
    {
        BeginPlayerObjectEditing(playerid, gPlayerObject[playerid]);
        SendClientMessage(playerid, 0xFFFFFFFF, "SERVER: You now edit your object!");
        return 1;
    }
    return 0;
}
```

## Notes

:::tip

Можете померати камеру док уређујете тако што ћете притиснути и држати `SPACE` (или W у возилу) и померати миш.

:::

## Повезане Функције

- [CreateObject](CreateObject): Креира објекат.
- [DestroyObject](DestroyObject): Уништава објекат.
- [MoveObject](MoveObject): Помера објекат.
- [EditAttachedObject](EditAttachedObject): Уреди прикачени објекат.
- [BeginObjectSelecting](BeginObjectSelecting): Изабери објекат.
- [EndObjectEditing](EndObjectEditing): Откажи уређивање објекта.
