---
title: Pareizrakstība - latviešu valodas pareizrakstība macOS
description: >-
  Pareizrakstība ir serviss, kas pievieno sistēmas līmeņa latviešu valodas pareizrakstības pārbaudi macOS operētājsistēmai
keywords:
  - latviešu pareizrakstība
  - pareizrakstības pārbaude macOS
  - latviešu valodas pārbaude
  - pareizrakstība
---

# Pareizrakstība

Serviss, kas pievieno sistēmas līmeņa latviešu valodas pareizrakstības pārbaudi macOS operētājsistēmai

![TextEdit](../media/screenshots/screen-01.png)

## Prasības

- macOS 12+
- Apple Silicon un Intel (Universāla)
- Pārbaudīts uz
  - macOS 27
  - macOS 12

## Instalēšana

- [Lejupielādē jaunāko laidienu](https://github.com/WARP-LAB/pareizrakstiba/releases/latest/download/Pareizrakstiba.dmg), vai skati [izmaiņu piezīmes](https://github.com/WARP-LAB/pareizrakstiba/releases/latest/), kur zem _Assets_ atradīsi DMG
- Atver DMG failu, palaid instalētāju `Pareizrakstiba.pkg`, seko norādēm
- Pēc instalācijas, ja vēlies lietot pareizrakstības pārbaudi kādā aplikācijā, kas bija jau atvērta, pārstartē to

## Atinstalēšana

- [Lejupielādē jaunāko laidienu](https://github.com/WARP-LAB/pareizrakstiba/releases/latest/download/Pareizrakstiba.dmg)
- Atver DMG failu, palaid `Uninstall Pareizrakstiba`, seko norādēm

## Lietošana

- Ieskatieties Apple macOS lietotāja rokasgrāmatā: [Check spelling and grammar on Mac](https://support.apple.com/en-gb/guide/mac-help/mchlp2299/mac)
- Nosedz visas lietotnes, kas izmanto macOS pareizrakstības dzinēju. Vienkāršs veids, kā noteikt atbalstu - vai lietotnei ir izvēlne _Edit : Spelling and Grammar_. Dažām nav.
- Lietotnēs pārliecinies, ka izvēlēta latviešu pareizrakstība: _Edit : Spelling and Grammar : Show Spelling and Grammar → Latviešu (Pareizrakstiba)_
- Sistēmas iestatījumi ir atrodami _System Settings : Keyboard : Input Sources → Edit…_ Turpat ir arī _Spelling_  izvēlne, kur var iestatīt vēlamo pareizrakstības valodu pēc noklusējuma. Vecākās macOS versijās iestatījumi atrodami _System Preferences : Keyboard : Text_.
- _LibreOffice_ lietotnes lietotājiem nav jālejupielādē un jāinstalē vārdnīcas pašās lietotnēs, jo minētās lietotnes izmanto macOS sistēmas līmeņa pareizrakstības pārbaudi. Turklāt, lietojot Pareizrakstību un pievienojot jaunus vārdus, tie attieksies uz visu OS.
- Bagātinātā teksta saturs vietnēs _Google Docs, Sheets & Slides_ nav sasniedzams macOS sistēmas līmeņa pareizrakstības pārbaudei, izmantojot pārlūkus, tā šis tīmekļa aplikācijas būvētas.
- Lietotāja apgūtā pareizrakstība tiek glabāta mapē `~/Library/Spelling/`.
- Reti izmantotā automātiskās pabeigšanas saraksta saīsne ir `Option+Esc` vai `F5` (pirms Mac OS X 10.6 tā bija `Esc`).

## Instalēšanas blakusefekti

Instalēšanas laikā Pareizrakstība noņem visas iepriekšējās tās versijas.

## Vecāku OS versiju atbalsts

- macOS 10.13+ Apple Silicon un Intel (Universāla) (not signed) [v4.1.0](https://github.com/WARP-LAB/Pareizrakstiba/releases/tag/v4.1.0)
- Mac OS X 10.7 līdz Mac OS X 10.9 Intel 32/64-bit [Pareizrakstiba-Archive](https://github.com/WARP-LAB/Pareizrakstiba-Archive)
- Mac OS X 10.4 līdz Mac OS X 10.6 PPC un Intel 32/64-bit (Universāla) versijas pieglabātas citur

## Pareizrakstības konfigurēšana no CLI

Daži vienrindiņu piemēri, lai nevajadzētu rakņāties pa padziļi noslēptiem macOS iestatījumiem.

```zsh
# Izslēgt automātisku valodas noteikšanu
defaults write NSGlobalDomain NSSpellCheckerAutomaticallyIdentifiesLanguages -bool FALSE

# Mēģināt piespiest latviešu kā noklusējuma valodu, palaižot lietotnes
defaults write NSGlobalDomain NSPreferredSpellServerLanguage 'lv'

# Izslēgt sistēmas līmeņa automātisko labošanu
defaults write NSGlobalDomain NSAutomaticSpellingCorrectionEnabled -bool FALSE
```

## Kļūdu ziņošana un funkcijas pieprasījums

Izmantojot [GitHub Issues](https://github.com/WARP-LAB/pareizrakstiba/issues/new/choose)

## Versiju vēsture

Skati [CHANGELOG.md](https://github.com/WARP-LAB/pareizrakstiba/blob/master/CHANGELOG.md).

## Izmanto

- [Hunspell](https://hunspell.github.io)
- [Latviešu valodas Hunspell vārdnīcas](https://dict.dv.lv/home.php?prj=lv)
