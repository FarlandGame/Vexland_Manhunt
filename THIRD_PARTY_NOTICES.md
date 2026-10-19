# Integrated GrimAC and component notices — supplied 2.0.0

Vexland_Manhunt is co-created by Bardiya / Farland_game (FarlandGame) and Ali / Alivexor. GrimAC is a separate project by GrimAC / DefineOutside and contributors. Manhunt co-creator credit does not assert authorship of GrimAC or PacketEvents.

The user-supplied VexLandManhunt-2.0.0.jar is a flattened integration based on Manhunt 1.9.11 and GrimAC 2.3.73. Its descriptor reports version 1.9.11-grim.1, provides GrimAC and uses one shared Bukkit plugin instance. It is not the unchanged upstream Grim JAR distributed with the older 1.13.1 branch.

Static comparison found all 4,944 original Grim class paths: 4,941 classes are byte-identical, while InitManager, CommandRegister and GrimACBukkitLoaderPlugin are modified for integrated lifecycle/command ownership. Plugin metadata and service packaging also differ. GrimAC GPLv3 text, original notices and integration modification notes remain inside the unchanged supplied JAR.

## Source and license files

- GrimAC upstream: [GrimAnticheat/Grim](https://github.com/GrimAnticheat/Grim), [release v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73).
- Pinned upstream source: [879d566c05bc6b03918c5f24bb5da1a209352b99](https://github.com/GrimAnticheat/Grim/tree/879d566c05bc6b03918c5f24bb5da1a209352b99).
- Accompanying GPLv3 text: [GrimAC-2.3.73-LICENSE-GPLv3.txt](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/GrimAC-2.3.73-LICENSE-GPLv3.txt).
- Original bundled dependency notice: [GrimAC-2.3.73-bundled-SLF4J-LICENSE.txt](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/GrimAC-2.3.73-bundled-SLF4J-LICENSE.txt).
- Supplied integration source, build scripts, dependency inputs and licenses: [VexLandManhunt-2.0.0-source.zip](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0-source.zip).
- Source provenance and packaging scope: [SOURCE.md](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/SOURCE.md).
- Binary/source/notice hashes: [SHA256SUMS.txt](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/SHA256SUMS.txt).

The companion source package preserves all 681 supplied Java source files byte-for-byte. Fifty evidence files containing local test logs, transcripts, recovery state and temporary configuration backups were omitted; no source code was changed. The original JAR and original source archive were not modified. The source package's own prior build audit named the supplied JAR hash; no independent rebuild or live-server test was performed during publication.

The embedded older third-party notice referring to an unchanged accompanying Grim JAR describes the earlier standalone distribution; it must not be read as a claim that this integrated artifact is unchanged upstream Grim. Retain original copyright/license and dependency notices when redistributing components. These notes identify the supplied component licenses without declaring an additional license for unrelated portfolio repositories.

## Previous 1.13.1 standalone distribution

### GrimAC 2.3.73 — standalone attribution and notices

GrimAC is an upstream third-party anticheat by GrimAC / DefineOutside and contributors. The bundled configuration credits Copyright 2025 DefineOutside and contributors. Bardiya (FarlandGame) and Ali (Alivexor) are credited as the Manhunt co-creators; this credit does not assert GrimAC authorship.

The unchanged `grimac-bukkit-2.3.73.jar` matches the official GrimAC [Bukkit 2.3.73 distribution](https://modrinth.com/plugin/grimac/version/1FIGlM6Q) by SHA-512 and SHA-1. Its embedded commit is `879d566`, matching the official [v2.3.73 release](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73).

- Upstream project: [GrimAnticheat/Grim](https://github.com/GrimAnticheat/Grim).
- Official download: [GrimAC Bukkit 2.3.73](https://modrinth.com/plugin/grimac/version/1FIGlM6Q).
- Exact source: [commit 879d566c05bc6b03918c5f24bb5da1a209352b99](https://github.com/GrimAnticheat/Grim/tree/879d566c05bc6b03918c5f24bb5da1a209352b99).
- License: GNU GPLv3; the official Modrinth project identifies GPL-3.0-or-later. The full GPLv3 text accompanies this release as `GrimAC-2.3.73-LICENSE-GPLv3.txt`.
- Source archive: `GrimAC-2.3.73-source.tar.gz`; see `GrimAC-2.3.73-SOURCE.md`.

The original JAR retains all embedded resources and notices. Its `META-INF/LICENSE.txt` is a separate MIT-style QOS.ch Sarl/SLF4J dependency notice (Copyright 2004-2022), not the GrimAC GPL license. A byte-for-byte copy accompanies this release as `GrimAC-2.3.73-bundled-SLF4J-LICENSE.txt`.

The JAR also embeds Maven POMs identifying Apache 2.0 licenses for SnakeYAML, HikariCP, dynamics, json-simple, GeantyRef and fluent. These observations are not a complete dependency-license audit; consult the unchanged JAR and exact upstream source for the full dependency context. Retain upstream attribution, license text and bundled third-party notices when redistributing.

No server or gameplay compatibility test was performed.


## Accompanying release files

- [GrimAC-2.3.73-source.tar.gz](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/GrimAC-2.3.73-source.tar.gz)
- [GrimAC-2.3.73-LICENSE-GPLv3.txt](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/GrimAC-2.3.73-LICENSE-GPLv3.txt)
- [GrimAC-2.3.73-bundled-SLF4J-LICENSE.txt](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/GrimAC-2.3.73-bundled-SLF4J-LICENSE.txt)
- [GrimAC-2.3.73-SOURCE.md](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/GrimAC-2.3.73-SOURCE.md)
- [GrimAC-2.3.73-THIRD-PARTY-NOTICES.md](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/GrimAC-2.3.73-THIRD-PARTY-NOTICES.md)
- [SHA256SUMS.txt](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/SHA256SUMS.txt)
