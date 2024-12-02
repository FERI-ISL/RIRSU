# 7. Naloga: Napovedni model kot spletna storitev

Rok za zagovor: **19. december 2024, 23.55**

Število točk: **3** 

## Obvezen del (1,5 točke)

Z uporabo programskega jezika Python ter do sedaj naučenih regresijskih napovednih modelov implementirajte spletno storitev, ki bo za podane vhodne podatke napovedala število izposojenih koles.

Cilj naloge je naloge je naučene napovedne modele uporabiti v obliki REST API spletne storitve.

Za pomoč pri razvoju lahko uporabite kateregakoli izmed Python ogrodij za razvoj spletnih storitev ([flask](https://flask.palletsprojects.com/en/stable/), [FastAPI](https://fastapi.tiangolo.com/)...)

### Priprava napovednih modelov

Najboljši napovedni model zgrajen v prejšnji nalogi (obvezni del naloge 6) ter najboljši regresijski napovedni model iz 4. naloge (obvezni del) serializirajte v datoteko. Pri tem ne pozabite serializirati morebitne scalerje (MinMaxScaler, StandardScaler, ipd.), ki so potrebni za pravilno preoblikovanje podatkov prejetih preko spletne storitve.

Serializirane objekte prenesete v spletno storitev, kjer jih ob zagonu storitve deserializirate oz. poskrbite, da jih bo mogoče uporabljati znotraj funkcij, ki bodo izvršene ob klicu na posamezno končno točko (endpoint) razvite spletne storitve.

### Zahteve spletne storitve

Potrebno je implementirati dve REST končni točki s sledečimi specifikacijami:

- **POST: /predict/naloga4** - V telesu zahtevka prejme podatke za en primerek v JSON obliki, ki je uporabljen za napovedovanje števila izposojenih koles. Odgovor storitve naj bo v sledeči JSON obliki:```{"prediction":95}```
- **POST: /predict/naloga6** - V telesu zahtevka prejme 186 primerkov v JSON obliki, na podlagi katerih zgradi eno časovno vrsto. Model nad to časovno vrsto napove naslednjo vrednost v zaporedju. Odgovor storitve naj bo v sledeči JSON obliki: ```{"prediction":95}```

Razvito spletno storitev testirajte z uporabo orodja [Postman](https://www.postman.com/) ali katero izmed podobnih orodij.

Končno razvito rešitev zapakirajte v obliko Docker slike. Vse potrebne datoteke za poganjanje spletne storitve kot tudi serializirane modele zapakirajte v zip arhiv, ki ga oddate.

## Dodaten del (1,5 točke)

Spletno storitev nadgradite na način, da bo omogočala klasifikacijo slik podatkovne zbirke "rock-paper-scissors".

### Priprava napovednih modelov

Najboljši napovedni model iz 5. naloge (obvezni del) serializirajte v datoteko. Serializirane objekte prenesete v spletno storitev, kjer jih ob zagonu storitve deserializirate oz. poskrbite, da jih bo mogoče uporabljati znotraj funkcij, ki bodo izvršene ob klicu na posamezno končno točko (endpoint) razvite spletne storitve.

### Zahteve spletne storitve
Potrebno je implementirati REST končno točko s sledečimi specifikacijami:

- POST: /predict/naloga5 - V telesu zahtevka prejme sliko v obliki base64 kodiranja. Na podlagi prejete slike izvede klasifikacijo in kot odgovor v JSON obliki poda razred v katerega slika sodi. Odgovor storitve naj bo v sledeči JSON obliki: ```{"prediction": "Rock"}```

## Zagovor naloge
Nalogo je potrebno zagovoriti na vajah pri asistentu.