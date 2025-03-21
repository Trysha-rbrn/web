---
title: AddStaticPickup
sidebar_label: AddStaticPickup
description: Эта функция добавляет статический пикап в игру.
tags: []
---

## Описание

Эта функция добавляет статический пикап в игру. Эти пикапы поддерживают: оружие, здоровье, броня и т.д., с возможностью работы этих функций без скрипта (оружие/здоровье/броня будет выдано автоматически если в параметре ```model``` указан соответствующий ID).

| Параметр                                | Описание                                                                         |
| ----------------------------------- | ----------------------------------------------------------------------------------- |
| [model](../resources/pickupids)  | Модель пикапа.                                                            |
| [type](../resources/pickuptypes) | Тип пикапа. Определяет реакцию пикапа при поднятии.                 |
| Float:X                             | Координата X для создания пикапа.                                           |
| Float:Y                             | Координата Y для создания пикапа.                                           |
| Float:Z                             | Координата Z для создания пикапа.                                           |
| virtualworld                        | ID виртуального мира в который следует поместить пикап (-1 чтобы поместить во все миры). |

## Возвращаемые данные

1: пикап был успешно создан.

0: не удалось создать пикап.

## Примеры

```c
public OnGameModeInit()
{
    // Создание пикапа с броней
    AddStaticPickup(1242, 2, 1503.3359, 1432.3585, 10.1191, 0);

    // Создание пикапа со здоровьем, рядом с броней
    AddStaticPickup(1240, 2, 1506.3359, 1432.3585, 10.1191, 0);

    return 1;
}
```

## Примечания

:::tip

Эта функция не возвращает ID пикапа который можно использовать, к примеру в OnPlayerPickUpPickup. Используйте CreatePickup если хотите получить ID.

:::

## Связанные функции

- [CreatePickup](CreatePickup): Создать пикап.
- [DestroyPickup](DestroyPickup): Уничтожить пикап.
- [OnPlayerPickUpPickup](../callbacks/OnPlayerPickUpPickup): Вызывается когда игрок подбирает пикап.
