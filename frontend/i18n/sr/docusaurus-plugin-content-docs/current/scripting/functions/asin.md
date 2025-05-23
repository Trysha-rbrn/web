---
title: asin
sidebar_label: asin
description: Добија инверзну вредност синуса у степенима.
tags: ["math"]
---

<LowercaseNoteSR />

## Опис

Добија инверзну вредност синуса у степенима. У тригонометрији, арксинус је инверзна операција синуса.

| Име        | Опис                                                |
| ----------- | ---------------------------------------------------------- |
| Float:value | Вредност чији арксинус се рачуна, у интервалу [-1,+1]. |

## Враћа

Угао у степенима, у интервалу [-90.0,+90.0].

## Примери

```c
//The arc sine of 0.500000 is 30.000000 degrees.

public OnGameModeInit()
{
    new Float:param, Float:result;
    param = 0.5;
    result = asin(param);
    printf("The arc sine of %f is %f degrees.", param, result);
    return 1;
}
```

## Повезане функције

- [floatsin](floatsin): Добија синус из одређеног угла.
- [floatcos](floatcos): Добија косинус из одређеног угла.
- [floattan](floattan): Добија тангенту из одређеног угла.
- [acos](acos): Добија инверзну вредност косинуса у степенима.
- [atan](atan): Добија инверзну вредност тангента у степенима.
- [atan2](atan2): Добија мулти-вредносну инверзну вредност тангента у степенима.
