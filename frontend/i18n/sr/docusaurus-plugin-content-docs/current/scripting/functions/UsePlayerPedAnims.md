---
title: UsePlayerPedAnims
sidebar_label: UsePlayerPedAnims
description: Користи стандардну анимацију ходања играча (анимација CJ skin-а) уместо прилагођених анимација за сваки skin (нпр. клизање за skin-у скејтера).
tags: ["player"]
---

## Опис

Користи стандардну анимацију ходања играча (анимација CJ skin-а) уместо прилагођених анимација за сваки skin (нпр. клизање за skin-у скејтера).

## Примери

```c
public OnGameModeInit()
{
    UsePlayerPedAnims();
    return 1;
}
```

## Белешке

:::tip

Ова функција ради само када се постави испод [OnGameModeInit](../callbacks/OnGameModeInit).

Немогућност коришћења ове функције доводи до тога да се двоструко руковане оружје (не двоструко оружје - једно оружје које се држи са обе руке) држи само у једној руци.

:::

:::tip

Такође можете омогућити стандардну анимацију ходања играча преко [config.json](../../server/config.json)

```json
"use_player_ped_anims": true,
```

:::

## Повезане функције

- [ApplyAnimation](ApplyAnimation): Примените анимацију на играча.
- [ClearAnimations](ClearAnimations): Очистите све анимације које играч изводи.
