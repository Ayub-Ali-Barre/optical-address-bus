# Optisk Adressbuss-Simulator

En webbaserad simulator för optisk kamerakommunikation (Optical Camera Communication / OCC). 
Simulatorn visar 4 rektangulära ljuskällor mot en mörk bakgrund med hög kontrast, optimerad för avläsning med webbkamera och datorseende (OpenCV).

## Funktioner

- **16 Adressbussar (0–15):** Varje adress representeras av ett unikt 4-bitars färgmönster över 4 rektanglar.
- **Färgkodning:**
  - 🔴 **Röd** = Logisk `0`
  - ⚪ **Vit** = Logisk `1`
- **Exempel:**
  - Adressbuss 0: `0000` (Röd, Röd, Röd, Röd)
  - Adressbuss 5: `0101` (Röd, Vit, Röd, Vit)
  - Adressbuss 15: `1111` (Vit, Vit, Vit, Vit)
- **Kameravy-läge:** Möjlighet att dölja all kringliggande text och endast visa de 4 rektanglarna mot ren svart bakgrund.
- **Auto-loop:** Sekvensering genom alla 16 adresser med inställbar hastighet för kontinuerlig testning av OpenCV-skript.
