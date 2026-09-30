# Konvence práce na projektu

Revize: 2026-09-30.

## Tři vrstvy informací

| vrstva | poznáš podle | kam |
|---|---|---|
| **trvalá** | platilo by to i za půl roku a zjišťování stálo práci | soubor v `context/` |
| **dočasná** | mění se a nikdo to nedokáže odvodit, musí to někdo zapsat | `context/status/`, vždy s datem |
| **pomíjivá** | mění se a jde to spočítat ze zdroje za pár vteřin | nikam, generovat skriptem |

Trvalé je rozhodnutí a jeho důvod, konvence, sémantika dat, past v datech nebo nástroji, výsledek
analýzy. Piš **důvod, ne jen pravidlo**. Zapsané pomíjivé číslo (počet souborů, záznamů) je horší
než žádné: zastará a přitom vypadá jako fakt.

## Společný zápis dvou lidí

- **Paměť asistenta nepoužíváme.** Je jen u jednoho z nás a druhý do ní nevidí. Všechno trvalé jde
  sem do `context/`, jinak o tom druhý (a jeho agent) neví.
- **Zapisuj průběžně**, hned když něco zjistíš nebo rozhodneš, ne na konci práce.
- **Před prací `git pull`, po zápisu commit a push.** Kontext se commituje zvlášť od kódu nebo
  aspoň se zprávou `context: …`, ať je v historii vidět, kdo co kdy doplnil.
- **Měň cíleně, nepřepisuj celý soubor.** Druhý mohl mezitím do souboru psát. Agent soubor vždy
  nejdřív přečte a upraví jen konkrétní místo.
- **Nové téma = nový soubor `NN_tema.md` + řádek v tabulce `00_index.md`**, nikde jinde. Číslujeme
  po desítkách (10, 20, 30…), ať jde vkládat mezi.
- **Nesouhlas nepřepisuj potichu.** Když tvrzení druhého neodpovídá tomu, co vidíš, oprav ho
  s datem a důvodem; když nevíš, která verze platí, dej to do `status/otevrene_otazky.md`
  a označ, u koho otázka leží.
- **Ve `status/` jen otevřené věci**, s datem a jménem (kdo na tom dělá / na koho se čeká).
  Hotové se nepíše jako deník: závěr patří do `context/`, průběh je v historii gitu.
- **Konflikt při merge** v `context/` řeš sloučením obou verzí, ne výběrem jedné.

## Jazyk

- Kontext píšeme česky, odborné názvy a názvy souborů v originále.
