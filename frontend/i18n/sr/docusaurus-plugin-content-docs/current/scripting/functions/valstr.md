---
title: valstr
sidebar_label: valstr
description: Претвара цео број у низ карактера.
tags: ["string"]
---

<LowercaseNoteSR />

## Опис

Претвара цео број у низ карактера.

## Парамтери

| Назив              | Опис                                       |
| ----------------- | ------------------------------------------------- |
| dest              | Одредиште за низ карактера.                    |
| value             | Вредност која се претвара у низ.                 |
| pack *(опционо)* | Да ли да се пакује одредиште (по дефаулту искључено). |

## Враћа

Ова функција не враћа никакве специфичне вредности.

## Примери

```c
new string[4];
new value = 250;
valstr(string, value); // string is now "250"
```

## Notes

:::warning

Прелазак високе вредности може изазвати замрзавање/крушење сервера. Постоје решења која су доступна. Испод је поправка коју можете директно поставити у ваш скрипт (пре него што било где користите valstr). [fixes.inc](https://github.com/pawn-lang/sa-mp-fixes) укључује ову поправку.


```c
// valstr fix by Slice
stock FIX_valstr(dest[], value, bool:pack = false)
{
    // format can't handle cellmin properly
    static const cellmin_value[] = !"-2147483648";

    if (value == cellmin)
        pack && strpack(dest, cellmin_value, 12) || strunpack(dest, cellmin_value, 12);
    else
        format(dest, 12, "%d", value), pack && strpack(dest, dest, 12);
}
#define valstr FIX_valstr
```

:::

## Повезане функције

- [strval](strval): Претвара стринг у цео број.
- [strcmp](strcmp): Поређење два стринга да би се проверило да ли су исти.
