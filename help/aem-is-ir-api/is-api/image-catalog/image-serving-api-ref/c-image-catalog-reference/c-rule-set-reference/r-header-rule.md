---
description: Elemento intestazione di risposta HTTP. Facoltativo negli elementi <rule>.
seo-description: Elemento intestazione di risposta HTTP. Facoltativo negli elementi <rule>.
seo-title: header
solution: Experience Manager
title: header
topic: Scene7 Image Serving - Image Rendering API
uuid: 89ec0f27-fc12-47c2-b9dd-e0ee768587b5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# header{#header}

Elemento intestazione di risposta HTTP. Facoltativo negli `<rule>` elementi.

## Attributi {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;**: Obbligatorio. Specifica il nome dell’intestazione HTTP.

**`Action`= &quot;set&quot;|`"add"`**: Facoltativo. Il valore predefinito è`"set"`, che sostituisce qualsiasi valore di intestazione corrente. Specificate`"add"`per aggiungere il valore dell’intestazione, separato da una virgola.

## Dati {#section-a387f541396c49d99c29692a38032914}

Valore intestazione.

## Descrizione {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Consente di aggiungere nuove intestazioni di risposta HTTP e di aggiungere o sostituire valori di intestazioni predefinite. I nomi e i valori devono essere conformi agli standard HTTP. Non verrà applicata alcuna codifica aggiuntiva.

Le variabili di sostituzione Image Server possono essere utilizzate nel nome dell’intestazione e nel valore dell’intestazione. Questo consente di controllare entrambe le stringhe dalla richiesta.

## Esempio {#section-cb5b738b9b93407cb2f4d35af3e59c02}

La regola seguente applica un&#39;intestazione personalizzata quando il valore dell&#39;intestazione è specificato nella richiesta come variabile:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Questa regola viene attivata dalla seguente richiesta, impostando l’intestazione della risposta HTTP `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
