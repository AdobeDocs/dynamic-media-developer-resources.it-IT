---
title: Localizzazione degli elementi dell’interfaccia utente
description: Alcuni contenuti visualizzati dal visualizzatore a comparsa sono soggetti a localizzazione. Questo contenuto include le descrizioni comandi degli elementi dell’interfaccia utente e i messaggi informativi visualizzati dalla visualizzazione a comparsa al momento del caricamento.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 57941e90-1462-43e6-80db-6b111e004f9b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Localizzazione degli elementi dell’interfaccia utente{#localization-of-user-interface-elements}

Alcuni contenuti visualizzati dal visualizzatore a comparsa sono soggetti a localizzazione. Questo contenuto include le descrizioni comandi degli elementi dell’interfaccia utente e i messaggi informativi visualizzati dalla visualizzazione a comparsa al momento del caricamento.

Ogni contenuto testuale nel visualizzatore che può essere localizzato è rappresentato da uno speciale identificatore SDK del visualizzatore denominato SYMBOL. A qualsiasi SYMBOL è associato un valore di testo predefinito per le impostazioni internazionali inglesi ( `"en"`) fornita con il visualizzatore predefinito. Può anche avere valori definiti dall&#39;utente impostati per tutte le impostazioni internazionali necessarie.

All’avvio del visualizzatore, controlla le impostazioni internazionali correnti per vedere se esiste un valore definito dall’utente per ogni SYMBOL supportato per le impostazioni internazionali. In caso affermativo, utilizza il valore definito dall’utente; in caso contrario, torna al testo predefinito preconfigurato.

I dati di localizzazione definiti dall&#39;utente possono essere trasmessi al visualizzatore come oggetto JSON di localizzazione. Tale oggetto contiene l&#39;elenco delle impostazioni internazionali supportate, i valori di testo SYMBOL per ciascuna impostazione internazionale e le impostazioni internazionali predefinite.

Un esempio di tale oggetto di localizzazione è il seguente:

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
}, 
defaultLocale:"en" 
}
```

Nell’esempio precedente, l’oggetto di localizzazione definisce due impostazioni internazionali ( `"en"` e `"fr"`) e fornisce la localizzazione di due elementi dell&#39;interfaccia utente in ciascuna impostazione internazionale.

Il codice della pagina web deve passare l’oggetto di localizzazione al costruttore del visualizzatore, come valore del `localizedTexts` campo dell&#39;oggetto di configurazione. Un&#39;opzione alternativa è quella di passare l&#39;oggetto di localizzazione chiamando il `setLocalizedTexts(localizationInfo)` metodo .

Sono supportati i seguenti SYMBOL:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SIMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>Etichetta ARIA per l’elemento visualizzatore di livello principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del ruolo ARIA per il componente visualizzazione principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Suggerimenti per l’utilizzo di ARIA per gli utenti di tastiera. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Visualizzazione zoom a comparsa.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>Messaggio informativo per i sistemi desktop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Visualizzazione zoom a comparsa.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>Messaggio informativo per i dispositivi touch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante di scorrimento a sinistra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante di scorrimento a destra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante di scorrimento verso l'alto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante di scorrimento verso il basso. </p> </td> 
  </tr> 
 </tbody> 
</table>
