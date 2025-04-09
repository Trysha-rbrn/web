---
title: AreAllAnimationsEnabled
sidebar_label: AreAllAnimationsEnabled
description: Да ли су омогућене анимације које недостају у неким верзијама?
tags: ["animation"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Проверава да ли су омогућене све анимације, укључујући оне које недостају у појединим верзијама.

## Враћа

**true**: Омогућене су.

**false**: Није омогућено.

## Примери

```c
if (AreAllAnimationsEnabled())
{
    // Изврши неку радњу
}
```

## Повезане функције

- [EnableAllAnimations](EnableAllAnimations): Омогућава коришћење анимација које недостају у неким верзијама.
- [ApplyAnimation](ApplyAnimation): Примењује анимацију на играча.
- [ClearAnimations](ClearAnimations): Уклања све анимације које играч изводи.

## Повезани ресурси

- [Анимације](../resources/animations)
