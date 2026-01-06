# Protsess: ligipääsude haldus (IAM)

## 1. Eesmärk

Tagada, et ligipääsud infosüsteemile ja selle andmetele antakse, muudetakse ja eemaldatakse kontrollitult, minimaalse vajalikkuse põhimõttel ning auditeeritavalt.

## 2. Skoop

- Kehtib: kõik kasutajad (töötajad, partnerid), teenuskontod ja administraatorid.
- Keskkonnad: [dev/test/stage/prod] (täpsusta).
- Erandid: break-glass ligipääsud (kirjeldada eraldi).

## 3. Seosed E-ITS meetmetega

- E-ITS viide/ID: [täida]
- Seotud teemad: autentimine, autoriseerimine, privileegid, ülevaatus, logimine.

## 4. Rollid ja vastutused

| Roll | Vastutus | Asendaja | Märkused |
|---|---|---|---|
| Teenuseomanik | kinnitab ligipääsu vajaduse |  |  |
| Süsteemiadmin / IAM admin | rakendab ligipääsu tehniliselt |  |  |
| Infoturve | kontrollib erandjuhtumeid ja ülevaatusi |  |  |
| Kasutaja juht | kinnitab rolli/vajaduse (kui kohaldub) |  |  |

## 5. Sisendid ja väljundid

- Sisendid: ligipääsutaotlus; tööleasumine/lahkumine; rollimuudatus; intsident; auditileid.
- Väljundid: loodud/muudetud/eemaldatud konto; õiguste muutuse logi; perioodilise ülevaatuse protokoll.

## 6. Sammud (töövoog)

1. **Taotlus**: kasutaja või tema juht esitab ligipääsutaotluse (põhjendus + soovitud roll).
2. **Kinnitamine**: teenuseomanik (ja vajadusel infoturve) kinnitab/keeldub.
3. **Rakendamine**: admin/IAM admin lisab õigused rollipõhiselt.
4. **Kontroll**: admin kontrollib, et õigused vastavad taotlusele (minimaalsus).
5. **Dokumenteerimine**: taotluse ID + rakenduse aeg + tegija salvestatakse (ticket/auditilog).
6. **Eemaldamine**: lahkumisel või rollivahetusel eemaldatakse õigused kokkulepitud SLA jooksul.
7. **Perioodiline ülevaatus**: vähemalt [kvartalis/poolaastas] tehakse õiguste ülevaatus ja kinnitused.

## 7. Logimine ja tõendusmaterjal

- Ligipääsu sündmused: konto loomine, rollimuutus, privileegne ligipääs, ebaõnnestunud sisselogimised.
- Tõendid: ticketid, IAM auditilogid, süsteemi auditilogid, perioodilise ülevaatuse raport.
- Säilitusaeg: [täida].

## 8. Mõõdikud ja regulaarne ülevaatus

- Õiguste eemaldamise aeg lahkumisel (SLA).
- Perioodiliste ülevaatuste läbiviimise määr.
- Privilegeeritud ligipääsude arv ja kasutusjuhtumid.

## 9. Erandolukorrad ja eskalatsioon

- Break-glass ligipääs: ajutine, ajaliselt piiratud, kohustusliku järelkontrolliga.
- Tuvastatud ülearune ligipääs: eemaldatakse esimesel võimalusel, infoturve kaasatakse.

