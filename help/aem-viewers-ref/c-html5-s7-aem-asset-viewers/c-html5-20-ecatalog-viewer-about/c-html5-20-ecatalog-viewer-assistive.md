---
description: Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l'integrazione con tecnologie di supporto come gli assistenti vocali.
seo-description: Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l'integrazione con tecnologie di supporto come gli assistenti vocali.
seo-title: Supporto per tecnologie di assistenza
solution: Experience Manager
title: Supporto per tecnologie di assistenza
topic: Dynamic media
uuid: 8565383e-5c13-4af0-9b6e-2d583c18f19c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---


# Supporto per la tecnologia di assistenza{#assistive-technology-support}

Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l&#39;integrazione con tecnologie di supporto come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha l’attributo ruolo `region` e `aria-label` impostato sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di localizzazione `Container.LABEL`.

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label`. Il valore dell&#39;attributo `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, l&#39;attributo `aria-disabled` viene impostato di conseguenza.

La vista principale ha il ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dal simbolo di localizzazione `ROLE_DESCRIPTION` del componente di visualizzazione principale corrispondente. I suggerimenti di navigazione per gli utenti della tastiera sono forniti utilizzando `aria-describedby`, il testo per il suggerimento sull&#39;utilizzo proviene dal simbolo di localizzazione `USAGE_HINT`. Se una risorsa ha un&#39;etichetta definita nel campo UserData, l&#39;attributo `aria-label` viene impostato con il valore di tale etichetta.

Le aree sensibili, le aree geografiche e le mappe immagine hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label`, con il valore dell&#39;etichetta di area sensibile o mappa immagine. Quando l&#39;utente mette a fuoco aree sensibili o mappe immagine, i suggerimenti di navigazione per gli utenti della tastiera sono forniti utilizzando `aria-describedby`, con il testo per il suggerimento sull&#39;utilizzo proveniente dal simbolo di localizzazione `USAGE_HINT`.

Le miniature hanno il ruolo `dialog` con l&#39;attributo `aria-label` controllato dal simbolo di localizzazione `ThumbnailGridView.LABEL`. Le singole miniature hanno il ruolo `button`. Se è selezionata una miniatura, l&#39;attributo `aria-selected` viene impostato su `true`.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con l&#39;attributo `aria-label` impostato sul valore del simbolo di localizzazione `LABEL` di tale componente. I singoli campioni hanno il ruolo `option` con gli attributi `aria-setsize` e `aria-posinset` per descrivere la posizione dei campioni nel set. Se viene selezionato un campione, l&#39;attributo `aria-selected` viene impostato su `true`.

Gli elenchi a discesa sono attivati dai pulsanti con l&#39;attributo aggiuntivo `aria-haspopup` impostato su `true` e l&#39;attributo `aria-controls` che fa riferimento all&#39;elemento effettivo del pannello a discesa. Il pannello a discesa stesso ha il ruolo `menu` con elementi secondari con il ruolo `menuitem`. Per ogni voce di menu è specificato l&#39;attributo `aria-label`.

Le finestre di dialogo modali hanno il ruolo `dialog`. All&#39;elemento header della finestra di dialogo viene fatto riferimento dall&#39;attributo `aria-labelledby`.
