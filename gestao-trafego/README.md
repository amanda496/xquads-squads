# Gestão de Tráfego Stark

## Overview

Squad de tráfego pago baseado no **Método Stark de Otimizações Meta Ads**. Conecta criativo, mídia e dados para maximizar performance de campanhas com estrutura, processo e decisões baseadas em thresholds reais.

## Purpose

Este squad implementa a metodologia operacional da Stark para gestão de tráfego pago — do onboarding de novo cliente ao daily review e às decisões de scale-or-kill. Não é um assistente genérico de marketing digital. É um sistema de agentes que pensa e age como gestores Stark treinados.

**Princípios centrais:**
- Performance precede escala
- Padronização precede refinamento
- Feeling com estrutura = expertise. Feeling sem dados = chute

## Quando Usar

Use este squad quando você precisa:

- Lançar campanhas Meta Ads com estrutura e nomenclatura padronizada
- Fazer daily review de contas e decidir o que escalar, manter ou pausar
- Diagnosticar por que o CPL subiu e identificar o gargalo real (CPM, CTR ou Conversão)
- Gerar relatórios semanais com análise por criativo, público, região e posicionamento
- Fazer onboarding técnico de novo cliente (D+0 a D+10)

## O que Está Incluído

### Agentes

| Agente | Tier | Papel |
|--------|------|-------|
| `traffic-chief` | 0 | Orquestrador — conecta criativo, mídia e dados. Decide estratégia e roteia trabalho |
| `media-buyer` | 1 | Execução técnica — cria e configura campanhas com estrutura Stark |
| `analytics-analyst` | 1 | Análise de dados — diagnóstica gargalos e gera relatórios |

### Workflows

| Workflow | Descrição |
|----------|-----------|
| `wf-launch-campaign.yaml` | Brief → Criativo → Setup → Publicar |
| `wf-daily-review.yaml` | Pull dados → Diagnóstico → Plano de ação |
| `wf-scale-or-kill.yaml` | Thresholds → Decisão → Executar |

### Dados de Referência

| Arquivo | Conteúdo |
|---------|----------|
| `data/thresholds-stark.md` | CPL meta, benchmarks por funil, critérios de decisão |
| `data/publicos-padrao.md` | Públicos padrão Stark por estágio de funil |

### Checklists

| Arquivo | Uso |
|---------|-----|
| `checklists/setup-conta.md` | Verificação de configurações inegociáveis antes de subir campanhas |

## Como Usar

### Ativar o squad

```
@traffic-chief
```

### Comandos principais

```
*launch-campaign   — Lançar campanha (brief → setup → publicar)
*daily-review      — Analisar campanhas e gerar plano de ação
*scale-or-kill     — Decidir escala ou pausa com thresholds reais
*onboarding        — Setup completo de conta nova (D+0 a D+10)
```

### Ativar agentes diretamente

```
@media-buyer       — Para execução técnica de campanhas
@analytics-analyst — Para análise de dados e relatórios
```

## Estrutura do Squad

```
squads/gestao-trafego/
├── agents/
│   ├── traffic-chief.md       # Orquestrador Tier 0
│   ├── media-buyer.md         # Execução técnica Tier 1
│   └── analytics-analyst.md   # Análise de dados Tier 1
├── workflows/
│   ├── wf-launch-campaign.yaml
│   ├── wf-daily-review.yaml
│   └── wf-scale-or-kill.yaml
├── tasks/
│   ├── onboarding-cliente.md
│   ├── setup-campaign.md
│   ├── build-audience.md
│   ├── upload-creative.md
│   ├── optimize-adset.md
│   ├── setup-tracking.md
│   ├── analyze-performance.md
│   ├── weekly-report.md
│   ├── diagnose-campaign.md
│   ├── creative-analysis.md
│   └── audience-analysis.md
├── checklists/
│   └── setup-conta.md
├── data/
│   ├── thresholds-stark.md
│   └── publicos-padrao.md
├── templates/
│   └── relatorio-semanal.md
├── config.yaml
└── README.md
```

## Proibições Inegociáveis

O squad veta automaticamente qualquer configuração que viole o Método Stark:

| Configuração | PROIBIDO | CORRETO |
|---|---|---|
| Posicionamento | Advantage+ / Automático | Feed + Stories (manual) |
| Público | Advantage+ Audience | Segmentação manual |
| Idade | Automática | 25-55 anos (manual) |
| CTA | Automático | Manual (ex: "Agende Agora") |
| Conteúdo | Viral / Dança / Terceiros | Depoimento, A&D, Educativo |
| Mix de campanha | Corpo + Face juntos | CORPO ou FACE — nunca ambos |

## Métricas por Funil

| Funil | Métrica-chave | Benchmark |
|-------|--------------|-----------|
| TOFU | CpS (Custo por Seguidor) | ≤ R$ 1,50 |
| MOFU | CTR | ≥ 1,5% |
| BOFU | CPL (Custo por Lead) | R$ 7 – R$ 12 |

## Versão

- **v1.0.0** — Squad inicial com 1 chief + 2 masters. Baseado no Método Stark de Otimizações Meta Ads, Playbook de Onboarding e POPs operacionais.

---

**Pronto para conectar criativo, mídia e dados? Ative com `@traffic-chief`.**

_Versão: 1.0.0 | Compatível com AIOX-FULLSTACK v4+_
