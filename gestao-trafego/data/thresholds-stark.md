# Thresholds e Benchmarks — Método Stark

Alinhado ao Playbook de Onboarding — Gestor de Tráfego Stark v1.0 (abr/2026), §8 e §10.

## Métricas por Estágio de Funil

| Estágio | Métrica-chave | Benchmark | Alerta | Ação automática |
|---------|--------------|-----------|--------|-----------------|
| TOFU | CpS (Custo por Seguidor) | R$ 1,50 – R$ 2,59 | > R$ 2,59 | Desativar se CpS > R$ 3,00 |
| MOFU | CTR | ≥ 1,5% | < 1,5% | Desativar se CTR < 1,5% |
| BOFU | CPL (Custo por Lead) | R$ 7 – R$ 12 | > R$ 15 | Desativar se CPL > R$ 20 |

## Benchmarks de Negócio (Cirurgia Plástica Brasil)

| Métrica | Benchmark |
|---|---|
| CAC médio | R$ 800 – R$ 2.500 |
| LTV médio | R$ 8.000 – R$ 25.000 |
| ROI esperado | 3:1 a 6:1 |
| Investimento mensal de referência | R$ 5.000 – R$ 15.000 |

## Critérios de Classificação CPL

- **ÓTIMO:** CPL < Meta do cliente
- **BOM:** CPL = Meta do cliente (±10%)
- **RUIM:** CPL > Meta do cliente

## Dado Mínimo para Decisão

- **Decisão de pausa/escala:** Gasto ≥ 2x CPL meta (ex: meta R$12 → aguardar R$24 gastos)
- **Análise de tendência:** Mínimo 3 dias consecutivos
- **Decisão estrutural:** 7 dias de dado
- **Períodos de análise semanal:** 7D, 14D, 4D, 3D, Ontem e Hoje

## Ciclo de Otimização (72h)

- Analisar o CpS de **todos** os anúncios
- Nenhum atingiu a meta? Reduzir o orçamento dos que estão com CpS > R$ 3,00 —
  **não pausar ainda**
- Realocar verba: **67%** para escalar o melhor, **33%** para novos testes
- Pausar definitivamente os ruins **somente após** substitutos validados

## Regras de Escala

- Incremento máximo por vez: **20-30%**
- Frequência mínima entre escalas: **72 horas**
- CPM pode subir após escala — normal até 48h. Se CPL não cair → reverter

## Limites de Frequência

- **Nunca olhar a frequência acumulada** — sempre filtrar os últimos 30 dias
- Frequência acima de **3.0** (janela de 30 dias) = sinal de fadiga de criativo
- Alta frequência só é problema quando **custo sobe E audiência é pequena**
- Audiência grande + reach baixo → duplicar o conjunto para mudar a fadiga
- Trocar criativo apenas quando: audiência pequena + frequência alta + feedback em queda
- Seguidores em público BOFU: **máximo 30 dias** → remover depois

## Thresholds de Criativo

- CTR abaixo de **0,8%** no feed = criativo candidato à pausa
- CTR acima de **2,0%** = criativo de alto potencial
- Criativo dominante (>80% da verba) com CPL bom = manter + criar variações

## Distribuição Orçamentária (BOFU)

- **Fase de teste:** 30% do orçamento
- **Fase de escala:** 70% do orçamento
- Mover para escala apenas com CPL validado por 7D

## Cenários por Orçamento

Orçamento não define o método — define **quanto** do método se executa simultaneamente.

| Faixa | TOFU | MOFU | BOFU |
|---|---|---|---|
| Até R$ 2.500 | CBO se pouco conteúdo; ABO se tiver. 1 público por teste | 1 conjunto único misto | 1 campanha (engaj. 365 + 180) |
| Até R$ 3.000 | ABO teste (sempre ativo) + CBO escala (60–70% da verba) | 3 conjuntos separados | 2 campanhas (teste + escala) |
| Acima de R$ 3.500 | Estrutura completa com separação total | Avançado com lookalikes | Campanhas por procedimento |

## Análise Semanal Consolidada

Diagnóstico único por conta, toda semana, cobrindo:

- **TOFU:** CpS e volume de novos seguidores
- **MOFU:** volume de visitas ao perfil e CTR dos criativos
- **BOFU:** CPL e volume de leads gerados
- **Criativos rejeitados:** inventário de ads com status rejeitado
- **Campanhas zeradas:** campanhas ativas com zero conversões nos últimos 7 dias
