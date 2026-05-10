# weekly-report

## Task: Relatório Semanal de Performance — Formato Stark

### Metadata
- **executor:** analytics-analyst
- **elicit:** true
- **mode:** sequential
- **output:** relatorio-semanal.md completo + insights acionáveis

### Inputs Required
```
cliente: Nome do cliente
semana_referencia: Data início e fim (ex: 05/05 a 11/05/2025)
campanhas_ativas: Lista de campanhas ativas no período
cpl_meta: CPL alvo do cliente
dados_7d: Métricas dos últimos 7 dias por campanha/conjunto/criativo
```

### Elicitation
```
Qual o cliente e a semana de referência?
> [cliente e datas]

Quais campanhas estavam ativas nessa semana?
> [lista]

Qual o CPL meta do cliente?
> [valor]
```

### Execution Steps

#### Step 1: Coletar Dados Completos da Semana
Exportar do Gerenciador de Anúncios:
- Breakdown por campanha (7D)
- Breakdown por conjunto de anúncios (7D)
- Breakdown por anúncio/criativo (7D)
- Breakdown por idade (7D)
- Breakdown por posicionamento (7D)
- Breakdown por região (7D)

#### Step 2: Performance Geral da Semana
Calcular totais consolidados:
- Gasto total da semana
- Total de leads gerados
- CPL médio ponderado
- CPL vs meta: [%] acima/abaixo
- CTR médio
- CPM médio
- Frequência média

#### Step 3: Análise por Estágio de Funil
Para cada estágio ativo:
- **TOFU:** CpS (Custo por Seguidor) vs benchmark R$1,50
- **MOFU:** CTR vs benchmark 1,5%
- **BOFU:** CPL vs meta do cliente

#### Step 4: Análise por Criativo
Ranking de criativos por performance:
1. CPL por anúncio (do melhor ao pior)
2. CTR por anúncio
3. Identificar criativo dominante (>80% da verba?)
4. Identificar criativos com CTR < 0,8% (candidatos à pausa)
5. Identificar criativos com CTR > 2,0% (alto potencial)

#### Step 5: Análise Segmentada (4 Dimensões)
- **Por faixa etária:** qual age range tem melhor CPL?
- **Por posicionamento:** Feed vs Stories vs Reels — qual converte melhor?
- **Por região:** alguma cidade/estado com CPL fora do padrão?
- **Por conjunto:** qual público está entregando melhor resultado?

#### Step 6: Diagnóstico e Recomendações
Baseado nos dados, gerar recomendações acionáveis:
- O que manter (está funcionando)
- O que escalar (CPL bom por 7 dias)
- O que reduzir (CPL médio com tendência neutra)
- O que pausar (CPL ruim por 3+ dias)
- O que testar (novo criativo, novo público)

#### Step 7: Gerar Relatório
Usar template `templates/relatorio-semanal.md` para formatar o relatório final.

### Output Format
Relatório gerado no padrão do template `relatorio-semanal.md` com:
- Capa com cliente, semana e KPIs principais
- Performance por campanha com classificação
- Análise de criativos com ranking
- Análise segmentada (4 dimensões)
- Diagnóstico com gargalo identificado
- Plano de ação para próxima semana

### Veto Conditions
- Gerar relatório com menos de 3 dias de dado → VETO (informar dado insuficiente)
- Relatório sem comparação vs CPL meta → incompleto
- Recomendação de escala sem dado de 7 dias → VETO
- Relatório sem análise de criativos → incompleto

### Completion Criteria
- Dados coletados por campanha, conjunto, criativo e segmentos
- KPIs calculados: gasto, leads, CPL, CTR, CPM, frequência
- Análise multi-dimensão (idade, posicionamento, região, conjunto)
- Classificação BOM/MÉDIO/RUIM para cada item
- Plano de ação com recomendações claras e priorizadas
- Relatório formatado no template padrão Stark
- Entregue ao @traffic-chief para aprovação antes de enviar ao cliente
