# 1. Naloga: Regresija 

Rok za zagovor: **19. december 2024, 23.55**

Število točk: **3** 

## Obvezen del (1,5 točke)

### Opis naloge
Z uporabo programskega jezika Python (Jupyter Notebook ali klasična Python datoteka) in knjižnic [pandas](https://pandas.pydata.org/docs/) in [scikit-learn](https://scikit-learn.org/stable/) implementirajte osnovno obdelavo podatkov za podano podatkovno zbirko. Zgradite napovedni model z uporabo linearne regresije in ga ovrednotite. Za izris grafov uporabi knjižnici [matplotlib](https://matplotlib.org/) ali [seaborn](https://seaborn.pydata.org/). 

Cilj naloge je z uporabo napovednega modela napovedati dnevno število izposojenih koles. Podatkovna zbirka je na voljo za prenos na [tej povezavi](bike_data.csv).

Opis spremenljivk podatkovne zbirke: 
- date: datum izposoje
- rented_bike_count: število izposoj koles
- hour: ura v dnevu
- temperature: temperatura v stopinjah celzija
- humidity: vlažnost zraka izražena v odstotkih
- windspeed: hitrost vetra izražena v m/s
- visibility: vidnost (10m)
- dew_point_temperature
- rosišče v stopinjah celzija
- solar_radiation: sončno sevanje izraženo v MJ/m2
- rainfall: padavine izražene v mm
- snowfall: sneženje izraženo v cm
- seasons: letni časi izraženi s kategorijami: winter, spring, summer, autumn
- holiday: prazniki izraženi s kategorijama: Holiday/No holiday
- work_hours: izposoja v času delovnika: Yes/No 

### Obdelava podatkov naj zajema
- Naložite podatkovno zbirko v [DataFrame](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html).
- Izpišite števila vrstic, ki imajo manjkajoče podatke, za vsak stolpec (spremenljivko).
- Zapolnite morebitne manjkajoče številske podatke s povprečjem tega stolpca.
- Pretvorite stolpec "date" v tri nove stolpce: "day", "month" in "year". Vrednosti stolpca "date so zapisane v obliki dan/mesec/leto). Po pretvorbi stolpec "date" izbrišite.
- Preoblikujte (kodirajte) stolpce, ki vsebujejo kategorične vrednosti z uporabo One-hot encoding.
- Izpišite opisno statistiko za celotno podatkovno množico.
- Izrišite histogram za vrednosti spremenljivke "temperature".
- Izrišite graf raztrosa za vrednosti spremenljivk "temperature" in "rented_bike_count". 
  
### Izgradnja napovednega modela
- Razdelite podatke na učno in testno množico (seveda ločeno na vhodne in izhodno spremenljivko - "rented_bike_count") tako, da bo testna množica zajemala 30% vseh podatkov pri čemer naj bo parameter **random_state** nastavljen na vrednost **1234**.
- Gradnjo (učenje) napovednega modela implementirajte z uporabo algoritma linearne regresije nad podatki iz učne množice. 

### Ovrednotenje napovednega modela
- Pridobite napovedane vrednosti z uporabo zgrajenega napovednega modela za vsak primerek iz množice testnih podatkov.
- Izračunajte in izpišite sledeče regresijske metrike:
  - povprečna absolutna napaka,
  - povprečna kvadratna napaka,
  - vrednost razložene variance.

## Dodaten del (1,5 točke)
Nalogo nadgradite na način, da za reševanje problema napovedovanja števila izposojenih koles, namesto algoritma linearne regresije uporabite Ridge algoritem. Učenje in ovrednotenje izvedite na popolnoma enak način kot v obveznem delu naloge.

Dodatno rezultate metrik obeh omenjenih algoritmov primerjajte in izrišite stolpične diagrame za vsako izmed metrik.

## Zagovor naloge
Nalogo je potrebno zagovoriti na vajah pri asistentu.