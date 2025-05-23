---
title: OnObjectMoved
sidebar_label: OnObjectMoved
description: Ова повратна функција се позива када се објекат помери након MoveObject (када се заустави са кретањем).
tags: ["object"]
---

## Опис

Ова повратна функција се позива када се објекат помери након [MoveObject](../functions/MoveObject) (када се заустави са кретањем).

| Име      | Опис                                |
| -------- | ----------------------------------- |
| objectid | ID објекта који је померен.         |

## Враћа

Увек се позива прва у филтер скриптама.

## Пример

```c
public OnObjectMoved(objectid)
{
    printf("Object %d finished moving.", objectid);
    return 1;
}
```

## Белешке

:::tip

[SetObjectPos](../functions/SetObjectPos) не функционише када се користи у овој повратној функцији. Да бисте исправили, поново креирајте објекат.

:::

## Повезане повратне функције

Следеће повратне функције могу бити корисне, јер су на неки начин повезане са овом повратном функцијом.

- [OnPlayerObjectMoved](OnPlayerObjectMoved): Ова повратна функција се позива када објекат играча престане да се креће.

## Повезане функције

Следеће функције могу бити корисне, јер су на неки начин повезане са овом повратном функцијом.

- [MoveObject](../functions/MoveObject): Померите објекат.
- [MovePlayerObject](../functions/MovePlayerObject): Померите објекат играча.
- [IsObjectMoving](../functions/IsObjectMoving): Проверава да ли се објекат креће.
- [StopObject](../functions/StopObject): Престаните да се објекат креће.
