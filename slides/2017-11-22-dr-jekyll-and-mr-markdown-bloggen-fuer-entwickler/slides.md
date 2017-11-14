## Dr. Jekyll and Mr. Markdown
### Bloggen für Entwickler

Ottmar Gobrecht, Markus Dötsch

DOAG Konferenz 2017, Nürnberg

-----

## Motivation (md)

---

### Wissen teilen!

Oder zumindest bewahren! :)

---

### Schnell und unkompliziert

Hürden minimieren!

---

### Bekannte Tools

Context Switches vermeiden!

---

### Bloggen als Teil der "normalen" Arbeit

Nicht als extra Teil ansehen!

-----

## Was ist Jekyll? (og)

---

### Ein Generator für statische Webseiten

Genauer, ein Ruby Skript

---

### Was soll das bringen?

---

- Geschwindigkeit
- Sicherheit

---

Geschwindigkeit dynamisch - schnell (DSL)

![WordPress Beispiel](./assets/ladezeit-dynamisch.png)

87 Requests - 1,3 MB - 2,7 s Ladezeit

---

Geschwindigkeit statisch - schnell (DSL)

![Jekyll Beispiel](./assets/ladezeit-statisch.png)

2 Requests - 5 KB - 0,1 s Ladezeit

---

Geschwindigkeit dynamisch - langsam (mobil)

![WordPress Beispiel](./assets/ladezeit-dynamisch-langsam-mobil.png)

86 Requests - 1,3 MB - 36,3 s Ladezeit

---

Geschwindigkeit statisch - langsam (mobil)

![Jekyll Beispiel](./assets/ladezeit-statisch-langsam-mobil.png)

2 Requests - 5 KB - 4,2 s Ladezeit

---

[Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/?hl=de&url=ogobrecht.github.io&tab=mobile)

![WordPress Beispiel](./assets/page-speed-statisch-mobil.png)

---

[Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/?hl=de&url=ogobrecht.github.io&tab=desktop)

![WordPress Beispiel](./assets/page-speed-statisch-desktop.png)

---

[Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/?hl=de&url=www.thatjeffsmith.com&tab=mobile)

![WordPress Beispiel](./assets/page-speed-dynamisch-mobil.png)

---

[Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/?hl=de&url=www.thatjeffsmith.com&tab=desktop)

![WordPress Beispiel](./assets/page-speed-dynamisch-desktop.png)

---

### FIXME Screenshot DokuWiki einfügen wegen Sicherheit

-----

## Was ist Markdown? (og)

---

### Eine vereinfachte Auszeichnungssprache

Vornehmlich zur HTML Erstellung

---

### Ziel

Ohne Konvertierung leicht les- und schreibbar

```markdown
# Eine Überschrift der ersten Ordnung

## Eine Überschrift zweiter Ordnung

Ein Absatz mit *kursivem Text* , **fettem Text** und
einer ***Kombination aus fett und kursiv***.

- Ein Aufzählungspunkt
- Noch einer
  - Ein Unterpunkt

[Ein Link](https://daringfireball.net/projects/markdown/syntax)

![Ein Bild](/assets/john-gruber.png)
```

---

### Abgrenzung

HTML = Publikations-Format

Markdown = Schreib-Format

---

### Toolunterstützung

![Editor Atom mit Live-Vorschau](./assets/editor-atom.png)

[Editor Atom](https://atom.io/) mit [Plugin Markdown-Writer](https://atom.io/packages/markdown-writer)

---

...

-----

## Online in 5 Minuten (og)

Alles im Browser - Demo ...

---

- Login to your [GitHub](https://github.com/)
- Fork repository [HydeBar](https://github.com/ogobrecht/hydebar)
- Edit `_config.yml` (url, baseurl)
- Change repository settings
    - Rename to yourUserName.github.io
    - Evtl. activate GitHub Pages

---

### Vervollständigung Konfiguration

- `_data/authors`
- `_config.yml`
  - permalink: /posts/:year-:month-:day-:title (einstellen und nicht mehr ändern)
  - ...

---

...

-----

## Optionale Installation lokal (md)

Für Neugierige und "Selbermacher"

---

### Installation Git Client

- https://git-scm.com/docs/gittutorial
- http://rogerdudler.github.io/git-guide/index.de.html

---

### Installation Ruby

- https://www.ruby-lang.org/de/documentation/installation/
- https://rubyinstaller.org/

---

### Installation Jekyll

- https://jekyllrb.com/docs/installation/
- https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/

Paketmanager und Jekyll:
```sh
gem install bundler
bundle install
```

Anmerkung:

- Windows ist von Jekyll nicht offiziell unterstützt
- Dokumentation - https://jekyllrb.com/docs/windows/
- Windows 10 - Integrierte Bash verwenden

---

### Installation Blog

Im (übergeordneten) Projektverzeichnis:
```sh
git clone yourForkedRepoURL.git
```

Das lokale Verzeichnis wird automatisch angelegt

```sh
cd yourForkedRepoName
bundle install
```

Notwendige Jekyll files werden installiert

Anmerkung:

GitHub URL = https://github.com/UserName/RepoName.git
Beispiel: https://github.com/Madtsch/madtsch.github.io.git

---


### Starten Devserver

Automatischer refresh bei Änderungen
```sh
bundle exec jekyll serve
```

Server ist unter http://http://127.0.0.1:4000 aufrufbar

Einmaliger refresh
```sh
bundle exec jekyll build
```

---

### Publishen der Änderungen auf GitHub

```sh
git push yourForkedRepoURL.git
```

---

### Spätere Updates von Jekyll

```sh
bundle update
```

-----

## Inhalte Erstellen (md)

---

### Online

- GitHub
- Trello

---

### Demo...

---

### Offline Toolempfehlungen

- Editor Atom
  - Plugin: Markdown-Writer
- Editor Visual Studio Code
  - Plugin: Markdown All in One
- ...

---

### Demo...

---

### Spezialitäten im Jekyll Umfeld

- Reveal.js
- Bild: `![Python Pandas](./assets/pandas.pydata.org.png) <!-- .element: width="600px" -->`
- Beispiel Bildergalerien (Touch-Ünterstützung)
- TOC: {% raw %}`{% include toc %}`{% endraw %}

---

Demo...

---

...

-----

## Die Jekyll Blackbox (md)

---

### Was ist ein Post?

---

- liegt im Ordner `_posts`
- Namenskonvention (ISO Datum)
-

---

### Was ist eine Page?

---

### Frontmatter

Die Metadaten

---

### Verzeichnisstruktur

---

### Implizite Metadaten

- Verweis Doku
-

-----

## Jekyll selbst erweitern (og)
Beispiel Reveal.js Integration

---

### Liquid

Die Templatesprache

- https://shopify.github.io/liquid/
- https://shopify.github.io/liquid/basics/variations/
- http://jekyllrb.com/docs/templates/

---

### Erweiterungsvorschläge

- Eigene Domain für den Blog
- Migration von existierenden Blogs (Wordpress, usw.) - http://import.jekyllrb.com/docs/home/
- Disqus für Kommentarfunktion
- Einsatz von Google Analytics

-----

## Links (og)

---

### Weitere Jekyll Themes/Templates

- Mit ["Fork Quick Start"](https://github.com/barryclark/jekyll-now#other-forkable-themes)
- [Step by Step Anleitung](http://jmcglone.com/guides/github-pages/)

---

## Weitere Static Site Generators

- [Hugo](https://gohugo.io/) (Go)
- [Hexo](https://hexo.io/) (Node.js)
- [Gatsby](https://www.gatsbyjs.org/) (Node.js, React)
- [Pelican](https://blog.getpelican.com/) (Python)
- ...
- [Top Ten Liste 2017](https://www.netlify.com/blog/2017/05/25/top-ten-static-site-generators-of-2017/)
- [Übersicht nach Beliebtheit](https://www.staticgen.com/)

---

## The End

### Fragen?

[ogobrecht.github.io](https://ogobrecht.github.io)

[madtsch.github.io](https://madtsch.github.io)  
