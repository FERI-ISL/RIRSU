# 3. Naloga: Ansambelske metode 

Rok za zagovor: **19. december 2024, 23.55**

Število točk: **3** 

## Obvezen del (1,5 točke)
Opis naloge Z uporabo programskega jezika Python (Jupyter Notebook ali klasična Python datoteka) in knjižnic [pandas](https://pandas.pydata.org/docs/), [numpy](https://numpy.org/doc/stable/), [pillow](https://pillow.readthedocs.io/en/stable/?badge=latest), [scikit-learn](https://scikit-learn.org/stable/) in [XGBoost](https://xgboost.readthedocs.io/en/stable/) implementirajte osnovno obdelavo podatkov za podani podatkovni zbirki (zbirki iz naloge 1 in 2). Zgradite napovedne modele z uporabo ansambelskih metod in jih ovrednotite z uporabo 5-kratne prečne validacije (5-fold cross-validation). 

Cilj naloge je naloge je z uporabo ansambelskih metod zgraditi napovedne modele za problema iz 1. in 2. naloge. Povezava do podatkovnih množic je dostopna na prej omenjenih nalogah.

### Obdelava podatkov naj zajema
Postopka obdelave podatkov se lotite na popolnoma enak način kot ste se jih lotili pri prejšnjih dveh nalogah. 

### Izgradnja napovednega modela
- Razdelite podatkovne zbirke z uporabo 5-kratne prečne validacije.
- Gradnjo (učenje) napovednega modela implementirajte z uporabo ansambelskih metod (pri vseh metodah, kjer je mogoče nastavite parameter random_state na vrednost 1234):
  - Za regresijski problem uporabite:
    - Bagging regresor
    - Random forest regresor
    - Adaboost regresor
    - XGBoost regresor 
  - Za klasifikacijski problem uporabite:
    - Bagging klasifikator 
    - Random forest klasifikator
    - Adaboost klasifikator
    - XGBoost klasifikator 

### Ovrednotenje napovednega modela
- Pridobite napovedane vrednosti z uporabo zgrajenih napovednih modelov za vsak primerek iz množice testnih podatkov, za vsak prečni rez.
- Izračunajte vrednosti metrik za vsak prečni rez:
  - Regresijski problem:
    - povprečno absolutno napako,
    - povprečno kvadratno napako,
    - vrednost razložene variance.
  - Klasifikacijski problem:
    - točnost,
    - utežena F1 vrednost,
    - utežena preciznost,
    - utežen priklic.
- Primerjava napovednih modelov:
  - Shranite vse vrednosti vseh metrik za posamezen algoritem strojnega učenja.
  - Izračunajte povprečne vrednosti posamezne metrike za posamezen algoritem strojnega učenja glede na vrednosti v prečnih rezih.
  - Izrišite stolpične diagrame za vse povprečne vrednosti posamezne metrike (posebej za klasifikacijski problem in posebej za regresijski problem) uporabljenih ansambelskih metod pri čemer pri klasifikacijskem problemu vključite rezultate pridobljene v nalogi 2, pri regresijskem problemu pa vključite rezultate pridobljene v nalogi 1 (skupno torej 7 slik). 
  - Za ansambelske metode (posebej za klasifikacijski problem in posebej za regresijski problem) izrišite grafikone kvartilov (angl. boxplot) za vsako izmed izračunanih metrik, pri čemer naj bodo v obeh primerih za vse štiri algoritme strojnega učenja grafikoni kvartilov združeni na eni sliki (skupno torej 7 slik).

## Dodaten del (1,5 točke)

Uporabljene ansambelske metode v obveznem delu, na popolnoma enak način naučite in ovrednotite nad spodaj podanima podatkovnima zbirkama.

[Regresijska podatkovna zbirka](mbajk_dataset.csv)

[Klasifikacijska podatkovna zbirka](agriculture-crops.zip)

## Zagovor naloge

Nalogo je potrebno zagovoriti na vajah pri asistentu.