---
title: OnPlayerUpdate
sidebar_label: OnPlayerUpdate
description: This callback is called every time a client/player updates the server with their status.
tags: ["player"]
---

## คำอธิบาย

This callback is called every time a client/player updates the server with their status. It is often used to create custom callbacks for client updates that aren't actively tracked by the server, such as health or armor updates or players switching weapons.

| Name     | Description                                |
| -------- | ------------------------------------------ |
| playerid | ID of the player sending an update packet. |

## ส่งคืน

0 - Update from this player will not be replicated to other clients.

1 - Indicates that this update can be processed normally and sent to other players.

มันถูกเรียกในฟิลเตอร์สคริปต์ก่อนเสมอ

## ตัวอย่าง

```c
public OnPlayerUpdate(playerid)
{
    new iCurWeap = GetPlayerWeapon(playerid); // Return the player's current weapon
    if (iCurWeap != GetPVarInt(playerid, "iCurrentWeapon")) // If he changed weapons since the last update
    {
        // Lets call a callback named OnPlayerChangeWeapon
        OnPlayerChangeWeapon(playerid, GetPVarInt(playerid, "iCurrentWeapon"), iCurWeap);
        SetPVarInt(playerid, "iCurrentWeapon", iCurWeap);//Update the weapon variable
    }
    return 1; // Send this update to other players.
}

stock OnPlayerChangeWeapon(playerid, oldweapon, newweapon)
{
    new     s[128],
        oWeapon[24],
        nWeapon[24];

    GetWeaponName(oldweapon, oWeapon, sizeof(oWeapon));
    GetWeaponName(newweapon, nWeapon, sizeof(nWeapon));

    format(s, sizeof(s), "You changed weapon from %s to %s!", oWeapon, nWeapon);

    SendClientMessage(playerid, 0xFFFFFFFF, s);
}
public OnPlayerUpdate(playerid)
{
    new Float:fHealth;

    GetPlayerHealth(playerid, fHealth);

    if (fHealth != GetPVarFloat(playerid, "faPlayerHealth"))
    {
        // Player health has changed since the last update -> server, so obviously thats the thing updated.
        // Lets do further checks see if he's lost or gained health, anti-health cheat? ;)

        if (fHealth > GetPVarFloat(playerid, "faPlayerHealth"))
        {
            /* He has gained health! Cheating? Write your own scripts here to figure how a player
            gained health! */
        }
        else
        {
            /* He has lost health! */
        }

        SetPVarFloat(playerid, "faPlayerHealth", fHealth);
    }
}
```

## บันทึก

:::tip

NPC สามารถเรียก Callback นี้ได้

:::

:::warning

This callback is called, on average, 30 times per second, per player; only use it when you know what it's meant for (or more importantly what it's NOT meant for). The frequency with which this callback is called for each player varies, depending on what the player is doing. Driving or shooting will trigger a lot more updates than idling.

:::

## ฟังก์ชั่นที่เกี่ยวข้องกัน
