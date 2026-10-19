# Source package — supplied combined 2.0.0

The release file is VexLandManhunt-2.0.0.jar. Its internal descriptor is 1.9.11-grim.1; its gameplay foundation is Manhunt 1.9.11, integrated with modified GrimAC 2.3.73. Dedicated 1.13.1 spectator features are not part of this build.

The accompanying VexLandManhunt-2.0.0-source.zip is a source publication copy of the supplied integration project. It retains all 681 Java source files, upstream sources, three modified Grim sources, integration sources, resources, build scripts, tooling, pinned dependency inputs, license texts and notices. The original evidence directory's 50 test/runtime files were excluded. An empty evidence directory remains for build scripts that write new outputs there. Every retained file's payload is unchanged; no source code was patched.

- Source ZIP: [VexLandManhunt-2.0.0-source.zip](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/VexLandManhunt-2.0.0-source.zip).
- Source ZIP bytes: 28,654,465.
- Source ZIP SHA-256: fca5ccfee08e7ded8be2b828917f817e29679e8b5f54076325163e1ad3216bbd.
- Original binary bytes: 14,914,959.
- Original binary SHA-256: d17347ecc8d1770e67d24bc76694194ce59c128d87768b0290a8dca57db41a07.
- Upstream Grim source: [879d566c05bc6b03918c5f24bb5da1a209352b99](https://github.com/GrimAnticheat/Grim/tree/879d566c05bc6b03918c5f24bb5da1a209352b99).
- License and component information: [INTEGRATION-NOTICES.md](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v2.0.0/INTEGRATION-NOTICES.md).

All 723 files in the supplied pinned upstream Grim tree matched the previously verified official Git tree. The supplied source project's prior final-jar audit recorded the exact provided binary hash, and all source resources matched runtime JAR resources. These are static correspondence checks; an independent reproducible build was not performed. Consult the supplied source README and build scripts for building. Source reconstruction and bundled upstream input artifacts are documented by the supplied project; the publication does not claim all shaded libraries were independently rebuilt from source.

The original program remains byte-for-byte as received. No plugin or server code was executed during this release inspection. No anti-cheat accuracy, false-positive-free movement, compatibility beyond the inspected requirements, or performance benchmark is asserted.

## Previous 1.13.1 standalone source arrangement

### GrimAC 2.3.73 — standalone source and integrity

This release accompanies the unchanged upstream GrimAC Bukkit 2.3.73 binary with the upstream source archive and GNU GPLv3 license text.

- Project: [GrimAnticheat/Grim](https://github.com/GrimAnticheat/Grim).
- Upstream tag: [v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73).
- Exact commit: [879d566c05bc6b03918c5f24bb5da1a209352b99](https://github.com/GrimAnticheat/Grim/tree/879d566c05bc6b03918c5f24bb5da1a209352b99).
- Official source archive URL: [tar.gz at the exact commit](https://github.com/GrimAnticheat/Grim/archive/879d566c05bc6b03918c5f24bb5da1a209352b99.tar.gz).
- Accompanying source asset: `GrimAC-2.3.73-source.tar.gz` (607,921 bytes).
- Source archive SHA-256: `80d130429c1e232afe857ba1e8f2b20736569677b3c27a2bc17cf94f339c4eb3`.
- License: [upstream GPLv3](https://github.com/GrimAnticheat/Grim/blob/v2.3.73/LICENSE), also supplied as `GrimAC-2.3.73-LICENSE-GPLv3.txt`.

The source archive was downloaded directly from GitHub for the exact upstream release commit; it was not extracted, changed or executed. It is the upstream repository snapshot, with its build scripts and dependency declarations; it is not a bundled offline copy of all external dependencies. The [tagged README](https://github.com/GrimAnticheat/Grim/blob/v2.3.73/README.md) documents building from source.

## Binary provenance

The [official GrimAC distribution](https://modrinth.com/plugin/grimac/version/1FIGlM6Q) (Modrinth project `LJNGWSvH`, Bukkit version `1FIGlM6Q`) publishes the same filename, 10,578,230-byte size, SHA-512 and SHA-1 as the supplied JAR. The official metadata was inspected without downloading another JAR.

| Hash | Unchanged supplied JAR |
|---|---|
| SHA-256 | `a095331a8ba47286b27bdb9b51f0d35ae4a227632a2c50b25cedba85439f1810` |
| SHA-512 | `bf9be1194eb45afe1dec6bd8e98d078dacf41539025c8aabe24d31337cbea86625774e30842568b47f34ca174472c724c7876cc30793945e7408b03609672655` |
| SHA-1 | `f1cd0a6b8b4470dd10a542964784ec5937e0c19a` |

The embedded build properties name `GrimAnticheat/Grim`, version `2.3.73`, commit `879d566` and release mode. The four English default configuration resources also exactly match the tagged source.

The binary was never executed or modified during preparation. This confirms distribution-file identity by published hashes; no reproducible-build or runtime compatibility test was performed.

