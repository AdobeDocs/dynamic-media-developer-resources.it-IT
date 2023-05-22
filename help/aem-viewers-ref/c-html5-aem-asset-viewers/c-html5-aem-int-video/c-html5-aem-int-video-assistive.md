---
title: Supporto di tecnologie assistive
description: Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Supporto di tecnologie assistive{#assistive-technology-support}

Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L’elemento visualizzatore di primo livello ha il ruolo `region` e `aria-label` attributo impostato per impostazione predefinita sul nome del visualizzatore. Puoi controllare l’etichetta con `Container.LABEL` simbolo di localizzazione.

I pulsanti hanno il ruolo `button` e set di testo descrittivo con `aria-label` attributo. Il valore di `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, `aria-disabled` viene impostato di conseguenza.

I componenti cursore hanno il ruolo `slider` con attributi `aria-valuenow`, `aria-valuemin`, e `aria-valuemax` per descrivere la posizione corrente del cursore.

Le miniature hanno il ruolo `dialog` con `aria-label` attributo controllato da `ThumbnailGridView.LABEL` simbolo di localizzazione. Le singole miniature hanno il ruolo `button`. Se è selezionata una miniatura, questa viene `aria-selected` attributo impostato su `true`.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con `aria-label` attributo impostato sul valore del `LABEL` simbolo di localizzazione del componente. I singoli campioni hanno il ruolo `option` con `aria-setsize` e `aria-posinset` attributi per descrivere la posizione del campione nel set. Se viene selezionato un campione, questo ottiene `aria-selected` attributo impostato su `true`.

Gli elenchi a discesa vengono attivati da pulsanti con `aria-haspopup` attributo impostato su `true` e `aria-controls` attributo che fa riferimento all’elemento effettivo del pannello a discesa. Il pannello a discesa ha il ruolo `menu` con sottoelementi che hanno il ruolo `menuitem`. Ogni voce di menu ha il `aria-label` attributo specificato.

Le finestre di dialogo modali hanno il ruolo `dialog`. L&#39;elemento intestazione della finestra di dialogo è indicato da `aria-labelledby` attributo.
