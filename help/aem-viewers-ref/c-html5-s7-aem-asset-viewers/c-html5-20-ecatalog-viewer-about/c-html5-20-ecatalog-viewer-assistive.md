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

---


# Supporto per tecnologie di assistenza{#assistive-technology-support}

Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l&#39;integrazione con tecnologie di supporto come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha ruolo `region` e `aria-label` attributo impostati sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di `Container.LABEL` localizzazione.

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39; `aria-label` attributo . Il valore dell&#39; `aria-label` attributo viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, l&#39; `aria-disabled` attributo viene impostato di conseguenza.

La visione principale ha un ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dal simbolo di `ROLE_DESCRIPTION` localizzazione del componente di visualizzazione principale corrispondente. I suggerimenti di navigazione per gli utenti della tastiera vengono forniti utilizzando `aria-describedby`, il testo per il suggerimento di utilizzo viene dal simbolo di `USAGE_HINT` localizzazione. Se una risorsa ha un&#39;etichetta definita nel campo UserData, l&#39; `aria-label` attributo è impostato con il valore di tale etichetta.

Le aree sensibili, le aree geografiche e le mappe immagine hanno il ruolo `button` e il testo descrittivo impostato con `aria-label` l&#39;attributo, con il valore dell&#39;etichetta di area sensibile o mappa immagine. Quando l&#39;utente mette a fuoco aree sensibili o mappe immagine, vengono forniti suggerimenti di navigazione per gli utenti della tastiera, `aria-describedby`con il testo del suggerimento relativo all&#39;utilizzo che proviene dal simbolo di `USAGE_HINT` localizzazione.

Le miniature hanno il ruolo `dialog` con `aria-label` attributo controllato dal simbolo di `ThumbnailGridView.LABEL` localizzazione. Le singole miniature hanno un ruolo `button`. Se è selezionata una miniatura, l&#39; `aria-selected` attributo viene impostato su `true`.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con `aria-label` l’attributo impostato sul valore del simbolo di `LABEL` localizzazione del componente. I singoli campioni hanno il ruolo `option` con `aria-setsize` e `aria-posinset` gli attributi per descrivere la posizione del campione nel set. Se viene selezionato un campione, l’ `aria-selected` attributo viene impostato su `true`.

Gli elenchi a discesa sono attivati dai pulsanti con `aria-haspopup` attributo aggiuntivo impostato su `true` e dall&#39; `aria-controls` attributo che fa riferimento all&#39;elemento del pannello a discesa effettivo. Il pannello a discesa stesso ha il ruolo `menu` di elementi secondari `menuitem`. A ciascuna voce di menu è stato specificato l&#39; `aria-label` attributo.

Le finestre di dialogo modali hanno il ruolo `dialog`. All&#39;elemento header della finestra di dialogo viene fatto riferimento dall&#39; `aria-labelledby` attributo.
