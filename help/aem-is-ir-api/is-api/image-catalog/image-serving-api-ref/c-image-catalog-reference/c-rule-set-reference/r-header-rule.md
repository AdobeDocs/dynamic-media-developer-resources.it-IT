---
title: intestazione
description: Elemento intestazione di risposta HTTP. Facoltativo negli elementi <rule>.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---

# intestazione{#header}

Elemento intestazione di risposta HTTP. Facoltativo negli elementi `<rule>`.

## Attributi {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : obbligatorio. Specifica il nome dell&#39;intestazione HTTP.

**`Action`= &quot;set&quot; |`"add"`**: facoltativo. Il valore predefinito è `"set"`, che sostituisce qualsiasi valore di intestazione corrente. Specificare `"add"` in modo da poter aggiungere il valore dell&#39;intestazione, separato da una virgola.

## Dati {#section-a387f541396c49d99c29692a38032914}

Valore intestazione.

## Descrizione {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Consente di aggiungere nuove intestazioni di risposta HTTP e di aggiungere o sostituire valori di intestazioni predefinite. I nomi e i valori devono essere conformi agli standard HTTP. Nessuna codifica aggiuntiva applicata.

Le variabili di sostituzione Image Server possono essere utilizzate nel nome e nel valore dell’intestazione. Questo consente di controllare entrambe le stringhe dalla richiesta.

## Esempio {#section-cb5b738b9b93407cb2f4d35af3e59c02}

La regola seguente applica un’intestazione personalizzata quando il valore dell’intestazione è specificato nella richiesta come variabile:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Questa regola viene attivata dalla seguente richiesta, impostando l&#39;intestazione di risposta HTTP `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
