# onboarding-cliente

## Task: Onboarding de Novo Cliente — Método Stark

Processo completo do Gestor de Tráfego ao assumir um novo cliente: da validação dos
ativos Meta até as campanhas no ar e a conferência final com o Coordenador.

**Fontes:** Playbook de Onboarding — Gestor de Tráfego Stark v1.0 (abr/2026) ·
POP-OPR-013 (ATI-3/IT-3.1, ATI-8/IT-8.1) · POP-OPR-014 (ATI-3).
**Espelha:** ClickUp — "Configurar tráfego" (SUB-04, Onboarding Cliente) e a IT-5.1 do Doc.

### Metadata
- **executor:** traffic-chief
- **apoio:** media-buyer (execução), analytics-analyst (rastreamento), Coordenador (conferência final)
- **elicit:** true
- **mode:** sequential
- **output:** briefing-cliente.md + conta configurada no padrão Stark + campanhas no ar
- **prazo de referência:** D+3 a D+10

### Filosofia

> Padronização precede refinamento. Performance precede escala. Processo precede sofisticação.
> Feeling sem estrutura é chute; feeling com estrutura é expertise.

Todo gestor, independente do nível, segue a estrutura-base antes de propor variações.

### Inputs Required
```
nome_cliente: Nome do cliente / clínica
bm_cliente: ID do Gerenciador de Negócios (gestor precisa ser Admin)
conta_meta_ads: ID ou nome da conta no Gerenciador
conta_google_ads: ID da conta Google Ads
ga4_id: ID da propriedade GA4 (G-)
gtm_id: ID do container GTM
procedimentos_reais: Procedimentos que o médico de fato opera
objetivo_negocio: O que o cliente espera (leads WPP, Direct, formulário, agendamento)
orcamento_mensal: Budget total disponível por mês
meta_cpl: CPL alvo do cliente (se souber)
fase_atual: Conta zerada ou conta com histórico?
concorrentes: 3 concorrentes principais (lista fornecida pelo cliente)
```

### Elicitation — Perguntas Obrigatórias do Diagnóstico
```
1. O cliente é completamente novo ou já rodou tráfego antes?
2. Possui conteúdo gravado disponível? Quantas peças utilizáveis?
3. A base de seguidores é orgânica ou comprada?
4. A base já vendeu antes (pacientes reais)?
5. Possui lista de pacientes/leads exportável (e-mail/telefone)?
6. Possui dados de CRM exportáveis?
7. Quais procedimentos o médico de fato opera?
8. Qual a verba mensal disponível para anúncios?
```

---

## Execution Steps

### Bloco 1 — Validar os ativos Meta (R1–R6)

Reusa IT-3.1 (POP-OPR-013 / ATI-3). **Pré-condição:** gestor Admin na BM do cliente.
Ver `checklists/validacao-ativos-meta.md`.

- R1 — Página do Facebook ativa e vinculada à BM
- R2 — Conta do Instagram comercial ativa e vinculada à BM
- R3 — WABA com número dedicado registrado
- R4 — Conta de Anúncios ativa
- R5 — Verificação da empresa com status **Verificado**
- R6 — Nenhum ativo com restrição, bloqueio ou aviso
- Comunicar ao cliente: responder ≥ 80% das mensagens e 1ª resposta em ≤ 24h

**VETO:** qualquer ativo com restrição → tratar antes de avançar. Não iniciar o cadastro
do cartão (ATI-4) com R6 falso.

### Bloco 2 — Diagnóstico inicial da conta

- Responder as 8 perguntas obrigatórias (acima)
- **Se houver histórico** (antes de alterar qualquer coisa):
  - Filtrar 3 meses (ou 30 dias se dados insuficientes)
  - Gasto por objetivo de campanha
  - CPL macro — apenas campanhas de conversão/mensagens
  - Públicos frios (interesses, lookalikes) que entregaram resultado
  - Públicos quentes (RMKT, video viewers, engajamento) que performaram
  - Melhores criativos por CPC, CTR e CPL
  - Estratégias já aplicadas + **3 ações ainda não testadas**
- **Auditoria de Pixel e conversões:** jornada e gatilhos, atribuição de valor por evento,
  Medição Agregada de Eventos, API de Conversões, aba Diagnóstico do Gerenciador de Eventos
- **Análise de concorrência (3 concorrentes):** Biblioteca de Anúncios (formato, emoção,
  gatilhos, benefícios), landing pages (oferta, preço, prova social, CTA), screenshots
  SimilarWeb e SocialBlade, mystery shopping nos concorrentes e no próprio cliente

### Bloco 3 — Setup Meta Ads

Ver `data/padroes-stark.md` para públicos, nomenclatura e UTMs.

- Instalar as colunas personalizadas Stark (template conforme objetivo: Mensagem ou Cadastro)
- Criar **todos** os públicos padrão Stark em sessão dedicada
  - ⚠️ **Regra crítica:** nunca criar públicos no momento de subir campanhas
- Criar os públicos CRM 180 dias (Lead · Lead Qualificado · Consulta Agendada) e o
  Semelhante 1% da etapa mais qualificada — IT-8.1
- Carregar a lista de exclusão dos já convertidos
- Aplicar as regras inegociáveis — ver `checklists/setup-conta.md`
- Aplicar a nomenclatura padrão nos 3 níveis
- Configurar UTMs em todos os anúncios, sem exceção

### Bloco 4 — Setup Google Ads

- Campanhas separadas **Corporal** e **Facial**
  - Grupo de Termos Genéricos/Institucionais obrigatório em ambas
  - Grupos por procedimento realmente operado
  - Técnica exclusiva (Lipo HD, R24R, Cicatriz Mínima) → grupo próprio + LP específica
- Negativar palavras **antes** de subir (grátis, SUS, fotos bizarras)
- Correspondência apenas Frase ou Exata — proibida Ampla
- Rede de Display desmarcada em campanhas de Pesquisa
- 3 RSAs por grupo, 15 títulos + 5 descrições cada
- Extensões completas: 4+ sitelinks, frases de destaque, snippets, 3–5 imagens, chamada, GMN
  - 🚫 Proibido em imagens: antes/depois com exposição de pele, cicatriz aberta, centro cirúrgico
- Conta: Maximizar Conversões · conversão = WhatsApp/formulário · raio real da clínica ·
  upload da lista de clientes antigos · interesses em Observação
- UTMs no nível de conta + nos sitelinks e extensões (especialmente o link do WhatsApp)

### Bloco 5 — Rastreamento (GTM + GA4)

- Importar o container modelo Stark (`Modelo de Contêiner1.1.json`) no GTM do cliente
- Preencher as 3 variáveis: `[GA4] - Tag` (G-) · `[FB] - Pixel ID` · `[GG] - Tag ID` (AW-)
- Publicar o container e testar com o Google Tag Assistant
- GA4: vincular ao Google Ads · ativar Google Signals · marcar `generate_lead` como conversão
- Prova de atribuição para reuniões: GA4 › Publicidade › Atribuição › Caminhos de Conversão

### Bloco 6 — Reportei e acompanhamento

- Criar o cliente no Reportei e conectar Meta Ads, Google Ads e Instagram
  - Conectar cedo é crítico: sem histórico mínimo, a Reunião de Resultados sofre
- Configurar a planilha de acompanhamento semanal (Planilha Master)
- Garantir a pasta do cliente no Google Drive

### Bloco 7 — Estrutura de campanhas, subida e conferência final

Orçamento não define o método — define **quanto** do método se executa simultaneamente.

| Verba | TOFU | MOFU | BOFU |
|---|---|---|---|
| Até R$ 2.500 | CBO se pouco conteúdo; ABO se tiver. 1 público por teste | 1 conjunto único misto | 1 campanha (engaj. 365 + 180) |
| Até R$ 3.000 | ABO teste (sempre ativo) + CBO escala (60–70% da verba) | 3 conjuntos separados | 2 campanhas (teste + escala) |
| Acima de R$ 3.500 | Estrutura completa com separação total | Avançado com lookalikes | Campanhas por procedimento |

**TOFU — Atrair.** CpS benchmark R$ 1,50–2,59.
- Cenário A (conta zerada): CBO, 3 públicos abertos (Luxo + Profissões), subir todos os
  materiais, testar vencedores em ABO, mover para CBO definitivo
- Cenário B (conteúdo validado): ABO, 1 criativo por conjunto, ~R$ 6/conjunto, teste de
  7 dias, 2–3 vencedores para CBO de escala

**MOFU — Educar.** CTR mínimo 1,5%. Três conjuntos por tipo de conteúdo: antes e depois ·
depoimentos · quebra-objeções. Verba baixa → conjunto único e rotação por saturação.

**BOFU — Converter.** CPL R$ 7–12. Sempre teste + escala. Seguidores em BOFU apenas nos
primeiros 30 dias (fadiga de frequência). Verba maior → separar por procedimento.

**Criativos de onboarding:** subir classificados por nível de consciência P0–P5 —
ver `data/padroes-stark.md`.

**Fechamento:**
- Registrar todas as configurações no dossiê do cliente
- Documentar as pendências de acesso
- Conferência final com o Coordenador de Tráfego
- Marcar a tarefa de onboarding como concluída no ClickUp

---

### Output Format
```markdown
# Briefing de Onboarding — [Nome do Cliente]
**Data:** [data]  ·  **Gestor:** [nome]  ·  **Coordenador:** [nome]

## Ativos Meta (R1–R6)
| Req | Status | Observação |
|---|---|---|
| R1 Página FB | ✅ / ❌ | |
| R2 Instagram | ✅ / ❌ | |
| R3 WABA | ✅ / ❌ | |
| R4 Conta de Anúncios | ✅ / ❌ | |
| R5 Verificação | Verificado / Em análise | |
| R6 Sem restrição | ✅ / ❌ | |

## Dados da Conta
- Conta Meta Ads: [ID]  ·  Google Ads: [ID]  ·  GA4: [G-]  ·  GTM: [GTM-]
- Procedimentos reais: [lista]
- Objetivo: [leads WPP / Direct / Form / Agendamento]
- Orçamento mensal: R$ [valor]  ·  CPL meta: R$ [valor]
- Fase: [conta zerada / com histórico]

## Diagnóstico
- Conteúdo gravado: [n peças]
- Base: [orgânica / comprada]  ·  Já vendeu: [sim / não]
- Listas exportáveis: [leads / CRM / nenhuma]
- Histórico (3 meses): CPL macro R$ [valor], melhores públicos [lista],
  melhores criativos [lista]
- 3 ações ainda não testadas: [1] [2] [3]

## Rastreamento
- Pixel: [instalado / pendente]  ·  API Conversões: [ok / pendente]
- Medição Agregada de Eventos: [ok / pendente]
- GTM: [publicado e testado / pendente]  ·  Google Signals: [ativo / pendente]
- `generate_lead` como conversão: [ok / pendente]

## Concorrência
| Concorrente | Formato dominante | Oferta / LP | Observação |
|---|---|---|---|

## Estrutura Subida
- Faixa de verba: [até 2.500 / até 3.000 / acima de 3.500]
- TOFU: [CBO/ABO, públicos, verba]
- MOFU: [conjuntos, verba]
- BOFU: [teste + escala, públicos, verba]
- Criativos por nível de consciência: [P0-P1: n] [P2-P3: n] [P4-P5: n]

## Pendências de Acesso
| Pendência | Bloqueia o quê | Responsável | Prazo |
|---|---|---|---|

## Próximos Passos
1. [Ação]
2. [Ação]
```

### Veto Conditions
- Ativo Meta com restrição ativa (R6 falso) → **VETO**, não avançar
- Iniciar campanhas sem Pixel instalado e disparando → **VETO**
- Subir Google Ads sem palavras negativas configuradas → **VETO**
- Rede de Display marcada em campanha de Pesquisa → **VETO**
- Correspondência Ampla no Google Ads → **VETO**
- Campanha mistura CORPO + FACE → **VETO**
- Anunciar procedimento que o médico não opera → **VETO**
- Iniciar BOFU sem público quente mínimo de 1.000 pessoas → **VETO**
- Definir CPL meta acima de R$ 20 sem justificativa de nicho → **ALERTA**
- Verificação da empresa "Em análise" há mais de 7 dias úteis → **ALERTA**, acionar Tecnologia

### Exceções
| Situação | Como resolver |
|---|---|
| Acessos parciais | Configurar o possível e marcar pendências — a atividade é condicional |
| Verificação "Em análise" | Segue em paralelo; encerramento exige status Verificado |
| Opção de verificação não aparece | Forçar criando um aplicativo dentro da BM (Configurações › Apps) |
| Instagram não aparece na BM | Conta deve ser Profissional/Comercial e vinculada à Página |
| Pixel não aparece como fonte de público | Conectar o Pixel à Conta de Anúncios (volta a IT-7.1) |
| Público CRM vazio | Esperado até a 1ª execução real do funil; checar automações Publicadas |
| UTM não aparece no card do contato | Confirmar parâmetros completos e aguardar o próximo clique |
| Cliente sem conteúdo validado | Cenário A do TOFU: subir tudo em CBO, validar vencedores em ABO |

### Escalonamento — Escadinha Stark
| Situação | Quem resolve | Papel do outro |
|---|---|---|
| Dúvida sobre segmentação ou criativo | Coordenador | Fica ciente via planilha de validados |
| Conta bloqueada ou erro de pixel | Coordenador | Fica ciente se houver impacto no faturamento |
| Conflito leve / dúvida técnica do cliente | Coordenador | Monitora NPS e retenção |
| Crise grave / ameaça de cancelamento | Head | Recebe o histórico completo do coordenador |

### Completion Criteria
Todos os itens de `checklists/onboarding-gestor-trafego.md` aprovados, mais:
- Briefing documentado com todos os campos preenchidos
- Configurações registradas no dossiê e pendências documentadas
- Conferência final com o Coordenador realizada
- Próximos passos comunicados ao @media-buyer
