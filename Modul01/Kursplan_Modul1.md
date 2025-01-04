
### Modul 1: Kom i gang: Verktøyoppsett

#### **Læringsmål**

- Gi deltakerne en grunnleggende forståelse av typiske verktøy brukt av utviklere.
- Opprette et fungerende utviklingsmiljø for videre arbeid i kurset.

---

### **Undervisningsinnhold**

#### **0. Oversikt over moduler som kommer**

1. Kom i gang: Verktøyoppsett
2. Grunnleggende programmering (Python)
3. Webrammeverk (Flask)
4. Versjonshåndtering (Git)
5. CI/CD
6. Skydeployering (Azure)
7. Logging
8. Debugging
9. Kodestandarder
10. Teknisk gjeld
11. Sikkerhet
12. API-integrasjon og AI

---

#### **1. Verktøyoppsett (20 min)**

- **Mål:** Installere og konfigurere Visual Studio Code (VSC) og Python-miljø.

- **Detaljerte trinn:**

  1. Først skal du laste ned og installere Visual Studio Code (VSC). VSC er et utviklingsverktøy, i praksis et verktøy for å skrive tekst. Du kan laste ned ulike moduler som tilpasser det for ulike programmeringsspråk. Last ned fra [https://code.visualstudio.com](https://code.visualstudio.com).
     - Velg riktig versjon for ditt operativsystem (Windows, macOS, eller Linux).
     - Under installasjonen, velg alternativet for å legge til VSC i systemets PATH (valgfritt, men anbefalt).
  2. Neste steg er å installere et kjøremiljø for Python. Et kjøremiljø lar deg ta tekstfiler, oversette dette til maskinkode og kjøre denne. Installer Python fra [https://www.python.org](https://www.python.org).
     - Velg den nyeste stabile versjonen av Python.
     - Huk av for "Add Python to PATH" under installasjonen.
  3. Du vil også trenge noen moduler i VSC for å kunne jobbe med Python. Start Visual Studio Code og gå til "Extensions"-panelet ved å klikke på ikonet til venstre eller trykke `Ctrl+Shift+X`.
     - Søk etter og installer følgende utvidelser:
       - **Python** (Microsoft) – Gir støtte for Python-språket i VSC.
  4. Siden du antagelig ikke har administrative tilganger på din PC, vil VSC ikke automatisk finne Python. Derfor må du manuelt fortelle VSC hvor du installerte Python:
     - Åpne kommandopaletten i VSC ved å trykke `Ctrl+Shift+P`.
     - Søk etter og velg `Python: Select Interpreter`.
     - Klikk på `Enter interpreter path` nederst.
     - Velg `Find...` for å åpne filutforskeren.
     - Naviger til der Python er installert. Typisk sti kan være:
       ```
       C:\Users\<DittBrukernavn>\AppData\Local\Programs\Python\PythonXX\python.exe
       ```
     - Klikk `OK` for å bekrefte.
     - Etter dette bør VSC bruke riktig Python-interpreter.

---

#### **2. Første program: Hello World (15 min)**

- **Mål:** Lære å opprette en prosjektmappe, skrive og kjøre et Python-program.
- **Aktivitet:**
  1. Opprett en prosjektmappe:
     - Velg et sted på datamaskinen (f.eks. "Documents" eller "Desktop").
     - Opprett en ny mappe med navnet "PythonProsjekt".
  2. Åpne Visual Studio Code.
     - Klikk på "File" > "Open Folder" og velg mappen "PythonProsjekt".
     - Opprett en ny fil i denne mappen ved å klikke på "File" > "New File".
     - Lagre filen som `hello_world.py` ved å klikke på "File" > "Save As" og skrive inn filnavnet med `.py`-utvidelse.
  3. Installer nødvendige utvidelser (hvis ikke allerede installert):
     - Sjekk at Python-utvidelsen er aktivert (du vil bli bedt om dette når du åpner en `.py`-fil).
  4. Skriv følgende kode i filen:
     ```python
     print("Hello, World!")
     ```
  5. Kjør programmet:
     - Klikk på "Run"-ikonet øverst til høyre i VSC eller trykk `Ctrl+F5` for å kjøre koden direkte i editoren.
     - Alternativt kan du åpne terminalen i VSC ved å trykke \`Ctrl+\`\` og skrive følgende kommando:
       ```bash
       python hello_world.py
       ```
  6. Kjør programmet direkte fra bash:
     - Åpne en terminal utenfor VSC (f.eks. Command Prompt eller Terminal).
     - Naviger til katalogen hvor `hello_world.py` er lagret ved hjelp av `cd`-kommandoen.
     - Skriv følgende kommando for å kjøre programmet:
       ```bash
       python hello_world.py
       ```

---

#### **3. Klargjøring for kloning av kursmateriale (15 min)**

- **Mål:** Installere Git og konfigurere Visual Studio Code for å klone et Git-repositorium med kursmateriale.

- **Forberedelser:**

  1. **Installer Git:**
     - Last ned Git fra [https://git-scm.com](https://git-scm.com).
     - Kør installasjonsfilen og følg instruksjonene.
     - Under installasjonen:
       - Velg alternativet "Add Git to PATH" for å sikre at Git fungerer fra terminalen.
       - Bruk standardvalg for andre innstillinger, med mindre annet er spesifisert.
     - Hvis du ikke har admin tilgang:
       - Trykk Win + S, søk etter miljøvariabler, og velg "Rediger miljøvariabler for kontoen din".
       - Under "Brukervariabler", finn variabelen Path og klikk Rediger.
       - Klikk Ny, og lim inn: "C:\Program Files\Git\bin". Kill OK for å lagre.
       - Restart maskinen din 
  2. **Verifiser Git-installasjon:**
     - Åpne en terminal i Visual Studio Code (trykk \`Ctrl+\`\`) og skriv:
       ```bash
       git --version
       ```
     - Du skal se versjonsnummeret til Git.
  3. **Registrer en GitHub-konto:**
     - Hvis du ikke allerede har en GitHub-konto, gå til [https://github.com](https://github.com) og opprett en gratis konto.

- **Hva skjer under kloning?**

  - Kloning oppretter en lokal kopi av repositoriet fra GitHub, inkludert alle filer, mapper og historikk.
  - Den lokale kopien er koblet til det opprinnelige repositoriet på GitHub, slik at du kan hente (“pull”) endringer eller laste opp (“push”) egne oppdateringer.
  - Du jobber på din egen lokale kopi og gjør ikke endringer direkte i det opprinnelige repositoriet før du sender oppdateringer med en push-kommando.

- **Aktivitet:**

  1. Åpne en terminal i Visual Studio Code.
  2. Naviger til mappen der du vil lagre repositoriet:
     ```bash
     cd <sti_til_mappen>
     ```
  3. Klon repositoriet ved å bruke Git:
     ```bash
     git clone https://github.com/jkosmo/SWutviklingForPMs.git
     ```
  4. Utforsk prosjektfiler:
     - Naviger til den klonede mappen i Visual Studio Code og åpne noen av filene for å få oversikt over innholdet.
  5. Bekreft kloning:
     - Åpne en fil for redigering og bekreft at du kan gjøre endringer.

---

### **Hjemmelekse**

1. **Se:** En kort YouTube-video om introduksjon til Python-programmering, for eksempel ["Learn Python in 20 Minutes"](https://www.youtube.com/watch?v=8DvywoWv6fI).

2. **Utvid:** Modifiser "Hello, World!"-eksempelet ved å legge til et nytt element inspirert av innholdet i YouTube-videoen. For eksempel:

   - La programmet be brukeren om deres navn og hilse dem med en personlig melding.
   - Eksempel:
     ```python
     name = input("Hva er navnet ditt? ")
     print(f"Hei, {name}! Velkommen til Python.")
     ```

3. **Kjør og svar på quiz:**

   - Åpne quizen for Modul 1 som gitt i kursmaterialet.
   - Besvar spørsmålene og test kunnskapene dine om emnene som er dekket.

---
