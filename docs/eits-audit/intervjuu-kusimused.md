# Intervjuu küsimused (E-ITS / EITS)

## 1. Süsteemi omanik / teenuseomanik

- Mis on teenuse eesmärk ja kriitilisus? (mõju, sõltuvused)
- Mis on skoobis ja mis mitte? Kas see on dokumenteeritud?
- Kes vastutab infoturbe riskide eest? Kuidas riskid aktsepteeritakse?
- Millised on RTO/RPO ja kas need on testitud?

## 2. Infoturbejuht (CISO) / infoturbe spetsialist

- Milline on infoturbe juhtimissüsteem/korraldus (poliitikad, rollid, kontrollid)?
- Kuidas hallatakse turbenõuete elutsüklit (muudatused, ülevaatus, kinnitused)?
- Kuidas tehakse turbeintsidentide käsitlust ja aruandlust?
- Kuidas tehakse turbealast koolitust ja teavitust?

## 3. Arendus (Tech lead / arendajad)

- Kuidas turbenõuded jõuavad arendusse? (Definition of Done, threat modeling)
- Kuidas toimub koodireview ja millised kontrollid on CI-s?
- Kuidas hallatakse sõltuvusi ja haavatavusi? (SCA, CVE protsess)
- Kas on turvatestid (SAST/DAST), kuidas tulemusi käsitletakse?

## 4. Ops / SRE / Admin

- Kuidas hallatakse konfiguratsioone (IaC, secrets, keskkonnamuutujad)?
- Kuidas tagatakse logide säilitus ja terviklus? Kes pääseb ligi?
- Milline on monitooring/alerting (mida jälgitakse, reageerimisajad)?
- Kuidas tehakse varundusi ja taastamist? Millal viimati testiti?

## 5. Andmekaitse (DPO), kui kohaldub

- Millised isikuandmed töödeldakse ja mis on õiguslik alus?
- Millised on säilitusajad ja kustutamise protsess?
- Kuidas on lahendatud andmesubjekti päringud (juurdepääs, kustutus, parandamine)?

## 6. Teenusepakkujad / tarnijad

- Millised teenusepakkujad on kriitilised ja miks?
- Millised turbenõuded on lepingutes ja kuidas nende täitmist kontrollitakse?
- Kuidas käsitletakse tarnija intsidente ja teavitusi?

