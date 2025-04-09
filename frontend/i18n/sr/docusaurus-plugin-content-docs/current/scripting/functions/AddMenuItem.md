---
title: AddMenuItem
sidebar_label: AddMenuItem
description: Додаје ставку у одређени мени.
tags: ["menu"]
---

## Опис

Додаје ставку у одређени мени.

## Парамтери

| Назив             | Опис                                |
| ---------------- | ------------------------------------------ |
| Menu:menuid      | ID менија у који се додаје ставка.             |
| column           | Колона у коју се додаје ставка.             |
| const title[]    | Наслов нове ставке у менију.           |
| OPEN_MP_TAGS:... | Неодређен број аргумената било ког типа. |

## Враћа

Индекс реда у који је ставка додата.

## Примери

```c
new Menu:gExampleMenu;

public OnGameModeInit()
{
    gExampleMenu = CreateMenu("Your Menu", 2, 200.0, 100.0, 150.0, 150.0);
    AddMenuItem(gExampleMenu, 0, "item 1");
    AddMenuItem(gExampleMenu, 0, "item 2");
    return 1;
}
```

## Notes

:::tip

- Долази до креша ако се проследи неисправан ID менија.
- Можете имати само 12 ставки по менију (13. иде у десни део заглавља колоне — обојено, 14. и више се уопште не приказују).
- Дозвољене су само 2 колоне (0 и 1).
- Можете додати највише 8 кодова боја по једној ставки (r, g итд.). Максимална дужина ставке у менију је 31 знак.

:::

## Повезане функције

- [CreateMenu](CreateMenu): Креира мени.
- [SetMenuColumnHeader](SetMenuColumnHeader): Подешава заглавље за једну од колона у менију.
- [DestroyMenu](DestroyMenu): Уништава мени.
- [IsMenuRowDisabled](IsMenuRowDisabled): Проверава да ли је ред у менију онемогућен.

## Повезане повратне функције

- [OnPlayerSelectedMenuRow](../callbacks/OnPlayerSelectedMenuRow): Позива се када играч изабере ред у менију.
- [OnPlayerExitedMenu](../callbacks/OnPlayerExitedMenu): Позива се када играч напусти мени.
