---
title: OnPlayerText
sidebar_label: OnPlayerText
description: Fonksiyon, oyuncu sohbet mesajı gönderdiğinde çağrılır.
tags: ["player"]
---

## Açıklama

Fonksiyon, oyuncu sohbet mesajı gönderdiğinde çağrılır.

| Parametre | Açıklama                                 |
| --------- | ---------------------------------------- |
| playerid  | Sohbet mesajı gönderen oyuncunun ID'si.  |
| text[]    | Oyuncunun yazdığı metin.                 |

## Çalışınca Vereceği Sonuçlar

Her zaman Filterscript komutlarında ilk olarak çağrılır, bu nedenle 0 döndürmek diğer scriptlerin görmesini engeller. 

## örnekler

```c
public OnPlayerText(playerid, text[])
{
    new pText[144];
    format(pText, sizeof (pText), "(%d) %s", playerid, text);
    SendPlayerMessageToAll(playerid, pText);
    return 0; // varsayılan metni yoksay ve özel olanı gönder
}
```

## Notlar

<TipNPCCallbacks />

## Bağlantılı Fonksiyonlar

- [SendPlayerMessageToPlayer](../functions/SendPlayerMessageToPlayer): Bir oyuncuyu bir oyuncu için metin göndermeye zorlama. 
- [SendPlayerMessageToAll](../functions/SendPlayerMessageToAll): Bir oyuncuyu tüm oyunculara metin göndermeye zorlama. 
