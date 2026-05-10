# optimize-adset

## Task: Otimização de Conjunto de Anúncios — Ajustes Stark

### Metadata
- **executor:** media-buyer
- **elicit:** true
- **mode:** sequential
- **output:** log de alterações com timestamp

### Inputs Required
```
plano_acao: Lista de ações definidas pelo @traffic-chief no *scale-or-kill
cliente: Nome do cliente
data_analise: Data base da análise
```

### Elicitation
```
Qual o plano de ação aprovado pelo @traffic-chief?
> [lista de ações: escalar X, pausar Y, reduzir Z]

Confirmando: todas as ações têm dado suficiente (≥ 2x CPL meta e ≥ 3 dias)?
> [sim — prosseguir / não — retornar ao @traffic-chief]
```

### Execution Steps

#### Step 1: Receber e Confirmar Plano
- Ler lista de ações do @traffic-chief
- Confirmar que cada ação tem justificativa com dado específico
- Se qualquer ação sem dado → retornar ao @traffic-chief para revisão

#### Step 2: Executar Ações (uma por vez)
Para cada ação na lista:

**ESCALAR orçamento:**
- Verificar: incremento ≤ 30% do orçamento atual
- Verificar: última escala foi há ≥ 72 horas
- Aplicar novo valor no conjunto
- Registrar: [data/hora] ESCALA [conjunto] [valor anterior] → [valor novo] (+X%)

**PAUSAR conjunto/criativo:**
- Verificar: CPL ruim documentado por ≥ 3 dias
- Pausar o conjunto ou anúncio
- Registrar: [data/hora] PAUSA [conjunto/anúncio] CPL=[valor] Meta=[valor]

**REDUZIR orçamento:**
- Calcular redução de 20%
- Aplicar novo valor
- Registrar: [data/hora] REDUÇÃO [conjunto] [valor anterior] → [valor novo] (-20%)

**MANTER:**
- Documentar decisão
- Registrar: [data/hora] MANUTENÇÃO [conjunto] — CPL [situação] — monitorar 48h

#### Step 3: Log de Alterações
Documentar cada ação com:
- Data e hora exatas
- Conjunto/anúncio afetado
- Tipo de ação (ESCALA / PAUSA / REDUÇÃO / MANUTENÇÃO)
- Valores antes e depois
- Justificativa (CPL do período, dado base)

#### Step 4: Confirmar ao @traffic-chief
- Enviar log completo de alterações
- Indicar se alguma ação não pôde ser executada e o motivo

### Output Format
```
LOG DE ALTERAÇÕES — [Nome do Cliente]
Data: [data] | Hora início: [hora] | Hora fim: [hora]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[HH:MM] ESCALA | [Nome Conjunto] | R$150 → R$180/dia (+20%)
         Motivo: CPL 7D = R$8,50 (meta R$12) — BOM por 5 dias consecutivos

[HH:MM] PAUSA | [Nome Anúncio] | R$0/dia (pausado)
         Motivo: CPL 7D = R$19 (meta R$12) — RUIM por 4 dias | CTR=0,6%

[HH:MM] MANUTENÇÃO | [Nome Conjunto] | R$100/dia (sem alteração)
         Motivo: CPL 7D = R$11 — MÉDIO — aguardar mais 48h

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Total: [N] ações executadas | [N] escalas | [N] pausas | [N] manutenções

Confirmado ao @traffic-chief: ✅
```

### Veto Conditions
- Escalar mais de 30% de uma vez → VETO (retornar ao @traffic-chief)
- Pausar sem dado de 3+ dias → VETO
- Alterar campanha não listada no plano → VETO
- Executar ação sem registrar no log → VETO
- Fazer escalas com menos de 72h da última → VETO

### Completion Criteria
- Todas as ações do plano executadas (ou justificada impossibilidade)
- Log de alterações completo com timestamp por ação
- Confirmação enviada ao @traffic-chief
- Nenhuma ação fora do plano executada
