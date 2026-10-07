# Wild Guns (SNES) — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/super-nintendo/wild-guns)**.

Traducción al **español de España** de *Wild Guns* (Super Nintendo, 1994), el
*shooter* de galería del Oeste con robots de Natsume, que nunca salió en
español. Se ha traducido desde la versión **estadounidense en inglés**; no es
una traducción directa del japonés.

La traducción se reparte como **parche**: no incluye el juego. Necesitas tu propia
copia para aplicarlo.

## Estado

Última versión: **[v1.0 — Primera publicación](../../releases/tag/v1.0)**.

| Parte | Estado |
|---|---|
| Diálogos (demo y final con Kid) | **16 de 16** páginas traducidas y revisadas |
| Menú del título, opciones, ¿continuar?, resultados, récords | Traducidos |
| Nombres de fase, «¡SUERTE!», bocadillo «¡OJO!» y rótulo «JEFE» | Redibujados en el estilo original |
| Recuento final y créditos | Traducidos (los nombres del equipo se conservan) |
| Caracteres españoles | Diálogos: **á é í ó ú ü ñ Á É Í Ó Ú Ñ ¡ ¿**; menús: **Á É Í Ó Ú Ñ ¡ ¿ º** |
| Logotipos y rótulos grandes | Se conservan (ver abajo) |
| Revisión durante una partida | Partida completa con ayudas de emulador (ver abajo) |

Se mantienen en inglés, a propósito, el logotipo WILD GUNS, el de Natsume y el
aviso legal, y los rótulos grandes ilustrados que forman parte de la imagen del
juego: SELECT★PLAYER, STAGE SELECT, la insignia BONUS, BONUS STAGE!, GAME OVER,
ALL CLEAR, THE END y WINNER!, además de los letreros del decorado y el marcador.

Nombres de fase: CARSON CITY se queda (es un lugar real); el resto son
BARRANCO YERMO, ARSENAL, MINA DE ORO, TREN BLINDADO y DUELO FINAL. La letra de
esos rótulos no admite tildes legibles, por eso se eligieron nombres sin ellas.

### Cambios técnicos

- La ROM se **amplía a 2 MB** (16 Mbit, LoROM). Las fuentes, los diálogos y los
  gráficos con texto se vuelven a comprimir con los mismos formatos del juego y
  se colocan en la ampliación. Funciona en emuladores y flashcarts que admiten
  ROMs de ese tamaño.
- Fuente de diálogos y fuente de menús con letras españolas nuevas, dibujadas a
  partir de las del juego, con el mismo color, sombra y contraste.
- Los textos de menú que no cabían en su sitio se han trasladado con un pequeño
  añadido al intérprete de menús del juego.

### Comprobaciones y trabajo pendiente

- Una auditoría automática vuelve a leer la ROM construida y comprueba que cada
  diálogo, menú, fuente y gráfico es exactamente el previsto, que nada más ha
  cambiado y que el *checksum* interno es correcto.
- Se ha jugado en emulador (snes9x) **desde arranque en frío**: logos, demo con
  sus cuatro conversaciones, menús y opciones, selección de personaje, las seis
  fases y las de bonificación, resultados, ¿continuar?, el final con Clint y con
  Annie, el recuento, los créditos y la entrada de récords; también la primera
  fase a dos jugadores y el modo VS contra la CPU hasta la pantalla WINNER! Las fases se recorrieron **con
  ayudas** del emulador (vidas y tiempo modificados en memoria), no como una
  partida normal. Esa partida completa se hizo con la candidata anterior; la
  publicada solo cambia algunas tildes de la fuente de menús, el aviso de vida
  extra y dos frases. Las variantes alternativas del diálogo final se vieron
  forzando la página en memoria. La versión publicada se comprobó desde
  arranque en frío (aviso legal, título, opciones, demo, récords, primera fase)
  y repitiendo las pantallas cambiadas.
- **Pendiente:** el final con dos jugadores y en FÁCIL/DIFÍCIL, el modo 1P VS
  2P completo, la prueba en consola física y una revisión humana
  independiente. La traducción y su revisión se han hecho con asistencia de IA.
  Por eso la versión figura «en revisión»; si encuentras algo, abre una incidencia.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia del juego en versión **USA**. El parche solo funciona con
   esa versión exacta, sin cabecera de copiadora:

   | | |
   |---|---|
   | Archivo | `Wild Guns (USA).sfc` |
   | Tamaño | 1.048.576 bytes (1 MB) |
   | MD5 | `94d30063d9b17567d32079e766251569` |
   | CRC32 | `085D8D14` |

   ```bash
   md5sum "Wild Guns (USA).sfc"                        # Linux
   md5 "Wild Guns (USA).sfc"                           # macOS
   CertUtil -hashfile "Wild Guns (USA).sfc" MD5        # Windows
   ```

   Si tu archivo mide 1.049.088 bytes tiene una cabecera de 512 bytes: quítala
   antes de parchear. Si el MD5 no coincide, el parche fallará.
3. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "Wild Guns (USA).sfc" wild-guns-snes-es-v1.0.xdelta "Wild Guns (ES).sfc"`
4. Comprueba que la ROM resultante mide **2.097.152 bytes** (2 MB) y tiene MD5
   **`82b5cd77e6ca876293ccb6e8edc18eb4`**.
5. Juega en tu emulador o flashcart (el juego no guarda partidas).

## Cambios por versión

### v1.0 — 7 de octubre de 2026

- Primera publicación: diálogos, menús, nombres de fase, resultados, final y
  créditos en castellano de España.
- Fuentes con letras españolas y rótulos «¡SUERTE!», «¡OJO!» y «JEFE»
  redibujados; ROM ampliada a 2 MB.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin
relación alguna con Natsume ni con los actuales titulares de *Wild Guns*. Aquí
no se distribuye el juego ni ninguna parte de él: solo un parche que modifica
una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia
y lo hago.
