---
title: DisableMenuRow
sidebar_label: DisableMenuRow
description: Disable a specific row in a menu for all players.
tags: ["menu"]
---

## คำอธิบาย

Disable a specific row in a menu for all players. It will be greyed-out and can't be selected by players.

| Name        | Description                                                                                                       |
| ----------- | ----------------------------------------------------------------------------------------------------------------- |
| Menu:menuid | The ID of the menu to disable a row of. Ensure this is valid, as an invalid menu ID will crash the entire server. |
| row         | The ID of the row to disable (rows start at 0).                                                                   |

## ส่งคืน

This function always returns 1, even if the function fails. If an invalid row is specified, nothing will happen. If an invalid menu ID is specified, the server will crash.

## ตัวอย่าง

```c
new Menu:WeaponMenu;

WeaponMenu = CreateMenu("Weapons", 1, 50.0, 180.0, 200.0, 200.0);
AddMenuItem(WeaponMenu, 0, "Rocket Launcher");
AddMenuItem(WeaponMenu, 0, "Flamethrower");
AddMenuItem(WeaponMenu, 0, "Minigun");
AddMenuItem(WeaponMenu, 0, "Grenades");
if (!strcmp(cmdtext, "/disablemenu", true))
{
    DisableMenuRow(WeaponMenu, 2); //Disable the "Minigun" row
    return 1;
}
```

## บันทึก

:::tip

Crashes when passed an invalid menu ID. This function disabled the specified menu row for all players. There is no function to disable a menu row for a specific player. You'd have to create two menus - one with a row disabled, and one without. Or one per player.

:::

## ฟังก์ชั่นที่เกี่ยวข้องกัน

- [CreateMenu](../../scripting/functions/CreateMenu.md): Create a menu.
- [DestroyMenu](../../scripting/functions/DestroyMenu.md): Destroy a menu.
- [AddMenuItem](../../scripting/functions/AddMenuItem.md): Add an item to a menu.
