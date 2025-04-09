---
title: ApplyActorAnimation
sidebar_label: ApplyActorAnimation
description: Примењује анимацију на актора.
tags: ["actor", "animation"]
---

<VersionWarnSR version='SA-MP 0.3.7' />

## Опис

Примењује анимацију на актора.

## Параметри

| Назив                     | Опис                                                                                                                                                                                            |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| actorid                  | ID актора на ког се примењује анимација.                                                                                                                                                         |
| const animationLibrary[] | Име анимационе библиотеке из које се узима анимација.                                                                                                                                                |
| const animationName[]    | Име анимације која се примењује из наведене библиотеке.                                                                                                                                      |
| float:delta              | Брзина којом се анимација пушта (користити 4.1).                                                                                                                                                             |
| bool:loop                | Ако је true, анимација ће се понављати у петљи. Ако је false, одиграће се једном.                                                                                                                |
| bool:lockX               | Ако је false, актор се након анимације враћа на претходну X координату (за анимације које померају актора, као што је ходање). Ако је true, остаје на новој позицији. |
| bool:lockY               | Исто као и lockX, али за Y осу. Треба да буде исто као и претходни параметар.                                                                                                                   |
| bool:freeze              | Ако је true, актор ће остати у последњем кадру анимације. Ако је false, неће.                                                                                                                 |
| time                     |Тајмер у милисекундама. За бесконачну петљу користити 0.                                                                                                                                         |

## Враћа

**true** - Функција је успешно извршена.

**false** - Функција није извршена (актор не постоји).

## Примери

```c
new gMyActor;

public OnGameModeInit()
{
    gMyActor = CreateActor(179, 316.1, -134.0, 999.6, 90.0); // Actor as salesperson in Ammunation
    ApplyActorAnimation(gMyActor, "DEALER", "shop_pay", 4.1, false, false, false, false, 0); // Pay anim
    return 1;
}

public OnPlayerConnect(playerid)
{
    // Preload the 'DEALER' animation library for the player
    ApplyAnimation(playerid, "DEALER", "null", 4.1, false, false, false, false, 0);
    return 1;
}
```

## Белешке

:::tip

Морате прво преучитати анимациону библиотеку за играча који гледа актора, а не за самог актора. У супротном, анимација неће бити примењена док функција поново не буде извршена.

:::

## Повезане функције

- [ClearActorAnimations](ClearActorAnimations): Уклања све анимације које су примењене на актора.
- [GetActorAnimation](GetActorAnimation): Враћа тренутну анимацију коју актор изводи.
