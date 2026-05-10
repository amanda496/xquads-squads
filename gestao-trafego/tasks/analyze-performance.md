# analyze-performance

## Task: Análise de Performance — Diagnóstico Stark Multi-Período

### Metadata
- **executor:** analytics-analyst
- **elicit:** true
- **mode:** sequential
- **output:** diagnóstico com classificação BOM/MÉDIO/RUIM e recomendação

### Inputs Required
```
cliente: Nome do cliente
periodo_analise: 7D | 4D | 3D | Ontem | Hoje
campanhas: Lista de campanhas e conjuntos a analisar
cpl_meta: CPL alvo do cliente
dados_meta_ads: Métricas exportadas do Gerenciador (ou acesso via MCP)
```

### Elicitation
```
Qual o cliente e o período de análise?
> [cliente e período]

Qual o CPL meta do cliente?
> [valor em R$]

Quais campanhas/conjuntos devem ser analisados?
> [todas ou lista específica]
```

### Execution Steps

#### Step 1: Coletar Métricas Brutas
Para cada campanha/conjunto, coletar:
- Gasto total no período
- Impressões e Alcance
- Cliques (todos) e CTR
- CPM (Custo por 1.000 impressões)
- Leads gerados (ou mensagens iniciadas)
- CPL (Custo por Lead/Resultado)
- Frequência

#### Step 2: Análise Multi-Período (Framework Stark)
Coletar dados em 5 janelas temporais e comparar:

| Janela | Dados | Tendência |
|--------|-------|-----------|
| 7D | CPL base | [valor] |
| 4D | CPL recente | [valor] → [↑↓=] vs 7D |
| 3D | CPL próximo | [valor] → [↑↓=] vs 4D |
| Ontem | CPL último dia | [valor] → [↑↓=] vs 3D |
| Hoje | CPL atual | [valor parcial] |

Identificar padrão de tendência:
- **Melhora consistente:** 7D>4D>3D>Ontem → tendência positiva
- **Piora consistente:** 7D<4D<3D<Ontem → ação necessária
- **Estabilidade:** variação < 10% entre janelas → manter
- **Ruído:** padrão sem lógica → aguardar mais dados

#### Step 3: Classificação por CPL Meta
Para cada campanha/conjunto:
- **ÓTIMO:** CPL < CPL meta do cliente
- **BOM:** CPL = CPL meta (±10%)
- **MÉDIO:** CPL entre meta e alerta
- **RUIM:** CPL > alerta (ex: >R$15 se meta é R$12)

#### Step 4: Decomposição de Gargalo (CPL = CPM × CTR × Conversão)
Se CPL ruim, identificar onde está o problema:

| Problema | Sintoma | Causa |
|----------|---------|-------|
| CPM alto | CPM > R$40 sem escala recente | Público muito pequeno ou esgotado |
| CTR baixo | CTR < 1,0% | Criativo fraco ou público errado |
| Conversão baixa | Cliques mas sem leads | Landing page, CTA fraco, oferta |

**Regra:**
- CPM alto = problema de **público**
- CTR baixo = problema de **criativo**
- Conversão baixa = problema de **oferta/página**

#### Step 5: Verificar Dado Mínimo
Antes de qualquer recomendação:
- Gasto ≥ 2x CPL meta? (ex: meta R$12 → mínimo R$24 gastos)
- Mínimo 3 dias rodando?
- Se não → informar: "dado insuficiente, aguardar"

### Output Format
```
ANÁLISE DE PERFORMANCE — [Nome do Cliente]
Período: [período] | Data: [data]
CPL Meta: R$ [valor]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CAMPANHA: [nome]
├── Gasto: R$ [valor] | Leads: [N] | CPL: R$ [valor]
├── CTR: [%] | CPM: R$ [valor] | Frequência: [N]
│
├── Multi-Período:
│   7D: R$[cpl] | 4D: R$[cpl] | 3D: R$[cpl] | Ontem: R$[cpl]
│   Tendência: [↑PIORANDO / ↓MELHORANDO / =ESTÁVEL]
│
├── Classificação: [ÓTIMO / BOM / MÉDIO / RUIM]
├── Gargalo: [PÚBLICO / CRIATIVO / OFERTA / sem gargalo]
└── Recomendação: [ESCALAR / MANTER / REDUZIR / PAUSAR]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
RESUMO EXECUTIVO:
[N] campanhas analisadas
[N] para escalar | [N] para manter | [N] para reduzir | [N] para pausar

Encaminhar decisão final ao @traffic-chief: *scale-or-kill
```

### Veto Conditions
- Analisar com gasto < 2x CPL meta → VETO (informar dado insuficiente)
- Recomendar ação sem tendência de pelo menos 3 dias → VETO
- Classificar sem comparar com CPL meta do cliente → VETO
- Diagnóstico sem decomposição de gargalo → incompleto

### Completion Criteria
- Métricas coletadas para todas as campanhas/conjuntos
- Análise multi-período (7D/4D/3D/Ontem) para cada item
- Classificação BOM/MÉDIO/RUIM baseada no CPL meta
- Gargalo identificado (CPM/CTR/Conversão) onde aplicável
- Recomendação de ação para cada item
- Relatório entregue ao @traffic-chief para decisão final
