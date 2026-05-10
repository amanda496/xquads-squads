# diagnose-campaign

## Task: Diagnóstico de Campanha — Identificar Gargalo e Causa Raiz

### Metadata
- **executor:** analytics-analyst
- **elicit:** true
- **mode:** sequential
- **output:** diagnóstico com gargalo identificado + hipótese + ação recomendada

### Inputs Required
```
cliente: Nome do cliente
campanha_problema: Nome da campanha ou conjunto com problema
cpl_atual: CPL atual observado
cpl_meta: CPL alvo do cliente
periodo: Quantos dias de dado disponível
sintoma_principal: O que está errado (CPL alto, poucos leads, CTR baixo, etc.)
```

### Elicitation
```
Qual campanha ou conjunto está com problema?
> [media-buyer informa]

Qual o sintoma principal observado?
> [CPL alto / poucos leads / CTR baixo / CPM alto / frequência alta / etc.]

Há quantos dias o problema persiste?
> [N dias]
```

### Execution Steps

#### Step 1: Verificar Dado Mínimo
- Campanha tem gasto ≥ 2x CPL meta? (se não → aguardar, não é problema ainda)
- Campanha rodou ≥ 3 dias? (se não → aguardar, pode ser fase de aprendizado)
- Se ambos OK → prosseguir com diagnóstico

#### Step 2: Identificar Gargalo pelo Framework CPL
**Fórmula:** `CPL = CPM ÷ (CTR × Taxa de Conversão)`

| Componente | Normal | Alerta | Diagnóstico |
|------------|--------|--------|-------------|
| CPM | R$15-35 | >R$45 | Problema de público |
| CTR | ≥1,5% | <1,0% | Problema de criativo |
| Conversão | ≥3% | <1% | Problema de oferta/página |

**Diagnóstico de gargalo:**
- CPM alto + CTR OK + Conversão OK → **Gargalo: PÚBLICO**
  - Público muito pequeno, esgotado ou competitivo
- CPM OK + CTR baixo + Conversão OK → **Gargalo: CRIATIVO**
  - Criativo não atrai atenção suficiente
- CPM OK + CTR OK + Conversão baixa → **Gargalo: OFERTA/PÁGINA**
  - Oferta não converte, página lenta ou CTA fraco
- Combinação de problemas → diagnosticar primário vs secundário

#### Step 3: Análise de Frequência
- Frequência > 3.0? → **Fadiga de criativo**
  - Público já viu o anúncio muitas vezes
  - Solução: novo criativo ou novo público
- Frequência < 1.5 com CPL alto? → Alcance insuficiente ou CPM muito alto

#### Step 4: Análise de Criativo Dominante
- Algum criativo consumindo >80% da verba?
  - Se CPL bom → manter e criar variações
  - Se CPL ruim → pausar e redistribuir verba

#### Step 5: Verificar Contexto Externo
- Houve mudança recente na campanha? (alteração de orçamento, criativo, público)
- Período sazonal (feriados, datas comemorativas) afetando CPM?
- Concorrentes aumentando investimento no mesmo público?

#### Step 6: Formular Hipótese e Ação
Com base no diagnóstico, formular:
- **Hipótese:** "O CPL está alto porque [gargalo] está [problema]"
- **Evidência:** métricas que sustentam a hipótese
- **Ação recomendada:** o que mudar para resolver
- **Como validar:** o que monitorar nas próximas 48-72h

### Output Format
```
DIAGNÓSTICO — [Nome do Cliente] | [Nome Campanha]
Data: [data] | Período analisado: [N] dias
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

SINTOMA: CPL = R$[atual] (meta: R$[meta]) — +[%]% acima da meta

DECOMPOSIÇÃO CPL:
  CPM: R$[valor] → [NORMAL / ALTO] (benchmark R$15-35)
  CTR: [%] → [NORMAL / BAIXO] (benchmark ≥1,5%)
  Conversão: [%] → [NORMAL / BAIXA] (benchmark ≥3%)

GARGALO IDENTIFICADO: [PÚBLICO / CRIATIVO / OFERTA/PÁGINA / MÚLTIPLOS]

FREQUÊNCIA: [valor] → [NORMAL / ALTA — possível fadiga]

CRIATIVO DOMINANTE: [sim — [nome] com [%] da verba / não]

CONTEXTO: [alterações recentes / sazonalidade / sem contexto relevante]

HIPÓTESE:
"O CPL está acima da meta porque [causa principal]. 
Evidência: [métrica específica]."

AÇÃO RECOMENDADA:
  1. [ação principal]
  2. [ação secundária se aplicável]

COMO VALIDAR:
  Monitorar [métrica] nas próximas [N]h
  Esperado: [resultado esperado se hipótese estiver correta]

ENCAMINHAR AO @traffic-chief: decisão de scale-or-kill
```

### Veto Conditions
- Diagnosticar com < 2x CPL meta em gasto → VETO (aguardar dado)
- Diagnosticar com < 3 dias de dado → VETO (pode ser aprendizado do algoritmo)
- Recomendar ação sem hipótese embasada em dado → VETO
- Recomendar pausa sem evidência de 3+ dias de CPL ruim → VETO

### Completion Criteria
- Dado mínimo verificado (gasto ≥ 2x CPL meta, ≥ 3 dias)
- Gargalo identificado via decomposição CPL (CPM/CTR/Conversão)
- Frequência verificada
- Hipótese formulada com evidência de dado
- Ação recomendada com critério de validação
- Diagnóstico entregue ao @traffic-chief para decisão
