---
title: Supporto tecnologico per assistenza
description: Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video,Accessibility
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Supporto tecnologico per assistenza{#assistive-technology-support}

Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L’elemento visualizzatore di livello superiore ha un ruolo `region` e `aria-label` impostato per impostazione predefinita sul nome del visualizzatore. Puoi controllare l’etichetta con la `Container.LABEL` simbolo di localizzazione.

I pulsanti hanno il ruolo `button` e testo descrittivo con `aria-label` attributo. Il valore di `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, `aria-disabled` attributo viene impostato di conseguenza.

Ruolo dei componenti cursore `slider` con attributi `aria-valuenow`, `aria-valuemin`e `aria-valuemax` per descrivere la posizione corrente del dispositivo di scorrimento.

Gli elenchi a discesa sono attivati da pulsanti con informazioni aggiuntive `aria-haspopup` attributo impostato su `true` e `aria-controls` attributo che fa riferimento all’elemento del pannello a discesa effettivo. Il pannello a discesa stesso ha il ruolo `menu` con sottoelementi aventi il ruolo `menuitem`. Ogni voce di menu ha `aria-label` attributo specificato.

Le finestre di dialogo modali hanno il ruolo `dialog`. L&#39;elemento di intestazione della finestra di dialogo è referenziato dal `aria-labelledby` attributo.
