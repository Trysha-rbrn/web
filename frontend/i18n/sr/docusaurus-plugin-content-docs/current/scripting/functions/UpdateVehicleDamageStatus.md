---
title: UpdateVehicleDamageStatus
sidebar_label: UpdateVehicleDamageStatus
description: Поставља различите визуелне статусе оштећења возила, као што су прснуте гуме, покварена светла и оштећене панели.
tags: ["vehicle"]
---

:::tip

За неке корисне функције за рад са вредностима оштећења возила, погледајте [овде](../resources/damagestatus).

:::

## Опис

Поставља различите визуелне статусе оштећења возила, као што су прснуте гуме, покварена светла и оштећене панели.

## Параметри

| Назив                        | Опис                                       |
| --------------------------- | ------------------------------------------------- |
| vehicleid                   | ID возила за које се поставља оштећење.       |
| VEHICLE_PANEL_STATUS:panels | Скуп битова који садржи статус оштећења панела. |
| VEHICLE_DOOR_STATUS:doors   | Скуп битова који садржи статус оштећења врата.  |
| VEHICLE_LIGHT_STATUS:lights | Скуп битова који садржи статус оштећења светала. |
| VEHICLE_TIRE_STATUS:tires   | 	Скуп битова који садржи статус оштећења гума.  |

## Враћа

Ова функција не враћа никакве специфичне вредности.

## Примери

```c
new 
	VEHICLE_PANEL_STATUS:panels,
	VEHICLE_DOOR_STATUS:doors,
	VEHICLE_LIGHT_STATUS:lights,
	VEHICLE_TIRE_STATUS:tires;

GetVehicleDamageStatus(vehicleid, panels, doors, lights, tires);

tires = VEHICLE_TIRE_STATUS:15; // Setting tires to 15 will pop them all

// Or do it like this:
tires = (VEHICLE_TIRE_STATUS_FRONT_LEFT_POPPED | VEHICLE_TIRE_STATUS_FRONT_RIGHT_POPPED | VEHICLE_TIRE_STATUS_REAR_LEFT_POPPED | VEHICLE_TIRE_STATUS_REAR_RIGHT_POPPED);

UpdateVehicleDamageStatus(vehicleid, panels, doors, lights, tires);
```

## Повезане Функције

- [SetVehicleHealth](SetVehicleHealth): Поставља здравље возила.
- [GetVehicleHealth](GetVehicleHealth): Проверите здравље возила.
- [RepairVehicle](RepairVehicle): Потпуно поправља возило.
- [GetVehicleDamageStatus](GetVehicleDamageStatus): Добија стање оштећења возила за сваки део појединачно.

## Повезани Повратни Позиви

- [OnVehicleDamageStatusUpdate](../callbacks/OnVehicleDamageStatusUpdate): Позива се када се статус оштећења возила промени.

## Повезани Ресурси
<!--Mrzelo me da prevodim jbg..
Takodje treba umesto Povratnih poziva svugde da se pise povratne funkcije :)
God help me please >.<>
-->
- [Damage Status](../resources/damagestatus)
- [Vehicle Panel Status](../resources/vehicle-panel-status)
- [Vehicle Door Status](../resources/vehicle-door-status)
- [Vehicle Light Status](../resources/vehicle-light-status)
- [Vehicle Tire Status](../resources/vehicle-tire-status)
