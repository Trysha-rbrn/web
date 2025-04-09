---
title: UseGangZoneCheck
sidebar_label: UseGangZoneCheck
description: Омогућава позивну функцију када играч уђе/напусти ову зону.
tags: ["player", "gangzone"]
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Омогућава позивну функцију када играч уђе/напусти ову зону.

| Назив        | Опис                                                    |
| ----------- | -------------------------------------------------------------- |
| zoneid      | ID зоне за коју ће бити омогућена детекција подручја.               |
| bool:enable | Да ли треба започети или зауставити детекцију улаза? (`true`/`false`) |

## Враћа

**1:** - Функција је успешно извршена.

**0:** - Функција није успела да се изврши. Зона која је наведена не постоји.

## Примери

```c
new gGangZoneID = INVALID_GANG_ZONE;

public OnGameModeInit()
{
    gGangZoneID = GangZoneCreate(1248.011, 2072.804, 1439.348, 2204.319);

    // Enabled the callback when a player enters/leaves this zone
    UseGangZoneCheck(gGangZoneID, true);
}

public OnPlayerEnterGangZone(playerid, zoneid)
{
    if (zoneid == gGangZoneID)
    {
        new string[64];
        format(string, sizeof(string), "You are entering gangzone %i", zoneid);
        SendClientMessage(playerid, 0xFFFFFFFF, string);
    }
    return 1;
}

public OnPlayerLeaveGangZone(playerid, zoneid)
{
    if (zoneid == gGangZoneID)
    {
        new string[64];
        format(string, sizeof(string), "You are leaving gangzone %i", zoneid);
        SendClientMessage(playerid, 0xFFFFFFFF, string);
    }
    return 1;
}
```

## Повезане повратне функције

Следеће повратне функције могу бити корисне, јер су на неки начин повезане са овом функцијом.

- [OnPlayerEnterGangZone](../callbacks/OnPlayerEnterGangZone): Овај повратни позив се позива када играч уђе у зону.
- [OnPlayerLeaveGangZone](../callbacks/OnPlayerLeaveGangZone): Овај повратни позив се позива када играч напусти зону.

## Повезане функције

Следеће функције могу бити корисне, јер су на неки начин повезане са овом функцијом.

- [GangZoneCreate](GangZoneCreate): Креира зону.
- [GangZoneDestroy](GangZoneDestroy): Уништава зону.
- [GangZoneShowForPlayer](GangZoneShowForPlayer): Приказује зону за играча.
- [GangZoneShowForAll](GangZoneShowForAll): Приказује зону за све играче.
- [GangZoneHideForPlayer](GangZoneHideForPlayer): Скрива зону за играча.
- [GangZoneHideForAll](GangZoneHideForAll): Скрива зону за све играче.
- [GangZoneFlashForPlayer](GangZoneFlashForPlayer): Узрокује да зона трепће за играча.
- [GangZoneFlashForAll](GangZoneFlashForAll): Узрокује да зона трепће за све играче.
- [GangZoneStopFlashForPlayer](GangZoneStopFlashForPlayer): Зауставља трептање зоне за играча.
- [GangZoneStopFlashForAll](GangZoneStopFlashForAll): Зауставља трептање зоне за све играче.
- [IsValidGangZone](IsValidGangZone): Проверава да ли је зона валидна.
- [IsPlayerInGangZone](IsPlayerInGangZone): Проверава да ли је играч у зони.
- [IsGangZoneVisibleForPlayer](IsGangZoneVisibleForPlayer): Проверава да ли је зона видљива за играча.