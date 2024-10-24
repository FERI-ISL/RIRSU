# 1. Naloga: Regresija 

Rok za zagovor: **19. december 2024, 23.55**

Število točk: **3** 

## Obvezen del (1,5 točke)

### Opis naloge
Z uporabo programskega jezika Python (Jupyter Notebook ali klasična Python datoteka) in knjižnic pandas in scikit-learn implementirajte osnovno obdelavo podatkov za podano podatkovno zbirko. Zgradite napovedni model z uporabo linearne regresije in ga ovrednotite. Za izris grafov uporabi knjižnici matplotlib ali seaborn. 

Cilj naloge je z uporabo napovednega modela napovedati dnevno število izposojenih koles. Podatkovna zbirka je na voljo za prenos na tej povezavi.

Opis spremenljivk podatkovne zbirke: 
- date: datum izposoje
- rented_bike_count: število izposoj koles
- hour: ura
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
- work_hours: čas delovnika izražen s kategorijama: Yes/No 

### Obdelava podatkov naj zajema
- Nalaganje podatkovne zbirke v DataFrame.
- Izpis števila vrstic, ki ima manjkajoče podatke, za vsak stolpec (spremenljivko).
- Zapolnitev morebitnih manjkajočih številskih podatkov s povprečjem tega stolpca.
- Pretvorba stolpca "date" v tri nove stolpce: "day", "month" in "year". Vrednosti stolpca "date so zapisane v obliki dan/mesec/leto). Po pretvorbi naj se stolpec "date" izbriše.
- Preoblikovanje (kodiranje) stolpcev, ki vsebujejo kategorične vrednosti.
- Izpis opisne statistike celotne podatkovne množice.
- Izrišite histogram za vrednosti spremenljivke "temperature".
- Izrišite graf raztrosa za vrednosti spremenljivk "temperature" in "rented_bike_count". 
  
### Izgradnja napovednega modela
- Razdelitev podatkov na učno in testno množico (seveda ločeno na vhodne in izhodno spremenljivko - "rented_bike_count") tako, da bo testna množica zajemala 30% vseh podatkov pri čemer naj bo parameter **random_state** nastavljen na vrednost **1234**.
- Gradnjo (učenje) napovednega modela implementirajte z uporabo algoritma linearne regresije nad podatki iz učne množice. 

### Ovrednotenje napovednega modela
- Pridobivanje napovedane vrednosti z uporabo zgrajenega napovednega modela za vsak primerek iz množice testnih podatkov.
- Izračun in izpis sledečih metrik nad testnimi podatki:
  - povprečna absolutna napaka,
  - povprečna kvadratna napaka,
  - vrednost razložene variance.

## Dodaten del (1,5 točke)


## Zagovor naloge

Nalogo je potrebno zagovoriti na vajah pri asistentu.

