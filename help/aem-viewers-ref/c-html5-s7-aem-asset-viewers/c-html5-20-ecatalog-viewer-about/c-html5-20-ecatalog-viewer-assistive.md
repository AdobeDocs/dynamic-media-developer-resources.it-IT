---
title: Supporto tecnologico per assistenza
description: Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Supporto tecnologico per assistenza{#assistive-technology-support}

Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L’elemento visualizzatore di livello superiore ha un ruolo `region` e `aria-label` impostato per impostazione predefinita sul nome del visualizzatore. Puoi controllare l’etichetta con la `Container.LABEL` simbolo di localizzazione.

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con il `aria-label` attributo. Il valore di `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, la funzione `aria-disabled` attributo viene impostato di conseguenza.

La vista principale ha un ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dalla `ROLE_DESCRIPTION` simbolo di localizzazione del componente di visualizzazione principale corrispondente. I suggerimenti per la navigazione degli utenti di tastiera vengono forniti utilizzando `aria-describedby`, il testo per il suggerimento di utilizzo proviene dal `USAGE_HINT` simbolo di localizzazione. Se una risorsa ha un&#39;etichetta definita nel campo UserData , la variabile `aria-label` attributo è impostato con il valore di tale etichetta.

Le aree calde, le aree geografiche e le mappe immagine hanno il ruolo `button` e testo descrittivo con `aria-label` attributo , con il valore dell&#39;etichetta dell&#39;area sensibile o della mappa immagine. Quando l&#39;utente mette a fuoco aree sensibili o mappe immagine, i suggerimenti di navigazione per gli utenti della tastiera sono forniti utilizzando `aria-describedby`, con il testo dell&#39;suggerimento di utilizzo proveniente dal `USAGE_HINT` simbolo di localizzazione.

Le miniature hanno il ruolo `dialog` con `aria-label` attributo controllato dal `ThumbnailGridView.LABEL` simbolo di localizzazione. Le singole miniature hanno un ruolo `button`. Se è selezionata una miniatura, questa viene `aria-selected` attributo impostato su `true`.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con `aria-label` impostato sul valore del `LABEL` simbolo di localizzazione del componente. Il ruolo dei singoli campioni `option` con `aria-setsize` e `aria-posinset` per descrivere la posizione del campione nel set. Se è selezionato un campione, ottiene il `aria-selected` attributo impostato su `true`.

Gli elenchi a discesa sono attivati da pulsanti con informazioni aggiuntive `aria-haspopup` attributo impostato su `true` e `aria-controls` attributo che fa riferimento all’elemento del pannello a discesa effettivo. Il pannello a discesa stesso ha il ruolo `menu` con sottoelementi aventi il ruolo `menuitem`. Ogni voce di menu ha `aria-label` attributo specificato.

Le finestre di dialogo modali hanno il ruolo `dialog`. L&#39;elemento di intestazione della finestra di dialogo è referenziato dal `aria-labelledby` attributo.
