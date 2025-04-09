---
title: ToggleVehicleSirenEnabled
sidebar_label: ToggleVehicleSirenEnabled
description: Укључи или искључи сирену на возилу.
tags: ["vehicle"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Укључи или искључи сирену на возилу.

## Параметри

| Name         | Description                   |
|--------------|-------------------------------|
| vehicleid    | ID возила.    |
| bool:enabled | **true**: Укључено  - **false**: Искључено |

## Примери

```c
ToggleVehicleSirenEnabled(vehicleid, true);
```

## Повезане функције

- [GetVehicleSirenState](GetVehicleSirenState): Добија стање сирене на возилу.
- [GetPlayerSirenState](GetPlayerSirenState): Добија стање сирене на возилу играча.
