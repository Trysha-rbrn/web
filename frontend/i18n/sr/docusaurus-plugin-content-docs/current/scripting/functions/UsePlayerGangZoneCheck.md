---
title: UsePlayerGangZoneCheck
sidebar_label: UsePlayerGangZoneCheck
description: Омогућава позивну функцију када играч уђе/напусти зону.
tags: ["player", "gangzone", "playergangzone"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Омогућава позивну функцију када играч уђе/напусти зону.

| Назив        | Опис                                                                                                   |
| ----------- | ------------------------------------------------------------------------------------------------------------- |
| playerid    | ID играча за којег желите да омогућите позивну функцију када играч уђе/напусти ову зону. |
| zoneid      | ID зоне играча за коју ће бити омогућена детекција подручја.                                                       |
| bool:enable | Да ли треба започети или зауставити детекцију улаза? (`true`/`false`).                                                |

## Враћа

**true** - Функција је успешно извршена.

**false** - Функција није успела да се изврши. Зона која је наведена не постоји.

## Примери

```c
// This variable is used to store the id of the gangzone
// so that we can use it throught the script
new gGangZoneID[MAX_PLAYERS] = {INVALID_GANG_ZONE, ...};

public OnPlayerConnect(playerid)
{
    // Create the gangzone
    gGangZoneID[playerid] = CreatePlayerGangZone(playerid, 2236.1475, 2424.7266, 2319.1636, 2502.4348);

    // Enabled the callback when a player enters/leaves this zone
    UsePlayerGangZoneCheck(playerid, gGangZoneID[playerid], true);
}

public OnPlayerEnterPlayerGangZone(playerid, zoneid)
{
    if (zoneid == gGangZoneID[playerid])
    {
        new string[64];
        format(string, sizeof(string), "You are entering player gangzone %i", zoneid);
        SendClientMessage(playerid, 0xFFFFFFFF, string);
    }
    return 1;
}

public OnPlayerLeavePlayerGangZone(playerid, zoneid)
{
    if (zoneid == gGangZoneID[playerid])
    {
        new string[64];
        format(string, sizeof(string), "You are leaving player gangzone %i", zoneid);
        SendClientMessage(playerid, 0xFFFFFFFF, string);
    }
    return 1;
}
```

## Повезани повратни позиви

Следећи повратни позиви могу бити корисни, јер су на неки начин повезани са овом функцијом.

- [OnPlayerEnterPlayerGangZone](../callbacks/OnPlayerEnterPlayerGangZone): Овај повратни позив се позива када играч уђе у зону играча.
- [OnPlayerLeavePlayerGangZone](../callbacks/OnPlayerLeavePlayerGangZone): Овај повратни позив се позива када играч напусти зону играча.

## Повезане функције

Следеће функције могу бити корисне, јер су на неки начин повезане са овом функцијом.

- [CreatePlayerGangZone](CreatePlayerGangZone): Креира зону играча.
- [PlayerGangZoneDestroy](PlayerGangZoneDestroy): Уништава зону играча.
- [PlayerGangZoneShow](PlayerGangZoneShow): Приказује зону играча.
- [PlayerGangZoneHide](PlayerGangZoneHide): Скрива зону играча.
- [PlayerGangZoneFlash](PlayerGangZoneFlash): Започиње трептање зоне играча.
- [PlayerGangZoneStopFlash](PlayerGangZoneStopFlash): Зауставља трептање зоне играча.
- [PlayerGangZoneGetFlashColour](PlayerGangZoneGetFlashColour): Добија боју трептања зоне играча.
- [PlayerGangZoneGetColour](PlayerGangZoneGetColour): Добија боју зоне играча.
- [PlayerGangZoneGetPos](PlayerGangZoneGetPos): Добија позицију зоне играча, представљену минималним и максималним X, Y координатама.
- [IsValidPlayerGangZone](IsValidPlayerGangZone): Проверава да ли је зона играча валидна.
- [IsPlayerInPlayerGangZone](IsPlayerInPlayerGangZone): Проверава да ли је играч у зони играча.
- [IsPlayerGangZoneVisible](IsPlayerGangZoneVisible): Проверава да ли је зона играча видљива.
