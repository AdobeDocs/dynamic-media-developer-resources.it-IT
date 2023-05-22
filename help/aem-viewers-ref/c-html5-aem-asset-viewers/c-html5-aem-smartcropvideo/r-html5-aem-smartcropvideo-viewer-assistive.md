---
title: Supporto di tecnologie assistive
description: Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
exl-id: b2bfd93b-707e-4a03-a14e-14ec23328fdd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Supporto di tecnologie assistive{#assistive-technology-support}

Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L’elemento visualizzatore di primo livello ha il ruolo `region` e `aria-label` attributo impostato per impostazione predefinita sul nome del visualizzatore. Puoi controllare l’etichetta con `Container.LABEL` simbolo di localizzazione.

I pulsanti hanno il ruolo `button` e set di testo descrittivo con `aria-label` attributo. Il valore di `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, `aria-disabled` viene impostato di conseguenza.

I componenti cursore hanno il ruolo `slider` con attributi `aria-valuenow`, `aria-valuemin`, e `aria-valuemax` per descrivere la posizione corrente del cursore.

Gli elenchi a discesa vengono attivati da pulsanti con `aria-haspopup` attributo impostato su `true` e `aria-controls` attributo che fa riferimento all’elemento effettivo del pannello a discesa. Il pannello a discesa ha il ruolo `menu` con sottoelementi che hanno il ruolo `menuitem`. Ogni voce di menu ha il `aria-label` attributo specificato.

Le finestre di dialogo modali hanno il ruolo `dialog`. L&#39;elemento intestazione della finestra di dialogo è indicato da `aria-labelledby` attributo.
