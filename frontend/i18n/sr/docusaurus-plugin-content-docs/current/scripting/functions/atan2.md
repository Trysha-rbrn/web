---
title: atan
sidebar_label: atan
description: Добија мулти-вредносну инверзну вредност тангента у степенима.
tags: ["math"]
---

<LowercaseNoteSR />

:::warning

Обратите пажњу да је y-вредност први параметар, а x-вредност други параметар. Ово је зато што је математичка нотација y/x (тј. y подељено са x), а конвенција је да се операнди пишу у редоследу операције која се на њима врши.

:::

## Опис

Добија мулти-вредносну инверзну вредност тангента у степенима. У тригонометрији, арктангенус је инверзна операција тангента. Да би се израчунала вредност, функција узима у обзир знак оба аргумента како би одредила квадрант.

| Име    | Опис                                            |
| ------- | ------------------------------------------------------ |
| Float:y | Вредност која представља пропорцију y-координате. |
| Float:x | Вредност која представља пропорцију x-координате. |

## Враћа

Угао у степенима, у интервалу [-180.0,+180.0].

## Пример

```c
//The arc tangent for (x=-10.000000, y=10.000000) is 135.000000 degrees.

public OnGameModeInit()
{
    new Float:x, Float:y, Float:result;
    x = -10.0;
    y = 10.0;
    result = atan2(y, x);
    printf("The arc tangent for (x=%f, y=%f) is %f degrees.", x, y, result);
    return 1;
}
```

## Related Functions

- [floatsin](floatsin): Добија синус из одређеног угла.
- [floatcos](floatcos): Добија косинус из одређеног угла.
- [floattan](floattan): Добија тангенту из одређеног угла.
- [asin](asin): Добија инверзну вредност синуса у степенима.
- [acos](acos): Добија инверзну вредност косинуса у степенима.
- [atan](atan): Добија инверзну вредност тангента у степенима.
