# Padrões Stark — Públicos, Nomenclatura, UTMs e Criativos

Referência única para o setup de conta. **Fonte:** Playbook de Onboarding — Gestor de
Tráfego Stark v1.0 (abr/2026) · IT-8.1 (POP-OPR-013).

---

## 1. Públicos Padrão Stark (Meta Ads)

> ⚠️ **Regra crítica:** NUNCA criar públicos no momento de subir campanhas. Reservar
> tempo dedicado para criar todas as segmentações e retargeting antes.

### Listas de clientes (4)
- `[LC] Lista Completa (Operados)`
- `[LC] Lista Completa (Agendados)`
- `[LC] Lista Completa (MQL)`
- `[LC] Lista Completa (Outros)`

### Engajamento Facebook (8)
- `FB - Engagement [ALL]` — 365D / 180D / 90D / 60D / 30D / 14D / 7D / 2D

### Engajamento Instagram
- `IG - Engagement [ALL]` — 365D / 180D / 90D / 60D / 30D / 14D / 7D / 2D
- `IG - FOLLOWERS`
- `IG - Saved Post` — 365D / 180D / 90D / 60D / 30D / 14D / 7D / 2D
- `IG - Sent Message` — 365D / 180D / 90D / 60D / 30D / 14D / 7D / 2D

### Tráfego do site (6)
- `[SITE] Todos os Visitantes` — 7D / 15D / 30D / 60D / 90D / 180D

### Visualização de vídeo
- `[VV] Video View 75%` — 365D / 180D / 90D / 60D / 30D
- `[VV] Video View 50%` — 30D
- `[VV] Video View/Thruplay 95%` — 365D
- `[VV] Video View 95%` — 180D / 90D / 60D / 30D

### Lookalikes
- `LAL 1%` — Semelhança 1% Brasil
  - Fonte: lista de leads · Alternativa: IG Engagement 365D

### Interesses
- `INT - LUXO + PROFISSÕES`
- `INT - LUXO + PROFISSÕES (DERMATOLOGIA)`

### Exclusão
- Upload da lista de contatos já convertidos (e-mail/telefone) como Custom Audience de exclusão

### Públicos CRM (IT-8.1)
`Gerenciador de Anúncios › Públicos › Criar Público Personalizado › Site`

| Público | Evento | Retenção |
|---|---|---|
| `Leads CRM 180 dias` | `Lead` | 180 dias |
| `Lead Qualificado CRM 180 dias` | `CompleteRegistration` | 180 dias |
| `Consulta Agendada CRM 180 dias` | `Purchase` | 180 dias |

- Fonte: **Pixel do cliente** — precisa estar conectado à Conta de Anúncios, senão não
  aparece na lista
- Descrição de uma linha por público (ex.: "Leads criados no CRM nos últimos 180 dias")
- Criar o **Semelhante 1%** a partir da etapa mais qualificada (Consulta Agendada) —
  criar agora e deixar popular, mesmo sem volume imediato
- Público novo mostrando "sem eventos recebidos" é **esperado** até a 1ª execução real
  do funil. Não refazer.

> ⚠️ Nunca expor ao cliente o uso de listas internas da agência. A inteligência é interna.

---

## 2. Nomenclatura Padrão de Campanhas

Obrigatória em toda conta Stark, nos 3 níveis, para manter rastreabilidade e facilitar
análises. **Fonte:** Estrutura Padrão — Nomenclatura das Contas.

### 2.1 Nível de campanha

**Objetivo:** identificar a etapa da estratégia, o que está sendo promovido e a fase.

```
[FUNIL][OBJETIVO][PRODUTO/EXPERT][TIPO][ORÇAMENTO][ADV]
```

| Campo | Descrição | Valores |
|---|---|---|
| `[FUNIL]` | Etapa da estratégia | TOFU (topo) · MOFU (meio) · BOFU (fundo) |
| `[OBJETIVO]` | Objetivo otimizado no Meta | Tráfego · Leads · Vendas · Engajamento · Alcance · LEAD-FORMULARIO · LEAD-RESPONDI |
| `[PRODUTO/EXPERT]` | O que está sendo promovido | DrIngrid · R24R · Botox · Lipo · Mama · Abdômen · Mommy · SEGUIDORES · FORMULÁRIO-META · FORMULÁRIO-RESPONDI · WHATSAPP · WHATS |
| `[TIPO]` | Fase da campanha | `[TESTE]` · `[ESCALA]` |
| `[ORÇAMENTO]` | Onde fica o orçamento | ABO (por conjunto) · CBO (por campanha) |
| `[ADV]` | Público Advantage | `[ADV]` quando a campanha usa público Advantage |

**Exemplos:**
- `[TOFU][Tráfego][SEGUIDORES][TESTE][ABO][ADV]`
- `[BOFU][Engajamento][WPP][R24R][ESCALA][CBO][ADV]`
- `[MOFU][Tráfego][Rejuvenescimento][ESCALA][CBO][ADV]`

### 2.2 Nível de conjunto de anúncios (Ad Set)

**Objetivo:** organizar a hierarquia de públicos, geolocalização e posicionamento.

```
[PÚBLICO][CONVERSÃO][GEO]
```

| Campo | Descrição | Valores |
|---|---|---|
| `[PÚBLICO]` | Nome descritivo da audiência | Aberto Mulheres · Int. Beleza · Envolvimento 30D · LAL Lista Clientes · Luxo |
| `[CONVERSÃO]` | Local da conversão | SITE · WPP · Formulário - Meta · Seguidores · Perfil IG · Formulário - Respondi |
| `[GEO]` | Localização geográfica | BR · SP · RJ · Raio 10km · Mix cidades · bairros nobres |

**Exemplos:**
- `[Aberto Mulheres 25-55_WPP_BR]`
- `[Int. Cirurgia Plástica_SITE_SP]`
- `[RMKT Envolvimento 90D_WHATS_IG_BR]`

### 2.3 Nível de anúncio (Ad)

**Objetivo:** identificar o criativo, a variação e a data de upload, para controle de
validade e fadiga.

```
[DATA][NOME DO CRIATIVO][FORMATO][VARIAÇÃO][TIPO]
```

| Campo | Descrição | Valores |
|---|---|---|
| `[DATA]` | Data de subida do anúncio | 16.jan · jan26 · 16.01 |
| `[NOME]` | Identificação visual rápida | Ingrid Espelho · Felipe Box · Antes e Depois — ou o início da legenda do post |
| `[FORMATO]` | Tipo de mídia | IMG (imagem) · VID (vídeo) · CAR (carrossel) |
| `[VARIAÇÃO]` | Teste A/B (opcional) | Copy A · Copy B · Capa 1 · Capa 2 · Ad1 · V1 · V2 |
| `[TIPO]` | Posicionamento do post | Feed · Dark post |

**Exemplos:**
- `[16.01_AnteseDepois_IMG_V1_Feed]`
- `[16.01_Depoimento_VID_V1_Feed]`
- `[16.01_AnteseDepois_CAR_V1_Feed]`
- `[25.02_A flacidez facial não aparece_CAR_Feed]`

### 2.4 Glossário de abreviações

Para manter a consistência, toda a equipe deve usar as mesmas siglas.

| Sigla | Significado |
|---|---|
| LAL 1% | Lookalike 1% (Semelhante) |
| RMKT | Remarketing — público que já interagiu |
| WHATS | WhatsApp |
| DIRECT | Mensagem no Instagram |
| IG | Instagram |
| FB | Facebook |
| CBO | Campaign Budget Optimization — orçamento na campanha |
| ABO | Ad Set Budget Optimization — orçamento no conjunto |
| AUTO | Posicionamento automático |
| ADV | Advantage (Andrômeda) |

### 2.5 Exemplo de estrutura completa

```
Campanha: [TOFU][Tráfego][Perfil Ingrid][TESTE][ABO]
├── Conjunto: [Aberto Mulheres 25-55_BR]
│   ├── Anúncio: [16.01_AnteseDepois_IMG_V1_Feed]
│   └── Anúncio: [16.01_Depoimento_VID_V1_Feed]
└── Conjunto: [Int. Cirurgia Plástica_SP]
    └── Anúncio: [25.02_A flacidez facial não aparece_CAR_Feed]
```

### 2.6 Pontos em aberto

Divergências entre o documento de nomenclatura e o Playbook, a resolver com a Coordenação:

1. **`[ADV]` × regra inegociável.** O documento de nomenclatura prevê a tag `[ADV]` para
   campanhas com público Advantage, mas o Playbook (§3.3) e o `checklists/setup-conta.md`
   determinam Advantage+ Audience **desativado**. Definir em que casos o Advantage é
   permitido — ou a tag não deve ser usada.
2. **Campo `[DATA]` no nível de campanha.** O cabeçalho do documento lista
   `[FUNIL][OBJETIVO][PRODUTO/EXPERT][TIPO][DATA]`, mas a tabela de campos e os exemplos
   usam `[ORÇAMENTO]` e `[ADV]`, sem `[DATA]`. Adotada aqui a versão da tabela e dos
   exemplos.
3. **`VD` × `VID`.** Um dos exemplos do documento usa `VD` para vídeo; a tabela de campos
   define `VID`. Padronizado aqui como `VID`.

---

## 3. UTMs

### Meta Ads
Campo **Parâmetros de URL** do anúncio. Obrigatório em todos os anúncios, sem exceção.

```
utm_source=meta&utm_medium=cpc&utm_campaign={{campaign.name}}&utm_term={{adset.name}}&utm_content={{ad.name}}
```

| Parâmetro | Valor | Descrição |
|---|---|---|
| `utm_source` | `meta` | Identifica Meta Ads como origem |
| `utm_medium` | `cpc` | Tráfego pago por clique (fixo) |
| `utm_campaign` | `{{campaign.name}}` | Preenchido automaticamente pelo Meta |
| `utm_term` | `{{adset.name}}` | Nome do conjunto de anúncios |
| `utm_content` | `{{ad.name}}` | Nome do anúncio/criativo |

⚠️ Não colocar `?` no início — o Meta adiciona automaticamente.

### Google Ads
Nível de conta: `Configurações › Rastreamento › Modelo de Acompanhamento`.
Inserir também em todos os Sitelinks e Extensões, especialmente no link do WhatsApp.

```
{lpurl}?utm_source=google&utm_medium=cpc&utm_campaign={campaignid}&utm_content={creative}&utm_term={keyword}
```

**Validação:** as UTMs devem aparecer na aba **Contatos** do CRM — o 1º e o último clique
ficam no card do contato (atribuição). Se não aparecer, confirmar os parâmetros no
criativo e aguardar o próximo clique.

---

## 4. Framework de Consciência (Eugene Schwartz)

Todo criativo subido no onboarding deve ser classificado por nível.

| Nível | Descrição | Funil | Exemplo de CTA |
|---|---|---|---|
| P0 — Inconsciente | Sente a dor mas não nomeou | TOFU | Compartilhe com uma amiga |
| P1 — Ciente do Problema | Sabe que tem o problema | TOFU | Siga para mais conteúdo |
| P2 — Ciente da Solução | Sabe que existem soluções | MOFU | Comente FACE |
| P3 — Ciente do Produto | Já conhece o médico/clínica | MOFU/BOFU | Fale comigo no Direct |
| P4–P5 — Totalmente Ciente | Já decidiu, precisa do empurrão | BOFU | Agende sua consulta |

---

## 5. Sistema AROS (DNA do Médico)

Antes de aplicar qualquer template de criativo, construir o DNA do médico:

- **Personalidade (A):** trajetória, valores, estilo de comunicação, filosofia de cuidado
- **Público (R):** personas, dores, desejos, objeções, nível de consciência dominante
- **Produto/Serviço (O):** procedimentos, UVP, Método Único, diferenciais técnicos

## 6. Clusters de Clientes (ICPs)

| Cluster | Perfil | Procedimentos | Sofisticação |
|---|---|---|---|
| 1 | Cirurgião facial em capital | Lifting, Blefaro, Mento, Facelift, Rino | Nível 4–5 (saturado) |
| 2 | Cirurgião corporal em capital | Masto, Abdômino, Lipo, Mommy, Implantes | Nível 3–5 (variável) |
| 3 | Cirurgião corporal em cidade menor | Mesmos do Cluster 2 | Nível 2–4 (menos saturado) |

## 7. Produção Semanal de Conteúdo

- **Linha de Criação:** 5 peças novas por semana (inovação e volume)
- **Linha de Otimização:** 5 variações de hooks, ritmo, cenário, CTA (escalar vencedores)
- **Planejamento semanal:** 3 peças no mesmo tema — 1 Carousel · 1 formato variável
  (estático/reels/stories) · 1 Reels
- Sempre misturar estágios do funil (TOFU + MOFU + BOFU) na mesma semana, com CTAs ajustados

---

## 8. Funil Stark — 7 Estágios

| Estágio | Descrição | Sinal de progressão |
|---|---|---|
| 1. Visitante (TOFU) | Primeiro contato via ads/posts | % de vídeo assistido, cliques no perfil |
| 2. Base Social | Começou a seguir e interagir | Frequência de interações crescente |
| 3. Lead | Forneceu dados de contato | Iniciou conversa no WhatsApp, preencheu form |
| 4. MQL | Lead qualificado pelo marketing | — |
| 5. SAL | Aceito pelo comercial como válido | Contato válido, interesse confirmado |
| 6. SQL | Em negociação ativa | Reservando data, discutindo fechamento |
| 7. Cliente | Completou a compra | Consulta agendada e paga |
