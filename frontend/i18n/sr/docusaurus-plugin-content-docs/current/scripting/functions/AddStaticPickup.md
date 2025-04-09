---
title: AddStaticPickup
sidebar_label: AddStaticPickup
description: Ова функција додаје 'статички' pickup у игру.
tags: ["pickup"]
---

## Опис

Ова функција додаје 'статички' pickup у игру. Ови pickup-и подржавају оружја, здравље, оклоп итд., и функционишу без потребе за додатним скриптирањем (оружје/здравље/оклоп се дају аутоматски).

## Параметри

| Назив                             | Опис                                                                         |
| -------------------------------- | ----------------------------------------------------------------------------------- |
| [model](../resources/pickupids)  | Модел pickup-а.                                                            |
| [type](../resources/pickuptypes) | Тип pickup-а. Одређује како ће се понашати када га играч покупи.                 |
| Float:x                          | X координата на којој се pickup креира.                                           |
| Float:y                          | 	Y координата на којој се pickup креира.                                           |
| Float:z                          | Z координата на којој се pickup креира.                                           |
| virtualWorld                     | ID виртуелног света у који се поставља pickup. Користити -1 за све светове. |

## Враћа

**1** - ако је pickup успешно креиран.

**0** - ако креирање није успело.

## Примери

```c
public OnGameModeInit()
{
    // Create a pickup for armor
    AddStaticPickup(1242, 2, 1503.3359, 1432.3585, 10.1191, 0);

    // Create a pickup for some health, right next to the armour
    AddStaticPickup(1240, 2, 1506.3359, 1432.3585, 10.1191, 0);

    return 1;
}
```

## Белешке

:::tip

Ова функција не враћа ID pickup-а који можете користити, на пример, у OnPlayerPickUpPickup. Ако желите да имате pickup ID, користите [CreatePickup](CreatePickup).

:::

## Повезане функције

- [CreatePickup](CreatePickup): Креира pickup.
- [DestroyPickup](DestroyPickup): Уништава pickup.

## Повезани ресурси

- [Pickup ID-еви](../resources/pickupids)
