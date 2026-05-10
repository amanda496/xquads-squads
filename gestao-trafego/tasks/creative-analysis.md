# creative-analysis

## Task: Análise de Criativos — Performance e Decisão de Pausa ou Escala

### Metadata
- **executor:** analytics-analyst
- **elicit:** true
- **mode:** sequential
- **output:** ranking de criativos + decisão recomendada por anúncio

### Inputs Required
```
cliente: Nome do cliente
periodo: 7D (mínimo para análise de criativo)
lista_anuncios: Lista de anúncios ativos com métricas
cpl_meta: CPL alvo do cliente
```

### Elicitation
```
Qual o cliente e período de análise?
> [cliente, período]

Qual o CPL meta?
> [valor]

Quais anúncios devem ser analisados? (todos os ativos ou seleção?)
> [todos / lista específica]
```

### Execution Steps

#### Step 1: Coletar Métricas por Anúncio
Para cada anúncio, coletar:
- Gasto no período
- Impressões
- CTR (taxa de clique)
- CPM
- Leads / Resultados
- CPL
- Frequência

#### Step 2: Ranking por CTR
Ordenar anúncios por CTR (maior para menor):

| Posição | Anúncio | CTR | CPL | Gasto | Classificação |
|---------|---------|-----|-----|-------|---------------|
| 1 | [nome] | [%] | R$[val] | R$[val] | ALTO POTENCIAL |
| 2 | [nome] | [%] | R$[val] | R$[val] | NORMAL |
| N | [nome] | [%] | R$[val] | R$[val] | CANDIDATO PAUSA |

**Referências de CTR (feed):**
- > 2,0% → Alto potencial — priorizar verba
- 1,0% – 2,0% → Normal — manter
- 0,8% – 1,0% → Atenção — monitorar
- < 0,8% → Candidato à pausa

#### Step 3: Identificar Criativo Dominante
- Algum criativo consumindo >80% do orçamento do conjunto?
  - **Se CPL bom:** manter + criar variações do mesmo criativo
  - **Se CPL ruim:** pausar + redistribuir verba para os demais

#### Step 4: Análise de Fadiga
- Frequência > 3.0 por criativo? → Fadiga confirmada
  - Sintomas: CTR caindo semana a semana com CPM subindo
  - Ação: pausar e substituir por novo criativo

#### Step 5: Classificação Final por Anúncio
Para cada anúncio, definir:

| Classificação | Critério | Ação |
|--------------|----------|------|
| ESCALAR | CTR >2% + CPL ≤ meta | Aumentar verba ou criar variações |
| MANTER | CTR 1-2% + CPL dentro da meta | Manter como está |
| MONITORAR | CTR 0,8-1% ou CPL próximo do alerta | Dar mais 48-72h |
| PAUSAR | CTR <0,8% por 3+ dias ou CPL >alerta por 3+ dias | Pausar |

#### Step 6: Recomendações de Novos Criativos
Se há criativos com baixa performance ou fadiga, recomendar:
- Tipo de conteúdo que está funcionando (depoimento / antes-depois / educativo)
- Formato que está performando melhor (Reels / Feed / Stories)
- Público que mais converte (faixa etária, posicionamento)

### Output Format
```
ANÁLISE DE CRIATIVOS — [Nome do Cliente]
Período: [período] | Data: [data]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

RANKING DE CRIATIVOS (por CTR):

1. [Nome Anúncio]
   CTR: [%] 🔥 | CPL: R$[val] ✅ | Gasto: R$[val] | Freq: [N]
   → ESCALAR — criar variações V2 e V3

2. [Nome Anúncio]
   CTR: [%] | CPL: R$[val] ✅ | Gasto: R$[val] | Freq: [N]
   → MANTER

3. [Nome Anúncio]
   CTR: [%] ⚠️ | CPL: R$[val] ❌ | Gasto: R$[val] | Freq: [N]
   → PAUSAR — CPL ruim por [N] dias consecutivos

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
CRIATIVO DOMINANTE: [nome] — [%] da verba
  Status: [CPL bom — manter / CPL ruim — pausar]

FADIGA DETECTADA: [sim — [nome] freq=[N] / não]

TIPO QUE MELHOR PERFORMA: [Depoimento / Antes-Depois / Educativo]
FORMATO QUE MELHOR PERFORMA: [Reels / Feed / Stories]

RECOMENDAÇÃO NOVOS CRIATIVOS:
  → Criar [N] variações de [tipo] em formato [formato]
  → Focar em: [tema/ângulo que está funcionando]

Encaminhar decisões ao @traffic-chief: *scale-or-kill
```

### Veto Conditions
- Recomendar pausa com < 3 dias de dado → VETO
- Classificar CTR sem verificar dado mínimo de impressões → incompleto
- Análise de criativo sem verificar frequência → incompleto
- Pausa de criativo dominante com CPL bom → VETO

### Completion Criteria
- Ranking de criativos por CTR gerado
- Classificação ESCALAR/MANTER/MONITORAR/PAUSAR para cada anúncio
- Criativo dominante identificado e avaliado
- Fadiga verificada (frequência)
- Recomendação de novos criativos quando necessário
- Análise entregue ao @traffic-chief para decisão
