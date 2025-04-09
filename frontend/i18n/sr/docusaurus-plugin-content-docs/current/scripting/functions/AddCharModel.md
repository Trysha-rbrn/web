---
title: AddCharModel
sidebar_label: AddCharModel
description: Додаје нови прилагођени модел карактера за преузимање.
tags: ["custom skin", "char model"]
---

<VersionWarnSR version='SA-MP 0.3.DL R1' />

## Опис

Додаје нови прилагођени модел лика за преузимање. Датотеке модела ће бити сачуване у Documents\GTA San Andreas User Files\SAMP\cache у фолдеру сервера (IP и порт) у CRC формату имена датотеке.

## Парамтери

| Назив                   | Опис                                                                                                    |
| ---------------------- | -------------------------------------------------------------------------------------------------------------- |
| baseid                 | Основна ID вредност модела која се користи (понашање лика и оригинални лик који се користи када преузимање не успе). |
| newid                  | Нова ID вредност модела (од 20001 до 30000 - 10000 слотова) која ће се касније користити са SetPlayerSkin.             |
| const dff[]            | Назив .dff датотеке модела (колизија) која се налази у models фолдеру сервера (подразумевана локација - artpath подешавање).            |
| const textureLibrary[] | Назив .txd датотеке текстуре модела која се налази у models фолдеру сервера (подразумевана локација - artpath подешавање).              |

## Враћа

**1:** Функција је успешно извршена.

**0:** Функција није успела да се изврши.

## Examples

```c
public OnGameModeInit()
{
    AddCharModel(305, 20001, "lvpdpc2.dff", "lvpdpc2.txd");
    AddCharModel(305, 20002, "lapdpd2.dff", "lapdpd2.txd");
    return 1;
}
```

```c
AddCharModel(305, 20001, "lvpdpc2.dff", "lvpdpc2.txd");
AddCharModel(305, 20002, "lapdpd2.dff", "lapdpd2.txd");
```

## Белешке

:::tip

**useartwork** или **artwork.enable** морају бити омогућени у подешавањима сервера да би ово радило.

:::

:::warning

Тренутно нема ограничења када можете позвати ову функцију, али имајте на уму да ако је не позовете у [OnFilterScriptInit](../callbacks/OnFilterScriptInit)/[OnGameModeInit](../callbacks/OnGameModeInit), постоји ризик да неки играчи који су већ на серверу можда неће преузети моделе.

:::

## Повезане функције

- [SetPlayerSkin](SetPlayerSkin): Поставља скин играчу.
