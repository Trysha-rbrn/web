---
title: IsPlayerNPC
sidebar_label: IsPlayerNPC
description: Проверава да ли је играч прави или NPC.
tags: ["player", "npc"]
---

## Опис

Проверава да ли је играч прави или NPC.

## Парамтери 

| Назив     | Опис                 |
| -------- | --------------------------- |
| playerid | ID играча који се проверава. |

## Враћа

**true**: Играч је NPC.

**false**: Играч није NPC.

## Примери

```c
public OnPlayerConnect(playerid)
{
    if (IsPlayerNPC(playerid))
    {
        SendClientMessageToAll(-1, "An NPC connected!");
        return 1;
    }

    // Даљи код неће бити извршен уколико 'playerid' није играч
}
```

## Повезане функције

- [ConnectNPC](ConnectNPC.md): Повезује NPC-a.
- [IsPlayerAdmin](IsPlayerAdmin.md): Проверава да ли је играч повезан на RCON.
