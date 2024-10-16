# Tag 4 des Praktikumsberichts

# Einrichtung und Test einer Docker-Entwicklungsumgebung

## Aufgabenübersicht

1. **Docker Entwicklungsumgebung einrichten**
2. **Recherchieren zu Docker Mount Binds und Volumes**
3. **Einrichten eines nginx Containers mit Mount Bind**
4. **Erstellen einer eigenen index.html und CSS**
5. **Erstellen und Testen eines Docker Images mit einer eigenen HTML-Datei**

---

## 1. Docker Entwicklungsumgebung einrichten

Zunächst habe ich eine Docker-Entwicklungsumgebung erstellt und die Grundlagen von Docker Mount Binds recherchiert. Ich habe die Unterschiede zwischen Mount Binds und Docker Volumes untersucht:

- **Mount Binds**: Erlauben es, ein Verzeichnis oder eine Datei von der Host-Maschine in den Container zu mounten.
- **Volumes**: Docker verwaltet die Speicherung und den Zugriff auf Daten, die unabhängig von der Container-Lebensdauer sind.

### Relevante Dokumentation

- [Docker Bind Mounts](https://docs.docker.com/engine/storage/bind-mounts/)

---

## 2. Erstellen eines neuen Verzeichnisses

Ich habe ein neues Verzeichnis in meinem Praktikums-Repository erstellt:

```bash
mkdir nginx_dev_environment
```

## 3. Erstellen von index.html Datei 

```bash
<!doctype html>
<html lang="de">
<head>
    <meta charset="utf-8">
    <title>Lebenslauf</title>
    <link rel="stylesheet" href="style.css">
</head>
<body style="background-color:#edededcc;">

    <h1 style="font-size:100px; text-align:center;">Lebenslauf</h1>

    <h2 style="font-size:40px;">Persönliche Daten</h2>
    <p>Jonas Mann</p>
    <p>Geboren am: 28. April 2006</p>
    <p>Adresse: Handstraße 34, 51469 Bergisch Gladbach</p>
    <p>E-Mail: jonasmann@bkgl.bgl.schule</p>

    <h2 style="font-size:40px;">Hobbys</h2>
    <ul>
        <li>Kochen</li>
        <li>Kickboxen</li>
        <li>Motiongrafics</li>
    </ul>

    <h2 style="font-size:40px;">Berufserfahrung</h2>
    <h3>Beispielunternehmen</h3>
    <p>Position: Softwareentwickler</p>
    <p>Zeitraum: 2015 - 2024</p>
    <p>Beschreibung: Entwicklung von Webanwendungen mit modernsten Technologien.</p>

    <h2 style="font-size:40px;">Ausbildung</h2>
    <h3>Beispieluniversität</h3>
    <p>Studiengang: Informatik</p>
    <p>Abschluss: Bachelor of Science</p>
    <p>Zeitraum: 2010 - 2015</p>

    <img src="Hund_Image.webp" alt="Hund Test" width="500" height="500" style="display:block; margin:auto;">

    <nav>
        <ul class="menu">
            <li><a href="#">Home</a></li>
            <li>
                <a href="#">Über uns</a>
                <ul class="dropdown">
                    <li><a href="#">Team</a></li>
                    <li><a href="#">Geschichte</a></li>
                </ul>
            </li>
            <li><a href="#">Kontakt</a></li>
        </ul>
    </nav>
    
</body>
</html>
```

## 3. Erstellen von style.CSS Datei 

```bash
body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    background-color: #f5f5f5;
    margin: 0;
    padding: 20px;
}

nav {
    background-color: #333;
    padding: 10px;
}

.menu {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.menu > li {
    display: inline-block;
    position: relative;
}

.menu a {
    color: white;
    text-decoration: none;
    padding: 10px 15px;
    display: block;
}

.menu a:hover {
    background-color: #575757;
}

.dropdown {
    display: none;
    position: absolute;
    background-color: #333;
    min-width: 160px;
    z-index: 1;
}

.dropdown li {
    display: block;
}

.menu li:hover .dropdown {
    display: block;
}

.container {
    max-width: 800px;
    margin: auto;
    background-color: white;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

h1 {
    color: rgb(47, 47, 47);
    font-size: 3em;
    margin-bottom: 20px;
}

h2 {
    color: rgb(47, 47, 47);
    font-size: 2em;
    margin-top: 30px;
    margin-bottom: 10px;
    border-bottom: 2px solid #e0e0e0;
    padding-bottom: 10px;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    color: rgb(47, 47, 47);
    font-size: 1.2em;
    margin-bottom: 10px;
}

img {
    max-width: 100%;
    height: auto;
    border-radius: 20px;
    margin-top: 20px;
}
```
## 3. Erstellen von Dockerdatei

```bash
FROM httpd:latest

COPY index.html /usr/local/apache2/htdocs/
COPY styles.css /usr/local/apache2/htdocs/
COPY cat.jpg /usr/local/apache2/htdocs/

WORKDIR /usr/local/apache2/htdocs/
```