# Lukuvinkkikirjasto

Ohtu-miniprojekti

[![GitHub Actions](https://github.com/brontto/ohtu-miniprojekti/workflows/CI/badge.svg)](https://github.com/brontto/ohtu-miniprojekti/actions)
[![codecov](https://codecov.io/gh/brontto/ohtu-miniprojekti/branch/main/graph/badge.svg?token=DYFHMFXATT)](https://codecov.io/gh/brontto/ohtu-miniprojekti)

## Definition of Done
- Toiminnallisuus on looginen osa ohjelmaa
- Koodille on kirjoitettu testit
- Testikattavuus on 70% 

[Burndown-käyrä](https://docs.google.com/spreadsheets/d/1m27JJOADbrihQkSxDsu489VpF2iS6y8GJkZCpKXE13c/edit#gid=139589834)

[Product backlog](https://github.com/brontto/ohtu-miniprojekti/projects/1)


## Heroku 
[Heroku App](https://damp-dawn-78777.herokuapp.com/)

## Tietokannan käyttöönotto

Asenna PostgreSQL

Asenna uudet riippuvuudet 
```
poetry install
```
Luo juurihakemistoon tiedosto *.env* ja lisää sinne rivi
```
DATABASE_URL=postgresql:///database_name
```
missä `database_name` on käyttämäsi tietokannan nimi (todennäköisesti joko `postgres` tai käyttäjänimesi).

Alusta tietokantataulut komennolla
```
psql < schema.sql
```
Jos haluat testata pelkkiä lukuvinkkejä ilman käyttäjien luomista, pitää tietokantaan luoda yksi käyttäjä, tämä onnistuu psql-tulkissa komennolla
```
INSERT INTO kayttajat (tunnus, salasana) VALUES ('testaaja', 'testi');
```
