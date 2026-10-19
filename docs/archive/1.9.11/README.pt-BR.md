# Vexland_Manhunt — 1.9.11 / 1.6.4

> Guia das versões arquivadas · [2.0.0 →](../../README.pt-BR.md)

[English](README.md) | [日本語](README.ja.md) | [فارسی](README.fa.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Español](README.es.md) | [Português (Brasil)](README.pt-BR.md) | [Italiano](README.it.md) | [Nederlands](README.nl.md) | [Polski](README.pl.md) | [Українська](README.uk.md) | [Türkçe](README.tr.md) | [Русский](README.ru.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [한국어](README.ko.md) | [हिन्दी](README.hi.md) | [Bahasa Indonesia](README.id.md)

**Uma experiência completa de Minecraft com Corredores contra Caçadores, criada em conjunto por [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) e [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt reúne configuração de partidas, papéis das equipes, perseguição inicial, rastreamento, progressão, recompensas, resultados e administração em um único plugin para servidores Paper. Os Corredores tentam derrotar o Ender Dragon, enquanto os Caçadores tentam eliminar o último Corredor. O plugin suporta vários Corredores e mantém a perseguição durante mortes, renascimentos, mudanças de dimensão e reconexões. Seu centro de controle `/mhgui` permite que administradores gerenciem uma partida por menus, com mensagens e livros de instruções traduzidos para os jogadores.

## Downloads e compatibilidade

| Versão do plugin | Download | Ambiente de destino |
| --- | --- | --- |
| **1.9.11** — compilação atual fornecida | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Paper **1.21.11**, Java **21** |
| **1.6.4** — compilação anterior | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Paper **1.21.11**, Java **21** |

**1.6.4 e 1.9.11 são números de versão do plugin.** As duas compilações fornecidas declaram a API do Minecraft `1.21.11` e arquivos de classe Java 21. São plugins de servidor para Minecraft Java Edition. Os [requisitos de Java do Paper por versão](https://docs.papermc.io/paper/getting-started/) também indicam Java 21 para Paper 1.21.11. Os descritores fornecidos não declaram dependências de outros plugins.

Estas são **compilações originais para servidor pessoal, com acesso administrativo elevado específico dos criadores**, preservadas exatamente como fornecidas. O guia abaixo cobre os controles públicos do Manhunt.

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

## O que há de novo na 1.9.11?

Estas mudanças foram identificadas comparando as duas compilações fornecidas, incluindo metadados, recursos de mensagens e classes compiladas.

| Adição ou mudança | Comportamento na 1.9.11 |
| --- | --- |
| **Smart Hunter Kit V3** | Os kits adaptativos de renascimento consideram equipamentos dos Corredores, equipes e contexto da partida. O sistema procura manter os kits dos Caçadores abaixo da média dos equipamentos dos Corredores e pode ser ativado/desativado por `/mhkit` ou pela GUI. |
| **Spawn automático no Overworld** | Move o spawn do mundo para perto de um Corredor elegível no Overworld em um intervalo escolhido: desligado, 5, 10, 15, 20 ou 30 minutos. O sistema escolhe um ponto seguro na superfície e ignora casos inadequados. |
| **Pausa e retomada** | `/mhpause` congela a jogabilidade e os temporizadores da partida, o rastreamento e a movimentação do spawn; `/mhresume` continua. O tempo pausado é descontado do tempo ativo da partida. |
| **Recuperação após reinício/falha** | Uma camada de recuperação restaura estado da partida, papéis, alvos dos rastreadores, progresso, temporizadores de recompensas/mortes e estado de reconexão usando snapshots principais/de reserva, salvamentos periódicos e salvamentos ao desligar. |
| **Configurações de reconexão dos Corredores** | Uma janela configurável substitui a janela anterior fixa de 60 minutos. Padrão inicial: 15 minutos, com 10 segundos de proteção ao retornar. O tempo com o servidor desligado é excluído; a expiração pode transformar o Corredor em Caçador ou encerrar a partida. |
| **Administração ampliada** | Altere papéis durante uma partida ao vivo preservando o último Corredor; ações sobre jogadores selecionados, teletransporte/congelamento de equipes, ressincronização do estado de execução e atalhos facilitam o gerenciamento. |
| **Restauração de configurações com confirmação** | Dois cliques em oito segundos aplicam Smart Kit ON, spawn automático a cada 15 minutos e reconexão de 15 minutos. Isso difere do padrão de spawn automático OFF de uma instalação nova. |
| **VexAC 3.0** | Verificações de movimento, combate, AutoClick, velocidade/repulsão e construção; controles de grupos/geral, registro de evidências, alertas aos administradores e exceções por ambiente/lag. |
| **Ultra Deep Debug v4** | `/mhdebug` fornece diagnósticos de máquina de estados, GUI, kits sintéticos/estresse, placeholders de idioma, ciclo de recuperação e integridade. |
| **Indicadores ampliados** | Mais detalhes de progressão, indicadores da vida do dragão, resultados de MVP/dano/distância e informações de ping no TAB. |
| **Mudanças nos comandos** | Adiciona `/mhkit`, `/mhspawn`, `/mhpause`, `/mhresume` e `/mhdebug`; remove `/mhnone`; adapta `/mhhelp` para jogador/administrador e adiciona aliases de `/trash`. |
| **Mais mensagens traduzidas** | Os recursos de tradução passam de 446 chaves de mensagem por idioma para 683. |

As verificações incluídas no VexAC cobrem Fly, Speed, Timer, Phase, Step, NoSlow, GroundSpoof, Reach, KillAura, AimAssist, golpes através de paredes, BadPackets, padrões de tempo do AutoClick, repulsão alterada, Scaffold, Tower, FastPlace, Nuker e alcance de blocos. A interface usa um rótulo de apenas monitoramento, mas o código compilado também contém caminhos de expulsão; confirme o comportamento real de moderação em um servidor de teste antes de confiar nesse rótulo. A compilação anterior contém controles legados Anti AutoClick e Anti Fly.

## Configuração e uso completos com `/mhgui`

### 1. Instale uma compilação no servidor

Pare seu servidor **Paper 1.21.11 / Java 21**. Coloque um dos JARs baixados no diretório `plugins/`. Mantenha apenas uma compilação do VexLandManhunt instalada por vez. Inicie o servidor com um reinício completo após substituir a compilação. O nome interno do plugin continua sendo `VexLandManhunt`; o nome público do projeto é `Vexland_Manhunt`.

### 2. Abra o centro de controle

Entre no servidor como administrador com **OP** ou a permissão **`vexland.admin`** e digite:

```text
/mhgui
```

As instruções abaixo cobrem a interface pública da versão **1.9.11** do plugin, usando os nomes dos botões em inglês. Os nomes seguem o idioma selecionado no servidor. Para usar toda a GUI, use uma conta **OP** de confiança: a permissão do descritor permite abrir o comando, mas alguns manipuladores da GUI fornecida aplicam verificações OP mais rigorosas. O inventário principal tem cinco linhas de nove espaços. Passe o cursor sobre um botão para ler sua descrição e configuração atual. A maioria usa clique normal; ações especiais do mouse e confirmações são explicadas abaixo. O menu menor da 1.6.4 é explicado ao final.

#### Configure sua primeira partida

1. Abra **Player Roles**. Clique na cabeça de cada participante até que o papel exibido esteja correto. Na 1.9.11, o papel alterna entre **Runner** e **Hunter**; um participante sem papel se torna Corredor no primeiro clique. Clique esquerdo/direito/com Shift não são atalhos separados para escolher papéis. Use **Previous Page**, **Next Page** e **Back to Control Center** quando necessário.
2. Atribua pelo menos um Corredor e pelo menos um Caçador. A rotina de início pode transformar os jogadores online restantes sem papel em Caçadores; atribuir todos explicitamente deixa as equipes claras.
3. Clique em **Friendly Fire** para escolher se companheiros podem causar dano uns aos outros. Verifique o indicador ON/OFF após clicar.
4. Clique em **Language** para escolher o idioma de todo o servidor. Essa configuração afeta mensagens, interfaces, avisos e livros de instruções de todos, não apenas do seu jogador.
5. Confira **Smart Hunter Kit**, **Auto World Spawn** e **Anti-Cheat**. Leia o guia do administrador pelo botão do livro se precisar de explicações dentro do jogo.
6. Certifique-se de que **Server Freeze** esteja desligado e clique em **Start Match**. O início prepara jogadores e inventários, executa a apresentação e a roleta aleatória da vantagem inicial antes de liberar os Caçadores, e começa a caçada. Antes de iniciar, guarde fora dos inventários dos participantes tudo que precisar preservar.

#### Botões principais do centro de controle

As posições abaixo contam linhas de cima para baixo e colunas da esquerda para a direita. Elas descrevem o layout final decorado da 1.9.11.

| Posição | Botão em inglês | Função |
|---|---|---|
| Linha 2, coluna 2 | Player Roles | Abre o menu paginado de cabeças de jogadores Corredores/Caçadores. |
| Linha 2, coluna 3 | Target Player | Alterna entre outros jogadores online para ações administrativas sobre o alvo selecionado. Confira o nome atual. |
| Linha 2, coluna 4 | Friendly Fire | Ativa/desativa dano entre companheiros. |
| Linha 2, coluna 5 | Match Info | Envia um relatório rápido do estado da partida, equipes, fogo amigo e alvo selecionado. |
| Linha 2, coluna 6 | Start Match | Executa o início normal da partida e a sequência aleatória de vantagem inicial. |
| Linha 2, coluna 7 | Full Heal | Restaura a vida de todos os jogadores online. |
| Linha 2, coluna 8 | Reset Match | Executa o reinício completo da partida. É diferente de Reset Settings. |
| Linha 3, coluna 2 | Full Hunger | Restaura alimentação e saturação de todos os jogadores online. |
| Linha 3, coluna 3 | Release Hunters | Libera os Caçadores que estão esperando antes do fim da vantagem inicial. |
| Linha 3, coluna 4 | Clear Effects | Remove efeitos de poções de todos os jogadores online. |
| Linha 3, coluna 5 | Server Freeze | Ativa/desativa o congelamento global do servidor; jogadores comuns sem OP ficam congelados. |
| Linha 3, coluna 6 | Clear Target Inventory | Limpa inventário, armadura e mão secundária do jogador selecionado após confirmação. |
| Linha 3, coluna 7 | Teleport Everyone | Traz todos os jogadores online à sua posição atual. |
| Linha 3, coluna 8 | Kill Target | Mata o jogador selecionado após confirmação; as regras normais de morte podem afetar a partida. |
| Linha 4, coluna 2 | Anti-Cheat | Abre os controles do VexAC Security. |
| Linha 4, coluna 3 | Freeze Target | Ativa/desativa o congelamento individual do jogador selecionado. |
| Linha 4, coluna 4 | Emergency Restore | Restaura vida, alimentação e saturação de todos online. |
| Linha 4, coluna 5 | Freeze Team | Clique esquerdo alterna Corredores; direito alterna Caçadores; Shift-clique remove congelamentos individuais/de equipe. |
| Linha 4, coluna 6 | Set Day | Define o horário diurno no seu mundo atual. |
| Linha 4, coluna 7 | Clear Weather | Interrompe chuva e trovoadas no seu mundo atual. |
| Linha 4, coluna 8 | Language | Abre o seletor global de idioma. |
| Linha 5, coluna 2 | Smart Hunter Kit | Ativa/desativa kits adaptativos de renascimento dos Caçadores; mostra ON/OFF. |
| Linha 5, coluna 3 | Clear Dropped Items | Remove entidades de itens caídos no seu mundo atual. |
| Linha 5, coluna 4 | Pause Match / Resume Match | Para ou retoma a jogabilidade ativa e os temporizadores da partida. |
| Linha 5, coluna 5 | Emergency Sync | Ressincroniza papéis, rastreadores e o estado de execução relacionado. |
| Linha 5, coluna 6 | Reset Settings | Restaura configurações equilibradas após confirmação de dois cliques. |
| Linha 5, coluna 7 | Close | Fecha o centro de controle. |
| Linha 5, coluna 8 | Auto World Spawn | Abre o seletor de intervalo do spawn automático no Overworld. |
| Linha 5, coluna 9 | Manhunt Administrator Guide | Fornece o livro de instruções traduzido para administradores. |

Os vidros decorativos e itens de título/status não são botões de jogo.

#### Papéis e alvos selecionados

**Player Roles** muda a equipe real de Manhunt de um participante. Clique em sua cabeça e leia o papel atualizado. Durante STARTING/RUNNING, a interface permite mudanças Corredor/Caçador, mas recusa transformar o último Corredor em Caçador. Isso preserva o lado dos Corredores na partida em andamento. Faça mudanças de papel conscientemente, pois o estado de execução das equipes e os rastreadores são sincronizados após uma mudança.

**Target Player** é separado: seleciona alguém para ações como Freeze Target, Clear Target Inventory ou Kill Target sem mudar sua equipe. Alterne até aparecer o nome do jogador online desejado. Se um alvo salvo ficar indisponível, o código pode recorrer ao primeiro outro jogador online; por isso, confirme sempre o nome imediatamente antes de agir sobre um alvo. Se ninguém mais estiver online, informa que não há alvo disponível.

**Clear Target Inventory** e **Kill Target** exigem clicar na mesma ação para o mesmo alvo duas vezes em **cinco segundos**. O primeiro clique prepara a confirmação e identifica o alvo; o segundo executa a ação. Mudar de alvo ou esperar demais exige nova confirmação. Limpar um inventário apaga seu conteúdo; matar um Corredor pode encerrar ou alterar a partida conforme as regras normais de morte.

**Freeze Team** tem os únicos atalhos de mouse específicos de equipe nesse menu: clique esquerdo normal seleciona os Corredores, clique direito normal seleciona os Caçadores e Shift-clique remove todos os congelamentos individuais/de equipe gerenciados por essa ferramenta. O interruptor global Server Freeze é um controle separado e deve ser desligado separadamente se os jogadores continuarem congelados.

#### Smart Hunter Kit

Clique em **Smart Hunter Kit** para ligar ou desligar kits adaptativos de renascimento dos Caçadores. O botão mostra o estado atual. Quando ligado, um Caçador que renasce pode receber um kit adaptado ao equipamento dos Corredores e ao contexto da partida; o guia fornecido descreve esse kit como mais fraco que a média dos Corredores. Quando desligado, Caçadores não recebem kit automático após morrer. Isso não desliga a bússola rastreadora.

Para definir diretamente em vez de alternar, use `/mhkit on`, `/mhkit off` ou `/mhkit status`. O valor de fallback inspecionado para uma configuração nova é ON.

#### Auto World Spawn

Clique em **Auto World Spawn** e escolha **OFF**, **5 minutes**, **10 minutes**, **15 minutes**, **20 minutes** ou **30 minutes**. Selecionar uma opção a salva e retorna a `/mhgui`; **Back** retorna sem selecionar outro intervalo.

Quando ativado, o sistema procura periodicamente uma superfície segura no Overworld perto de um Corredor ativo nessa dimensão e move o spawn do mundo para lá. Ele não move o spawn se nenhum Corredor estiver no Overworld ou se não encontrar um ponto seguro. O fallback de configuração nova é OFF. Para os mesmos controles por comando, use `/mhspawn off`, `/mhspawn 15` ou `/mhspawn status`, substituindo 15 por qualquer intervalo suportado.

#### Pausa, reconexão e recuperação

**Pause Match** está disponível quando a partida está RUNNING. Congela sistemas de jogo, movimento/interações, temporizadores da partida, rastreamento e movimentação do spawn. **Resume Match** retoma esses sistemas e compensa o tempo pausado. Server Freeze apenas congela jogadores e não deve substituí-lo quando você precisar pausar o relógio da partida.

A janela de reconexão dos Corredores é configurável, com fallback inicial de **15 minutos**. Retornar dentro do prazo restaura o estado do Corredor e fornece dez segundos de proteção. O tempo de indisponibilidade do servidor não consome o prazo de reconexão salvo. Vagas de Corredores expiradas se tornam Caçadores; o prazo esgotado do último Corredor pode dar a vitória aos Caçadores.

**Não há um seletor separado de duração de reconexão na GUI 1.9.11 fornecida**. Para personalizar, pare o servidor, edite `plugins/VexLandManhunt/config.yml`, preserve as demais configurações e defina:

```yaml
features:
  custom-reconnect-minutes: 15
```

Reinicie após editar. Valores abaixo de um minuto são limitados a um. **Reset Settings** restaura esse valor para 15 minutos. A compilação também salva estado de partida/reconexão e snapshots de reserva para recuperação após reinícios/falhas do servidor; deixe o plugin gerenciar esses arquivos em vez de editá-los durante o jogo.

#### Reset Settings e Reset Match

**Reset Settings** exige clicar no botão duas vezes em **oito segundos**. O primeiro clique prepara a confirmação; o segundo restaura **Smart Kit ON**, **Auto Spawn a cada 15 minutos**, **Reconexão de 15 minutos** e uma **vantagem inicial aleatória**. Isso difere de uma instalação nova, em que Auto World Spawn usa fallback OFF. Altera a configuração; não substitui o reinício completo da partida.

**Reset Match** executa o reinício existente da partida, limpando estado/itens temporários e retornando jogadores ao spawn do Overworld para outra rodada. Seu botão principal não usa a confirmação de dois cliques de Reset Settings. **Start Match** pode preparar/limpar inventários dos participantes. Confira qual controle de reinício/início pretende usar antes de clicar.

#### Controles de idioma e anti-cheat

**Language** abre o seletor global. Clique no idioma desejado. As duas compilações fornecidas contêm inglês, persa, árabe, espanhol, francês, alemão, russo, chinês simplificado, hindi e português. O idioma selecionado é compartilhado pelo servidor e salvo. A documentação README em japonês não adiciona japonês ao seletor de idiomas dentro do jogo.

**Anti-Cheat** abre **VexAC Security**. Clique em **VexAC Master** para ativar/desativar o mecanismo interno ou em **Movement**, **Combat**, **AutoClick**, **Velocity / AntiKB** ou **World / Scaffold** para alternar esse grupo. **Anti X-Ray** alterna o Anti-Xray configurado no Paper; reinicie o servidor para aplicar essa alteração. Os itens de status, registro de evidências e modelo de detecção explicam os sistemas atuais. **Back to Control Center** retorna ao menu principal.

A interface descreve moderação somente por monitoramento, mas a inspeção estática mantém um caminho de expulsão baseado em limites. Trate a indicação de ausência de expulsões do menu como uma divergência entre implementação/documentação e confirme a moderação em um servidor controlado antes de depender dela.

#### Guia dentro do jogo e solução de problemas

Clique em **Manhunt Administrator Guide** ou use `/mhhelp` para obter um livro de instruções traduzido. Jogadores podem usar `/mhhelp` para o guia adequado ao seu papel na 1.9.11. Caçadores clicam com o botão direito na bússola para selecionar um Corredor; essa interface de rastreamento é separada do seletor Target Player do administrador.

Se um papel ou rastreador parecer fora de sincronia, **Emergency Sync** atualiza o estado de execução relacionado. **Match Info** ajuda a verificar as equipes e o estado atual. Se uma tentativa de início falhar, confira se a partida está pronta, o congelamento do servidor está desligado e há equipe de Corredores/Caçadores. Após mudar o JAR, use um reinício completo do servidor em vez de `/reload`. `/mhdebug` é um comando de diagnóstico administrativo incluído na 1.9.11; sua presença não afirma que essas versões passaram por testes em servidor ao vivo.

#### Uso do centro de controle antigo da 1.6.4

A 1.6.4 mantém **Player Roles**, **Friendly Fire**, **Start Match**, **Reset Match**, **Release Hunters Now**, **Server Lock**, **Teleport Everyone To Me**, **Heal & Feed Everyone**, **Match Status**, seleção de idioma, **Anti Cheat** e um guia do administrador. Seus papéis alternam **None → Runner → Hunter**, e mudanças de papel ficam bloqueadas enquanto uma partida está iniciando/em execução.

Seu menu anti-cheat contém os controles legados **Anti AutoClick** (regra de 30 CPS com aviso/expulsão), **Anti Fly** e **Anti X-Ray** do Paper. A janela de reconexão dos Corredores é fixa em **60 minutos**. A opção Smart Hunter Kit V3 mais recente, o seletor Auto World Spawn, pausa/retomada, confirmação Reset Settings e ferramentas ampliadas de alvo/mundo descritas acima pertencem à 1.9.11 e não devem ser esperados no menu antigo.

Este guia foi elaborado a partir dos metadados dos JARs fornecidos, textos de idioma/ajuda incluídos e desmontagem estática. A interface não foi executada em um servidor Minecraft ao vivo durante essa inspeção.

### 3. Jogue a perseguição

Os Corredores escapam durante a vantagem inicial aleatória e avançam até derrotar o Ender Dragon. Os Caçadores esperam a liberação e clicam com o botão direito na bússola rastreadora para selecionar um Corredor. Os alvos podem mudar durante o jogo, inclusive quando a perseguição atravessa dimensões. Use `/teammsg <message>` para falar apenas com sua equipe e `/mhhelp` para o guia traduzido do seu papel na 1.9.11.

Se um Corredor morrer, os restantes continuam jogando e o jogador morto se torna Caçador. Um Caçador pode renascer e continuar rastreando. A morte do último Corredor ou o fim do prazo de reconexão de um Corredor pode encerrar a partida para os Caçadores; derrotar o Ender Dragon encerra para os Corredores.

### 4. Pause, finalize e prepare outra partida

Na 1.9.11, pause com `/mhpause` e continue com `/mhresume`. Use `/mhrelease` se os Caçadores precisarem ser liberados antes do fim da contagem da vantagem inicial. Para uma nova partida, use o reinício completo do centro de controle ou `/mhreset`; o reinício limpa estado e itens temporários e retorna jogadores ao spawn do Overworld. Alterações do Paper Anti-Xray exigem reinício do servidor.

## Configurações padrão na 1.9.11

Os valores de fallback inspecionados para configuração nova são:

```yaml
features:
  adaptive-hunter-kit: true
  auto-world-spawn-minutes: 0
  custom-reconnect-minutes: 15
```

`0` significa que a movimentação automática do spawn está desligada. A ação de restauração confirmada da GUI define o intervalo como 15 minutos. Use a GUI ou `/mhkit` e `/mhspawn` para as configurações correspondentes.

## Referência de comandos públicos

Os comandos administrativos listados aqui usam `vexland.admin`, que por padrão é OP. Chat de equipe, lixeira e visão noturna não têm permissão no descritor; `/mhhelp` passa a ser um guia para jogador/administrador na 1.9.11.

| Comando | Finalidade | Disponibilidade |
| --- | --- | --- |
| `/mhgui` | Abrir o centro de controle | Ambas as compilações |
| `/mhstart` | Executar toda a sequência de início | Ambas as compilações |
| `/mhreset` | Reiniciar completamente a partida atual | Ambas as compilações |
| `/mhrelease` | Liberar Caçadores antes da hora | Ambas as compilações |
| `/mrunner <player>` | Atribuir um Corredor | Ambas as compilações |
| `/mhunter <player>` | Atribuir um Caçador | Ambas as compilações |
| `/mhnone <player>` | Remover um papel | Apenas 1.6.4 |
| `/teammsg <message>` | Enviar mensagem privada aos companheiros | Ambas as compilações |
| `/trash` | Abrir o inventário descartável de 54 espaços | Ambas; aliases da 1.9.11: `/mhtrash`, `/vextrash` |
| `/nv` | Alternar visão noturna pessoal | Ambas as compilações |
| `/mhlang` | Abrir o seletor global de idioma | Ambas as compilações; administrador |
| `/mhhelp` | Receber um livro de instruções traduzido | 1.6.4 apenas administrador; 1.9.11 guia para jogador/administrador |
| `/mhkit <on\|off\|toggle\|status>` | Configurar kits inteligentes dos Caçadores | 1.9.11 |
| `/mhspawn <off\|5\|10\|15\|20\|30\|status>` | Configurar movimentação automática do spawn | 1.9.11 |
| `/mhpause` | Pausar a partida em execução | 1.9.11 |
| `/mhresume` | Retomar a partida pausada | 1.9.11 |
| `/mhdebug` | Executar diagnósticos internos | 1.9.11 |

## Idiomas do jogo e idiomas da documentação

As duas compilações fornecidas têm **10 idiomas dentro do jogo**: inglês, persa, árabe, espanhol, francês, alemão, russo, chinês simplificado, hindi e português. Um administrador escolhe o **idioma global do servidor** com `/mhlang`; mensagens, menus, avisos e livros de instruções usam essa seleção, salva em `language.txt`.

A documentação do GitHub está sendo publicada em **18 idiomas, sem uma edição da documentação em árabe**. Japonês, turco e as outras traduções adicionais do README ajudam leitores a entender o projeto; não adicionam idiomas ao jogo nesses JARs originais.

## Histórico de versões e próxima compilação

[CHANGELOG.md](../../../CHANGELOG.md) registra as diferenças entre as versões enviadas. A compilação adicional com um recurso dedicado de espectador está **aguardando recebimento para uma versão futura**. Referências existentes ao Spectator padrão não comprovam esse recurso novo nos dois downloads fornecidos. Cada compilação posteriormente fornecida terá seu próprio download, checksum e notas de mudanças após comparação com a versão anterior.

## Um desafio bem-humorado ao Dream

Uma pequena provocação de Minecraft do Bardiya 😄

> "Ah... Ali e eu fizemos um plugin de Manhunt cem vezes melhor que o do Dream, mas o Dream está com medo e não quer jogar o nosso!"

## Criadores e escopo do projeto

**Criado em conjunto por [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) e [Ali · Alivexor](https://github.com/Alivexor).** Os dois nomes também estão registrados como autores nos descritores originais do plugin.

Este repositório apresenta as versões compiladas originais, sua documentação e notas de versão como um projeto de portfólio compartilhado. As descrições dos recursos se baseiam na inspeção estática dos JARs fornecidos. Compatibilidade em servidor ao vivo, desempenho da recuperação, equilíbrio e precisão do anti-cheat não foram testados neste fluxo de publicação.

[Portfólio do Bardiya no GitHub](https://github.com/FarlandGame) · [GitHub do Ali](https://github.com/Alivexor) · [Todas as versões](https://github.com/FarlandGame/Vexland_Manhunt/releases)
