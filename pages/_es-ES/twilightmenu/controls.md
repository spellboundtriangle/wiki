---
lang: es-ES
layout: wiki
section: twilightmenu
category: other
title: Controles
long_title: TWiLight Menu++ Controls
description: Controls for using TWiLight Menu++
---

#### Temas de Nintendo DSi, Nintendo 3DS, SEGA Saturn y Homebrew Launcher
- <kbd>Izq</kbd> / <kbd>Der</kbd>: Seleccionar juego / app
- <kbd class="face">A</kbd> / <kbd>START</kbd>: Abrir juego / app
- <kbd class="l">L</kbd> / <kbd class="r">R</kbd> o <kbd>SELECT</kbd> + <kbd>Izq</kbd> / <kbd>Der</kbd>: Cambiar de página
- (Temas DSi/Saturn/HBL) <kbd>SELECT</kbd> + <kbd>Arr</kbd> / <kbd>Abj</kbd> y soltar <kbd>SELECT</kbd>: Cambiar entre la tarjeta SD y la flashcard
- <kbd class="face">Y</kbd>: Ajustes del juego
   - <kbd class="face">X</kbd>: Trucos
      - <kbd class="face">A</kbd>: Activar truco
      - <kbd class="face">B</kbd>: Salir del menú de trucos
      - <kbd class="face">X</kbd>: Guardar y salir del menú de trucos
      - <kbd class="face">Y</kbd>: Mostrar descripción del truco
      - <kbd class="l">L</kbd>: Desactivar todos los trucos
- <kbd class="face">X</kbd>: Borrar/ocultar juego
- (Temas DSi/Saturn/HBL) <kbd>SELECT</kbd>: Menú SELECT o Menú Clásico DS (donde se puede acceder al menú del sistema, los ajustes de TWLMenu++ y el Modo GBA)

#### Tema R4
- <kbd>Arr</kbd> / <kbd>Abj</kbd>: Seleccionar juego / app
- <kbd class="face">A</kbd>: Abrir juego / app
- <kbd class="l">L</kbd>: Cambiar entre la tarjeta SD y la flashcard
- <kbd class="face">Y</kbd>: Ajustes del juego
   - <kbd class="face">X</kbd>: Trucos
      - <kbd class="face">A</kbd>: Activar truco
      - <kbd class="face">B</kbd>: Salir del menú de trucos
      - <kbd class="face">X</kbd>: Guardar y salir del menú de trucos
      - <kbd class="face">Y</kbd>: Mostrar descripción del truco
      - <kbd class="l">L</kbd>: Desactivar todos los trucos

#### DS ROMs (using nds-bootstrap)
- <kbd class="l">L</kbd> + <kbd class="r">R</kbd> + <kbd>Up</kbd> + <kbd class="face">X</kbd> for 1 second: Swap the screens
- <kbd class="l">L</kbd> + <kbd class="r">R</kbd> + <kbd>Down</kbd> + <kbd class="face">A</kbd> for 3 seconds: Dump RAM to `sd:/_nds/nds-bootstrap`, as `ramDump.bin`
- <kbd class="l">L</kbd> + <kbd>Down</kbd> + <kbd>SELECT</kbd>: Open the in-game menu
   - RAM Viewer
      - <kbd>Up</kbd> / <kbd>Down</kbd>: Scroll
      - <kbd>Left</kbd> / <kbd>Right</kbd>: Fast scroll
      - <kbd class="face">A</kbd>: Enter RAM Editor
      - <kbd class="face">B</kbd>: Return to in-game menu
      - <kbd class="face">Y</kbd>: Specify an address to jump to
        - <kbd>Up</kbd> / <kbd>Down</kbd>: Increase / Decrease selected value
        - <kbd>Left</kbd> / <kbd>Right</kbd>: Select a value
        - <kbd class="face">A</kbd> / <kbd class="face">B</kbd>: Return to RAM Viewer/Editor at specified address
   - RAM Editor
      - <kbd>Up</kbd> / <kbd>Down</kbd> / <kbd>Left</kbd> / <kbd>Right</kbd>: Select a value
      - <kbd class="face">A</kbd>: Modify selected value
         - <kbd>Up</kbd> / <kbd>Down</kbd>: Increase / Decrease value by 1h
         - <kbd>Left</kbd> / <kbd>Right</kbd>: Increase / Decrease value by 10h
         - <kbd class="face">A</kbd> / <kbd class="face">B</kbd>: Finish modifying value
      - <kbd class="face">B</kbd>: Return to RAM Viewer
      - <kbd class="face">Y</kbd>: Specify an address to jump to
        - <kbd>Up</kbd> / <kbd>Down</kbd>: Increase / Decrease selected value
        - <kbd>Left</kbd> / <kbd>Right</kbd>: Select a value
        - <kbd class="face">A</kbd> / <kbd class="face">B</kbd>: Return to RAM Viewer/Editor at specified address

#### Atajos al arrancar
Estos comandos pueden hacerse en la pantalla de bienvenida de TWiLight Menu++ / justo después de la de Nintendo DSi.

- <kbd>SELECT</kbd>: Abrir los ajustes
- <kbd class="face">A</kbd> + <kbd class="face">B</kbd> + <kbd class="face">X</kbd> + <kbd class="face">Y</kbd>: Restablecer los ajustes de TWiLight Menu++
- <kbd class="face">B</kbd>: Iniciar la última Rom usada o viceversa, dependiendo de si el inicio automático de la última ROM está activado
