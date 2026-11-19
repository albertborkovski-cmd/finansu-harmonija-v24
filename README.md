# Finansų harmonija V24

Užšaldyta V24 testavimo versija (žyma `v24`). Ji sukurta iš V23 šaltinių `c057a07fa44f753fc9ba5483d2d5e61f59c18e0a` (žyma `v23.1.0`) ir apima visus V24 patobulinimus. Visi tolesni pakeitimai atliekami tik atskiroje V25 kopijoje. V24 ir ankstesni leidimai nekeičiami.

V24 testavimas: https://albertborkovski-cmd.github.io/finansu-harmonija-v24/.

## V24.0.1 pataisa (2026-11-19)

Naudotojo prašymu pridėtas „Organization not found“ filtras, „Uploaded documents“ pagal nutylėjimą pažymėta „Digitizing“ ir „Rejected“, o iš bendro dokumentų registro organizacijos dantračio pašalintas „Chart of accounts“. Pataisa taip pat pritaikyta vietinei V25. Pradinė `v24` žyma nepakeista; tikslūs šaltiniai ir patikrų rezultatai pateikti atnaujintame archyve bei `release.json`.

## Paleidimas

```bash
npm ci
npm run dev
```

V24 vietinis adresas: http://127.0.0.1:5205/. V24 turi atskirą Git saugyklą be nuotolinių saugyklų. Vietiniai duomenys laikomi atskirai ir nepublikuojami.

## Leidimo turinys

Įtraukta visa dabartinė programa: dokumentai ir sąskaitų kūrimas, bankas, kasa, sandėlis, sudengimas, BŽ ir susietų dokumentų redagavimas, OCR darbuotojo / TeamLead eiga ir mokymo taisyklės, administravimas bei lietuvių ir anglų kalbų perjungimas.

V24 GitHub saugykloje pateikta sukompiliuota svetainė ir tikslus `source-v24.zip` archyvas, `source-manifest.json` bei `release.json` su SHA-256 ir patikrų rezultatais. Vietinė šaltinių Git istorija niekada nepakeičia GitHub artefaktų istorijos.

„Apžvalgos“ sąraše rodomi tik penki svarbiausi pranešimai: pirmiausia „Critical“, tada „Warning“, vienodo svarbumo – naujausi. Bendras aktyvių pranešimų skaičius ir „View all“ išlieka.

## Demonstracinis prisijungimas

- Vidinis administratorius: `albertborkvski@gmail.com`.
- Išorinis naudotojas: `aurika.z@meso.lt`.
- Slaptažodžio laukas prototipe tikrina formatą: bent 6 simboliai, didžioji raidė ir specialus simbolis. Naudokite išgalvotą testinę reikšmę, ne tikrą slaptažodį.

Tai demonstracinis prototipas, ne produkcinė apskaitos sistema. GitHub Pages neturi saugaus serverinio autentifikavimo, bendros duomenų bazės, tikro OCR, banko, apskaitos sistemos ar el. laiškų siuntimo API. Mokėjimai išsaugomi kaip juodraščiai, ne siunčiami į banką. Connect bank išsaugo teikėjo pasirinkimą, tačiau nepradeda banko autorizacijos ir nepakeičia būsenos į Connected. Demonstracinės prijungimo būsenos nėra tikras banko ryšys.

Vietiniai `.env`, `.meso-shared-data.json`, `node_modules` ir kiti privatūs darbo failai nepublikuojami. Nenaudokite konfidencialių dokumentų ar tikrų slaptažodžių. To paties GitHub Pages domeno leidimai gali dalytis naršyklės saugykla; izoliuotam testavimui naudokite atskirą naršyklės profilį.

## Patikros

TypeScript patikra, leidimo kompiliavimas ir tiksliniai dokumentų bei OCR darbo eigos testai tikrinami prieš publikavimą. Pilno testų rinkinio rezultatai ir žinomi senesnių testinių pakaitalų neatitikimai dokumentuojami `release.json`; nesėkmingi testai nelaikomi praėjusiais.
