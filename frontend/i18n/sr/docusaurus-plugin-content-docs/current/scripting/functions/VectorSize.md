---
title: VectorSize
sidebar_label: VectorSize
description: Враћа норму (дужину) дату вектору.
tags: ["math"]
---

## Опис

Враћа норму (дужину) дату вектору.

## Парамтери

| Name    | Description                           |
| ------- | ------------------------------------- |
| Float:x | Величина вектора на X оси. |
| Float:y | Величина вектора на Y оси. |
| Float:z | Величина вектора на Z оси. |

## Враћа

Норму (дужину) дату вектору као тип `float`.

## Примери

```c
stock Float:GetDistanceBetweenPoints(Float:x1, Float:y1, Float:z1, Float:x2, Float:y2, Float:z2)
{
    return VectorSize(x1-x2, y1-y2, z1-z2);
}
```

## Повезане функције

- [GetPlayerDistanceFromPoint](GetPlayerDistanceFromPoint): Враћа раздаљину између играча и тачке.
- [GetVehicleDistanceFromPoint](GetVehicleDistanceFromPoint): Враћа раздаљину између возила и тачке.
- [floatsqroot](floatsqroot): Израчунава квадратни корен од вредности типа `float`.
