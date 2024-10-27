# 2. Naloga: Regresija 

Rok za zagovor: **19. december 2024, 23.55**

Število točk: **3** 

## Obvezen del (1,5 točke)

### Opis naloge
Z uporabo programskega jezika Python (Jupyter Notebook ali klasična Python datoteka) in knjižnic [numpy](https://numpy.org/doc/stable/), [pillow](https://pillow.readthedocs.io/en/stable/?badge=latest) ter [scikit-learn](https://scikit-learn.org/stable/) implementirajte osnovno obdelavo podatkov za podano podatkovno zbirko. Zgradite napovedni model z uporabo [klasifikacijskega drevesa](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html) in ga ovrednotite. 

Cilj naloge je z uporabo napovednega modela napovedati v katero izmed kategorij sodi posamezna slika. Podana podatkovna zbirka skupno zajema 300 slik, ki so razvrščene v tri kategorije: krog (100 slik), kvadrat (100 slik) in trikotnik (100 slik). Podatkovna zbirka je na voljo za prenos na [tej povezavi](shapes.zip).

### Obdelava podatkov naj zajema
- Izgradite seznam poti do slik podatkovne množice.
- Izgradite seznama oznak (label) za posamezno sliko.
- Izrišite primerek slike posamezne kategorije.
- Izgradite dvodimenzionalno polje slik
  - Naložite (preberite) posamezno sliko (PIL - Image, convert 'L'),
  - Prebrano sliko (dvodimenzionalno polje) pretvorite v enodimenzionalno polje,
  - Enodimenzionalno polje dodate na polje slik.

### Izgradnja napovednega modela
- Razdelite podatke na učno in testno množico tako, da bo testna množica zajemala 30% vseh podatkov pri čemer naj bo parameter random_state nastavljen na vrednost 4321 ter parameter shuffle na vrednost True.
- Gradnjo (učenje) napovednega modela implementirajte z uporabo algoritma odločitveno drevo nad podatki iz učne množice. Pri izgradnji odločitvenega drevesa nastavite parameter random_state na vrednost 1234.
- Izrišite odločitveno drevo.

### Ovrednotenje napovednega modela
- Pridobite napovedane vrednosti z uporabo zgrajenega napovednega modela za vsak primerek iz množice testnih podatkov.
- Izračunajte sledeče klasifikacijske metrike:
  - točnost,
  - utežena F1 vrednost,
  - utežena preciznost,
  - utežen priklic. 

## Dodaten del (1,5 točke)
Nalogo nadgradite na način, da za reševanje problema klasifikacije slik, namesto algoritma odločitvenega drevesa uporabite algoritem K-najbližjih sosedov. Učenje in ovrednotenje izvedite na popolnoma enak način kot v obveznem delu naloge.

Dodatno rezultate metrik obeh omenjenih algoritmov primerjajte in izrišite stolpične diagrame za vsako izmed metrik.

## Zagovor naloge
Nalogo je potrebno zagovoriti na vajah pri asistentu.