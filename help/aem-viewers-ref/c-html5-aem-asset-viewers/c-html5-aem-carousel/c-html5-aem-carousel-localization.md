---
title: Localizzazione degli elementi dell’interfaccia utente
description: Alcuni contenuti visualizzati nel visualizzatore carosello sono soggetti a localizzazione. Questo contenuto include pulsanti di spostamento tra le diapositive.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
TQID: 'https://experienceleague.adobe.com/frmjZyGwMg5FjUgGAIU9xgolVGEJ1nbnaMcJq5z33hw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 317
ht-degree: 0%

---

# Localizzazione degli elementi dell’interfaccia utente{#localization-of-user-interface-elements}

Alcuni contenuti visualizzati nel visualizzatore carosello sono soggetti a localizzazione. Questo contenuto include pulsanti di spostamento tra le diapositive.

Ogni contenuto testuale del visualizzatore che può essere localizzato è rappresentato dallo speciale identificatore SDK del visualizzatore denominato SYMBOL. Qualsiasi SYMBOL ha un valore di testo associato di default per una lingua inglese ( `"en"`) fornita con il visualizzatore predefinito e può anche avere valori definiti dall&#39;utente impostati per tutte le lingue necessarie.

All&#39;avvio, il visualizzatore controlla le impostazioni locali correnti per verificare se esiste un valore definito dall&#39;utente per ciascun SIMBOLO supportato per tali impostazioni locali. In caso affermativo, viene utilizzato il valore definito dall’utente; in caso contrario, viene utilizzato il testo predefinito.

I dati di localizzazione definiti dall’utente possono essere trasmessi al visualizzatore come oggetto JSON di localizzazione. Tale oggetto contiene l&#39;elenco delle impostazioni locali supportate, i valori di testo SYMBOL per ciascuna impostazione locale e le impostazioni locali predefinite.

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

Nell&#39;esempio precedente, l&#39;oggetto di localizzazione definisce due impostazioni locali ( `"en"` e `"fr"`) e fornisce la localizzazione per due elementi dell&#39;interfaccia utente in ciascuna impostazione locale.

Il codice della pagina Web deve passare l&#39;oggetto di localizzazione al costruttore del visualizzatore, come valore del campo `localizedTexts` dell&#39;oggetto di configurazione. In alternativa, passare l&#39;oggetto di localizzazione chiamando il metodo `setLocalizedTexts(localizationInfo)`.

Sono supportati i seguenti SIMBOLI:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SIMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione comando per... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Stato del pulsante Pausa di riproduzione selezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Stato del pulsante Pausa riproduzione non selezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> Descrizione comando ed etichetta ARIA per i pulsanti diapositiva precedente e successiva. </p> <p>Accetta due token di sostituzione: <span class="codeph"> $CURRENT_FRAME$ </span> per l'indice della diapositiva corrente e <span class="codeph"> $TOTAL_FRAMES$ </span> per il numero totale di diapositive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> Etichetta ARIA per l’elemento visualizzatore di primo livello. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> Descrizione del ruolo ARIA per il componente della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> Suggerimenti per l’utilizzo di ARIA per gli utenti che utilizzano la tastiera. </p> </td> 
  </tr> 
 </tbody> 
</table>
