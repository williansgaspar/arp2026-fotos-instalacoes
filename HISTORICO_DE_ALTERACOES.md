# Histórico de Alterações — Registro fotográfico das instalações (ARP 2026)

Registro cronológico (mais recente no topo) de **achados, alterações, correções de bug,
edições, exclusões e adições** relevantes deste projeto, para fins de auditoria e
rastreabilidade — mesmo padrão adotado em `16_Plataforma_App` e `Salomao_Energy_AI`. É
especialmente relevante aqui por ser uma consulta **pública**, usada por licitantes do pregão.

Cada entrada traz **o que, por quê, quando e quem**.

**Regra:** toda mudança que afete o que o público vê ou o escopo dos dados (UCs incluídas/
excluídas, critério de casamento foto↔UC, rótulos de lote) ganha uma entrada aqui na mesma
tarefa em que acontece.

| Campo | Conteúdo |
|---|---|
| Tipo | Achado / Alteração / Correção / Edição / Exclusão / Adição |
| O que | Descrição objetiva e verificável |
| Por quê | Motivação, decisão ou causa raiz |
| Quando | Data |
| Quem | Quem decidiu/autorizou + quem executou |
| Referência | Commit relacionado |

---

## 2026-09-26

### Alteração (segurança) — Commits assinados e ligados ao perfil GitHub
- **O que:** a partir de agora, os commits feitos no XPS saem **assinados** com uma chave SSH
  guardada no cofre **Bitwarden** e com o e-mail privado do GitHub
  (`25888051+williansgaspar@users.noreply.github.com`), aparecendo como **Verified** e ligados
  ao perfil `williansgaspar`. Vale para este repositório pela configuração global do git; nada
  no código mudou. Os commits anteriores (e-mail `williansgaspar@x2p34.onmicrosoft.com`, que não
  estava cadastrado no GitHub) continuam como estão.
- **Por quê:** rastreabilidade de autoria.
- **Quando:** 2026-09-26.
- **Quem:** Willians Gaspar, via Claude Code.
- **Referência:** `16_Plataforma_App/SEGURANCA_CREDENCIAIS.md`.

## 2026-09-05

### Adição — Este arquivo (prática de auditoria)
- **O que:** criação do `HISTORICO_DE_ALTERACOES.md` como registro cronológico único do
  projeto.
- **Por quê:** pedido explícito do Willians por rastreabilidade e auditagem de todo achado,
  alteração, correção, edição, exclusão e adição em seus projetos ativos — mesmo padrão
  replicado em `16_Plataforma_App` e `Salomao_Energy_AI`.
- **Quando:** 2026-09-05.
- **Quem:** Willians Gaspar, via Claude Code.

---

## Entradas retroativas (reconstruídas a partir do `git log` e de decisões já registradas em
## memória de sessões anteriores — ver nota de precisão ao final)

### 2026-09-01 — Alteração — Escopo da consulta pública travado em "ARP (174)"
- **O que:** filtro de Escopo na consulta pública passou a abrir travado em "ARP (174)" — o
  universo oficial de UCs do pregão (fonte: `UC_Stats_v2.csv`), em vez de mostrar por padrão
  todas as UCs (incluindo correlatas fora do escopo).
- **Por quê:** evitar que um licitante interprete uma UC "correlata" (fora do escopo oficial da
  ARP, mas presente na base por outro motivo) como parte do universo licitado.
- **Quando:** 2026-09-01.
- **Quem:** Willians Gaspar (execução não registrada com detalhe de ferramenta nesta entrada
  retroativa).
- **Referência:** commit `2b6429e`.

### 2026-09-01 — Adição — UC 420001779 (H.M. Álvaro Ramos) incluída como correlata fora do escopo
- **O que:** UC adicionada à base como correlata, marcada explicitamente fora do escopo oficial
  da ARP (não removida, só sinalizada — regra geral do projeto: `escopo_arp:false` em vez de
  exclusão, ver `[[project_consulta_fotos_arp2026_escopo]]` na memória).
- **Por quê:** manter rastreabilidade de UCs que aparecem na base de fotos/documentos mas não
  pertencem ao universo licitado de 174 UCs, sem apagar o registro.
- **Quando:** 2026-09-01.
- **Quem:** Willians Gaspar (execução não registrada com detalhe de ferramenta nesta entrada
  retroativa).
- **Referência:** commit `667bdc5`.

### 2026-09-01 — Adição/Correção — Fotos 400026999 e 400102717 registradas; rótulo de lote das correlatas ajustado
- **O que:** registro de fotos para os códigos de instalação 400026999 e 400102717; correção do
  rótulo de lote exibido para as UCs correlatas.
- **Por quê:** completar a cobertura fotográfica das instalações e corrigir uma inconsistência
  de exibição encontrada na tela pública.
- **Quando:** 2026-09-01.
- **Quem:** Willians Gaspar (execução não registrada com detalhe de ferramenta nesta entrada
  retroativa).
- **Referência:** commit `2c92021`.

> **Nota de precisão:** as três entradas acima foram reconstruídas em 2026-09-05 a partir da
> mensagem de cada commit e de memórias de sessões anteriores já registradas
> (`project_consulta_fotos_arp2026_escopo`, `feedback_match_registro_por_codigo_numerico`) — não
> de uma revisão linha a linha do diff de cada commit. O campo "Quem" nessas entradas não
> distingue se a execução foi manual ou via algum assistente, por não haver esse registro na
> época. A partir de 2026-09-05, toda nova entrada deve trazer essa distinção com precisão.
