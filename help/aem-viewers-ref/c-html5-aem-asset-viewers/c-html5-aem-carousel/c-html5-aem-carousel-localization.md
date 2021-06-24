---
description: Alcuni contenuti visualizzati nel visualizzatore carosello sono soggetti a localizzazione. Ciò include i pulsanti di spostamento delle diapositive.
solution: Experience Manager
title: Localizzazione degli elementi dell’interfaccia utente
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Developer,Business Practitioner
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Localizzazione degli elementi dell’interfaccia utente{#localization-of-user-interface-elements}

Alcuni contenuti visualizzati nel visualizzatore carosello sono soggetti a localizzazione. Ciò include i pulsanti di spostamento delle diapositive.

Ogni contenuto testuale nel visualizzatore che può essere localizzato è rappresentato dallo speciale identificatore SDK del visualizzatore denominato SYMBOL. A qualsiasi SYMBOL è associato un valore di testo predefinito per un’impostazione internazionale inglese ( `"en"`) fornito con il visualizzatore predefinito e possono essere impostati valori definiti dall’utente per tutte le impostazioni internazionali necessarie.

All&#39;avvio del visualizzatore, controlla le impostazioni internazionali correnti per vedere se esiste un valore definito dall&#39;utente per ogni SYMBOL supportato per tali impostazioni internazionali. In caso affermativo, utilizza il valore definito dall’utente; in caso contrario, torna al testo predefinito preconfigurato.

I dati di localizzazione definiti dall&#39;utente possono essere trasmessi al visualizzatore come oggetto JSON di localizzazione. Tale oggetto contiene l&#39;elenco delle impostazioni internazionali supportate, i valori di testo SYMBOL per ciascuna impostazione internazionale e le impostazioni internazionali predefinite.

Un esempio di tale oggetto di localizzazione è il seguente:

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
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
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Stato del pulsante Riproduci pausa selezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Stato del pulsante di pausa di riproduzione deselezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO  </span> </p> </td> 
   <td colname="col2"> <p> Descrizione comandi ed etichetta ARIA per i pulsanti di diapositiva precedente e successivo. </p> <p>Accetta due token di sostituzione: <span class="codeph"> $CURRENT_FRAME$ </span> per l'indice di diapositiva corrente e <span class="codeph"> $TOTAL_FRAMES$ </span> per il numero totale di diapositive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p> Etichetta ARIA per l’elemento visualizzatore di livello superiore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p> Descrizione del ruolo ARIA per il componente visualizzazione principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p> Suggerimenti per l’utilizzo di ARIA per gli utenti di tastiera. </p> </td> 
  </tr> 
 </tbody> 
</table>
