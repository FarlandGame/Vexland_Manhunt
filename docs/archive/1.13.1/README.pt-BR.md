# Vexland_Manhunt — 1.13.1

> Guia da versão arquivada · [2.0.0 →](../../README.pt-BR.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Uma experiência completa de Minecraft com Corredores contra Caçadores, criada em conjunto por [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) e [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt reúne configuração de partidas, papéis das equipes, perseguição inicial, rastreamento, progressão, recompensas, resultados e administração em um único plugin para servidores Paper. Os Corredores tentam derrotar o Ender Dragon, enquanto os Caçadores tentam eliminar o último Corredor. O plugin suporta vários Corredores e mantém a perseguição durante mortes, renascimentos, mudanças de dimensão e reconexões. Seu centro de controle `/mhgui` permite que administradores gerenciem uma partida por menus, com mensagens e livros de instruções traduzidos para os jogadores.

## Downloads e compatibilidade

| Arquivo / versão | Download | Finalidade |
|---|---|---|
| **1.13.1 — atual** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Plugin Manhunt de Bardiya e Ali |
| **GrimAC 2.3.73 — obrigatório** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | Dependência anticheat separada, de terceiros |
| 1.9.11 — arquivada | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Compilação anterior do Manhunt |
| 1.6.4 — arquivada | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Compilação mais antiga do Manhunt |

**Plataforma: Paper 1.21.11, Java 21.** Os números 1.6.4, 1.9.11 e 1.13.1 são versões do plugin, não versões compatíveis do Minecraft. Na 1.13.1, GrimAC é uma dependência obrigatória e a ponte exige a API 2.3.73. Baixe **os dois JARs atuais**. São plugins de servidor; os jogadores não os instalam na pasta de mods do cliente.

Estas são as compilações originais de servidor pessoal, com acesso administrativo elevado específico dos criadores, preservadas exatamente como fornecidas. Este manual cobre os controles públicos do Manhunt.

## A experiência Manhunt

- **Equipes de Corredores e Caçadores:** atribua jogadores online a qualquer um dos lados. Uma partida precisa de pelo menos um Corredor e um Caçador ou um jogador online sem papel atribuído. Os Corredores sobreviventes continuam se um companheiro morrer; um Corredor morto se torna Caçador, a menos que essa morte encerre a partida.
- **Início cinematográfico da partida:** inventários e modos de jogo são preparados, as equipes são apresentadas e uma roleta escolhe a vantagem inicial dos Corredores. Os Caçadores ficam congelados durante essa contagem regressiva, com títulos e sons. A vantagem inicial é aleatória; administradores podem liberar os Caçadores antes da hora.
- **Bússola rastreadora com escolha de alvo:** os Caçadores recebem uma bússola especial. Clique nela com o botão direito para escolher um Corredor no menu de alvos e mudar de alvo durante a perseguição. Entre dimensões, o rastreamento segue a rota do portal correspondente até que o rastreamento direto seja possível. Os Caçadores recebem seu rastreador novamente após renascer.
- **Indicadores de progresso:** barras de chefe e informações da partida acompanham equipamentos e progressão dos Corredores por recursos do Nether, varas de blaze, pérolas, Olhos do Ender, fortaleza e End. A compilação mais recente adiciona etapas mais detalhadas e indicadores que consideram a vida do dragão.
- **Recompensas por abates dos Corredores:** quando um Corredor mata um Caçador durante uma partida ativa, é usado um conjunto ponderado de 50 recompensas que considera a progressão. Inclui sorteios animados, recompensas duplas/triplas, anúncios de sequências de abates e comemorações de itens raros.
- **Vitória e resultados:** a morte do último Corredor dá a vitória aos Caçadores; derrotar o Ender Dragon dá a vitória aos Corredores. Inclui títulos de encerramento, comemorações, informações de abates/mortes e limpeza de itens temporários. A compilação mais recente também informa MVP, dano e distância.
- **Comunicação da equipe e utilidades:** mensagens privadas entre companheiros com `/teammsg`, um inventário descartável de 54 espaços com `/trash` e visão noturna pessoal com `/nv`.
- **Administração por menus:** papéis, início/reinício, liberação antecipada dos Caçadores, fogo amigo, bloqueio do servidor, teletransporte de todos, cura/alimentação, idioma, configurações de proteção, status e guias estão disponíveis no centro de controle. O congelamento e o reinício completo ajudam a preparar a próxima partida.
- **Guias traduzidos:** livros para Corredores, Caçadores e administradores explicam objetivos, uso do rastreador, mortes, configuração e comandos. A versão 1.9.11 oferece aos jogadores um guia conforme seu papel por `/mhhelp`.
- **Integração com Paper Anti-Xray:** os controles do menu configuram a proteção do Paper por mundo; as alterações exigem reiniciar o servidor para entrar em vigor.

## O que há de novo na 1.13.1?

Em comparação com a compilação 1.9.11 fornecida:

- **Espectadores fantasmas:** função separada, atribuição por administrador, voo protegido, jogadores ocultos, estado salvo/restaurado e menu paginado de teleporte para participantes.
- **Central de controle redesenhada:** menus por categoria, seleção explícita entre quatro funções, seletor de alvos por nome, duração de reconexão, predefinições Classic/Fast/Hardcore/Custom e telas próprias de confirmação com 30 segundos.
- **Integração com GrimAC:** o GrimAC 2.3.73 obrigatório substitui o caminho ativo de inicialização do VexAC. A interface oferece controle geral, cinco grupos de verificações, alertas e modos de monitoramento/aplicação. Paper Anti-Xray continua independente.
- **Novo planejador Smart Hunter Kit:** adapta equipamentos e suprimentos aos equipamentos/encantamentos dos Runner, ao Runner mais próximo, aos tamanhos dos times, à distância, dimensão e terreno. Preserva equipamentos melhores já existentes, evita ferramentas duplicadas e limita a reposição de consumíveis com histórico de 30 segundos. Isso não garante uma diferença fixa de equipamento nem equilíbrio medido.
- **Recuperação validada:** snapshots selados com SHA-256, verificações de esquema/estado e uso de backup válido como alternativa; snapshots inválidos ou de formato mais novo são preservados sem sobrescrita. O estado dos espectadores tem persistência própria.
- **Mensagens ampliadas:** as chaves traduzidas passam de 683 para 762 por tradução incluída, ainda nos mesmos dez idiomas do jogo. Dois comandos públicos novos são registrados: `/mspectator <player>` e `/mhspectate`.
- **Alternativa ao redefinir:** se não houver uma superfície segura perto do spawn do Overworld, a redefinição poderá pular esse teleporte em vez de forçá-lo.

## Configuração e uso completos com `/mhgui`

Pare o servidor e guarde backup dos mundos e dos dados dos plugins. Coloque os dois JARs atuais em `plugins/`, mantendo apenas um JAR Manhunt e um JAR GrimAC nessa pasta. Preserve as configurações/dados existentes em `plugins/VexLandManhunt/` ao atualizar. Inicie completamente o servidor Paper 1.21.11 / Java 21; faça uma reinicialização completa ao substituir compilações. GrimAC precisa carregar corretamente. O nome interno do plugin continua `VexLandManhunt`.

Este guia descreve a versão **1.13.1** do plugin com rótulos em inglês. Os rótulos seguem o idioma global do servidor. As linhas são contadas de cima para baixo e as colunas da esquerda para a direita. Use um clique esquerdo normal, salvo indicação de ação especial. Este guia vem de inspeção estática; nenhum servidor Minecraft foi executado.

### Preparar uma partida

1. Use `/mhgui` com `vexland.admin` (padrão: OP).
2. Abra **Player Roles**, clique no bloco com o nome de um jogador e escolha **Runner**, **Hunter**, **Spectator** ou **No Team**. Isso abre um seletor de função exata; clicar no jogador não alterna sua função em sequência.
3. Atribua pelo menos um Runner e um Hunter. Jogadores online sem função podem virar Hunter quando a partida começa; espectadores não preenchem a vaga necessária de nenhum dos times.
4. Revise **Match Settings**, **GrimAC Security** e **Global Language**. Desative Server Freeze antes de iniciar.
5. Abra **Match Controls → Start Match**. Os inventários dos participantes são preparados/esvaziados, a introdução é reproduzida e a roleta escolhe a vantagem antes de liberar os Hunter.

### Início: `/mhgui` (cinco linhas)

| Posição | Botão | Ação |
|---|---|---|
| R2 C2 | Match Controls | Iniciar, pausar/retomar, liberar e redefinir. |
| R2 C4 | Player Roles | Abrir a lista de funções dos jogadores online. |
| R2 C6 | Match Settings | Fogo amigo, kits, spawn, reconexão e predefinições. |
| R2 C8 | Player Management | Escolher um alvo e usar ferramentas de jogadores/mundo. |
| R4 C2 | GrimAC Security | Abrir as configurações de proteção. |
| R4 C4 | Global Language | Escolher o idioma usado por todos. |
| R4 C6 | Administrator Guide | Adicionar o livro administrativo traduzido ao inventário. |
| R5 C5 | Close | Fechar o menu. |

O sinalizador em R1 C5 informa o estado da partida e as quantidades de Runner/Hunter.

### Match Controls (cinco linhas)

| Posição | Botão | Ação |
|---|---|---|
| R2 C2 | Start Match | Iniciar a sequência completa. |
| R2 C4 | Pause Match / Resume Match | Pausar ou retomar o jogo e os cronômetros; disponível para uma partida RUNNING. |
| R2 C6 | Release Hunters | Encerrar antecipadamente a espera atual dos Hunter. |
| R2 C8 | Reset Match | Abrir a confirmação e então redefinir completamente a partida. |
| R4 C2 | Server Freeze | Alternar o congelamento global dos jogadores sem OP. |
| R4 C4 | Teleport Everyone | Abrir a confirmação e então trazer todos os jogadores online até você. |
| R4 C6 | Match Info | Enviar o relatório de partida e times. |

**Back** fica em R5 C1; **Close**, em R5 C9. Server Freeze é separado de Pause Match: use Pause quando o relógio e os sistemas de jogo precisarem parar juntos.

### Player Roles

A lista de jogadores com seis linhas mostra até 45 blocos de função com nomes, ordenados pelo nome do jogador, nas cinco primeiras linhas. Runner usa concreto verde-limão, Hunter concreto vermelho, Spectator um olho do Ender e No Team concreto cinza. A linha inferior tem **Previous Page** em C1, informações da página/jogadores online em C3, **Back to Control Center** em C5 e **Next Page** em C9.

Clique em um jogador para abrir **Choose Player Role** (três linhas):

| Posição | Função exata |
|---|---|
| R2 C2 | Runner |
| R2 C4 | Hunter |
| R2 C6 | Spectator |
| R2 C8 | No Team |

O nome/função atual aparece em R1 C5; **Back** fica em R3 C1 e **Close**, em R3 C9. Funções podem mudar durante a partida. Tirar a função Runner do último Runner atribuído durante RUNNING abre a confirmação **Last Runner: the match will end**. Aplicá-la pode dar a vitória aos Hunter. Comandos diretos de função têm efeito imediato: use-os com atenção. No Team pode ser atribuído aqui; a sincronização normal ao iniciar/entrar pode transformar um jogador sem função em Hunter durante uma partida ativa.

### Espectadores

Um administrador atribui `/mspectator <player>` ou escolhe **Spectator** em Player Roles. O comando verifica o acesso administrativo mesmo sem uma linha de permissão no descritor. Jogadores não entram nessa função por conta própria executando `/mhspectate`.

O espectador recebe uma bússola **Spectator teleport** no primeiro espaço da barra rápida. Segure-a na mão principal e clique com o botão direito, ou use `/mhspectate`, para abrir o menu de teleporte com seis linhas. Ele funciona somente enquanto o jogador tiver a função Spectator. As cinco primeiras linhas contêm até 45 Runner/Hunter vivos e online, ordenados pelo nome; clique em um bloco de função com nome para ir à posição atual daquele jogador, inclusive em outro mundo. A linha inferior tem **Previous Page** em C1, **Close** em C5 e **Next Page** em C9. Sem participante adequado, R3 C5 mostra **No players available**. Fechar esse menu não remove a função de espectador.

Espectadores voam, ficam ocultos dos outros jogadores, não colidem e são protegidos contra dano. A implementação usa modo Aventura com voo; não concede a câmera do modo Espectador vanilla nem passagem através de blocos. Ela bloqueia ataques, quebra/colocação de blocos, interações normais com blocos/entidades, coleta/descarte de itens, troca da mão secundária, cliques/arrastos no inventário, manipulação de suportes de armadura e coleta/ganho de experiência. Criaturas não podem mirá-los e mudanças de fome são canceladas. `/teammsg <message>` chega a outros jogadores com a função Spectator. Não forneça aos competidores localizações de participantes ou outras ajudas externas.

Para sair, um administrador atribui **Runner**, **Hunter** ou **No Team**, ou usa `/mrunner <player>` ou `/mhunter <player>`. Não há comando/botão específico para sair sozinho. A saída restaura inventário/cursor, localização, modo de jogo, voo, colisão e imunidade salvos; depois aplica o comportamento da nova função na partida. O estado do espectador é salvo para reconexão. Full Match Reset restaura esse estado, limpa as funções e move jogadores online para um spawn seguro do Overworld quando disponível. A limpeza normal no fim da partida exclui os espectadores do tratamento de itens/voo dos participantes.

### Match Settings (cinco linhas)

| Posição | Botão | Ação |
|---|---|---|
| R2 C2 | Friendly Fire | Alternar dano entre colegas de time. |
| R2 C4 | Smart Hunter Kit | Alternar kits adaptativos de renascimento dos Hunter. |
| R2 C6 | Auto World Spawn | Abrir a seleção de intervalo. |
| R2 C8 | Reconnect Grace | Abrir a seleção da duração de reconexão dos Runner. |
| R4 C2 | Match Preset | Escolher Classic, Fast, Hardcore ou Custom. |
| R4 C4 | Reset Settings | Confirmar ajustes equilibrados: Kit ON, Spawn 15m, Reconnect 15m. |
| R4 C6 | Random Head Start | Bloco informativo; a roleta continua escolhendo o atraso. |

**Back** fica em R5 C1; **Close**, em R5 C9.

O seletor **Reconnect Grace** com três linhas oferece **1, 5, 10, 15, 20, 30 minutos** em R2 C2–C7, nessa ordem. Clicar salva o valor e mantém o seletor aberto. Back fica em R3 C1; Close, em R3 C9.

O seletor **Match Preset** de três linhas coloca **Classic**, **Fast**, **Hardcore**, **Custom** em R2 C2, C4, C6, C8. Classic: Kit ON, Spawn 15m, Reconnect 15m. Fast: ON, 5m, 10m. Hardcore: OFF, OFF, 5m. Custom mantém os ajustes manuais atuais. As predefinições preservam a vantagem aleatória. A seleção mantém o menu aberto; Back fica em R3 C1, Close em R3 C9.

**Auto World Spawn** oferece OFF, 5m, 10m em R2 C2, C3, C4 e 15m, 20m, 30m em R2 C6, C7, C8. Back fica em R3 C5. Selecione um intervalo ou use `/mhspawn <off|5|10|15|20|30|status>`. Isso move o spawn do Overworld para perto de um Runner adequado no Overworld; pode ignorar a ação quando não houver candidato adequado. `/mhkit <on|off|toggle|status>` controla os kits diretamente.

### Player Management (seis linhas)

| Posição | Botão | Aplica-se a |
|---|---|---|
| R1 C5 | Target Player | Abrir um seletor de jogadores por nome. |
| R2 C2 | Full Heal | Todos os jogadores online. |
| R2 C4 | Full Hunger | Todos os jogadores online. |
| R2 C6 | Clear Effects | Todos os jogadores online. |
| R2 C8 | Freeze Target | Jogador selecionado. |
| R4 C2 | Clear Target Inventory | Jogador selecionado; exige confirmação. |
| R4 C4 | Kill Target | Jogador selecionado; exige confirmação e os resultados normais da partida se aplicam. |
| R4 C6 | Set Day | Seu mundo atual. |
| R4 C8 | Clear Weather | Seu mundo atual. |
| R5 C2 | Clear Dropped Items | Seu mundo atual; exige confirmação. |
| R5 C4 | Emergency Sync | Atualizar sistemas de função/execução dos jogadores online. |
| R5 C6 | Freeze Team | Esquerdo: Runner; direito: Hunter; Shift-clique: remover estes congelamentos de times/individuais. |

Back fica em R6 C1; Close, em R6 C9. A escolha de alvo não muda funções. O seletor oferece 28 outros jogadores online por página, nas linhas 2–5, colunas 2–8; clique em um nome para selecionar e voltar. Previous/Back/Next ficam em R6 C1/C5/C9. Confira novamente o alvo exibido antes de aplicar uma ação.

### Telas de confirmação

Reset Match, Teleport Everyone, Reset Settings, Clear Target Inventory, Kill Target, Clear Dropped Items e a mudança do último Runner pela interface usam uma tela separada **Confirm Action** de três linhas. Leia a ação/alvo em R1 C5 e clique no **Confirm** verde em R2 C3 ou no **Cancel** vermelho em R2 C7. A confirmação expira após **30 segundos**. Alvos alterados/offline ou funções alteradas exigem nova seleção. Nos novos caminhos do menu, isso substitui as instruções antigas de cliques repetidos em cinco/oito segundos.

### GrimAC Security e idioma

O menu Grim de seis linhas tem status em R1 C5; controles em R2 C2 **GrimAC Master**, C4 **Movement**, C6 **Combat**, C8 **Packets**; R4 C2 **Velocity / AntiKB**, C4 **World / Scaffold**, C6 **Anti X-Ray**, C8 **Admin Alerts**; e R5 C5 **Monitor mode**. Back fica em R6 C1 e Close em R6 C9. Monitor mode controla alertas/evidências em vez da aplicação de medidas. Paper Anti-Xray é independente e exige reinicialização após alterações. São controles GrimAC; a descrição antiga do menu VexAC/AutoClick não corresponde a esta versão.

Global Language vale para todos e atualiza menus/itens. Clique no idioma indicado pelo nome; Back fica em R3 C5. `/mhlang` abre o mesmo seletor e `/mhhelp` fornece o guia traduzido de jogador/administrador.

### Padrões atuais, reconexão e moderação

Os valores de fallback de uma configuração nova em `plugins/VexLandManhunt/config.yml` são:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` significa que o movimento automático do spawn está desligado. Reset Settings e Classic escolhem 15 minutos em seu lugar. Durante a janela de reconexão de um Runner, sua vaga é mantida; voltar a tempo concede dez segundos de proteção. O tempo de servidor parado salvo é excluído. O término do prazo pode transformar o Runner em Hunter ou encerrar a partida a favor dos Hunter. Pause/Resume congela sistemas de jogo e ajusta o tempo ativo da partida. Os arquivos de recuperação são gerenciados pelo plugin.

As configurações da ponte Grim persistem em `plugins/VexLandManhunt/grim-settings.yml`. Os padrões iniciais são Master ON, todos os cinco grupos ON, Admin Alerts ON e **Monitor mode OFF: a aplicação de medidas está ativada**. Monitor mode enfileira evidências/alertas e cancela os flags correspondentes. No modo de aplicação, a ponte pode transformar um comando de expulsão Grim em desconexão traduzida que permite reconectar; ela não estabelece uma política de banimento permanente. Os limites reais também dependem da configuração do Grim. Evidências são enfileiradas para `plugins/VexLandManhunt/anticheat/grim-evidence.log`; filas limitadas podem perder entradas sob carga. A ponte isenta espectadores, jogo pausado/congelado e certos contextos de veículos, com três segundos de tolerância após entrada, teleporte e renascimento. Não se afirma precisão do anticheat nem desempenho medidos.

## Referência dos comandos públicos — 1.13.1

Acesso administrativo significa OP ou `vexland.admin` (padrão OP). O manipulador de `/mspectator <player>` verifica isso apesar de não haver linha de permissão no descritor. Comandos diretos de função têm efeito imediato; mudar o último Runner durante RUNNING pode encerrar a partida. A interface oferece uma confirmação para esse caso.

| Comando | Finalidade | Acesso |
|---|---|---|
| `/mhgui` | Abrir a central de controle por categorias | Administrador |
| `/mhstart` | Iniciar a sequência completa da partida | Administrador |
| `/mhreset` | Redefinir toda a partida | Administrador |
| `/mhrelease` | Liberar os Hunter em espera | Administrador |
| `/mrunner <player>` | Atribuir Runner | Administrador |
| `/mhunter <player>` | Atribuir Hunter | Administrador |
| `/mspectator <player>` | Atribuir Spectator | Administrador; novo |
| `/mhspectate` | Abrir menu de teleporte para participantes | Spectator atual; novo |
| `/teammsg <message>` | Enviar para sua própria função/time | Jogador |
| `/trash` | Inventário descartável de 54 espaços; aliases `/mhtrash`, `/vextrash` | Jogador |
| `/nv` | Alternar visão noturna pessoal | Jogador |
| `/mhlang` | Abrir o seletor global de idioma | Administrador |
| `/mhkit <on\|off\|toggle\|status>` | Configurar kits adaptativos dos Hunter | Administrador |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Configurar movimento do spawn | Administrador |
| `/mhhelp` | Receber guia traduzido de função/administrador | Jogador / administrador |
| `/mhpause` | Pausar a partida em andamento | Administrador |
| `/mhresume` | Retomar a partida pausada | Administrador |
| `/mhdebug` | Diagnósticos internos | Administrador |

`/mhnone` não está registrado nesta versão; use No Team na interface. Hunter clicam com o botão direito na bússola rastreadora para escolher um Runner; isso é separado do teleporte de espectadores e do seletor administrativo de alvos. Runner vencem derrotando o Ender Dragon; Hunter vencem quando não resta nenhum Runner. Um Runner abatido vira Hunter se houver outros Runner restantes.

## Idiomas, histórico e créditos de terceiros

O plugin original oferece **10 idiomas no jogo**: inglês, persa, árabe, espanhol, francês, alemão, russo, chinês simplificado, hindi e português. `/mhlang` seleciona um idioma para todo o servidor, salvo em `language.txt`. O manual do GitHub tem **18 idiomas**, sem edição árabe da documentação. Japonês e outros idiomas extras do README não adicionam traduções ao jogo nos JARs inalterados.

O [histórico de versões](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/CHANGELOG.md) registra cada compilação fornecida. O manual completo anterior de 1.9.11 / 1.6.4 permanece no [arquivo de versões](../1.9.11/README.pt-BR.md). A compilação dedicada aos espectadores já foi fornecida e publicada como 1.13.1; seus recursos não devem ser atribuídos aos downloads antigos.

**GrimAC é um projeto independente dos colaboradores GrimAC, distribuído sob GPL-3.0.** Bardiya e Ali criaram Vexland_Manhunt e sua integração; não são creditados como autores do GrimAC. O JAR Grim fornecido corresponde aos SHA-512 e SHA-1 do artefato Bukkit oficial Modrinth 2.3.73. Seu commit de código embutido corresponde ao [upstream v2.3.73](https://github.com/GrimAnticheat/Grim/releases/tag/v2.3.73). A versão inclui binários inalterados, checksums, snapshot do código upstream, licença e [avisos de terceiros](../../../THIRD_PARTY_NOTICES.md). Esses avisos de componentes não atribuem uma licença ao projeto Manhunt separado.

## Um desafio bem-humorado ao Dream

Uma pequena provocação de Minecraft do Bardiya 😄

> "Ah... Ali e eu fizemos um plugin de Manhunt cem vezes melhor que o do Dream, mas o Dream está com medo e não quer jogar o nosso!"

## Criadores e escopo do projeto

**Criado em conjunto por [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) e [Ali · Alivexor](https://github.com/Alivexor).** Os dois nomes também estão registrados como autores nos descritores originais do plugin.

Este repositório apresenta as versões compiladas originais, sua documentação e notas de versão como um projeto de portfólio compartilhado. As descrições dos recursos se baseiam na inspeção estática dos JARs fornecidos. Compatibilidade em servidor ao vivo, desempenho da recuperação, equilíbrio e precisão do anti-cheat não foram testados neste fluxo de publicação.

[Portfólio do Bardiya no GitHub](https://github.com/FarlandGame) · [GitHub do Ali](https://github.com/Alivexor) · [Todas as versões](https://github.com/FarlandGame/Vexland_Manhunt/releases)
