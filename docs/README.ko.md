# Vexland_Manhunt

[English](../README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**[Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame)과 [Ali · Alivexor](https://github.com/Alivexor)가 공동 제작한 완전한 Minecraft 러너 대 헌터 경험입니다.**

Vexland_Manhunt는 경기 설정, 팀 역할, 시작 추격, 추적, 진행도, 보상, 결과, 관리 기능을 하나의 Paper 서버 플러그인에 담았습니다. 러너는 엔더 드래곤을 쓰러뜨리려 하고, 헌터는 마지막 러너를 제거하려 합니다. 플러그인은 여러 명의 러너를 지원하며 사망, 리스폰, 차원 이동, 재접속 이후에도 추격이 이어지도록 합니다. 관리자는 `/mhgui` 제어 센터의 메뉴로 경기를 관리할 수 있고, 플레이어는 현지화된 메시지와 안내서를 사용할 수 있습니다.

## 다운로드 및 호환성

| 파일 / 버전 | 다운로드 | 용도 |
|---|---|---|
| **1.13.1 — 현재 버전** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Bardiya와 Ali가 만든 Manhunt 플러그인 |
| **GrimAC 2.3.73 — 필수** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | 별도로 필요한 타사 부정행위 방지 의존성 |
| 1.9.11 — 보관 버전 | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | 이전 Manhunt 빌드 |
| 1.6.4 — 보관 버전 | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | 더 오래된 Manhunt 빌드 |

**대상 환경: Paper 1.21.11, Java 21.** 1.6.4, 1.9.11, 1.13.1은 플러그인 릴리스 번호이며, 지원하는 Minecraft 버전이 아닙니다. 1.13.1에서는 GrimAC가 필수 의존성이며 브리지는 2.3.73 API를 요구합니다. **현재 버전의 JAR 두 개를 모두** 다운로드하세요. 서버 플러그인이므로 플레이어가 클라이언트의 모드 폴더에 설치하지 않습니다.

이 파일들은 제작자별로 높은 수준의 관리 권한이 포함된 원본 개인 서버 빌드이며, 제공된 그대로 보존되어 있습니다. 이 설명서는 공개 Manhunt 제어 기능을 다룹니다.

## Manhunt 경험

- **러너와 헌터 팀:** 접속 중인 플레이어를 어느 한쪽에 배정합니다. 경기에는 최소 한 명의 러너와 한 명의 헌터 또는 아직 역할이 없는 접속 플레이어가 필요합니다. 팀원이 죽어도 살아남은 러너는 계속 경기를 진행합니다. 사망한 러너는 그 사망으로 경기가 끝나지 않는 한 헌터가 됩니다.
- **영화 같은 경기 시작:** 인벤토리와 게임 모드를 준비하고 팀을 소개한 다음, 룰렛으로 러너의 선행 시간을 정합니다. 이 카운트다운 동안 헌터는 움직일 수 없으며 제목과 소리로 안내를 받습니다. 선행 시간은 무작위이며, 관리자는 헌터를 일찍 풀어 줄 수 있습니다.
- **대상을 선택하는 추적 나침반:** 헌터에게 특수 나침반을 제공합니다. 우클릭하여 대상 메뉴에서 러너를 고르고 추격 중에도 대상을 바꿀 수 있습니다. 서로 다른 차원에 있을 때는 직접 추적이 가능해질 때까지 관련 포털 경로를 따라 추적합니다. 헌터는 리스폰 후 추적기를 다시 받습니다.
- **진행도 표시:** 보스바와 경기 정보는 러너의 장비 및 네더 자원, 블레이즈 막대, 엔더 진주, 엔더의 눈, 요새, 엔드로 이어지는 진행 상황을 반영합니다. 최신 빌드는 더 세분화된 단계와 드래곤 체력을 반영하는 진행도 표시를 추가합니다.
- **러너의 처치 보상:** 진행 중인 경기에서 러너가 헌터를 처치하면, 진행 상황을 반영하는 50개 항목의 가중치 보상 풀을 사용합니다. 추첨 애니메이션, 이중/삼중 보상, 연속 처치 알림, 희귀 아이템 축하 효과를 포함합니다.
- **승리와 결과:** 마지막 러너가 죽으면 헌터가 승리하고, 엔더 드래곤을 쓰러뜨리면 러너가 승리합니다. 경기 종료 제목, 축하 효과, 처치/사망 정보, 임시 아이템 정리가 포함됩니다. 최신 빌드는 MVP, 피해량, 이동 거리 결과도 보여 줍니다.
- **팀 소통과 편의 기능:** `/teammsg`로 팀원에게만 메시지를 보내고, `/trash`로 54칸짜리 아이템 폐기 인벤토리를 열며, `/nv`로 개인 야간 투시를 켜거나 끕니다.
- **메뉴를 통한 관리:** 제어 센터에서 역할, 시작/초기화, 헌터 조기 해제, 아군 피해, 서버 잠금, 전체 순간이동, 회복/허기 충전, 언어, 보호 설정, 상태, 안내서에 접근할 수 있습니다. 동결 기능과 전체 초기화는 다음 경기를 준비하는 데 도움이 됩니다.
- **현지화된 안내서:** 러너, 헌터, 관리자용 책에서 목표, 추적기 사용법, 사망, 설정, 명령어를 설명합니다. 1.9.11에서는 `/mhhelp`로 플레이어의 역할에 맞는 안내서를 제공합니다.
- **Paper Anti-Xray 연동:** 메뉴에서 Paper의 월드 단위 보호 기능을 설정합니다. 변경 사항을 적용하려면 서버를 재시작해야 합니다.

## 1.13.1의 새로운 기능

제공된 1.9.11 빌드와 비교한 변경 사항:

- **유령 관전자:** 별도 역할, 관리자의 지정, 보호되는 비행, 플레이어 숨김, 상태 저장/복원, 페이지가 나뉜 참가자 순간이동 메뉴가 추가되었습니다.
- **새롭게 설계한 제어 센터:** 범주별 메뉴, 네 가지 역할을 명시적으로 선택하는 기능, 이름으로 고르는 대상 선택기, 재접속 유예 시간 선택기, Classic/Fast/Hardcore/Custom 프리셋, 전용 30초 확인 화면이 추가되었습니다.
- **GrimAC 통합:** 필수 GrimAC 2.3.73이 기존에 활성화되던 VexAC 시작 경로를 대체합니다. GUI에서 마스터 스위치, 다섯 검사 그룹, 알림, 모니터링/제재 제어 기능을 제공합니다. Paper Anti-Xray는 독립적으로 유지됩니다.
- **새 Smart Hunter Kit 계획기:** Runner의 장비/마법 부여, 가장 가까운 Runner, 팀 인원, 거리, 차원, 지형에 맞춰 장비와 보급품을 조정합니다. 이미 가진 더 강한 장비는 유지하고, 도구 중복을 방지하며, 30초 이력을 이용해 소모품 보충을 제한합니다. 일정한 장비 격차나 측정된 균형을 보장하는 기능은 아닙니다.
- **검증된 복구:** SHA-256으로 봉인된 스냅샷, 스키마/상태 검사, 유효한 백업으로의 대체 복구를 제공합니다. 유효하지 않거나 더 새로운 형식의 스냅샷은 덮어쓰지 않고 보존합니다. 관전자 상태는 별도로 영속 저장됩니다.
- **확장된 메시지:** 포함된 각 번역의 번역 키가 683개에서 762개로 늘었으며, 게임 내 언어는 여전히 동일한 열 가지입니다. 새로운 공개 명령 두 개가 등록되었습니다: `/mspectator <player>` 및 `/mhspectate`.
- **초기화 대체 처리:** 오버월드 스폰 근처에서 안전한 지표면을 찾지 못하면, 초기화 시 순간이동을 강행하지 않고 생략할 수 있습니다.

## `/mhgui`로 전체 설정 및 사용하기

서버를 중지하고 월드와 플러그인 데이터의 백업을 보관하세요. 현재 버전의 JAR 두 개를 `plugins/`에 넣고, 해당 폴더에는 Manhunt JAR 한 개와 GrimAC JAR 한 개만 남겨 두세요. 업그레이드할 때 기존 `plugins/VexLandManhunt/` 설정/데이터를 유지하세요. Paper 1.21.11 / Java 21 서버를 완전히 시작하고, 빌드를 교체할 때는 완전한 재시작을 사용하세요. GrimAC가 정상적으로 로드되어야 합니다. 내부 플러그인 이름은 계속 `VexLandManhunt`입니다.

이 안내서는 플러그인 릴리스 **1.13.1**을 영어 레이블 기준으로 설명합니다. 레이블은 서버 전체 언어 설정을 따릅니다. 위치는 위에서 아래로 행을, 왼쪽에서 오른쪽으로 열을 셉니다. 특별한 동작이 명시되지 않았다면 일반적인 왼쪽 클릭을 사용하세요. 이 안내서는 정적 검사를 바탕으로 작성되었으며 Minecraft 서버는 실행하지 않았습니다.

### 경기 설정하기

1. `vexland.admin` 권한으로 `/mhgui`를 사용하세요(기본값: OP).
2. **Player Roles**를 열고 이름이 표시된 플레이어 타일을 클릭한 다음 **Runner**, **Hunter**, **Spectator**, **No Team** 중 하나를 선택하세요. 정확한 역할을 고르는 선택기가 열리며, 플레이어를 클릭하는 동작 자체가 역할을 순환시키지는 않습니다.
3. Runner와 Hunter를 각각 최소 한 명 지정하세요. 역할이 없는 온라인 플레이어는 경기 시작 시 Hunter가 될 수 있습니다. 관전자는 어느 팀에서도 필수 인원을 채우지 않습니다.
4. **Match Settings**, **GrimAC Security**, **Global Language**를 확인하세요. 시작하기 전에 Server Freeze를 끄세요.
5. **Match Controls → Start Match**를 여세요. 참가자 인벤토리가 준비/비워지고, 도입 연출이 재생되며, 룰렛이 Hunter의 출발 지연 시간을 정합니다.

### 홈: `/mhgui` (다섯 행)

| 위치 | 버튼 | 동작 |
|---|---|---|
| R2 C2 | Match Controls | 시작, 일시 중지/재개, 출발 허용, 초기화. |
| R2 C4 | Player Roles | 온라인 플레이어 역할 목록을 엽니다. |
| R2 C6 | Match Settings | 아군 피해, 키트, 스폰, 재접속, 프리셋. |
| R2 C8 | Player Management | 대상을 선택하고 플레이어/월드 도구를 사용합니다. |
| R4 C2 | GrimAC Security | 보호 설정을 엽니다. |
| R4 C4 | Global Language | 모두에게 적용할 언어를 선택합니다. |
| R4 C6 | Administrator Guide | 현지화된 관리자 책을 인벤토리에 추가합니다. |
| R5 C5 | Close | 메뉴를 닫습니다. |

R1 C5의 신호기는 경기 상태와 Runner/Hunter 수를 표시합니다.

### Match Controls (다섯 행)

| 위치 | 버튼 | 동작 |
|---|---|---|
| R2 C2 | Start Match | 전체 순서를 시작합니다. |
| R2 C4 | Pause Match / Resume Match | 게임 플레이와 경기 타이머를 일시 중지하거나 재개합니다. RUNNING 상태의 경기에서 사용할 수 있습니다. |
| R2 C6 | Release Hunters | 현재 Hunter 대기 시간을 일찍 끝냅니다. |
| R2 C8 | Reset Match | 확인 화면을 연 다음 경기를 완전히 초기화합니다. |
| R4 C2 | Server Freeze | OP가 아닌 플레이어의 전역 동결을 전환합니다. |
| R4 C4 | Teleport Everyone | 확인 화면을 연 다음 모든 온라인 플레이어를 자신에게 데려옵니다. |
| R4 C6 | Match Info | 경기 및 팀 보고서를 전송합니다. |

**Back**은 R5 C1, **Close**는 R5 C9에 있습니다. Server Freeze는 Pause Match와 별개입니다. 시계와 게임 플레이 시스템을 함께 멈춰야 할 때는 Pause를 사용하세요.

### Player Roles

여섯 행으로 된 플레이어 목록은 처음 다섯 행에 이름이 표시된 역할 타일을 최대 45개까지 플레이어 이름순으로 보여 줍니다. Runner는 연두색 콘크리트, Hunter는 빨간색 콘크리트, Spectator는 엔더의 눈, No Team은 회색 콘크리트를 사용합니다. 맨 아래 행의 C1에는 **Previous Page**, C3에는 페이지/온라인 정보, C5에는 **Back to Control Center**, C9에는 **Next Page**가 있습니다.

플레이어를 클릭하면 **Choose Player Role**(세 행)이 열립니다:

| 위치 | 지정할 정확한 역할 |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

플레이어 이름/현재 역할은 R1 C5에 표시되고, **Back**은 R3 C1, **Close**는 R3 C9에 있습니다. 경기 중에도 역할을 바꿀 수 있습니다. RUNNING 중 마지막으로 지정된 Runner를 다른 역할로 바꾸면 **Last Runner: the match will end** 확인 화면이 열립니다. 이를 적용하면 Hunter의 승리로 끝날 수 있습니다. 직접 역할 명령은 즉시 적용되므로 신중하게 사용하세요. 여기서 No Team을 지정할 수 있지만, 경기 진행 중의 일반적인 시작/접속 동기화 과정은 미지정 플레이어를 Hunter로 바꿀 수 있습니다.

### 관전자

관리자는 `/mspectator <player>`로 지정하거나 Player Roles에서 **Spectator**를 선택합니다. 이 명령은 설명자에 권한 행이 없어도 관리자 접근 권한을 검사합니다. 플레이어가 `/mhspectate`를 실행하여 스스로 관전자가 될 수는 없습니다.

관전자는 첫 번째 단축바 슬롯에 **Spectator teleport** 나침반을 받습니다. 주 손에 들고 오른쪽 클릭하거나 `/mhspectate`를 사용하면 여섯 행의 순간이동 메뉴가 열립니다. 이 메뉴는 플레이어의 역할이 Spectator일 때만 작동합니다. 처음 다섯 행에는 살아 있는 온라인 Runner/Hunter가 이름순으로 최대 45명 표시됩니다. 이름이 있는 역할 타일을 클릭하면 다른 월드를 포함해 해당 플레이어의 현재 위치로 순간이동합니다. 맨 아래 행의 C1에는 **Previous Page**, C5에는 **Close**, C9에는 **Next Page**가 있습니다. 적합한 참가자가 없으면 R3 C5에 **No players available**이 표시됩니다. 이 메뉴를 닫아도 관전자 역할은 유지됩니다.

관전자는 비행하고, 다른 플레이어에게 보이지 않으며, 충돌하지 않고 피해로부터 보호됩니다. 구현에는 비행을 허용한 모험 모드를 사용합니다. 바닐라 관전자 카메라나 블록 통과 이동을 부여하지는 않습니다. 공격, 블록 파괴/설치, 일반적인 블록/개체 상호작용, 아이템 줍기/버리기, 보조 손 교환, 인벤토리 클릭/드래그, 갑옷 거치대 조작, 경험치 줍기/획득을 차단합니다. 몹은 관전자를 대상으로 삼을 수 없고 허기 변화는 취소됩니다. `/teammsg <message>`는 Spectator 역할인 다른 플레이어에게 전달됩니다. 참가자 위치나 그 밖의 외부 도움을 경기 참가자에게 전달하지 마세요.

관전자를 그만두려면 관리자가 **Runner**, **Hunter**, **No Team** 중 하나를 지정하거나 `/mrunner <player>` 또는 `/mhunter <player>`를 사용해야 합니다. 스스로 나가기 위한 전용 명령/버튼은 없습니다. 나가면 저장된 인벤토리/커서, 위치, 게임 모드, 비행, 충돌, 무적 상태를 복원한 다음 새로운 역할의 경기 동작을 적용합니다. 관전자 상태는 재접속을 위해 저장됩니다. 전체 Match Reset은 관전자 상태를 복원하고 역할을 지우며, 안전한 오버월드 스폰이 있으면 온라인 플레이어를 그곳으로 이동시킵니다. 일반적인 경기 종료 정리에서는 관전자를 참가자 아이템/비행 처리 대상에서 제외합니다.

### Match Settings (다섯 행)

| 위치 | 버튼 | 동작 |
|---|---|---|
| R2 C2 | Friendly Fire | 팀원 피해를 전환합니다. |
| R2 C4 | Smart Hunter Kit | 적응형 Hunter 부활 키트를 전환합니다. |
| R2 C6 | Auto World Spawn | 주기 선택기를 엽니다. |
| R2 C8 | Reconnect Grace | Runner 재접속 유예 시간 선택기를 엽니다. |
| R4 C2 | Match Preset | Classic, Fast, Hardcore, Custom 중 하나를 선택합니다. |
| R4 C4 | Reset Settings | 균형 설정을 확인합니다: Kit ON, Spawn 15m, Reconnect 15m. |
| R4 C6 | Random Head Start | 정보 타일이며, 지연 시간은 여전히 룰렛이 정합니다. |

**Back**은 R5 C1, **Close**는 R5 C9에 있습니다.

세 행의 **Reconnect Grace** 선택기는 R2 C2–C7에서 순서대로 **1, 5, 10, 15, 20, 30 minutes**를 제공합니다. 클릭하면 값을 저장하고 선택기를 열린 상태로 유지합니다. Back은 R3 C1, Close는 R3 C9에 있습니다.

세 행의 **Match Preset** 선택기는 R2 C2, C4, C6, C8에 **Classic**, **Fast**, **Hardcore**, **Custom**을 배치합니다. Classic: Kit ON, Spawn 15m, Reconnect 15m. Fast: ON, 5m, 10m. Hardcore: OFF, OFF, 5m. Custom은 현재 수동 설정을 유지합니다. 프리셋은 무작위 출발 지연을 유지합니다. 선택해도 이 메뉴는 계속 열려 있습니다. Back은 R3 C1, Close는 R3 C9에 있습니다.

**Auto World Spawn**은 R2 C2, C3, C4에서 OFF, 5m, 10m를, R2 C6, C7, C8에서 15m, 20m, 30m를 제공합니다. Back은 R3 C5에 있습니다. 주기를 선택하거나 `/mhspawn <off|5|10|15|20|30|status>`를 사용하세요. 오버월드 스폰을 적합한 오버월드 Runner 근처로 이동시키며, 적합한 대상이 없으면 생략할 수 있습니다. `/mhkit <on|off|toggle|status>`는 키트를 직접 제어합니다.

### Player Management (여섯 행)

| 위치 | 버튼 | 적용 대상 |
|---|---|---|
| R1 C5 | Target Player | 이름으로 플레이어를 고르는 선택기를 엽니다. |
| R2 C2 | Full Heal | 모든 온라인 플레이어. |
| R2 C4 | Full Hunger | 모든 온라인 플레이어. |
| R2 C6 | Clear Effects | 모든 온라인 플레이어. |
| R2 C8 | Freeze Target | 선택한 플레이어. |
| R4 C2 | Clear Target Inventory | 선택한 플레이어. 확인이 필요합니다. |
| R4 C4 | Kill Target | 선택한 플레이어. 확인이 필요하며 일반적인 경기 결과 처리가 적용됩니다. |
| R4 C6 | Set Day | 자신의 현재 월드. |
| R4 C8 | Clear Weather | 자신의 현재 월드. |
| R5 C2 | Clear Dropped Items | 자신의 현재 월드. 확인이 필요합니다. |
| R5 C4 | Emergency Sync | 온라인 플레이어의 역할/런타임 시스템을 새로 고칩니다. |
| R5 C6 | Freeze Team | 왼쪽 클릭: Runner, 오른쪽 클릭: Hunter, Shift 클릭: 해당 팀/개인 동결 해제. |

Back은 R6 C1, Close는 R6 C9에 있습니다. 대상 선택은 역할을 바꾸지 않습니다. 선택기는 페이지마다 다른 온라인 플레이어 28명을 2–5행, 2–8열에 표시합니다. 이름을 클릭하면 선택하고 돌아갑니다. Previous/Back/Next는 R6 C1/C5/C9에 있습니다. 동작을 적용하기 전에 표시된 대상을 다시 확인하세요.

### 확인 화면

Reset Match, Teleport Everyone, Reset Settings, Clear Target Inventory, Kill Target, Clear Dropped Items 및 GUI에서 마지막 Runner를 변경하는 동작은 별도의 세 행 **Confirm Action** 화면을 사용합니다. R1 C5의 동작/대상을 읽은 다음 R2 C3의 녹색 **Confirm** 또는 R2 C7의 빨간색 **Cancel**을 클릭하세요. 확인은 **30초** 후 만료됩니다. 대상이 바뀌거나 오프라인이 되거나 역할이 바뀌면 새로 선택해야 합니다. 이 새 메뉴 경로에서는 이전 안내서의 5초/8초 반복 클릭 지침을 이 방식으로 대체합니다.

### GrimAC Security 및 언어

여섯 행의 Grim 메뉴는 R1 C5에 상태를 표시합니다. 전환 스위치는 R2 C2 **GrimAC Master**, C4 **Movement**, C6 **Combat**, C8 **Packets**, R4 C2 **Velocity / AntiKB**, C4 **World / Scaffold**, C6 **Anti X-Ray**, C8 **Admin Alerts**에 있고, R5 C5에는 **Monitor mode**가 있습니다. Back은 R6 C1, Close는 R6 C9에 있습니다. Monitor mode는 알림/증거 수집과 제재 중 어느 쪽을 사용할지 제어합니다. Paper Anti-Xray는 독립적이며 변경 후 재시작이 필요합니다. 이는 GrimAC 제어 기능입니다. 이전 VexAC/AutoClick 메뉴 설명은 이 릴리스를 설명하지 않습니다.

Global Language는 모두에게 적용되고 메뉴/아이템을 새로 고칩니다. 이름이 표시된 언어를 클릭하세요. Back은 R3 C5에 있습니다. `/mhlang`은 같은 선택기를 열고 `/mhhelp`는 현지화된 플레이어/관리자 안내서를 제공합니다.

### 현재 기본값, 재접속 및 관리

`plugins/VexLandManhunt/config.yml`에서 새 구성에 적용되는 대체 기본값은 다음과 같습니다:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0`은 자동 스폰 이동이 꺼져 있음을 뜻합니다. 반면 Reset Settings와 Classic은 15분을 선택합니다. Runner의 재접속 유예 기간에는 해당 자리가 유지되며, 제시간에 돌아오면 10초의 보호를 받습니다. 저장된 서버 중단 시간은 제외됩니다. 기간이 만료되면 Runner가 Hunter로 바뀌거나 Hunter의 승리로 경기가 끝날 수 있습니다. Pause/Resume은 게임 플레이 시스템을 멈추고 진행 중인 경기 시간을 조정합니다. 복구 파일은 플러그인이 관리합니다.

Grim 브리지 설정은 `plugins/VexLandManhunt/grim-settings.yml`에 영속 저장됩니다. 새 기본값은 Master ON, 다섯 그룹 모두 ON, Admin Alerts ON이며 **Monitor mode OFF: 제재가 활성화됩니다**. Monitor mode는 증거/알림을 대기열에 넣고 조건에 해당하는 위반 감지를 취소합니다. 제재 모드에서는 브리지가 Grim의 추방 명령을 재접속을 허용하는 현지화된 연결 해제로 바꿀 수 있습니다. 영구 차단 정책을 정하지는 않습니다. 실제 임계값은 Grim 구성에도 영향을 받습니다. 증거는 `plugins/VexLandManhunt/anticheat/grim-evidence.log`에 기록하도록 대기열에 넣으며, 용량이 제한된 대기열은 부하가 클 때 항목을 누락할 수 있습니다. 브리지는 관전자, 일시 중지/동결된 플레이, 특정 탈것 상황을 검사에서 제외하며 접속, 순간이동, 부활 후에는 3초의 유예를 줍니다. 부정행위 방지의 정확도나 성능에 대한 벤치마크를 주장하지 않습니다.

## 공개 명령 참조 — 1.13.1

관리자 접근 권한은 OP 또는 `vexland.admin`을 뜻합니다(기본값 OP). `/mspectator <player>` 처리기는 설명자에 권한 행이 없어도 이를 검사합니다. 직접 역할 명령은 즉시 적용됩니다. RUNNING 중 마지막 Runner를 바꾸면 경기가 끝날 수 있습니다. GUI는 해당 상황에 확인 화면을 제공합니다.

| 명령 | 용도 | 접근 권한 |
|---|---|---|
| `/mhgui` | 범주별 제어 센터 열기 | 관리자 |
| `/mhstart` | 전체 경기 순서 시작 | 관리자 |
| `/mhreset` | 경기 완전 초기화 | 관리자 |
| `/mhrelease` | 대기 중인 Hunter 출발 허용 | 관리자 |
| `/mrunner <player>` | Runner 지정 | 관리자 |
| `/mhunter <player>` | Hunter 지정 | 관리자 |
| `/mspectator <player>` | Spectator 지정 | 관리자; 새 명령 |
| `/mhspectate` | 참가자 순간이동 메뉴 열기 | 현재 Spectator; 새 명령 |
| `/teammsg <message>` | 자신의 역할/팀으로 전송 | 플레이어 |
| `/trash` | 버릴 물건용 54슬롯 인벤토리; 별칭 `/mhtrash`, `/vextrash` | 플레이어 |
| `/nv` | 개인 야간 투시 전환 | 플레이어 |
| `/mhlang` | 전역 언어 선택기 열기 | 관리자 |
| `/mhkit <on\|off\|toggle\|status>` | 적응형 Hunter 키트 설정 | 관리자 |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | 스폰 이동 설정 | 관리자 |
| `/mhhelp` | 현지화된 역할/관리자 안내서 받기 | 플레이어 / 관리자 |
| `/mhpause` | 진행 중인 경기 일시 중지 | 관리자 |
| `/mhresume` | 일시 중지된 경기 재개 | 관리자 |
| `/mhdebug` | 내부 진단 | 관리자 |

이 릴리스에는 `/mhnone`이 등록되어 있지 않습니다. GUI의 No Team 역할을 사용하세요. Hunter는 추적 나침반을 오른쪽 클릭하여 Runner를 고릅니다. 이는 관전자 순간이동 및 관리자의 대상 선택기와 별개입니다. Runner는 엔더 드래곤을 처치하면 승리하고, Hunter는 남은 Runner가 없으면 승리합니다. 다른 Runner가 남아 있다면 쓰러진 Runner는 Hunter가 됩니다.

## 언어, 이력 및 타사 기여자 표기

원본 플러그인은 **게임 내 언어 10개**를 제공합니다: 영어, 페르시아어, 아랍어, 스페인어, 프랑스어, 독일어, 러시아어, 중국어 간체, 힌디어, 포르투갈어. `/mhlang`은 서버 전체에 적용할 언어 하나를 선택하고 `language.txt`에 영속 저장합니다. GitHub 설명서는 **18개 언어**로 제공되며 아랍어 문서판은 제외됩니다. 일본어 및 그 밖의 추가 README 언어는 변경되지 않은 JAR에 게임 내 번역을 추가하지 않습니다.

[버전 이력](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md)은 제공된 각 빌드를 기록합니다. 이전 1.9.11 / 1.6.4의 전체 설명서는 [버전별 보관소](archive/1.9.11/README.ko.md)에 유지됩니다. 전용 관전자 빌드는 이제 1.13.1로 제공 및 게시되었습니다. 해당 기능을 이전 다운로드의 기능으로 설명해서는 안 됩니다.

**GrimAC는 GrimAC 기여자들이 만든 독립 프로젝트이며 GPL-3.0에 따라 배포됩니다.** Bardiya와 Ali는 Vexland_Manhunt 및 해당 통합을 만들었으며 GrimAC의 제작자로 표기되지 않습니다. 제공된 Grim JAR의 SHA-512와 SHA-1은 공식 Modrinth 2.3.73 Bukkit 배포물과 일치합니다. 내장된 소스 커밋은 [업스트림 v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73)과 일치합니다. 릴리스에는 변경되지 않은 바이너리, 체크섬, 업스트림 소스 스냅샷, 라이선스 및 [타사 고지](../THIRD_PARTY_NOTICES.md)가 포함됩니다. 이러한 구성 요소 고지는 별도 Manhunt 프로젝트에 라이선스를 부여하지 않습니다.

## Dream에게 보내는 장난스러운 도전

Bardiya가 건네는 가벼운 Minecraft 농담입니다 😄

> "휴... Ali와 나는 Dream 것보다 백 배 더 좋은 Manhunt 플러그인을 만들었는데, Dream은 겁이 나서 우리 걸 안 하려 하네!"

## 제작자와 프로젝트 범위

**[Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame)과 [Ali · Alivexor](https://github.com/Alivexor)가 공동 제작했습니다.** 두 핸들은 원본 플러그인 설명 파일에도 저자로 기록되어 있습니다.

이 저장소는 원본 컴파일 릴리스, 문서, 버전 기록을 공동 포트폴리오 프로젝트로 제공합니다. 기능 설명은 제공된 JAR의 정적 검사를 바탕으로 합니다. 이번 게시 작업 과정에서는 실제 서버 호환성, 복구 성능, 밸런스, 부정행위 방지 정확도를 테스트하지 않았습니다.

[Bardiya의 GitHub 포트폴리오](https://github.com/FarlandGame) · [Ali의 GitHub](https://github.com/Alivexor) · [모든 릴리스](https://github.com/FarlandGame/Vexland_Manhunt/releases)
