---
title: VehicleCanHaveComponent
sidebar_label: VehicleCanHaveComponent
description: Да ли је компонента дозвољена на моделу возила?
tags: ["vehicle"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Да ли је компонента дозвољена на датом моделу возила?

## Парамтери

| Name                                     | Description                   |
| ---------------------------------------- | ----------------------------- |
| [modelid](../resources/vehicleid)       | ID модела возила              |
| [component](../resources/carcomponentid) | 	ID компоненте коју проверавамо на возилу |

## Враћа

**true** - Компонента је дозвољена на возилу.

**false** - Компонента није дозвољена на возилу.

## Примери

```c
new vehicleid = GetPlayerVehicleID(playerid);

if (VehicleCanHaveComponent(GetVehicleModel(vehicleid), 1010))
{
    SendClientMessage(playerid, 0x00FF00FF, "Nitro is legal on this vehicle.");
}
else
{
    SendClientMessage(playerid, 0xFF0000FF, "Nitro is illegal on this vehicle.");
}
```

## Повезане функције

- [AddVehicleComponent](AddVehicleComponent): Додаје компоненту возилу.
- [RemoveVehicleComponent](RemoveVehicleComponent): Уклања компоненту са возила.
- [GetVehicleComponentInSlot](GetVehicleComponentInSlot): Проверава коју компоненту возило има у одређеном слоту.
- [GetVehicleComponentType](GetVehicleComponentType): Враћа тип компоненте на основу ID-а.

## Повезани ресурси

- [ID-еви компоненти возила](../resources/carcomponentid)
