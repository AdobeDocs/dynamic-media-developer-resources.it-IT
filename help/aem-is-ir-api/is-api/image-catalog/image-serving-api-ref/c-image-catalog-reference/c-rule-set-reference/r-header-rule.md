---
description: Elemento intestazione di risposta HTTP. Facoltativo negli elementi <rule> .
solution: Experience Manager
title: header
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# header{#header}

Elemento intestazione di risposta HTTP. Facoltativo negli elementi `<rule>`.

## Attributi {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : Obbligatorio. Specifica il nome dell&#39;intestazione HTTP.

**`Action`= &quot;set&quot; |`"add"`**: Facoltativo. Il valore predefinito è `"set"`, che sostituisce qualsiasi valore di intestazione corrente. Specifica `"add"` per aggiungere il valore dell&#39;intestazione, separato da una virgola.

## Dati {#section-a387f541396c49d99c29692a38032914}

Valore di intestazione.

## Descrizione {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Consente di aggiungere nuove intestazioni di risposta HTTP e di aggiungere o sostituire valori di intestazioni predefinite. I nomi e i valori devono essere conformi agli standard HTTP. Non verrà applicata alcuna codifica aggiuntiva.

Le variabili di sostituzione di Image Server possono essere utilizzate nel nome dell&#39;intestazione e nel valore dell&#39;intestazione. Questo consente di controllare entrambe le stringhe dalla richiesta.

## Esempio {#section-cb5b738b9b93407cb2f4d35af3e59c02}

La regola seguente applica un’intestazione personalizzata quando il valore dell’intestazione è specificato nella richiesta come variabile:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Questa regola viene attivata dalla richiesta seguente, impostando l&#39;intestazione di risposta HTTP `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
