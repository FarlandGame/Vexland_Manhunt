# Vexland_Manhunt


[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

<!-- PLAYFUL_INTRO_START -->
<p><img src="https://raw.githubusercontent.com/FarlandGame/Vexland_Manhunt/main/assets/portfolio-sticker.svg" width="88" height="88" alt=""></p>

> Los cazadores traen una brújula. Los corredores, un plan… y una excusa por si acaso. 🎮🧭

[Conoce a Kabir: mi historia, mis comienzos creativos y mis planes para Japón](https://github.com/FarlandGame/FarlandGame/blob/main/docs/story.es.md)
<!-- PLAYFUL_INTRO_END -->

**Una experiencia completa de Minecraft que enfrenta a Runner y Hunter, creada conjuntamente por [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) y [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt reúne la preparación de partidas, los roles de equipo, el inicio de la persecución, el rastreo, la progresión, las recompensas, los resultados y la administración en un solo plugin para servidores Paper. Los Runner intentan derrotar al Ender Dragon mientras los Hunter buscan eliminar al último Runner. El plugin admite varios Runner y mantiene la persecución durante muertes, reapariciones, cambios de dimensión y reconexiones. Su centro de control `/mhgui` permite administrar partidas mediante menús, con mensajes y libros de ayuda traducidos para los jugadores.

## Descargas y compatibilidad

| Versión suministrada | Descarga | Instalación |
|---|---|---|
| **2.0.0 — paquete combinado** | [VexLandManhunt-2.0.0.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0.jar) | **Un solo JAR**, con GrimAC 2.3.73 integrado |
| **1.13.1 — rama de espectadores** | [Versión y ambos JAR](https://github.com/FarlandGame/Vexland_Manhunt/releases/tag/v1.13.1) | Manhunt y GrimAC 2.3.73 por separado |
| 1.9.11 / 1.6.4 — anteriores | [Todas las versiones](https://github.com/FarlandGame/Vexland_Manhunt/releases) | Compilaciones independientes históricas |

**Paper 1.21.11 / Java 21.** Son plugins de servidor, no mods de cliente. El nombre del archivo suministrado y la versión pública son **2.0.0**, pero el descriptor sin cambios indica **`1.9.11-grim.1`** e identifica 1.9.11 como base de la jugabilidad. Este paquete combinado **no** contiene el rol Spectator dedicado, `/mspectator <player>`, `/mhspectate`, los menús por categorías ni otras incorporaciones de 1.13.1. Sigue usando la rama 1.13.1 que se indica por separado si necesitas esas funciones.

Las compilaciones originales para servidores personales con acceso administrativo elevado específico de los creadores se conservan tal como se suministraron. La guía cubre los controles públicos.

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

## ¿Qué ha cambiado en el paquete 2.0.0 suministrado?

- **Un solo JAR integrado:** Manhunt, GrimAC 2.3.73 modificado y PacketEvents incluido comparten una instancia de plugin Bukkit. Este paquete no necesita una instalación separada de GrimAC ni de PacketEvents. El descriptor proporciona `GrimAC`; el archivo está aplanado, no contiene un JAR de Grim anidado y sin modificar.
- **Estado del módulo:** el comando de administrador `/vexintegration` informa de Grim ACTIVE/INACTIVE, el propietario Bukkit, el estado de VexAC, el estado de PacketEvents y la cantidad de jugadores registrados. El módulo integrado registra los comandos nativos `/grim` y `/grimac`.
- **Inicio controlado:** el cargador requiere la API de configuración de Paper y exactamente Minecraft 1.21.11. Rechaza la carga en caliente con jugadores conectados y una instancia separada de GrimAC. Si falla el inicio integrado, el plugin se desactiva y registra que la protección de Grim está inactiva; el propio servidor puede continuar. Comprueba el estado antes de iniciar una partida.
- **Migración de datos existentes:** en la primera carga integrada, la migración crea copias de seguridad de ambos árboles de datos de los plugins antiguos y copia los datos antiguos de GrimAC solo cuando el destino integrado no existe. Si existen ambos, prevalecen los datos integrados existentes; no se combinan ni sobrescriben. Los datos originales se conservan.
- **Responsabilidad de la corrección de movimiento:** `plugins/VexLandManhunt/integration.properties` utiliza `movement-correction-owner=legacy` de forma predeterminada. La alternativa admitida es `grim`; otros valores abortan el inicio. Elegir grim suprime las rutas de corrección de VexAC por retroceso/teletransporte, mientras se mantienen las comprobaciones, alertas y pruebas de VexAC. No desactiva todos los castigos heredados.
- **Base de la jugabilidad:** el menú plano `/mhgui`, la alternancia de roles Runner/Hunter, los controles de VexAC, Smart Hunter Kit V3, la pausa/reanudación, la recuperación y las 683 claves traducidas siguen 1.9.11. Esta es una versión combinada de empaquetado/integración, no el conjunto de funciones de 1.13.1 con espectadores.

## Jugabilidad conservada desde la base 1.9.11

Los siguientes sistemas se añadieron a la base 1.9.11 y se conservan en este paquete combinado. Son funciones de jugabilidad heredadas, no nuevas funciones de espectadores de 2.0.0.

| Incorporación o cambio | Comportamiento en 1.9.11 |
| --- | --- |
| **Smart Hunter Kit V3** | Los kits adaptativos de reaparición consideran el equipo de los Runner, los equipos y el contexto de partida. El sistema pretende mantener los kits Hunter por debajo del promedio del equipo Runner y puede activarse o desactivarse con `/mhkit` o la interfaz. |
| **Punto de aparición automático del Overworld** | Mueve el punto de aparición del mundo cerca de un Runner apto del Overworld a intervalos elegidos: desactivado, 5, 10, 15, 20 o 30 minutos. El sistema selecciona una superficie segura y omite los casos inadecuados. |
| **Pausa y reanudación** | `/mhpause` congela el juego y los temporizadores, el rastreo y el desplazamiento del punto de aparición; `/mhresume` continúa. El tiempo pausado se descuenta del tiempo activo de partida. |
| **Recuperación tras reinicio o fallo** | Una capa de recuperación restaura estado, roles, objetivos de brújula, progreso, temporizadores de recompensa/muerte y reconexiones mediante instantáneas principales/de respaldo, guardados periódicos y guardados al apagar. |
| **Ajustes de reconexión Runner** | Un plazo configurable sustituye los 60 minutos fijos anteriores. Valor inicial: 15 minutos, con 10 segundos de protección al volver. El tiempo de servidor apagado se excluye; el vencimiento puede convertir al Runner en Hunter o terminar la partida. |
| **Administración ampliada** | Cambia roles durante una partida preservando al último Runner; acciones sobre jugadores elegidos, teletransporte/inmovilización de equipos, resincronización y accesos directos mejoran la gestión. |
| **Restablecimiento confirmado de ajustes** | Dos clics en ocho segundos establecen Smart Kit ACTIVADO, aparición automática cada 15 minutos y reconexión de 15 minutos. Difiere de una instalación nueva, donde la aparición automática está DESACTIVADA. |
| **VexAC 3.0** | Comprobaciones de movimiento, combate, AutoClick, velocidad/retroceso y construcción; controles generales/por grupos, registro de pruebas, alertas a administradores y excepciones por entorno/lag. |
| **Ultra Deep Debug v4** | `/mhdebug` ofrece diagnósticos de máquina de estados, interfaz, kits/pruebas de carga sintéticos, marcadores de traducción, recuperación de ida y vuelta e integridad. |
| **Indicadores ampliados** | Progresión más detallada, salud del dragón, resultados de MVP/daño/distancia e información de ping en TAB. |
| **Cambios de comandos** | Añade `/mhkit`, `/mhspawn`, `/mhpause`, `/mhresume` y `/mhdebug`; elimina `/mhnone`; adapta `/mhhelp` a jugador/administrador y añade alias de `/trash`. |
| **Más mensajes traducidos** | Los recursos pasan de 446 a 683 claves de mensajes por idioma. |

Las comprobaciones incluidas de VexAC cubren Fly, Speed, Timer, Phase, Step, NoSlow, GroundSpoof, Reach, KillAura, AimAssist, wall-hit, BadPackets, patrones temporales de AutoClick, retroceso alterado, Scaffold, Tower, FastPlace, Nuker y alcance de bloques. La interfaz indica un modo de solo supervisión, pero el código compilado también contiene rutas de expulsión; confirma el comportamiento real de moderación en un servidor de prueba antes de confiar en esa etiqueta. La versión anterior contiene en su lugar controles antiguos Anti AutoClick y Anti Fly.

## Preparación y uso completos con `/mhgui`

### 1. Instalar la compilación combinada

1. Detén por completo el servidor **Paper 1.21.11 / Java 21** y crea copias de seguridad de los mundos y los datos de los plugins.
2. Coloca únicamente `VexLandManhunt-2.0.0.jar` de esta versión en `plugins/`. Mueve los JAR antiguos de Manhunt y los JAR independientes de GrimAC fuera del directorio de plugins activos. Conserva sus carpetas de datos; no las elimines. Los jugadores no instalan este JAR en el cliente.
3. Inicia normalmente en lugar de usar `/reload`. El cargador integrado administra el ciclo de vida de Grim y PacketEvents.
4. Como OP o con `vexland.admin`, ejecuta `/vexintegration`. Comprueba `Grim=ACTIVE` y `PacketEvents=true` antes de pasar a `/mhgui`. Una protección inactiva es un problema de inicio, no una instalación integrada correcta.

La configuración de Grim está en `plugins/VexLandManhunt/grim/` (`config.yml`, `messages.yml`, `punishments.yml`, `discord.yml`), con historial opcional en `violations.sqlite`. Las copias de seguridad de la primera migración van a `plugins/VexLandManhunt-integration-backups/`; `plugins/VexLandManhunt/integration-migration-v1.txt` marca su finalización. Si existen tanto los datos antiguos de Grim como los integrados, se conserva el destino integrado y se registra una advertencia. La migración rechaza los enlaces simbólicos.

Revisa la responsabilidad del movimiento en `plugins/VexLandManhunt/integration.properties`; conserva los demás ajustes. Valor predeterminado de una instalación nueva:

```properties
movement-correction-owner=legacy
```

La guía completa de menús públicos que aparece a continuación sigue la base de jugabilidad 1.9.11 de este paquete. La rama de espectadores tiene su propia guía archivada.

### 2. Abrir el centro de control

Entra al servidor como administrador con **OP** o el permiso **`vexland.admin`** e introduce:

```text
/mhgui
```

Las instrucciones siguientes cubren la interfaz pública de la versión **2.0.0**, utilizando los nombres ingleses de sus botones. Las etiquetas siguen el idioma del servidor seleccionado. Para usar toda la interfaz, emplea una cuenta **OP** de confianza: el permiso del descriptor permite abrir el comando, pero algunos manejadores de la interfaz realizan comprobaciones OP más estrictas. El inventario principal tiene cinco filas de nueve espacios. Pasa el cursor sobre un botón para leer su descripción y ajuste actual. La mayoría utiliza un clic normal; las acciones especiales del ratón y confirmaciones se explican a continuación. El menú más pequeño de 1.6.4 aparece al final.

#### Preparar tu primera partida

1. Abre **Player Roles**. Haz clic en la cabeza de cada participante hasta que muestre el rol correcto. En 2.0.0 alterna entre **Runner** y **Hunter**; un participante sin asignar pasa a Runner con el primer clic. Los clics izquierdo/derecho/con Mayús no son atajos distintos de selección de rol. Utiliza **Previous Page**, **Next Page** y **Back to Control Center** cuando sea necesario.
2. Asigna al menos un Runner y un Hunter. La rutina de inicio puede convertir a los jugadores conectados restantes sin asignar en Hunter; asignar explícitamente a cada participante aclara los equipos.
3. Haz clic en **Friendly Fire** para elegir si los compañeros pueden hacerse daño. Comprueba el indicador ON/OFF después.
4. Haz clic en **Language** para elegir el idioma de todo el servidor. Afecta a mensajes, interfaces, avisos y guías de todos, no solo de tu jugador.
5. Revisa **Smart Hunter Kit**, **Auto World Spawn** y **Anti-Cheat**. Consulta la guía del administrador desde el botón del libro si necesitas una explicación dentro del juego.
6. Asegúrate de que **Server Freeze** esté desactivado y pulsa **Start Match**. El inicio prepara los jugadores e inventarios, ejecuta la presentación y la ruleta de demora aleatoria de los Hunter, y comienza la persecución. Antes de iniciar, guarda lo que necesites fuera de los inventarios de los participantes.

#### Botones principales del centro de control

Las posiciones cuentan filas de arriba abajo y columnas de izquierda a derecha. Describen el diseño decorado final de 2.0.0.

| Posición | Botón inglés | Función |
|---|---|---|
| Fila 2, columna 2 | Player Roles | Abre el menú paginado de cabezas de jugadores Runner/Hunter. |
| Fila 2, columna 3 | Target Player | Recorre otros jugadores conectados para acciones administrativas dirigidas. Comprueba el nombre actual. |
| Fila 2, columna 4 | Friendly Fire | Activa o desactiva el daño entre compañeros. |
| Fila 2, columna 5 | Match Info | Envía un informe breve del estado, equipos, fuego amigo y objetivo elegido. |
| Fila 2, columna 6 | Start Match | Ejecuta el inicio normal y la secuencia aleatoria de ventaja inicial. |
| Fila 2, columna 7 | Full Heal | Restaura la salud de todos los jugadores conectados. |
| Fila 2, columna 8 | Reset Match | Reinicia completamente la partida. Es diferente de Reset Settings. |
| Fila 3, columna 2 | Full Hunger | Restaura comida y saturación de todos los jugadores conectados. |
| Fila 3, columna 3 | Release Hunters | Libera a los Hunter en espera antes de acabar la ventaja inicial. |
| Fila 3, columna 4 | Clear Effects | Elimina los efectos de poción de todos los jugadores conectados. |
| Fila 3, columna 5 | Server Freeze | Alterna la inmovilización global; inmoviliza a jugadores normales sin OP. |
| Fila 3, columna 6 | Clear Target Inventory | Vacía inventario, armadura y mano secundaria del jugador elegido tras confirmación. |
| Fila 3, columna 7 | Teleport Everyone | Lleva a todos los jugadores conectados a tu posición actual. |
| Fila 3, columna 8 | Kill Target | Mata al jugador elegido tras confirmación; las reglas normales de muerte pueden afectar a la partida. |
| Fila 4, columna 2 | Anti-Cheat | Abre los controles de seguridad VexAC. |
| Fila 4, columna 3 | Freeze Target | Alterna la inmovilización individual del jugador elegido. |
| Fila 4, columna 4 | Emergency Restore | Restaura salud, comida y saturación de todos los conectados. |
| Fila 4, columna 5 | Freeze Team | Clic izquierdo alterna Runner; derecho, Hunter; clic con Mayús elimina inmovilizaciones individuales/de equipo. |
| Fila 4, columna 6 | Set Day | Establece el día en tu mundo actual. |
| Fila 4, columna 7 | Clear Weather | Detiene lluvia y tormenta en tu mundo actual. |
| Fila 4, columna 8 | Language | Abre el selector global de idioma. |
| Fila 5, columna 2 | Smart Hunter Kit | Activa o desactiva kits adaptativos de reaparición Hunter; muestra ON/OFF. |
| Fila 5, columna 3 | Clear Dropped Items | Elimina entidades de objetos tirados en tu mundo actual. |
| Fila 5, columna 4 | Pause Match / Resume Match | Detiene o reanuda el juego activo y los temporizadores de partida. |
| Fila 5, columna 5 | Emergency Sync | Resincroniza roles, brújulas y estado de ejecución relacionado. |
| Fila 5, columna 6 | Reset Settings | Restablece ajustes equilibrados tras confirmar con dos clics. |
| Fila 5, columna 7 | Close | Cierra el centro de control. |
| Fila 5, columna 8 | Auto World Spawn | Abre el selector de intervalo automático de aparición del Overworld. |
| Fila 5, columna 9 | Manhunt Administrator Guide | Entrega el libro traducido para administradores. |

El cristal decorativo y los objetos de título/estado no son botones de juego.

#### Roles y objetivos seleccionados

**Player Roles** cambia el equipo Manhunt real de un participante. Haz clic en su cabeza y lee el rol actualizado. Durante STARTING/RUNNING, la interfaz permite cambios Runner/Hunter, pero impide convertir al último Runner en Hunter. Así conserva el equipo Runner de la partida activa. Cambia roles deliberadamente, ya que el estado de equipos y las brújulas se sincronizan después.

**Target Player** es independiente: selecciona a alguien para Freeze Target, Clear Target Inventory o Kill Target sin cambiar su equipo. Recorre las opciones hasta ver el nombre deseado. Si un objetivo guardado deja de estar disponible, el código puede recurrir al primer otro jugador conectado; confirma siempre el nombre inmediatamente antes de una acción dirigida. Si no hay nadie más conectado, informa de que no hay objetivos disponibles.

**Clear Target Inventory** y **Kill Target** requieren pulsar la misma acción para el mismo objetivo dos veces en **cinco segundos**. El primer clic prepara la confirmación e identifica al objetivo; el segundo realiza la acción. Cambiar de objetivo o esperar demasiado exige una confirmación nueva. Vaciar un inventario elimina su contenido; matar a un Runner puede terminar o cambiar la partida según las reglas normales de muerte.

**Freeze Team** tiene los únicos atajos de ratón específicos de equipo de este menú: clic izquierdo normal selecciona Runner, clic derecho normal selecciona Hunter, y clic con Mayús elimina todas las inmovilizaciones individuales/de equipo gestionadas por esta herramienta. El interruptor global Server Freeze es independiente y debe desactivarse por separado si los jugadores siguen inmovilizados.

#### Smart Hunter Kit

Haz clic en **Smart Hunter Kit** para activar o desactivar los kits adaptativos de reaparición Hunter. El botón muestra su estado actual. Al estar activado, un Hunter que reaparece puede recibir un kit adaptado al equipo Runner y al contexto; la guía incluida lo describe como inferior al promedio de los Runner. Al desactivarlo, los Hunter no reciben kits automáticos después de morir. Esto no desactiva la brújula de rastreo.

Para fijar el estado en lugar de alternarlo, utiliza `/mhkit on`, `/mhkit off` o `/mhkit status`. El valor de respaldo inspeccionado para una configuración nueva es ACTIVADO.

#### Auto World Spawn

Haz clic en **Auto World Spawn** y elige **OFF**, **5 minutes**, **10 minutes**, **15 minutes**, **20 minutes** o **30 minutes**. Elegir una opción la guarda y vuelve a `/mhgui`; **Back** regresa sin seleccionar un intervalo nuevo.

Al activarlo, el sistema busca periódicamente una superficie segura del Overworld cerca de un Runner activo de esa dimensión y mueve allí el punto de aparición del mundo. Omite el movimiento si no hay Runner en el Overworld o no encuentra un lugar seguro. El valor de respaldo inicial es DESACTIVADO. Los mismos controles por comando son `/mhspawn off`, `/mhspawn 15` o `/mhspawn status`, sustituyendo 15 por cualquier intervalo admitido.

#### Pausa, reconexión y recuperación

**Pause Match** está disponible mientras la partida está RUNNING. Congela los sistemas de juego, movimiento/interacciones, temporizadores, rastreo y desplazamiento de aparición. **Resume Match** los continúa y compensa el tiempo pausado. Server Freeze solo inmoviliza jugadores y no sustituye una pausa del reloj de partida.

El plazo de reconexión Runner es configurable, con un valor de respaldo inicial de **15 minutos**. Volver a tiempo restaura el estado Runner y proporciona diez segundos de protección. El servidor apagado no consume el tiempo guardado de reconexión. Los puestos Runner vencidos pasan a Hunter; el vencimiento del último Runner puede dar la victoria a los Hunter.

La interfaz de 2.0.0 suministrada **no incluye un selector independiente de duración de reconexión**. Para personalizarla, detén el servidor, edita `plugins/VexLandManhunt/config.yml`, conserva los demás ajustes y establece:

```yaml
features:
  custom-reconnect-minutes: 15
```

Reinicia después. Los valores inferiores a un minuto se limitan a un minuto. **Reset Settings** restablece este valor a 15 minutos. La versión compilada también guarda el estado de partida/reconexión e instantáneas de respaldo para recuperarse tras reinicios/fallos; deja que el plugin gestione esos archivos en lugar de editarlos durante el juego.

#### Reset Settings y Reset Match

**Reset Settings** requiere dos clics en **ocho segundos**. El primero prepara la confirmación; el segundo restablece **Smart Kit ACTIVADO**, **Auto Spawn cada 15 minutos**, **Reconexión 15 minutos** y una **ventaja inicial aleatoria**. Difiere de una instalación nueva, donde Auto World Spawn utiliza DESACTIVADO como valor de respaldo. Cambia la configuración; no sustituye el reinicio completo de partida.

**Reset Match** realiza el reinicio existente, limpia estado/objetos temporales y devuelve los jugadores al punto de aparición del Overworld para otra ronda. Su botón principal no utiliza la confirmación de dos clics de Reset Settings. **Start Match** puede preparar/vaciar los inventarios de participantes. Revisa qué control de reinicio/inicio deseas usar antes de hacer clic.

#### Controles de idioma y antitrampas

**Language** abre el selector global. Haz clic en el idioma deseado. Ambas versiones incluyen inglés, persa, árabe, español, francés, alemán, ruso, chino simplificado, hindi y portugués. La selección es compartida por el servidor y se guarda. La documentación README en japonés no añade japonés al selector del plugin dentro del juego.

**Anti-Cheat** abre **VexAC Security**. Haz clic en **VexAC Master** para activar/desactivar el motor interno, o en **Movement**, **Combat**, **AutoClick**, **Velocity / AntiKB** o **World / Scaffold** para alternar cada grupo. **Anti X-Ray** alterna el Anti-Xray configurado de Paper; reinicia para aplicar el cambio. Los paneles de estado, registro de pruebas y modelo de detección explican los sistemas actuales. **Back to Control Center** vuelve al menú principal.

La interfaz describe moderación de solo supervisión, pero la inspección estática conserva una ruta de expulsión basada en umbrales. Considera el texto que promete ausencia de expulsiones como una discrepancia entre implementación y documentación, y confirma la moderación en un servidor controlado antes de confiar en él.

#### GrimAC integrado y VexAC heredado

La interfaz existente **VexAC Security** controla el motor VexAC heredado; sus botones Master/group no son un nuevo panel de control de Grim. GrimAC integrado se ejecuta junto a él. Usa `/vexintegration` para ver el estado del módulo y los comandos nativos `/grim` o `/grimac` para los comandos propios de Grim y sus herramientas sujetas a permisos. Los ajustes y las reglas de castigo de Grim están en `plugins/VexLandManhunt/grim/`.

El menú de supervisión/grupos de GrimBridge de 1.13.1 y `grim-settings.yml` no describen este paquete. No supongas que desactivar VexAC también desactiva GrimAC integrado, ni que una etiqueta de supervisión establece una política sin expulsiones. Paper Anti-Xray sigue siendo un ajuste independiente que requiere reiniciar.

#### Guía dentro del juego y solución de problemas

Haz clic en **Manhunt Administrator Guide** o usa `/mhhelp` para obtener un libro traducido. En 2.0.0, los jugadores pueden usar `/mhhelp` para su guía adaptada al rol. Los Hunter hacen clic derecho en su brújula para elegir un Runner; esta interfaz de rastreo es independiente del selector administrativo Target Player.

Si un rol o una brújula parecen desincronizados, **Emergency Sync** actualiza el estado de ejecución relacionado. **Match Info** ayuda a comprobar equipos y estado. Si falla un inicio, comprueba que la partida esté preparada, la inmovilización global desactivada y exista un equipo Runner/Hunter. Tras cambiar el JAR, reinicia completamente en lugar de usar `/reload`. `/mhdebug` es un comando de diagnóstico administrativo incluido en 2.0.0; su presencia no afirma que estas versiones hayan superado pruebas en servidores activos.

#### Usar el centro de control antiguo de 1.6.4

1.6.4 conserva **Player Roles**, **Friendly Fire**, **Start Match**, **Reset Match**, **Release Hunters Now**, **Server Lock**, **Teleport Everyone To Me**, **Heal & Feed Everyone**, **Match Status**, selección de idioma, **Anti Cheat** y una guía administrativa. Sus roles alternan **None → Runner → Hunter**, y se bloquean los cambios durante el inicio/la partida activa.

Su menú antitrampas contiene los antiguos **Anti AutoClick** (regla de 30 CPS con advertencias/expulsiones), **Anti Fly** y **Anti X-Ray** de Paper. Su plazo Runner de reconexión está fijado en **60 minutos**. El interruptor Smart Hunter Kit V3, selector Auto World Spawn, pausa/reanudación, confirmación Reset Settings y herramientas adicionales de jugador objetivo/mundo descritos arriba pertenecen a 2.0.0 y no deben esperarse en el menú antiguo.

Esta guía se obtuvo de los metadatos JAR suministrados, textos integrados de idioma/ayuda y desensamblado estático. La interfaz no se ejecutó en un servidor Minecraft activo durante esta inspección.

### 3. Jugar la persecución

Los Runner escapan durante la ventaja inicial aleatoria y progresan hacia derrotar al Ender Dragon. Los Hunter esperan su liberación y luego hacen clic derecho en la brújula para elegir un Runner. Pueden cambiarse objetivos durante el juego, incluso al atravesar dimensiones. Usa `/teammsg <message>` para hablar solo con tu equipo y `/mhhelp` para la guía traducida de rol en 2.0.0.

Si muere un Runner, los restantes continúan y el jugador caído pasa a Hunter. Un Hunter puede reaparecer y seguir rastreando. La muerte del último Runner o el vencimiento de su reconexión puede finalizar la partida para los Hunter; derrotar al Ender Dragon la termina para los Runner.

### 4. Pausar, terminar y preparar otra partida

En 2.0.0, pausa con `/mhpause` y continúa con `/mhresume`. Usa `/mhrelease` si deseas liberar a los Hunter antes de finalizar la cuenta atrás. Para otra partida, usa el reinicio completo del centro de control o `/mhreset`; limpia estado y objetos temporales y devuelve los jugadores al punto de aparición del Overworld. Cambiar Anti-Xray de Paper requiere reiniciar.

## Ajustes predeterminados del paquete combinado 2.0.0

Los valores de respaldo inspeccionados de una configuración nueva son:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` significa que el movimiento automático de aparición está desactivado. La acción confirmada de restablecimiento de ajustes de la interfaz fija el intervalo en 15 minutos. Utiliza la interfaz o `/mhkit` y `/mhspawn` para los ajustes correspondientes.

## Referencia de comandos públicos — versión combinada 2.0.0

Los comandos de administrador requieren OP o `vexland.admin` (OP por defecto). El chat de equipo, la papelera y la visión nocturna son utilidades para jugadores; `/mhhelp` ofrece la guía adaptada al rol. La tabla enumera los 17 comandos de Manhunt/integración; los comandos nativos de Grim tienen sus propios permisos. `/mhnone` no está registrado aquí.

| Comando | Función |
| --- | --- |
| `/vexintegration` | Mostrar el estado de Grim integrado, VexAC, PacketEvents y el propietario Bukkit compartido |
| `/mhgui` | Abrir el centro de control |
| `/mhstart` | Ejecutar la secuencia completa de inicio |
| `/mhreset` | Reiniciar completamente la partida actual |
| `/mhrelease` | Liberar a los Hunter antes de tiempo |
| `/mrunner <player>` | Asignar un Runner |
| `/mhunter <player>` | Asignar un Hunter |
| `/teammsg <message>` | Enviar un mensaje privado a compañeros |
| `/trash` | Abrir el inventario desechable de 54 espacios |
| `/nv` | Alternar visión nocturna personal |
| `/mhlang` | Abrir el selector global de idioma |
| `/mhhelp` | Recibir un libro traducido de ayuda |
| `/mhkit <on\|off\|toggle\|status>` | Configurar kits Smart Hunter |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Configurar movimiento automático de aparición |
| `/mhpause` | Pausar la partida activa |
| `/mhresume` | Reanudar la partida pausada |
| `/mhdebug` | Ejecutar diagnósticos internos |

## Idiomas del juego y documentación

Este paquete conserva **10 idiomas de juego**: inglés, persa, árabe, español, francés, alemán, ruso, chino simplificado, hindi y portugués. Cada traducción incluida tiene **683 claves**, siguiendo 1.9.11. `/mhlang` establece un solo idioma para todo el servidor, guardado en `language.txt`.

La documentación del proyecto tiene **18 idiomas**, sin una edición de la documentación en árabe. Estas traducciones no añaden japonés ni otros idiomas de juego adicionales al binario sin modificar.

## Historial de versiones, código fuente y créditos

[CHANGELOG.md](../CHANGELOG.md) registra cada versión suministrada. La [guía completa de espectadores de 1.13.1](archive/1.13.1/README.es.md) y la [guía anterior de 1.9.11 / 1.6.4](archive/1.9.11/README.es.md) siguen disponibles. Cada versión suministrada conserva su propia descarga y suma de comprobación.

**Manhunt es una creación conjunta de Bardiya / Farland_game y Ali / Alivexor. GrimAC es un proyecto independiente de GrimAC / DefineOutside y sus colaboradores.** Este artefacto integrado modifica tres clases de Grim; no es el binario oficial de Grim sin modificar de la anterior versión de dos archivos. El [paquete de código fuente](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0-source.zip) adjunto conserva el código fuente suministrado, los scripts de compilación, los insumos de dependencias y los avisos, omitiendo las pruebas de test/ejecución y sin modificar el código fuente. La versión también incluye el texto de GPLv3, sumas de comprobación y [avisos de terceros](../THIRD_PARTY_NOTICES.md). Durante esta publicación no se realizó ninguna prueba en un servidor activo ni de compilación reproducible.

## Un desafío divertido a Dream

Una pequeña broma de Minecraft de Bardiya 😄

> «Uf... Ali y yo hicimos un plugin Manhunt cien veces mejor que el de Dream, ¡pero Dream tiene miedo y no quiere jugar al nuestro!»

## Creadores y alcance del proyecto

**Creado conjuntamente por [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) y [Ali · Alivexor](https://github.com/Alivexor).** Ambos nombres también constan como autores en los descriptores originales del plugin.

Este repositorio presenta las versiones compiladas originales, su documentación y notas de versiones como un proyecto de portafolio compartido. Las descripciones de funciones se basan en la inspección estática de los JAR suministrados. La compatibilidad con servidores activos, el rendimiento de recuperación, el equilibrio y la precisión antitrampas no se han probado en este proceso de publicación.

[Portafolio GitHub de Bardiya](https://github.com/FarlandGame) · [GitHub de Ali](https://github.com/Alivexor) · [Todas las versiones](https://github.com/FarlandGame/Vexland_Manhunt/releases)
