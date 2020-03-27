---
description: Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l'integrazione con tecnologie di supporto come gli assistenti vocali.
seo-description: Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l'integrazione con tecnologie di supporto come gli assistenti vocali.
seo-title: Supporto per tecnologie di assistenza
solution: Experience Manager
title: Supporto per tecnologie di assistenza
topic: Dynamic media
uuid: 99fdb4fd-5a3d-4c4e-b1c5-10651c08bf39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto per tecnologie di assistenza{#assistive-technology-support}

Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l&#39;integrazione con tecnologie di supporto come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha ruolo `region` e `aria-label` attributo impostati sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di `Container.LABEL` localizzazione.

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39; `aria-label` attributo . Il valore dell&#39; `aria-label` attributo viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, l&#39; `aria-disabled` attributo viene impostato di conseguenza.

La visione principale ha un ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dal simbolo di `ROLE_DESCRIPTION` localizzazione del componente di visualizzazione principale corrispondente. I suggerimenti di navigazione per gli utenti della tastiera vengono forniti utilizzando `aria-describedby`, il testo per il suggerimento di utilizzo viene dal simbolo di `USAGE_HINT` localizzazione. Se una risorsa ha un&#39;etichetta definita nel campo UserData, l&#39; `aria-label` attributo è impostato con il valore di tale etichetta.
