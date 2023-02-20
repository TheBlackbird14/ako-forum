# Projekttagebuch

### Die Dokumentation meiner Arbeit zur Projektarbeit html 

---

## Inhalt

1. Anfangs Phase
    - [Vorarbeit/Vorwissen](#vorwissen)
    - [Einrichtung der Tools](#einrichtung)
2. Konzept Phase
    - [Erstes Kundengespräch](#Kundengespräch)
    - [Erstes Wireframe](#firstWireframe)
3. Design Phase
    - [Stunde vom **2.2**](#2.2)
    - [**3 - 5** Februar](#3.2-5.2)
4. Developing Phase
    - [**10 - 12** Februar](#10-12.2)
    - [**13 - 15** Februar](#13-15.2)
5. Integration Phase
6. Veröffentlichung

---

# Anfangs Phase

## Vorarbeit/Vorwissen <a name="vorwissen"></a>

Ich habe schon in Vorbereitung zu der Projektarbeit mir viel Material angeguckt, vor Allem zum Thema Design. Auf diese Thema wollte ich mich bei diesem Projekt fokussieren, da ich im Bereich des Web Developements schon eher erfahren war. Hierzu habe ich mir auf YouTube hauptsächlich eine Reihe zu dem Thema angeschaut, die von einem angeblich sehr erfahren Web Designer online zur Verfügung gestellt wurde. [Hier der Link.](https://www.youtube.com/playlist?list=PLXC_gcsKLD6n7p6tHPBxsKjN5hA_quaPI)

---

## <a name="einrichtung"></a> Einrichtung der Tools 

Als wir am **31.1** mit der Arbeit angefangen haben, habe ich erst mal das Github repo entsprechend mit dem Skeleton eingerichtet. Ebenfalls habe ich ein Project Board zum managen von Todos eingerichtet. In der restlichen Stunde habe ich mir von der bestehenden Ako Forum Seite einen Überblick verschafft und schon ein paar Konzept Ideen für die Landing Page auf meinem iPad entwickelt. 

--- 

# Konzept Phase

## Erstes Kundengespräch <a name="Kundengespräch"></a>

Am **Mittwoch, 1.2** hatte ich mein Erstes Gespräch mit Herrn Tabatabei. Dort haben wir ersteinmal die bestehende Ako Forum Seite besprochen, welche Funktionalitäten wichtig sind und welche verbessert werden könnten. Hierbei hat sich für mich Folgendes ergeben: <a name="voraussetzungen"></a>

- Die bestehende Webseite ist klaglos veraltet und besteht nur noch aus einem veralteten WordPress Projekt und existiert schon lange Jahre. 
- Die Hauptfunktionalität der Seite für das Ako Forum selber ist die Anmeldung. Diese verläuft über einen eMail Automatismus, einmal an das Forum und dann an an den Kunden
- Die Bearbeitung der Seite, beispielweise für neuen Blog Inhalt oder neue Kurs info, ist durch fehlende Expertise deutlich erschwert und nicht immer ohne "Kollateraleschaden" (durch bearbeiten einer Sache eine Andere Sache unwiderruflich durcheinanderbringen)

Für mich heißt das, dass ich einen Weg finden muss den einfachen Zugang für das Forum zu gewähren und dabei den eMail Automatismus aufrecht zu erhalten.

***Spezifische Design Ideen haben wir allerdings nicht besprochen.***

---

## Erstes Wireframe <a name="firstWireframe"></a>

In Anschluss an diese Gespräch habe ich am Nachmittag ein erstes schnelles wireframe für die Landing page in Adobe XD entwickelt um eine Idee zu kriegen, wo ich mit welchen Farben arbeiten könnte. Auf Typographie habe ich hier erst einmal keine Rücksicht genommen. 

![Der 1. Entwurf der Landing Page in XD](./assets/forumErstesWireframe.png)

---

## Stunde vom **2.2** <a name="2.2"></a>

In der Stunde habe ich mich informiert, welche Tools ich benutzen möchte, um die vorher genannten [Voraussetzungen](#vorraussetzungen) zu erfüllen. Hierbei habe ich mich dazu entschieden eine WordPress Seite zu benutzen, damit man über templates u.Ä. neuen Content einfach hinzufügen kann. Auch die eMail Automation kann man über diese Tool einrichten. Allerdings werde ich erst mal die Seite manuell designen und developen. 

---

## 3 - 5 Februar <a name="3.2-5.2"></a>

An diesem Wochenende habe ich die Landing page weiter designed damit man darunter die Kurskategorien auswählen kann:

![Kurskategorien Auswahl](./assets/kurseAuswahlDesign.png)

Zusätzlich habe ich auch noch die templates für die daran anhängenden Seiten entworfen, wo man dann eine Kurze kursübersicht zu allen Kursen in der Kategorie kriegt und dann zu dem Kurs weitergehen kann.

![Kursauswahl](./assets/offenesForumDesign.png)

---

## 10 - 12 Februar <a name="10-12.2"></a>

An diesem Wochenende habe aufgrund der sich immer näher rückenden Deadline mit dem Developement Prozess angefangen. Hierbei habe ich mich dazu entschieden nur eine Seite zu entwickeln, da ich sonst keine Zeit dazu habe. 
In den drei Tagen habe ich den CSS flex header geschrieben und den Hero (die titelseite) angefangen, obwohl ich hier bis auf den Titel nicht weit gekommen bin. So sieht es aber bisher aus:

![bestehende Website Hero Section Abschnitt](./assets/AkoForumDevPreviewHero1.png)

Besonders der flex header ist eher kompliziert da das CSS flexbox Modell nicht immer das macht was man möchte. Im ende hat ungefähr das hier für mich funktioniert. 

```css
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 12.685vw;
}

.navLinks {
  list-style: none;
  right: 1.041vw;
}

.navLinks li {
  display: inline-block;
  padding: 0 1.041vw;
 
}
```

---

## 13 - 15 Februar <a name="13-15.2"></a>

An den paar Tagen vor den Karnevalsferien habe ich hauptsächlich an daran gearbeitet, die Seite responsive zu machen, also dafür sorgen, dass die Inhalte auf allen bildschirmgrößen adäquat dargestellt werden kann. Hierzu muss ich im CSS code alle werte die eine feste Anzahl sind (px, cm, in) ersetzen durch eine relative (%, vw, rem). Dann habe ich beispielsweise statt diesem code:

```css
.logo {
  width: 105px;
  height: 125px;
  padding-left: 140px;
}
```

diesen code:

```css
.logo {
  width: 9.722vw;
  height: 11.574vw;
  margin-left: 7.29167vw;
}
```

Dies macht die Website viel zugänglicher für Alle und ist einfacher von Anfang an einzuführen, weil zurück gehen und alle werte ersetzen, dann wenn es nötig ist, keine einfache und fehlerlose Lösung ist. 

---

## Montag 20 Februar 