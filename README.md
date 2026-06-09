# Õpetajate Otsingusüsteem

## Projekti kirjeldus

Õpetajate Otsingusüsteem on veebirakendus, mis võimaldab õpilastel leida sobivaid eraõpetajaid, saata tunni taotlusi ning hinnata õpetajate tööd pärast tunni läbimist.

Süsteem ühendab õpilasi ja õpetajaid ühel platvormil, pakkudes mugavat suhtlust ning tundide haldamist.

---

## Figma link
https://www.figma.com/design/0RJm4mmnktwBLIJ1basxID/Prodigy?node-id=0-1&p=f&t=fuKbIZ78L3ZYM9c5-0

---

## Projekti eesmärk

Luua kasutajasõbralik veebikeskkond, kus:

* Õpilased saavad otsida õpetajaid.
* Õpetajad saavad hallata oma profiile ja tundide pakkumisi.
* Õpilased saavad saata tunni taotlusi.
* Kasutajad saavad jätta arvustusi ja hinnanguid.
* Õpetajad saavad teavitusi uutest päringutest.

---

## Peamised funktsioonid

### Õpilane

* Registreerimine ja sisselogimine
* Õpetajate otsimine
* Õpetajate filtreerimine
* Lemmikõpetajate salvestamine
* Tunni taotluse esitamine
* Õpetajate hindamine ja arvustamine

### Õpetaja

* Profiili haldamine
* Õppeainete lisamine
* Tunni taotluste vastuvõtmine
* Teavituste saamine uutest päringutest
* Arvustuste vaatamine

### Administraator

* Kasutajate haldamine
* Süsteemi jälgimine
* Probleemsete kontode haldamine

---

## Kasutatud tehnoloogiad

### Frontend

* HTML
* CSS
* JavaScript
* TypeScript

### Backend

* Node.js
* Express.js

### Andmebaas

* MySQL

### Muud tööriistad

* Git
* GitHub
* Postman
* Figma

---

## Andmebaasi peamised tabelid

* Users
* Profiles
* Tutors
* Subjects
* LessonRequests
* Reviews
* Favorites
* Notifications

---

## Kasutuslood

1. Õpilane otsib õpetajat.
2. Õpilane saadab tunni taotluse.
3. Õpetaja saab teavituse.
4. Õpetaja kinnitab või lükkab taotluse tagasi.
5. Pärast tundi jätab õpilane arvustuse ja hinnangu.

---

## Projekti autorid

* Vitali Kolesnikov
* Projektimeeskonna liikmed

---

## Projekti staatus

Projekt on loodud õppetöö raames ning on arendusjärgus.

# Kuidas süsteemi paigaldada / käivitada

## 1. Sõltuvused (Dependencies)

Enne süsteemi käivitamist peavad olema paigaldatud:

* Docker 24+
* Docker Compose 2+
* Git

## 2. Andmebaasi seadistamine

1. Klooni projekt:

```bash
git clone <repository-url>
cd project
```

2. Käivita andmebaas:

```bash
docker compose up -d db
```

3. Loo vajalikud tabelid:

```bash
docker compose exec app python manage.py migrate
```

4. Laadi testiandmed:

```bash
docker compose exec app python manage.py loaddata testdata.json
```

## 3. Süsteemi käivitamine

Käivita kogu süsteem:

```bash
docker compose up -d
```

Kontrollimiseks ava veebilehitsejas:

```text
http://localhost:8000
```

Kui avaleht avaneb ilma veateadeteta, on süsteem edukalt käivitatud.

