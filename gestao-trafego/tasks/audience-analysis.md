# audience-analysis

## Task: Análise de Público — Performance por Segmentação e Decisão de Otimização

### Metadata
- **executor:** analytics-analyst
- **elicit:** true
- **mode:** sequential
- **output:** ranking de públicos + recomendações de otimização de segmentação

### Inputs Required
```
cliente: Nome do cliente
periodo: 7D mínimo
conjuntos_ativos: Lista de conjuntos de anúncios por público
cpl_meta: CPL alvo do cliente
breakdown_disponivel: idade, posicionamento, região (quais estão disponíveis)
```

### Elicitation
```
Qual o cliente e o período de análise?
> [cliente e período]

Quais conjuntos de anúncios (públicos) serão analisados?
> [todos os ativos ou seleção]

Qual o CPL meta?
> [valor]
```

### Execution Steps

#### Step 1: Performance por Conjunto (Público)
Para cada conjunto, coletar:
- Gasto no período
- Alcance e frequência
- CTR
- CPM
- Leads
- CPL
- Classificação: BOM / MÉDIO / RUIM vs meta

#### Step 2: Análise por Faixa Etária
Breakdown de desempenho por idade:

| Faixa Etária | CPL | CTR | Gasto | % do Total |
|-------------|-----|-----|-------|------------|
| 25-34 | R$[val] | [%] | R$[val] | [%] |
| 35-44 | R$[val] | [%] | R$[val] | [%] |
| 45-55 | R$[val] | [%] | R$[val] | [%] |

Identificar: qual faixa etária tem melhor CPL? Qual tem pior?

**Recomendação possível:**
- Se 45-55 tem CPL muito acima da média → considerar ajustar limite superior
- Se 25-34 não converte → verificar se público está adequado ao procedimento

#### Step 3: Análise por Posicionamento
Breakdown por onde o anúncio está aparecendo:

| Posicionamento | CPL | CTR | Impressões | % do Gasto |
|----------------|-----|-----|------------|------------|
| Feed Instagram | R$[val] | [%] | [N] | [%] |
| Stories Instagram | R$[val] | [%] | [N] | [%] |
| Feed Facebook | R$[val] | [%] | [N] | [%] |
| Stories Facebook | R$[val] | [%] | [N] | [%] |

Identificar: qual posicionamento converte melhor?

**Nota:** Não remover posicionamentos individualmente — isso viola o método Stark (posicionamento manual completo). Usar para otimização de criativos por formato.

#### Step 4: Análise por Região (se relevante)
Se campanha é multi-região:

| Região | CPL | Leads | Gasto | % do Total |
|--------|-----|-------|-------|------------|
| [cidade 1] | R$[val] | [N] | R$[val] | [%] |
| [cidade 2] | R$[val] | [N] | R$[val] | [%] |

Identificar: há região com CPL fora do padrão?

#### Step 5: Análise de Sobreposição de Público (se CBO)
Em campanhas CBO com múltiplos conjuntos:
- Verificar se apenas 1 conjunto está recebendo verba
- Identificar qual público o algoritmo está priorizando e por quê
- Se 1 conjunto está consumindo >80% → avaliar se o público do conjunto favorecido é realmente o melhor

#### Step 6: Classificação e Recomendações
Para cada conjunto/público:

| Conjunto | CPL | Classificação | Recomendação |
|----------|-----|---------------|--------------|
| [nome] | R$[val] | BOM | Manter / Escalar |
| [nome] | R$[val] | MÉDIO | Monitorar 48h |
| [nome] | R$[val] | RUIM | Reduzir / Pausar |

**Recomendações de segmentação:**
- Expandir público que está funcionando?
- Criar novo LAL baseado no público com melhor CPL?
- Criar público de exclusão para segmentação mais precisa?

### Output Format
```
ANÁLISE DE PÚBLICO — [Nome do Cliente]
Período: [período] | Data: [data]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PERFORMANCE POR CONJUNTO (PÚBLICO):
┌─ [Nome Conjunto 1] — [Tipo de Público]
│  CPL: R$[val] [BOM/MÉDIO/RUIM] | CTR: [%] | Freq: [N]
│  Gasto: R$[val] | Leads: [N]
│  → MANTER / ESCALAR / PAUSAR

├─ [Nome Conjunto 2] — [Tipo de Público]
│  CPL: R$[val] [BOM/MÉDIO/RUIM] | CTR: [%] | Freq: [N]
│  → MANTER / PAUSAR

ANÁLISE POR FAIXA ETÁRIA:
  Melhor performance: [faixa] → CPL R$[val]
  Pior performance: [faixa] → CPL R$[val]
  Insight: [observação relevante]

ANÁLISE POR POSICIONAMENTO:
  Melhor: [posicionamento] → CTR [%]
  Pior: [posicionamento] → CTR [%]
  Insight: [criativo recomendado por formato]

ANÁLISE REGIONAL (se multi-região):
  Destaque positivo: [região] → CPL R$[val]
  Atenção: [região] → CPL R$[val]

SOBREPOSIÇÃO CBO (se aplicável):
  Conjunto dominante: [nome] — [%] da verba
  → [avaliar manutenção ou diversificação]

RECOMENDAÇÕES:
  1. [ação de público]
  2. [ação de segmentação]
  3. [nova audiência sugerida se necessário]

Encaminhar ao @traffic-chief: *scale-or-kill
```

### Veto Conditions
- Analisar público com < 3 dias de dado → VETO
- Remover posicionamento individual (quebra o método Stark) → VETO
- Reduzir faixa etária abaixo de 25 anos → VETO
- Expandir faixa etária acima de 55 anos sem justificativa → ALERTA

### Completion Criteria
- Performance por conjunto analisada com classificação
- Breakdown por faixa etária (25-34, 35-44, 45-55) realizado
- Breakdown por posicionamento realizado
- Análise regional realizada (se campanha multi-região)
- Sobreposição CBO verificada (se CBO)
- Recomendações de segmentação geradas
- Análise entregue ao @traffic-chief para decisão
