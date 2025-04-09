---
title: ClearBanList
sidebar_label: ClearBanList
description: Брише бан листу.
tags: []
---

<VersionWarnSR version='omp v1.1.0.2612' />

## Опис

Брише бан листу.

## Враћа    

**true** - Успешно.

**false** - Неуспешно извршавање функције.

## Examples

```c
public OnPlayerCommandText(playerid, cmdtext[])
{
    if (!strcmp(cmdtext, "/clearbanlist", true))
    {
        if (!IsPlayerAdmin(playerid))
        {
            return 1;
        }

        ClearBanList();
        SendClientMessage(playerid, -1, "[SERVER]: Ban list cleared.");
        return 1;
    }
    return 0;
}
```

## Белешке

:::tip

Бан листу можете погледати у **bans.json** фајлу.

:::

## Повезане Функције

- [BlockIpAddress](BlockIpAddress): Блокира IP адресу за повезивање на сервер на одређени временски период.
- [UnBlockIpAddress](UnBlockIpAddress): Одблокира IP који је раније био блокиран.
- [Ban](Ban): Банује играча да игра на серверу.
- [BanEx](BanEx): Банује играча са прилагођеним разлогом.
- [Kick](Kick): Избацује играча са сервера.
- [IsBanned](IsBanned): Проверава да ли је одређена IP адреса банована.
