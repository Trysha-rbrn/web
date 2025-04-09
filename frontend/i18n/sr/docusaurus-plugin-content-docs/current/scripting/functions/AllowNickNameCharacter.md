---
title: AllowNickNameCharacter
sidebar_label: AllowNickNameCharacter
description: Дозвољава употребу одређеног карактера у nick name-у.
tags: []
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Дозвољава употребу одређеног карактера у nick name-у.

## Параметри

| Назив       | Опис                         |
| ---------- | ----------------------------------- |
| character  | Карактер који се дозвољава или забрањује. |
| bool:allow | **true** – дозвољава, **false** – забрањује.          |

## Враћа

Ова функција не враћа никакве специфичне вредности.

## Примери

```c
public OnGameModeInit()
{
    AllowNickNameCharacter('*', true); // Дозволи карактер *
    AllowNickNameCharacter('[', false); // Забрани карактер [
    AllowNickNameCharacter(']', false); // Забрани карактер ]

    return 1;
}
```

## Повезане функције

- [IsNickNameCharacterAllowed](IsNickNameCharacterAllowed): Проверава да ли је карактер дозвољен у nick name-у.
- [IsValidNickName](IsValidNickName): Проверава да ли је nick name валидан.
- [SetPlayerName](SetPlayerName): Поставља име играча.
- [GetPlayerName](GetPlayerName): Враћа име играча.