---
title: VehicleColourIndexToColour
sidebar_label: VehicleColourIndexToColour
description: Претвара индекс боје возила у HEX боју (RGBA формат).
tags: ["vehicle"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Претвара индекс боје возила у HEX боју (RGBA формат).

## Парамтери

| Name         | Description                                    |
|--------------|------------------------------------------------|
| index        | [Индекс боје возила](../resources/vehiclecolorid). |
| alpha = 0xFF | Алфа канал (провидност).                                 |

## Примери

```c
new colour = VehicleColourIndexToColour(3, 0xFF);
```

## Повезане функције

- [GetRandomVehicleColourPair](GetRandomVehicleColourPair): Генерише насумичне индексе боја који су валидни за дати модел возила.
- [GetVehicleColours](GetVehicleColours): Враћа боје тренутно постављене на возило.
