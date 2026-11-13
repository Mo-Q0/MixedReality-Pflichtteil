# Mixed Reality – Pflichtteil (Arbeitsversion)

## Abgabeanforderungen (Moodle, 22.11.2026)

1. `inline-session.html`: Eine erweiterte Variante der offiziellen Inline-Session mit VR-Button und AR-Button.
2. `aframe-szene.html`: Eine A-Frame-Szene mit mindestens fünf Objekten, mindestens einem importierten 3D-Objekt, einer Textur, einer Lichtquelle und sichtbarem Schattenwurf.
3. Ein **echtes Demonstrationsvideo beider HTML-Seiten**. Dieses Video ist noch **nicht** in diesem Archiv enthalten und muss auf einem geeigneten Gerät selbst aufgenommen werden.

## Start

1. ZIP entpacken und Ordner in VS Code öffnen.
2. `index.html` mit Live Server starten. A-Frame funktioniert am PC mit Internetverbindung.
3. Für echte AR- und VR-Buttons `index.html` über **HTTPS (z. B. GitHub Pages)** auf einer geeigneten Meta Quest oder einem AR-fähigen Android-Gerät aufrufen.
4. Falls der normale PC kein WebXR besitzt, sind die XR-Tasten nicht verfügbar; dies ist kein Beweis für einen Codefehler.

### Inline Session

- Verwendet das Szenen-Modell aus den offiziellen WebXR-Samples (3D-Sonnensystem).
- Prüft getrennt `immersive-vr` und `immersive-ar`.
- Startet Inline, VR oder AR; in AR wird die Skybox ausgeblendet, sodass der reale Hintergrund sichtbar ist.
- Setzt die AR-Modellskalierung kleiner, damit sie in den Raum passt; die enthaltenen Objekte bleiben identisch.
- Nutzt Module und 3D-Assets aus dem offiziellen Online-Beispiel. **Dafür ist Internet nötig.**

### A-Frame-Szene

- Mehr als fünf Objekte: Boden, importierte Kiste, Plattform, Kugel, Zylinder, Kegel und Torus.
- `assets/cargo_crate.glb` ist ein lokal beigefügtes echtes, importiertes 3D-Modell.
- `assets/boden.png` ist eine lokal beigefügte Textur.
- `DirectionalLight` mit `castShadow: true`; bei den Objekten `shadow` auf cast/receive gestellt.
- Nutzt A-Frame per CDN. **Dafür ist Internet nötig.**

## Testliste vor der Abgabe

- [ ] Beide HTML-Dateien laden ohne rote Fehler in der Konsole.
- [ ] WebXR: Inline-Szene am Bildschirm sichtbar.
- [ ] WebXR: VR auf dem geeigneten HMD erfolgreich gestartet und beendet.
- [ ] WebXR: AR auf einem kompatiblen Gerät erfolgreich gestartet und beendet; echter Hintergrund sichtbar.
- [ ] A-Frame: alle Objekte einschließlich der importierten Kiste zu sehen.
- [ ] A-Frame: Bodentextur und Schattenwurf klar erkennbar.
- [ ] Ein kurzes Video zeigt **beide** Seiten und ihre Funktionen.

**Wichtig:** Der Code wurde statisch geprüft, aber die reale Ausführung mit Quest/Smartphone lässt sich hier nicht verifizieren. Vor einer endgültigen Abgabe selbst testen und eventuelle gerätespezifische Fehler korrigieren.

## Quellen / verwendete Materialien

- Immersive Web Community Group, WebXR Samples – „Inline Session“ und „Immersive AR Session“; MIT-Lizenz: https://github.com/immersive-web/webxr-samples
- WebXR Samples Demo und zugehörige JS-Module und GLTF-Assets: https://immersive-web.github.io/webxr-samples/
- A-Frame, Dokumentation: https://aframe.io/docs/
- A-Frame Shadow-Komponente: https://aframe.io/docs/1.8.0/components/shadow.html
- Three.js und WebXR aus den Vorlesungs- und Übungsmaterialien dieser Lehrveranstaltung.
- GLB-Kiste (`assets/cargo_crate.glb`) und Boden-Bildtextur (`assets/boden.png`) wurden für diese Arbeitsversion erzeugt.

Die Änderung der Original-Online-Beispiele ist in `inline-session.html` kommentiert. Die MIT-Lizenz des Beispielprojekts liegt unter `LIZENZ_WEBXR_SAMPLES.txt`.
