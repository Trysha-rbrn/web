---
title: CreateMenu
sidebar_label: CreateMenu
description: Креира мени.
tags: ["menu"]
---

## Опис

Креира мени.

| Назив               | Опис                                                                         |
| ------------------ | ----------------------------------------------------------------------------------- |
| const title[]      | Назив новог менија.                                                         |
| columns            | 	Колико колона ће имати нови мени.                                            |
| Float:x            | 	X позиција менија (640x460 платно - 0 ће поставити мени на леву страну). |
| Float:y            | Y позиција менија (640x460 платно - 0 ће поставити мени на горњу страну).  |
| Float:column1width | Ширина прве колоне.                                                     |
| Float:column2width | Ширина друге колоне.                                                    |
| OPEN_MP_TAGS:...   | Непознат број аргумената било ког типа.                                          |

## Враћа

ID новог менија или **-1** ако је дошло до грешке.

## Примери

```c
new Menu:exampleMenu;

public OnGameModeInit()
{
    exampleMenu = CreateMenu("Example Menu", 2, 200.0, 100.0, 150.0, 150.0);
    return 1;
}
```

## Белешке

:::tip

- Ова функција само КРЕИРА мени - за приказивање менија треба користити [ShowMenuForPlayer](ShowMenuForPlayer).
- Можете креирати и приступити само 2 колоне (0 и 1).
- Ако дужина наслова буде једнака или већа од 32 знака, наслов ће бити скраћен на 30 знакова.

:::

:::warning

Постоји ограничење од 12 ставки по менију и ограничење од 128 менија укупно.

:::

## Повезане функције

- [AddMenuItem](AddMenuItem): Додаје ставку у одређени мени.
- [SetMenuColumnHeader](SetMenuColumnHeader): Поставља заглавље за једну од колона у менију.
- [DestroyMenu](DestroyMenu): Уништава мени.
- [ShowMenuForPlayer](ShowMenuForPlayer): Приказује мени за играча.
- [HideMenuForPlayer](HideMenuForPlayer): Скрива мени за играча.

## Повезане поратне функције

- [OnPlayerSelectedMenuRow](../callbacks/OnPlayerSelectedMenuRow): Позива се када играч изабере ред у менију.
- [OnPlayerExitedMenu](../callbacks/OnPlayerExitedMenu): Позива се када играч изађе из менија.