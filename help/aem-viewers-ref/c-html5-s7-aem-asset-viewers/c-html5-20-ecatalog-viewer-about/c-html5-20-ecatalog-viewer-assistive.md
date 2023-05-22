---
title: Supporto di tecnologie assistive
description: Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Supporto di tecnologie assistive{#assistive-technology-support}

Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L’elemento visualizzatore di primo livello ha il ruolo `region` e `aria-label` attributo impostato per impostazione predefinita sul nome del visualizzatore. Puoi controllare l’etichetta con `Container.LABEL` simbolo di localizzazione.

I pulsanti hanno il ruolo `button` e testo descrittivo impostato con `aria-label` attributo. Il valore di `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, il `aria-disabled` viene impostato di conseguenza.

La visualizzazione principale ha un ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito da `ROLE_DESCRIPTION` simbolo di localizzazione del componente della vista principale corrispondente. Gli hint di navigazione per gli utenti che utilizzano la tastiera sono forniti tramite `aria-describedby`, il testo per l’hint di utilizzo proviene da `USAGE_HINT` simbolo di localizzazione. Se per una risorsa è stata definita un’etichetta nel campo UserData, il `aria-label` viene impostato con il valore di tale etichetta.

I punti attivi, le aree geografiche e le mappe immagine hanno il ruolo `button` e set di testo descrittivo con `aria-label` con il valore dell&#39;area sensibile o dell&#39;etichetta della mappa immagine. Quando l’utente mette a fuoco gli hot spot o le mappe immagine, vengono forniti suggerimenti di navigazione per gli utenti che utilizzano la tastiera utilizzando `aria-describedby`, con il testo per l’hint di utilizzo proveniente dalla sezione `USAGE_HINT` simbolo di localizzazione.

Le miniature hanno il ruolo `dialog` con `aria-label` attributo controllato da `ThumbnailGridView.LABEL` simbolo di localizzazione. Le singole miniature hanno il ruolo `button`. Se è selezionata una miniatura, questa viene `aria-selected` attributo impostato su `true`.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con `aria-label` attributo impostato sul valore del `LABEL` simbolo di localizzazione del componente. I singoli campioni hanno il ruolo `option` con `aria-setsize` e `aria-posinset` attributi per descrivere la posizione del campione nel set. Se viene selezionato un campione, questo ottiene `aria-selected` attributo impostato su `true`.

Gli elenchi a discesa vengono attivati da pulsanti con `aria-haspopup` attributo impostato su `true` e `aria-controls` attributo che fa riferimento all’elemento effettivo del pannello a discesa. Il pannello a discesa ha il ruolo `menu` con sottoelementi che hanno il ruolo `menuitem`. Ogni voce di menu ha il `aria-label` attributo specificato.

Le finestre di dialogo modali hanno il ruolo `dialog`. L&#39;elemento intestazione della finestra di dialogo è indicato da `aria-labelledby` attributo.
