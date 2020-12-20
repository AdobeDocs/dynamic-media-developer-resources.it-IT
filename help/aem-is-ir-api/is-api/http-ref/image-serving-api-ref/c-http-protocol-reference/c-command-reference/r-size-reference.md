---
description: Dimensione del livello. Specifica la dimensione o la dimensione massima del livello per un livello, prima che al livello vengano applicati rotate=, prospettiva= e estensioni=.
seo-description: Dimensione del livello. Specifica la dimensione o la dimensione massima del livello per un livello, prima che al livello vengano applicati rotate=, prospettiva= e estensioni=.
seo-title: size
solution: Experience Manager
title: size
topic: Scene7 Image Serving - Image Rendering API
uuid: c9c13062-7974-4dd9-aff4-f9502bcf442e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 1%

---


# size{#size}

Dimensione del livello. Specifica la dimensione o la dimensione massima del livello per un livello, prima che al livello vengano applicati rotate=, prospettiva= e estensioni=.

` size= *``*, *`larghezza`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> larghezza  </span>,  <span class="varname"> altezza  </span> </span> </p> </td> 
  <td class="stentry"> <p>Limite dimensione livello in pixel (int, int, 0 o superiore). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN  </span>,  <span class="varname"> heightN  </span> </span> </p> </td> 
  <td class="stentry"> <p>Limite dimensione livello normalizzato rispetto alla dimensione 0 del livello (reale, reale, 0,0...1.0). </p> </td> 
 </tr> 
</table>

Se specificato per un livello immagine, size= limita la larghezza, l’altezza o entrambi dell’immagine del livello. L&#39;immagine verrà ridimensionata in modo che non sia maggiore di `size=`. Se viene specificata una dimensione normalizzata, essa è relativa alla dimensione del livello 0. Se sono specificati sia *`width`* che *`height`*, l&#39;immagine di origine viene ridimensionata (dopo l&#39;applicazione di `crop=`) in modo che nessuna dimensione superi la dimensione specificata. Le proporzioni del rettangolo di origine vengono mantenute in tutti i casi. È possibile impostare *`width`* o *`height`* su 0; in questo caso il valore viene calcolato dal server in base alle proporzioni dell&#39;immagine.

Se specificato per un livello di testo, `size=` specifica la dimensione della casella di testo. *`width`* è obbligatorio;  *`height`* può essere impostato su 0, nel qual caso l’altezza del testo disposto viene usata come altezza del livello. Per impostazione predefinita, i motori di layout di testo inseriscono interruzioni di riga per assicurare che il testo si adatti sempre in orizzontale allo spazio disponibile. Se si specifica *`height`*, le righe che non rientrano nello spazio disponibile verranno ritagliate ( `text=`) o omesse ( `textPs=`). `text=` supporta modalità di adattamento aggiuntive; fare riferimento a  `textAttr=` per ulteriori dettagli.

Se specificato per un livello in tinta unita, `size=` definisce la dimensione esatta del livello; entrambi i valori devono essere specificati (a meno che non sia specificata una maschera). Se è stato specificato anche `mask=`, l&#39;immagine della maschera verrà ridimensionata in modo da adattarsi a `size=` allo stesso modo in cui le immagini vengono ridimensionate nei livelli immagine.

## Proprietà {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Attributo layer. Si applica al livello 0 se `layer=comp`. `sizeN=` non è consentito per  `layer=0` o  `layer=comp`. `sizeN=` è consentito per  `layer=0` e  `layer=comp` solo nei record di catalogo che definiscono le immagini delle filigrane. In questo caso, `sizeN` definisce il ridimensionamento dell&#39;immagine della filigrana rispetto all&#39;immagine composita a cui viene applicata la filigrana. Se si specifica `size=`, `res=` e `scale=` vengono ignorati per questo livello. Ignorato dai livelli degli effetti.

## Predefinito {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`, le dimensioni del livello non sono vincolate. Per i livelli di immagine, la dimensione del livello viene quindi determinata in base alla dimensione dell’immagine del livello dopo l’applicazione delle operazioni `crop=`, `scale=` o `res=`. Per i livelli di testo, se `size=` non è specificato, il livello viene ridimensionato automaticamente per adattarsi al testo di cui è stato effettuato il rendering.

I livelli di colore tinta unita richiedono un `size=` completamente specificato, un `mask=` o `clipPath=`.

## Esempio {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Vedere [Esempio A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ,  [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), livelli  [di testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
