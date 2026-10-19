# Vexland_Manhunt — 1.13.1

> Guía de la versión archivada · [2.0.0 →](../../README.es.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Una experiencia completa de Minecraft que enfrenta a Runner y Hunter, creada conjuntamente por [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) y [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt reúne la preparación de partidas, los roles de equipo, el inicio de la persecución, el rastreo, la progresión, las recompensas, los resultados y la administración en un solo plugin para servidores Paper. Los Runner intentan derrotar al Ender Dragon mientras los Hunter buscan eliminar al último Runner. El plugin admite varios Runner y mantiene la persecución durante muertes, reapariciones, cambios de dimensión y reconexiones. Su centro de control `/mhgui` permite administrar partidas mediante menús, con mensajes y libros de ayuda traducidos para los jugadores.

## Descargas y compatibilidad

| Archivo / versión | Descarga | Finalidad |
|---|---|---|
| **1.13.1 — actual** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Plugin Manhunt de Bardiya y Ali |
| **GrimAC 2.3.73 — obligatorio** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | Dependencia antitrampas independiente de terceros |
| 1.9.11 — archivada | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Compilación anterior de Manhunt |
| 1.6.4 — archivada | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Compilación más antigua de Manhunt |

**Plataforma: Paper 1.21.11, Java 21.** Los números 1.6.4, 1.9.11 y 1.13.1 son versiones del plugin, no versiones compatibles de Minecraft. En 1.13.1, GrimAC es una dependencia obligatoria y el puente requiere la API 2.3.73. Descarga **ambos JAR actuales**. Son plugins de servidor; los jugadores no los instalan en la carpeta de mods del cliente.

Estas son las compilaciones originales para un servidor personal, con acceso administrativo elevado específico de los creadores, conservadas exactamente como se entregaron. Este manual cubre los controles públicos de Manhunt.

## La experiencia Manhunt

- **Equipos Runner y Hunter:** asigna los jugadores conectados a cualquiera de los dos equipos. Una partida necesita al menos un Runner y un Hunter o un jugador conectado sin asignar. Los Runner supervivientes continúan si muere un compañero; un Runner muerto pasa a ser Hunter, salvo que esa muerte termine la partida.
- **Inicio cinematográfico:** se preparan los inventarios y modos de juego, se presentan los equipos y una ruleta elige la ventaja inicial de los Runner. Los Hunter quedan inmovilizados durante la cuenta atrás, con títulos y sonidos. La ventaja es aleatoria; los administradores pueden liberar a los Hunter antes de tiempo.
- **Brújula de rastreo con selección de objetivo:** los Hunter reciben una brújula especial. Haz clic derecho para elegir un Runner en el menú de objetivos y cambia de objetivo durante la persecución. Entre dimensiones, el rastreo sigue la ruta del portal pertinente hasta que sea posible el seguimiento directo. Los Hunter recuperan su brújula al reaparecer.
- **Indicadores de progreso:** las barras de jefe y la información de partida siguen el equipo de los Runner y su avance por los recursos del Nether, varas de Blaze, perlas, ojos de Ender, la fortaleza y el End. La versión más reciente incorpora etapas más detalladas y visualizaciones que tienen en cuenta la salud del dragón.
- **Recompensas por bajas de los Runner:** cuando un Runner mata a un Hunter durante una partida activa, se utiliza una selección ponderada de 50 recompensas que tiene en cuenta la progresión. Incluye sorteos animados, recompensas dobles/triples, anuncios de rachas y celebraciones de objetos raros.
- **Victoria y resultados:** la muerte del último Runner da la victoria a los Hunter; derrotar al Ender Dragon se la da a los Runner. Se incluyen títulos de final de partida, celebraciones, información de bajas y muertes y limpieza de objetos temporales. La versión nueva también informa del MVP, los daños y las distancias.
- **Comunicación de equipo y utilidades:** mensajes privados a compañeros con `/teammsg`, un inventario desechable de 54 espacios con `/trash` y visión nocturna personal con `/nv`.
- **Administración mediante menús:** roles, inicio/reinicio, liberación anticipada de Hunter, fuego amigo, bloqueo del servidor, teletransporte general, curación/alimentación, idioma, protección, estado y guías están disponibles desde el centro de control. La inmovilización y el reinicio completo ayudan a preparar la siguiente partida.
- **Guías traducidas:** los libros de Runner, Hunter y administrador explican objetivos, brújula, muertes, preparación y comandos. La versión 1.9.11 proporciona una guía adaptada al rol mediante `/mhhelp`.
- **Integración con Anti-Xray de Paper:** los controles del menú configuran la protección de Paper a nivel de mundo; los cambios requieren reiniciar el servidor.

## ¿Qué hay de nuevo en 1.13.1?

Respecto a la compilación 1.9.11 proporcionada:

- **Espectadores fantasma:** un rol independiente, asignación administrativa, vuelo protegido, jugadores ocultos, estado guardado/restaurado y menú paginado de teletransporte a participantes.
- **Centro de control rediseñado:** menús por categorías, selección explícita entre cuatro roles, selector de objetivos por nombre, duración de reconexión, preajustes Classic/Fast/Hardcore/Custom y pantallas de confirmación propias de 30 segundos.
- **Integración con GrimAC:** GrimAC 2.3.73 obligatorio sustituye la ruta activa de inicio de VexAC. La interfaz permite controlar el interruptor general, cinco grupos de comprobaciones, alertas y modos de supervisión/aplicación. Paper Anti-Xray sigue siendo independiente.
- **Nuevo planificador Smart Hunter Kit:** adapta equipo y suministros al equipo/encantamientos de los Runner, al Runner más cercano, al tamaño de los equipos, la distancia, la dimensión y el terreno. Conserva el equipo superior existente, evita herramientas duplicadas y limita la reposición de consumibles con un historial de 30 segundos. Esto no garantiza una diferencia fija de equipo ni un equilibrio medido.
- **Recuperación validada:** instantáneas selladas con SHA-256, comprobaciones de esquema/estado y respaldo válido como alternativa; las instantáneas inválidas o de formato más reciente se conservan sin sobrescribirlas. El estado del espectador tiene almacenamiento propio.
- **Mensajes ampliados:** las claves traducidas aumentan de 683 a 762 por traducción incluida, manteniendo los mismos diez idiomas de juego. Se registran dos comandos públicos nuevos: `/mspectator <player>` y `/mhspectate`.
- **Alternativa al reiniciar la partida:** si no se encuentra una superficie segura cerca de la aparición del Overworld, el reinicio puede omitir ese teletransporte en vez de forzarlo.

## Configuración y uso completos con `/mhgui`

Detén el servidor y conserva una copia de seguridad de mundos y datos de plugins. Coloca ambos JAR actuales en `plugins/`, dejando allí solo un JAR de Manhunt y uno de GrimAC. Conserva los ajustes/datos existentes de `plugins/VexLandManhunt/` al actualizar. Inicia por completo el servidor Paper 1.21.11 / Java 21; realiza un reinicio completo al sustituir compilaciones. GrimAC debe cargarse correctamente. El nombre interno del plugin sigue siendo `VexLandManhunt`.

Esta guía describe la versión **1.13.1** del plugin con etiquetas inglesas. Las etiquetas siguen el idioma común del servidor. Las filas se cuentan de arriba abajo y las columnas de izquierda a derecha. Usa un clic izquierdo normal salvo que se indique una acción especial. La guía procede de una inspección estática; no se ejecutó ningún servidor Minecraft.

### Preparar una partida

1. Usa `/mhgui` con `vexland.admin` (por defecto: OP).
2. Abre **Player Roles**, pulsa la casilla con el nombre de un jugador y elige **Runner**, **Hunter**, **Spectator** o **No Team**. Esto abre un selector de rol exacto; pulsar al jugador no cambia su rol de forma cíclica.
3. Asigna al menos un Runner y un Hunter. Los jugadores conectados sin asignar pueden convertirse en Hunter al comenzar; los espectadores no cubren la plaza necesaria de ninguno de los equipos.
4. Revisa **Match Settings**, **GrimAC Security** y **Global Language**. Desactiva Server Freeze antes de empezar.
5. Abre **Match Controls → Start Match**. Se preparan/vacían los inventarios de los participantes, se reproduce la introducción y la ruleta elige la ventaja antes de liberar a los Hunter.

### Inicio: `/mhgui` (cinco filas)

| Posición | Botón | Acción |
|---|---|---|
| R2 C2 | Match Controls | Iniciar, pausar/reanudar, liberar y reiniciar. |
| R2 C4 | Player Roles | Abrir la lista de roles de los jugadores conectados. |
| R2 C6 | Match Settings | Fuego amigo, kits, aparición, reconexión y preajustes. |
| R2 C8 | Player Management | Elegir un objetivo y usar herramientas de jugadores/mundo. |
| R4 C2 | GrimAC Security | Abrir los ajustes de protección. |
| R4 C4 | Global Language | Elegir el idioma que usará todo el mundo. |
| R4 C6 | Administrator Guide | Añadir el libro administrativo traducido al inventario. |
| R5 C5 | Close | Cerrar el menú. |

El faro en R1 C5 informa del estado de la partida y del número de Runner/Hunter.

### Match Controls (cinco filas)

| Posición | Botón | Acción |
|---|---|---|
| R2 C2 | Start Match | Iniciar la secuencia completa. |
| R2 C4 | Pause Match / Resume Match | Pausar o reanudar juego y temporizadores; disponible en una partida RUNNING. |
| R2 C6 | Release Hunters | Terminar antes el período actual de espera de los Hunter. |
| R2 C8 | Reset Match | Abrir la confirmación y después reiniciar toda la partida. |
| R4 C2 | Server Freeze | Alternar la congelación global de jugadores sin OP. |
| R4 C4 | Teleport Everyone | Abrir la confirmación y después traer a todos los jugadores conectados hacia ti. |
| R4 C6 | Match Info | Enviar el informe de partida y equipos. |

**Back** está en R5 C1; **Close**, en R5 C9. Server Freeze es independiente de Pause Match: usa Pause cuando el reloj y los sistemas de juego deban detenerse juntos.

### Player Roles

La lista de jugadores de seis filas muestra hasta 45 casillas de rol con nombre, ordenadas por nombre de jugador, en sus cinco primeras filas. Runner utiliza hormigón verde lima, Hunter hormigón rojo, Spectator un ojo de Ender y No Team hormigón gris. La fila inferior tiene **Previous Page** en C1, información de página/conexiones en C3, **Back to Control Center** en C5 y **Next Page** en C9.

Pulsa a un jugador para abrir **Choose Player Role** (tres filas):

| Posición | Rol exacto |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

El nombre/rol actual aparece en R1 C5; **Back** está en R3 C1 y **Close**, en R3 C9. Los roles pueden cambiar durante una partida. Retirar el rol Runner al último Runner asignado durante RUNNING abre la confirmación **Last Runner: the match will end**. Aplicarla puede dar la victoria a los Hunter. Los comandos directos de rol actúan inmediatamente: úsalos con criterio. Aquí puede asignarse No Team; la sincronización normal al iniciar/entrar puede convertir a un jugador sin asignar en Hunter durante una partida activa.

### Espectadores

Un administrador asigna `/mspectator <player>` o elige **Spectator** en Player Roles. El comando comprueba el acceso administrativo aunque su descriptor no tenga línea de permisos. Los jugadores no se inscriben por sí solos ejecutando `/mhspectate`.

Un espectador recibe una brújula **Spectator teleport** en la primera casilla de su barra rápida. Sostenla en la mano principal y haz clic derecho, o usa `/mhspectate`, para abrir el menú de teletransporte de seis filas. El menú solo funciona mientras el jugador tenga el rol Spectator. Las cinco primeras filas contienen hasta 45 Runner/Hunter vivos y conectados, ordenados por nombre; pulsa una casilla de rol con nombre para ir a la ubicación actual de ese jugador, incluso en otro mundo. La fila inferior tiene **Previous Page** en C1, **Close** en C5 y **Next Page** en C9. Sin participantes adecuados, R3 C5 muestra **No players available**. Cerrar el menú no elimina el rol de espectador.

Los espectadores vuelan, quedan ocultos para los demás jugadores, no colisionan y están protegidos contra el daño. La implementación usa modo Aventura con vuelo; no concede cámara de Espectador vanilla ni movimiento a través de bloques. Bloquea ataques, romper/colocar bloques, interacciones normales con bloques/entidades, recoger/soltar objetos, intercambio de mano secundaria, clics/arrastres de inventario, manipulación de soportes para armaduras y recogida/ganancia de experiencia. Las criaturas no pueden fijarlos como objetivo y se cancelan los cambios de hambre. `/teammsg <message>` llega a otros jugadores con rol Spectator. No pases a los competidores ubicaciones de participantes ni otras ayudas externas.

Para salir, un administrador asigna **Runner**, **Hunter** o **No Team**, o usa `/mrunner <player>` o `/mhunter <player>`. No existe un comando/botón exclusivo para salir por cuenta propia. Al salir se restauran inventario/cursor, posición, modo de juego, vuelo, colisión e inmunidad guardados; después se aplica el comportamiento de partida del nuevo rol. Se guarda el estado del espectador para volver a entrar. Full Match Reset restaura ese estado, borra los roles y mueve a los jugadores conectados a una aparición segura del Overworld cuando existe. La limpieza normal al terminar excluye a los espectadores de la gestión de objetos/vuelo de participantes.

### Match Settings (cinco filas)

| Posición | Botón | Acción |
|---|---|---|
| R2 C2 | Friendly Fire | Alternar daño entre compañeros. |
| R2 C4 | Smart Hunter Kit | Alternar kits adaptativos de reaparición de Hunter. |
| R2 C6 | Auto World Spawn | Abrir la selección de intervalo. |
| R2 C8 | Reconnect Grace | Abrir la selección de duración de reconexión de Runner. |
| R4 C2 | Match Preset | Elegir Classic, Fast, Hardcore o Custom. |
| R4 C4 | Reset Settings | Confirmar ajustes equilibrados: Kit ON, Spawn 15m, Reconnect 15m. |
| R4 C6 | Random Head Start | Casilla informativa; la ruleta sigue eligiendo el retraso. |

**Back** está en R5 C1; **Close**, en R5 C9.

El selector **Reconnect Grace** de tres filas ofrece **1, 5, 10, 15, 20, 30 minutos** en R2 C2–C7, en ese orden. Pulsar guarda el valor y mantiene abierto el selector. Back está en R3 C1; Close, en R3 C9.

El selector **Match Preset** de tres filas sitúa **Classic**, **Fast**, **Hardcore**, **Custom** en R2 C2, C4, C6, C8. Classic: Kit ON, Spawn 15m, Reconnect 15m. Fast: ON, 5m, 10m. Hardcore: OFF, OFF, 5m. Custom conserva los ajustes manuales actuales. Los preajustes mantienen la ventaja aleatoria. Seleccionar mantiene abierto el menú; Back está en R3 C1, Close en R3 C9.

**Auto World Spawn** ofrece OFF, 5m, 10m en R2 C2, C3, C4 y 15m, 20m, 30m en R2 C6, C7, C8. Back está en R3 C5. Elige un intervalo o usa `/mhspawn <off|5|10|15|20|30|status>`. Mueve la aparición del Overworld cerca de un Runner adecuado del Overworld; puede omitirse si no existe uno apropiado. `/mhkit <on|off|toggle|status>` controla los kits directamente.

### Player Management (seis filas)

| Posición | Botón | Se aplica a |
|---|---|---|
| R1 C5 | Target Player | Abrir un selector de jugadores por nombre. |
| R2 C2 | Full Heal | Todos los jugadores conectados. |
| R2 C4 | Full Hunger | Todos los jugadores conectados. |
| R2 C6 | Clear Effects | Todos los jugadores conectados. |
| R2 C8 | Freeze Target | Jugador seleccionado. |
| R4 C2 | Clear Target Inventory | Jugador seleccionado; requiere confirmación. |
| R4 C4 | Kill Target | Jugador seleccionado; requiere confirmación y se aplican las consecuencias normales de partida. |
| R4 C6 | Set Day | Tu mundo actual. |
| R4 C8 | Clear Weather | Tu mundo actual. |
| R5 C2 | Clear Dropped Items | Tu mundo actual; requiere confirmación. |
| R5 C4 | Emergency Sync | Actualizar sistemas de roles/ejecución para los jugadores conectados. |
| R5 C6 | Freeze Team | Izquierda: Runner; derecha: Hunter; Mayús-clic: quitar estas congelaciones de equipo/individuales. |

Back está en R6 C1; Close, en R6 C9. Seleccionar objetivo no cambia roles. Su selector ofrece 28 otros jugadores conectados por página, en filas 2–5 y columnas 2–8; pulsa un nombre para elegirlo y volver. Previous/Back/Next están en R6 C1/C5/C9. Revisa el objetivo mostrado antes de aplicar una acción.

### Pantallas de confirmación

Reset Match, Teleport Everyone, Reset Settings, Clear Target Inventory, Kill Target, Clear Dropped Items y el cambio del último Runner mediante la interfaz usan una pantalla independiente **Confirm Action** de tres filas. Lee la acción/objetivo en R1 C5 y pulsa **Confirm** verde en R2 C3 o **Cancel** rojo en R2 C7. La confirmación caduca a los **30 segundos**. Objetivos cambiados/desconectados o roles modificados requieren una nueva selección. En estas rutas nuevas del menú, esto sustituye las instrucciones antiguas de clics repetidos en cinco/ocho segundos.

### GrimAC Security e idioma

El menú Grim de seis filas tiene estado en R1 C5; interruptores en R2 C2 **GrimAC Master**, C4 **Movement**, C6 **Combat**, C8 **Packets**; R4 C2 **Velocity / AntiKB**, C4 **World / Scaffold**, C6 **Anti X-Ray**, C8 **Admin Alerts**; y R5 C5 **Monitor mode**. Back está en R6 C1 y Close en R6 C9. Monitor mode controla alertas/pruebas frente a la aplicación de medidas. Paper Anti-Xray es independiente y necesita reiniciarse tras cambios. Estos son controles GrimAC; la descripción antigua del menú VexAC/AutoClick no describe esta versión.

Global Language se aplica a todos y actualiza menús/objetos. Pulsa el idioma indicado por nombre; Back está en R3 C5. `/mhlang` abre el mismo selector y `/mhhelp` entrega la guía traducida de jugador/administrador.

### Valores actuales, reconexión y moderación

Los valores alternativos de una configuración nueva en `plugins/VexLandManhunt/config.yml` son:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` significa que el movimiento automático de aparición está desactivado. Reset Settings y Classic eligen 15 minutos en su lugar. Durante el plazo de reconexión de un Runner se conserva su plaza; regresar a tiempo otorga diez segundos de protección. Se excluye el tiempo de inactividad guardado del servidor. El vencimiento puede convertir al Runner en Hunter o terminar la partida para los Hunter. Pause/Resume congela sistemas de juego y ajusta el tiempo activo de partida. El plugin gestiona los archivos de recuperación.

Los ajustes del puente Grim se guardan en `plugins/VexLandManhunt/grim-settings.yml`. Los valores iniciales son Master ON, los cinco grupos ON, Admin Alerts ON y **Monitor mode OFF: la aplicación de medidas está activa**. Monitor mode encola pruebas/alertas y cancela los flags pertinentes. En modo de aplicación, el puente puede convertir un comando de expulsión de Grim en una desconexión traducida que permite volver; no establece una política de expulsión permanente. Los umbrales reales dependen también de la configuración de Grim. Las pruebas se encolan hacia `plugins/VexLandManhunt/anticheat/grim-evidence.log`; las colas limitadas pueden perder entradas bajo carga. El puente exime a espectadores, juego pausado/congelado y ciertos contextos de vehículos, con tres segundos de gracia tras entrar, teletransportarse y reaparecer. No se afirma ninguna precisión antitrampas ni rendimiento medidos.

## Referencia de comandos públicos — 1.13.1

Acceso administrativo significa OP o `vexland.admin` (OP por defecto). El manejador de `/mspectator <player>` lo comprueba aunque el descriptor carezca de línea de permisos. Los comandos directos de rol actúan inmediatamente; cambiar al último Runner durante RUNNING puede terminar la partida. La interfaz ofrece confirmación para ese caso.

| Comando | Finalidad | Acceso |
|---|---|---|
| `/mhgui` | Abrir el centro de control por categorías | Administrador |
| `/mhstart` | Iniciar la secuencia completa de partida | Administrador |
| `/mhreset` | Reiniciar por completo la partida | Administrador |
| `/mhrelease` | Liberar a los Hunter en espera | Administrador |
| `/mrunner <player>` | Asignar Runner | Administrador |
| `/mhunter <player>` | Asignar Hunter | Administrador |
| `/mspectator <player>` | Asignar Spectator | Administrador; nuevo |
| `/mhspectate` | Abrir el menú de teletransporte a participantes | Spectator actual; nuevo |
| `/teammsg <message>` | Enviar a tu propio rol/equipo | Jugador |
| `/trash` | Inventario desechable de 54 casillas; alias `/mhtrash`, `/vextrash` | Jugador |
| `/nv` | Alternar visión nocturna personal | Jugador |
| `/mhlang` | Abrir el selector de idioma global | Administrador |
| `/mhkit <on\|off\|toggle\|status>` | Configurar kits adaptativos de Hunter | Administrador |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Configurar movimiento de aparición | Administrador |
| `/mhhelp` | Recibir la guía traducida de rol/administrador | Jugador / administrador |
| `/mhpause` | Pausar la partida en curso | Administrador |
| `/mhresume` | Reanudar la partida pausada | Administrador |
| `/mhdebug` | Diagnósticos internos | Administrador |

`/mhnone` no está registrado en esta versión; usa No Team en la interfaz. Los Hunter hacen clic derecho con su brújula rastreadora para elegir un Runner; esto es independiente del teletransporte de espectadores y del selector administrativo de objetivos. Los Runner ganan al derrotar al Ender Dragon; los Hunter ganan cuando no queda ningún Runner. Un Runner caído se convierte en Hunter si quedan otros Runner.

## Idiomas, historial y créditos de terceros

El plugin original ofrece **10 idiomas de juego**: inglés, persa, árabe, español, francés, alemán, ruso, chino simplificado, hindi y portugués. `/mhlang` elige un idioma para todo el servidor, guardado en `language.txt`. El manual de GitHub tiene **18 idiomas**, sin edición árabe de la documentación. El japonés y los demás idiomas adicionales del README no añaden traducciones dentro del juego a los JAR sin modificar.

El [historial de versiones](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) registra cada compilación entregada. El manual completo anterior de 1.9.11 / 1.6.4 se conserva en el [archivo por versiones](../1.9.11/README.es.md). La compilación dedicada a espectadores ya se ha entregado y publicado como 1.13.1; sus funciones no deben atribuirse a las descargas antiguas.

**GrimAC es un proyecto independiente de sus colaboradores, distribuido bajo GPL-3.0.** Bardiya y Ali crearon Vexland_Manhunt y su integración; no se les atribuye la autoría de GrimAC. El JAR Grim entregado coincide con los SHA-512 y SHA-1 del artefacto Bukkit oficial de Modrinth 2.3.73. Su commit de código integrado corresponde a [la versión original v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73). La publicación incluye binarios sin modificar, sumas de verificación, instantánea del código original, licencia y [avisos de terceros](../../../THIRD_PARTY_NOTICES.md). Estos avisos de componentes no asignan una licencia al proyecto Manhunt independiente.

## Un desafío divertido a Dream

Una pequeña broma de Minecraft de Bardiya 😄

> «Uf... Ali y yo hicimos un plugin Manhunt cien veces mejor que el de Dream, ¡pero Dream tiene miedo y no quiere jugar al nuestro!»

## Creadores y alcance del proyecto

**Creado conjuntamente por [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) y [Ali · Alivexor](https://github.com/Alivexor).** Ambos nombres también constan como autores en los descriptores originales del plugin.

Este repositorio presenta las versiones compiladas originales, su documentación y notas de versiones como un proyecto de portafolio compartido. Las descripciones de funciones se basan en la inspección estática de los JAR suministrados. La compatibilidad con servidores activos, el rendimiento de recuperación, el equilibrio y la precisión antitrampas no se han probado en este proceso de publicación.

[Portafolio GitHub de Bardiya](https://github.com/FarlandGame) · [GitHub de Ali](https://github.com/Alivexor) · [Todas las versiones](https://github.com/FarlandGame/Vexland_Manhunt/releases)
