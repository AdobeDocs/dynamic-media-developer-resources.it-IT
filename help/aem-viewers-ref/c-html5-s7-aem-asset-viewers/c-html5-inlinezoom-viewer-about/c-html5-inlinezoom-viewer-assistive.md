---
title: Supporto tecnologico per assistenza
description: Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,User
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Supporto tecnologico per assistenza{#assistive-technology-support}

Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L’elemento visualizzatore di livello superiore ha un ruolo `region` e `aria-label` impostato per impostazione predefinita sul nome del visualizzatore. Puoi controllare l’etichetta con la `Container.LABEL` simbolo di localizzazione.

La vista principale ha un ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dalla `ROLE_DESCRIPTION` simbolo di localizzazione del componente di visualizzazione principale corrispondente. I suggerimenti per la navigazione degli utenti di tastiera vengono forniti utilizzando `aria-describedby`, il testo per il suggerimento di utilizzo proviene dal `USAGE_HINT` simbolo di localizzazione. Se una risorsa ha un&#39;etichetta definita nel campo UserData , la variabile `aria-label` attributo è impostato con il valore di tale etichetta.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con `aria-label` impostato sul valore del `LABEL` simbolo di localizzazione del componente. Il ruolo dei singoli campioni `option` con `aria-setsize` e `aria-posinset` per descrivere la posizione del campione nel set. Se è selezionato un campione, ottiene il `aria-selected` attributo impostato su `true`.
