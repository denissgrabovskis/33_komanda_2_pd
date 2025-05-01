# 33_komanda_2_pd

## Sākums
* Izmantojam [Orange rīku](https://orangedatamining.com/)
* Datu kopa: [Alžīrijas mežu ugunsgrēki](https://archive.ics.uci.edu/dataset/547/algerian+fores+fires+dataset)

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