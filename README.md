# Optisk LED-Transmitter & Timing-Simulator

En avancerad webbaserad simulator för optisk kamerakommunikation (Optical Camera Communication / OCC). 
Simulatorn sänder data och adressbussar genom en enda optisk LED-lampa som blinkar i en tidsinställbar takt optimerad för datorseende och OpenCV.

🌐 **Live GitHub Pages:** [https://ayub-ali-barre.github.io/optical-address-bus/](https://ayub-ali-barre.github.io/optical-address-bus/)

---

## Nya Funktioner

### 1. Optisk LED-Lampa
- **Avstängd (0):** Mörk skifferblå/svart med subtil kant, så kameran kan behålla positionen.
- **Tänd (1):** Intensivt elektrisk blå lampa med radial ljusspridning/glow.
- **Kameraläge (Helskärm):** Döljer all text och knappar och visar endast lampan mot en helsvart bakgrund.

### 2. Full Kontroll över Takt & Tajming
- **Bit-duration (30 – 1000 ms):** Justera exakt klocktakt i millisekunder eller välj snabbknappar (400ms, 200ms, 100ms, 50ms).
- **Startpuls (1x – 6x bit-tid):** Preamble-signal med hög puls för att synkronisera kamerans klocka.
- **Paus mellan paket (100 – 3000 ms):** Inter-paket-gap vid kontinuerlig loopning.
- **FPS-kalkylator:** Beräknar i realtid hur många bildrutor en 30 FPS och 60 FPS webbkamera fångar per bit.

### 3. Mönsterhanterare (Spara & Återanvänd)
- **Spara mönster:** Namnge och spara en kombination av binär sekvens + exakta millisekundstider.
- **LocalStorage:** Mönstren sparas direkt i webbläsaren och finns kvar vid återbesök.
- **Exportera & Importera:** Dela sparade mönster som `.json`-filer mellan enheter eller kollegor.

### 4. Realtids-Oscilloskop
- Visar en kontinuerlig vågform av den elektriska/optiska signalen i synk med lampans blinkningar.
