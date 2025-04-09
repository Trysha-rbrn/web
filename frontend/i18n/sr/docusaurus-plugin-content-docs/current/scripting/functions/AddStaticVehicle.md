---
title: AddStaticVehicle
sidebar_label: AddStaticVehicle
description: Додаје 'статично' возило (модели се учитавају унапред за играче) у gamemode-у.
tags: ["vehicle"]
---

## Опис

Додаје 'статично' возило (модели се учитавају унапред за играче) у gamemode-у.

## Параметри

| Назив                                   | Опис                                             |
| -------------------------------------- | ------------------------------------------------------- |
| spawnX                                 | [Модел ID](../resources/vehicleid) возила које се креира. |
| Float:spawnX                           | X координата на којој се возило спаунује.                       |
| Float:spawnY                           | Y координата на којој се возило спаунује.                       |
| Float:spawnZ                           | Z координата на којој се возило спаунује.                       |
| Float:angle                            | Угао под којим ће возило бити окренуто.                           |
| [colour1](../resources/vehiclecolorid) | Примарна боја возила. -1 за насумичну боју.                   |
| [colour2](../resources/vehiclecolorid) | Секундарна боја возила. -1 за насумичну боју.                 |

## Враћа

ID возила које је креирано (између 1 и MAX_VEHICLES).

INVALID_VEHICLE_ID (65535) ако возило није креирано (достигнута граница возила или прослеђен неважећи ID модела).

## Примери

```c
public OnGameModeInit()
{
    // Add a Hydra to the game
    AddStaticVehicle(520, 2109.1763, 1503.0453, 32.2887, 82.2873, 0, 1);

    return 1;
}
```

## Повезане функције

- [AddStaticVehicleEx](AddStaticVehicleEx): Додаје статично возило са прилагођеним временом респауна.
- [CreateVehicle](CreateVehicle): Креира возило.
- [DestroyVehicle](DestroyVehicle): Уништава возило.
- [GetVehicleParamsSirenState](GetVehicleParamsSirenState): Проверава да ли је сирена на возилу укључена.
- [SetVehicleSpawnInfo](SetVehicleSpawnInfo):  Подешава модел, локацију спауна, боје, респаун време и ентеријер.
- [GetVehicleSpawnInfo](GetVehicleSpawnInfo): Узима информације о месту спауна возила и његовим бојама.
- [ChangeVehicleColours](ChangeVehicleColours): Мења примарну и секундарну боју возила.
- [GetVehicleColours](GetVehicleColours): Узима боје возила.
- [SetVehicleRespawnDelay](SetVehicleRespawnDelay): Подешава време након којег се возило респаунује.
- [GetVehicleRespawnDelay](GetVehicleRespawnDelay): Узима подешено време респауна возила.

## Повезане повратне функције

- [OnVehicleSpawn](../callbacks/OnVehicleSpawn): Позива се када се возило респаунује.
- [OnVehicleSirenStateChange](../callbacks/OnVehicleSirenStateChange): Позива се када се сирена на возилу укључи или искључи.

## Повезани ресурси

- [Модели возила](../resources/vehicleid): Комплетна листа свих возила у игри.
- [ID-еви боја возила](../resources/vehiclecolorid): Листа ID-ева боја возила.
