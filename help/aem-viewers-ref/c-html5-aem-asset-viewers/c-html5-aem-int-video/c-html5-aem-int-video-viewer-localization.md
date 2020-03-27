---
description: Alcuni contenuti visualizzati dal visualizzatore video interattivo sono soggetti a localizzazione. Questo include le descrizioni comandi degli elementi dell'interfaccia utente e un messaggio di errore visualizzato quando il video non è in grado di essere riprodotto.
seo-description: Alcuni contenuti visualizzati dal visualizzatore video interattivo sono soggetti a localizzazione. Questo include le descrizioni comandi degli elementi dell'interfaccia utente e un messaggio di errore visualizzato quando il video non è in grado di essere riprodotto.
seo-title: Localizzazione degli elementi dell'interfaccia utente
solution: Experience Manager
title: Localizzazione degli elementi dell'interfaccia utente
topic: Dynamic media
uuid: 7c880e25-76dc-43d3-83fc-12de92afd35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Localizzazione degli elementi dell&#39;interfaccia utente{#localization-of-user-interface-elements}

Alcuni contenuti visualizzati dal visualizzatore video interattivo sono soggetti a localizzazione. Questo include le descrizioni comandi degli elementi dell&#39;interfaccia utente e un messaggio di errore visualizzato quando il video non è in grado di essere riprodotto.

Ogni contenuto testuale nel visualizzatore che può essere localizzato è rappresentato dallo speciale identificatore SDK del visualizzatore denominato SYMBOL. A ciascun SIMBOLO è associato un valore di testo predefinito per le impostazioni internazionali in lingua inglese ( `"en"`), fornito con il visualizzatore out-of-the-box, e possono essere impostati valori definiti dall’utente per tutte le impostazioni internazionali necessarie.

All&#39;avvio del visualizzatore, controlla le impostazioni internazionali correnti per verificare se esiste un valore definito dall&#39;utente per ciascun SIMBOLO supportato per tali impostazioni internazionali. In caso affermativo, utilizza il valore definito dall’utente; in caso contrario, torna al testo predefinito.

I dati di localizzazione definiti dall&#39;utente possono essere passati al visualizzatore come oggetto JSON di localizzazione. Tale oggetto contiene l&#39;elenco delle impostazioni internazionali supportate, i valori di testo SYMBOL per ciascuna impostazione internazionale e le impostazioni internazionali predefinite.

Un esempio di tale oggetto di localizzazione è il seguente:

```
{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

Nell&#39;esempio precedente, l&#39;oggetto localization definisce due impostazioni internazionali ( `"en"` e `"fr"`) e fornisce la localizzazione per due elementi dell&#39;interfaccia utente in ciascuna lingua.

Il codice della pagina Web deve trasmettere l&#39;oggetto di localizzazione al costruttore del visualizzatore, come valore del `localizedTexts` campo dell&#39;oggetto di configurazione. Un&#39;opzione alternativa consiste nel passare l&#39;oggetto di localizzazione chiamando il `setLocalizedTexts(localizationInfo)` metodo .

Sono supportati i seguenti SIMBOLI:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SIMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione comandi per... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>Etichetta ARIA per l’elemento visualizzatore di livello principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> Stato del pulsante Riproduci pausa selezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Stato pulsante Riproduci pausa deselezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY </span> </p> </td> 
   <td colname="col2"> <p> Riproduci lo stato del pulsante Pausa di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Scorrimento video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Tempo video sulla barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MablesVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> Volume modificabile selezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MablesVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Volume variabile deselezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MablesVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p> Etichetta della manopola del dispositivo di scorrimento del volume esposta tramite l'attributo ARIA <span class="codeph"> aria-value </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Pulsante a schermo intero in stato normale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Pulsante a schermo intero nello stato a schermo intero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> Stato del pulsante dei sottotitoli codificati selezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p> Stato del pulsante per sottotitoli codificati deselezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InteractiveSwatches.BANNER </span> </p> </td> 
   <td colname="col2"> <p>Didascalia per il banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Pulsante Scorri verso l’alto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Pulsante Scorri verso il basso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Strumento Condivisione social network. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Pulsante di condivisione collegamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Intestazione della finestra di dialogo Collegamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Pulsante Chiudi della finestra di dialogo Collega, in alto a destra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del collegamento di condivisione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Didascalia per il pulsante Annulla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Pulsante Annulla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Didascalia per il pulsante Seleziona tutto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Fate clic sul pulsante Tutti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Pulsante Condivisione Facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Pulsante Condividi su Twitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Pulsante Chiudi del pannello delle azioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR </span> </p> </td> 
   <td colname="col2"> <p>Messaggio di errore che viene visualizzato quando non è possibile riprodurre il video. </p> </td> 
  </tr> 
 </tbody> 
</table>

