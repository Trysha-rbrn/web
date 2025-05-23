---
title: OnPlayerLeaveRaceCheckpoint
sidebar_label: OnPlayerLeaveRaceCheckpoint
description: 当玩家离开竞速检查点时触发该回调函数。
tags: ["玩家", "检查点", "竞速检查点"]
---

## 描述

当玩家离开竞速检查点时触发该回调函数。

| 参数名   | 说明                   |
| -------- | ---------------------- |
| playerid | 离开竞速检查点的玩家ID |

## 返回值

该回调始终在滤镜脚本中优先触发

## 示例

```c
public OnPlayerLeaveRaceCheckpoint(playerid)
{
    printf("玩家 %d 离开了竞速检查点！", playerid);
    return 1;
}
```

## 注意事项

<TipNPCCallbacksZH_CN />

## 相关回调

以下回调函数可能与本回调相关：

- [OnPlayerEnterCheckpoint](OnPlayerEnterCheckpoint): 当玩家进入检查点时触发
- [OnPlayerLeaveCheckpoint](OnPlayerLeaveCheckpoint): 当玩家离开检查点时触发
- [OnPlayerEnterRaceCheckpoint](OnPlayerEnterRaceCheckpoint): 当玩家进入竞速检查点时触发

## 相关函数

以下函数可能与本回调函数相关：

- [SetPlayerCheckpoint](../functions/SetPlayerCheckpoint): 为玩家创建检查点
- [DisablePlayerCheckpoint](../functions/DisablePlayerCheckpoint): 禁用玩家的当前检查点
- [IsPlayerInCheckpoint](../functions/IsPlayerInCheckpoint): 检测玩家是否在检查点内
- [SetPlayerRaceCheckpoint](../functions/SetPlayerRaceCheckpoint): 为玩家创建竞速检查点
- [DisablePlayerRaceCheckpoint](../functions/DisablePlayerRaceCheckpoint): 禁用玩家的当前竞速检查点
- [IsPlayerInRaceCheckpoint](../functions/IsPlayerInRaceCheckpoint): 检测玩家是否在竞速检查点内
