---
title: Attach3DTextLabelToPlayer
sidebar_label: Attach3DTextLabelToPlayer
description:  Прикачи 3D текст етикету на играча.
tags: ["player", "3dtextlabel"]
---

## Опис

Прикачи 3D текст етикету на играча.

| Назив          | Опис                                                           |
| ------------- | --------------------------------------------------------------------- |
| Text3D:textid | ID 3D текст етикете коју треба прикачити. Враћа се из Create3DTextLabel. |
| playerid      | 	ID играча на који треба прикачити етикету.                          |
| Float:offsetX | X офсет у односу на играча.                                         |
| Float:offsetY | Y офсет у односу на играча.                                         |
| Float:offsetZ | Z офсет у односу на играча.                                         |

## Враћа

**true** - Функција је успешно извршена.

**false** - Функција није успела да се изврши. То значи да играч и/или етикета не постоје.

## Примери

```c
public OnPlayerConnect(playerid)
{
    new Text3D:textLabel = Create3DTextLabel("Hello, I am new here!", 0x008080FF, 30.0, 40.0, 50.0, 40.0, 0);
    Attach3DTextLabelToPlayer(textLabel, playerid, 0.0, 0.0, 0.7);
    return 1;
}
```

## Повезане функције

- [Create3DTextLabel](Create3DTextLabel): Креира 3D текст етикету.
- [Delete3DTextLabel](Delete3DTextLabel): Брише 3D текст етикету.
- [Get3DTextLabelAttachedData](Get3DTextLabelAttachedData): Враћа податке о прикаченој 3D текст етикети.
- [Attach3DTextLabelToVehicle](Attach3DTextLabelToVehicle): Прикачи 3D текст етикету на возило.
- [Update3DTextLabelText](Update3DTextLabelText): Мења текст 3D текст етикете.
- [CreatePlayer3DTextLabel](CreatePlayer3DTextLabel): Креира 3D текст етикету за једног играча.
- [DeletePlayer3DTextLabel](DeletePlayer3DTextLabel): Брише 3D текст етикету играча.
- [UpdatePlayer3DTextLabelText](UpdatePlayer3DTextLabelText): Мења текст 3D текст етикете играча.
