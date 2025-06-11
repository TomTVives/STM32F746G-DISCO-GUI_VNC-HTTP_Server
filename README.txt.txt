README.txt
===========

Project: STM32 Examen – Vraag A: Naam & Foto

1. Overzicht
------------
Dit project implementeert Vraag A van het examen:
- Tonen van mijn naam en foto op het TFT-scherm via de emWin GUI.  → gerealiseerd
- Tonen van mijn naam en foto in de webinterface van de HTTP-server.  → voorbereid, nog niet getest

2. Realisatie
-------------
- **TFT (emWin GUI):**
  - Foto (`photo.bmp`) toegevoegd in GUIBuilder als Picture-widget.
  - Tekstwidget gebruikt voor “Tom Truwant”.
  - Bij flashen verschijnt direct de naam (bovenaan) en de foto (eronder) op het LCD.

- **Webinterface (HTTP-server):**
  - HTML-pagina (`index_inlined.htm`) met inline Base64-encoded foto en `<h1>Tom Truwant</h1>` is voorbereid, maar nog niet getest.
  - In `HTTP_Server_CGI.c` is de functie `netCGI_Script` aangepast om de HTML-string direct te serveren; de volledige server-integratie moet nog worden afgerond.

3. Build & Flash
----------------
1. Open Keil µVision project `STM32F746G-Examen.uvprojx`.
2. Zorg dat `photo.bmp` in je projectmap staat en werk `index_inlined.htm` bij.
3. (Voor webinterface) Converteer de inlined HTML in een C-bestand:
