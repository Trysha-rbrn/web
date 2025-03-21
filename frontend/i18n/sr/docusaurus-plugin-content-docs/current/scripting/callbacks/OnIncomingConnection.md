---
title: OnIncomingConnection
sidebar_label: OnIncomingConnection
description: Ова повратна функција се позива када IP адреса покуша да се повезе на сервер.
tags: []
---

## Опис

Ова повратна функција се позива када IP адреса покуша да се повезе на сервер. Да бисте блокирали долазне везе, користите [BlockIpAdress](../functions/BlockIpAddress)

| Име          | Опис                                               |
| ------------ | -------------------------------------------------- |
| playerid     | ID играча који покушава да се повезе.              |
| ip_address[] | IP адреса играча који покушава да се повезе.       |
| port         | Порт покушане везе.                                |

## Враћа

**1** - Спречиће да друге филтер скрипте приме ову повратну функцију.

**0** - Индицира да ће ова повратна функција бити прослеђена следећој филтер скрипти.

Увек се позива прва у филтер скриптама.

## Примери

```c
public OnIncomingConnection(playerid, ip_address[], port)
{
    printf("Incoming connection for player ID %i [IP/port: %s:%i]", playerid, ip_address, port);
    return 1;
}
```

## Повезане повратне функције

Следеће повратне функције могу бити корисне, јер су на неки начин повезане са овом повратном функцијом.

- [OnPlayerConnect](OnPlayerConnect): Ова повратна функција се позива када се играч повезује на сервер.
- [OnPlayerDisconnect](OnPlayerDisconnect): Ова повратна функција се позива када се играч дисконектује са сервера.
- [OnPlayerFinishedDownloading](OnPlayerFinishedDownloading): Ова повратна функција се позива када играч заврши са преузимањем прилагођених модела.

## Повезане функције

Следеће функције могу бити корисне, јер су на неки начин повезане са овом повратном функцијом.

- [BlockIpAddress](../functions/BlockIpAddress): Блокирајте IP адресу од повезивања на сервер на одређено време.
- [UnBlockIpAddress](../functions/UnBlockIpAddress): Отклоните блокаду IP адресе која је претходно била блокирана.
