---
title: Localizzazione degli elementi dell’interfaccia utente
description: Alcuni contenuti visualizzati dal Visualizzatore immagini interattivo sono soggetti a localizzazione. Questo contenuto include le descrizioni comandi degli elementi dell’interfaccia utente e un messaggio informativo visualizzato dalla visualizzazione a comparsa al momento del caricamento.
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# Localizzazione degli elementi dell’interfaccia utente{#localization-of-user-interface-elements}

Alcuni contenuti visualizzati dal Visualizzatore immagini interattivo sono soggetti a localizzazione. Questo contenuto include le descrizioni comandi degli elementi dell’interfaccia utente e un messaggio informativo visualizzato dalla visualizzazione a comparsa al momento del caricamento.

Ogni contenuto testuale nel visualizzatore che può essere localizzato è rappresentato dallo speciale identificatore SDK del visualizzatore denominato SYMBOL. A qualsiasi SYMBOL è associato un valore di testo predefinito per le impostazioni internazionali inglesi ( `"en"`) fornito con il visualizzatore predefinito e possono essere impostati valori definiti dall’utente per tutte le impostazioni internazionali necessarie.

All&#39;avvio del visualizzatore, controlla le impostazioni internazionali correnti per vedere se esiste un valore definito dall&#39;utente per ogni SYMBOL supportato per tali impostazioni internazionali. In caso affermativo, utilizza il valore definito dall’utente; in caso contrario, torna al testo predefinito preconfigurato.

I dati di localizzazione definiti dall&#39;utente possono essere trasmessi al visualizzatore come oggetto JSON di localizzazione. Tale oggetto contiene l&#39;elenco delle impostazioni internazionali supportate, i valori di testo SYMBOL per ciascuna impostazione internazionale e le impostazioni internazionali predefinite.

Un esempio di tale oggetto di localizzazione è il seguente:

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
}, 
defaultLocale:"en" 
}
```

Nell’esempio precedente, l’oggetto di localizzazione definisce due impostazioni internazionali ( `"en"` e `"fr"`) e fornisce la localizzazione di due elementi dell’interfaccia utente in ciascuna impostazione internazionale.

Il codice della pagina web deve passare l’oggetto di localizzazione al costruttore del visualizzatore, come valore del campo `localizedTexts` dell’oggetto di configurazione. Un&#39;opzione alternativa consiste nel passare l&#39;oggetto di localizzazione chiamando il metodo `setLocalizedTexts(localizationInfo)` .

Sono supportati i seguenti SYMBOL:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SIMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione comandi per... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>Etichetta ARIA per l’elemento visualizzatore di livello principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del ruolo ARIA per il componente visualizzazione principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>Suggerimenti per l’utilizzo di ARIA per gli utenti di tastiera. </p> </td> 
  </tr> 
 </tbody> 
</table>
