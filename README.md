# 33_komanda_2_pd

## Sākums
* Izmantojam [Orange rīku](https://orangedatamining.com/)
* Datu kopa: [Alžīrijas mežu ugunsgrēki](https://archive.ics.uci.edu/dataset/547/algerian+fores+fires+dataset)

$\color{red}{\textsf{TODO: Noņemt}}$
Vēl atrādīju šadus datasetus:
* [Wholesale customers](https://archive.ics.uci.edu/dataset/292/wholesale+customers) - kā saprotu, tie ir fake dati
* [Steel Industry Energy Consumption](https://archive.ics.uci.edu/dataset/851/steel+industry+energy+consumption) - šitos vnk nesaprotu, bet vrb būtu vērts tājos apskatīt. idk

## I daļa
Datu kopā ir 244 piemēri diviem Alžīrijas regioniem: Bejaia un Sidi Bel-abbes. Mēs apvienojām to vienā. $\color{red}{\textsf{TODO: Noņemt šito?}}$

| Kolonma | Pilns vārds | Tips | Apraksts | Mērvienība | Komentārs $\color{red}{\textsf{TODO: noņemt šo kolonu}}$ |
| - | - | - | - | - | - |
| day |  | Int | | | Skipot? |
| month |  | Int | | | Skipot? |
| year |  | Int | | | Defo skipot, vienmēr 2012 |
| Temperature |  | Int | Temperatūra pūsdienlaikā | °C
| RH | Relative Humidity | Int | Relatīvais mitrums | %
| WS | Wind Speed | Int | Vēja ātrums | km/h
| Rain | | Float | | mm
| FFMC | Fine Fuel Moisture Code | Float | Smalkas degvielas mitruma kods (*Код влажности мелкого топлива*) | | Izpētīt
| DMC | Duff Moisture Code | Float | Duff mitruma kods (*Код влажности Даффа*)  | | Izpētīt
| DC | Drought Code | Float | Sausuma kodekss | | Izpētīt
| ISI | Initial Spread Index | Float | Sākotnējais izplatības indekss | | Izpētīt
| BUI | Buildup Index | Float | Uzkrāšanās indekss | | Izpētīt
| FWI | Fire Weather Index | Float | Ugunsgrēka laika indekss | | Izpētīt
| Fire | | Bool | Ir vai nav ugunsgrēks


$\color{red}{\textsf{TODO: Noņemt, atstāju priekš atskaitei}}$
Taisīju visu pēc šī [video](https://www.youtube.com/watch?v=bmwH3EcTBEM)
Pielādēju kopu, atvēru Orange rīkā. Pafiksēju tur datus, bija problēma ar pāris piemēriem. Skipoju Year kolonu, jo ta ir vnk 2012. Pārsaucēju Classes kolonu uz Fire. Ar Continuize widgetu visus pārējus kolonus normalizēju uz intervālu [0,1]. Pēc tam ar Impute widgetu nofiltrēju liekus piemērus ārā, bet tādu īsti nav. Pēc tām pievienoju Feature Statistics, Distributions un Scatter Plot. Visiem atzīmeju Fire kolonu kā Color, lai dati tika savakti, ņemot vērā šo kolonu kā galveno. Pedējā widgetā, palaižot 'Find Informative Projections', var ieraudzīt, ka vislābāk atdālā datus atribūtu kombinācija ISI/FFMC. Jā, mums tikai 2 klasi, hz vai tas ir slikti. IMO nav. Arī pievienoju Correlations widgetu, tur nekas interesants nav, vislābāka korelācija ir ISI:RH atributiem

## II daļa
$\color{red}{\textsf{TODO: Noņemt, atstāju priekš atskaitei}}$
Jaunus widgetus pievienoju zēmāk, lai labāk redzēt darba daļas. Pievienoju k-Means widgetu, ieliku iestātījumus gandrīz, ka [video](https://www.youtube.com/watch?v=ojxvlQSYLr0). Pēc tām pievienoju Scatter Plot, lai attēlotu dabūtos klasterus. Šoreiz palaižot Find Informative Projections, sanāca, ka labāk atdālā klasterus atrībutu kombinācija BUI/FFMC. Pēc tām pievienoju Distances un tam Hierarchical Clustering. Pēdējā widgetā jāpaspēlās ar to līniju, jāpabīdē to. Hz, man ne īsti sanāca.
