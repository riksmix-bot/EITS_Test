# Protsess: varundus ja taaste (Backup & Restore)

## 1. Eesmärk

Tagada andmete ja teenuse taastatavus kokkulepitud RPO/RTO alusel ning tõendada regulaarselt varunduste toimivust ja taastetestide tulemusi.

## 2. Skoop

- Kehtib: andmebaasid, failid, konfiguratsioonid, kriitilised artefaktid.
- Keskkonnad: [prod] (ja vajadusel stage).
- Erandid: ajutised keskkonnad (selgelt määratleda).

## 3. Seosed E-ITS meetmetega

- E-ITS viide/ID: [täida]
- Seotud teemad: jätkusuutlikkus, varahaldus, krüpto, logimine.

## 4. Rollid ja vastutused

| Roll | Vastutus | Asendaja | Märkused |
|---|---|---|---|
| Ops/SRE | varunduste seadistamine ja jälgimine |  |  |
| Teenuseomanik | RPO/RTO kinnitamine |  |  |
| Infoturve | kontrollib ligipääse ja krüptot |  |  |

## 5. Sisendid ja väljundid

- Sisendid: varunduse poliitika, varade nimekiri, konfiguratsioon.
- Väljundid: varunduse raportid, taastetestide protokoll, parandustegevused.

## 6. Sammud (töövoog)

1. **Plaan**: määratakse RPO/RTO, varundatavad varad, sagedus ja säilitus.
2. **Rakendamine**: varundusmehhanism seadistatakse (sh krüpto ja ligipääsud).
3. **Jälgimine**: jälgitakse varunduse edukust ja alertitakse ebaõnnestumisi.
4. **Taastetest**: vähemalt [kvartalis/poolaastas] tehakse taastetest (valimi alusel).
5. **Parandus**: ebaõnnestumisel dokumenteeritakse põhjus ja parandatakse.

## 7. Logimine ja tõendusmaterjal

- Varunduse edukuse raportid (ajalugu), alertid, taastetestide protokollid.
- Tõendid: tööriista raportid, ticketid, runbook.
- Säilitusaeg: [täida].

## 8. Mõõdikud ja regulaarne ülevaatus

- Varunduste edukuse määr (%).
- Taastetestide edukus ja RTO saavutamine.
- Ebaõnnestumiste keskmine lahendusaeg.

## 9. Erandolukorrad ja eskalatsioon

- Korduv varunduse ebaõnnestumine: eskalatsioon Ops + teenuseomanik.
- Kahtlus kompromiteerimisele: infoturve kaasamine; vajadusel võtmete vahetus.

