---
title: AddServerRule
sidebar_label: AddServerRule
description: Add a server rule.
tags: ["rule"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Додаје правило сервера.

| Назив             | Опис                                |
| ---------------- | ------------------------------------------ |
| const rule[]     | Назив правила сервера које се додаје.               |
| const format[]   | Вредност правила сервера.                     |
| OPEN_MP_TAGS:... | Неодређен број аргумената било ког таг типа. |

## Враћа

Враћа **true** ако је функција успешно извршена, у супротном **false**.

## Пример

```c
public OnGameModeInit()
{
    AddServerRule("discord", "discord.gg/samp");
    return 1;
}
```

## Повезане функције

- [RemoveServerRule](RemoveServerRule): Уклања правило сервера.
- [IsValidServerRule](IsValidServerRule): Проверава да ли је правило сервера важеће.
