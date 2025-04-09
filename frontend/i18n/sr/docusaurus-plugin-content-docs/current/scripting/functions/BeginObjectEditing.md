---
title: BeginObjectEditing
sidebar_label: BeginObjectEditing
description:  Омогућава играчу да уређује објекат (позицију и ротацију) користећи свој миш на графичком корисничком интерфејсу (GUI).
tags: ["player", "object"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Омогућава играчу да уређује објекат (позицију и ротацију) користећи свој миш на графичком корисничком интерфејсу (GUI).

| Назив     | Опис                                       |
| -------- | ------------------------------------------------- |
| playerid | ID играча који треба да уреди објекат. |
| objectid | 	ID објекта који играч треба да уреди.  |

## Враћа

`true` - Функција је успешно извршена. Успех се пријављује чак и када је наведени објекат неexistent, али се ништа неће десити.

`false` - Функција није успела да се изврши. Играч није повезан.

## Примери

```c
new objectid;

public OnGameModeInit()
{
    objectid = CreateObject(1337, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0);
    return 1;
}

public OnPlayerCommandText(playerid, cmdtext[])
{
    if (!strcmp(cmdtext, "/oedit", true))
    {
        BeginObjectEditing(playerid, objectid);
        SendClientMessage(playerid, 0xFFFFFFFF, "SERVER: You can now edit the object!");
        return 1;
    }
    return 0;
}
```

## Белешке

:::tip

Можете померити камеру током уређивања тако што ћете притиснути и држати `SPACE` (или W у возилу) и померати миш.

:::

## Повезане Функције

- [CreateObject](CreateObject): Креира објекат.
- [DestroyObject](DestroyObject): Уништава објекат.
- [MoveObject](MoveObject): Помера објекат.
- [BeginPlayerObjectEditing](BeginPlayerObjectEditing): Уреди објекат.
- [EditAttachedObject](EditAttachedObject): Уреди прикачени објекат.
- [BeginObjectSelecting](BeginObjectSelecting): Изабери објекат.
- [EndObjectEditing](EndObjectEditing): Откажи уређивање објекта.
