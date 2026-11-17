# Optisk LED-Transmitter & Timing-Simulator

Webbaserad sändarsimulator för optisk kamerakommunikation (Optical Camera Communication, OCC), uppdaterad för direkt testning mot mobilappen `optical-scanner-app` och `led_decoder.py`.

**Live GitHub Pages:** [https://ayub-ali-barre.github.io/optical-address-bus/](https://ayub-ali-barre.github.io/optical-address-bus/)

---

## Funktioner

### 1. Kontinuerlig 16-stegs kodtabell (Standardläge)
- Innehåller exakt samma 15 st 16-symbolsmönster (adress `1`–`15`) som mobilappen och `led_decoder.py`.
- Sänder cykliskt utan startpuls, slutsignal eller paus.
- Standardhastighet `50 ms` per symbol (snabbval `50 ms`, `100 ms` och `200 ms` matchar appens inställningsmeny).
- Faslåst klocka via `performance.now()` och `requestAnimationFrame` utan CSS-övergångar på lampan för skarpa, driftfria ljuspulser.

### 2. Kameraläge (Helskärm)
- Döljer reglage och visar lampan mot helsvart bakgrund (`#000000`) med lagom marginal så att kamerans siktruta får med både lampan och mörk kant utan full pixelklippning.
- Du kan byta adress `1`–`15` live under pågående sändning.

### 3. Anpassat paketläge & Sparade mönster
- Växla flik till **Anpassat paketläge** för egna binära sekvenser med startpuls, slutsignal och paus.
- Realtids-oscilloskop, FPS-estimator, sparning i `localStorage` samt JSON-export/import.
