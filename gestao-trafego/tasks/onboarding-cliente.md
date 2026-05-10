# onboarding-cliente

## Task: Onboarding de Novo Cliente — Método Stark

### Metadata
- **executor:** traffic-chief
- **elicit:** true
- **mode:** sequential
- **output:** briefing-cliente.md + estrutura inicial de conta

### Inputs Required
```
nome_cliente: Nome do cliente / clínica
conta_meta_ads: ID ou nome da conta no Gerenciador
produto_principal: Procedimento ou serviço a divulgar
objetivo_negocio: O que o cliente espera (leads, agendamentos, vendas)
orcamento_mensal: Budget total disponível por mês
meta_cpl: CPL alvo do cliente (se souber)
fase_atual: Novo cliente (conta zerada) ou conta existente?
```

### Elicitation
```
Qual o nome do cliente e da clínica/empresa?
> [cliente informa]

Qual o produto/procedimento principal a ser divulgado?
> [cliente informa]

Qual o objetivo: leads via WhatsApp, Direct Instagram, formulário Meta, ou agendamento direto?
> [cliente informa]

Qual o orçamento mensal disponível para tráfego pago?
> [cliente informa]

O cliente tem uma meta de CPL (Custo por Lead)? Se sim, qual?
> [cliente informa ou "não definido"]

A conta Meta Ads já tem histórico ou é nova?
> [cliente informa]
```

### Execution Steps

#### Step 1: Diagnóstico Inicial
- Verificar se conta Meta Ads existe e está configurada
- Verificar se Pixel está instalado e disparando
- Verificar se API de Conversões está configurada
- Verificar se GTM está instalado
- Verificar histórico de campanhas (se conta existente)
- Documentar situação atual da conta

#### Step 2: Definir Estrutura Stark
Baseado no orçamento mensal, definir estrutura:

| Verba Mensal | Estrutura |
|---|---|
| Até R$ 2.500 | 1 campanha teste ABO por estágio ativo |
| R$ 2.500 – R$ 5.000 | ABO teste + CBO escala (60-70% verba) |
| Acima R$ 5.000 | Estrutura completa separada por procedimento |

- Identificar estágio de funil prioritário (TOFU/MOFU/BOFU)
- Definir CPL meta (se cliente não souber: benchmark R$7-12)
- Definir públicos necessários por estágio
- Definir criativos iniciais necessários

#### Step 3: Verificar Proibições Inegociáveis
Confirmar que cliente entende e aceita as regras Stark:
- Posicionamento manual (sem Advantage+)
- Segmentação manual por faixa etária 25-55 anos
- CTA manual definido
- Conteúdo: depoimento / antes e depois / educativo
- Nomenclatura padronizada em todos os níveis
- Campanha foca em CORPO ou FACE — nunca ambos

#### Step 4: Briefing Final
- Documentar todas as informações coletadas
- Definir próximo passo: *launch-campaign ou configurar tracking primeiro
- Comunicar estrutura inicial ao @media-buyer

### Output Format
```markdown
# Briefing — [Nome do Cliente]
**Data:** [data]
**Gestor Responsável:** [nome]

## Dados da Conta
- Conta Meta Ads: [ID]
- Produto principal: [produto]
- Objetivo: [leads WPP / DIRECT / FORM / Agendamento]
- Orçamento mensal: R$ [valor]
- CPL meta: R$ [valor]
- Fase: [TESTE / ESCALA]

## Situação da Conta
- Pixel: [instalado / não instalado]
- API Conversões: [configurada / pendente]
- GTM: [instalado / pendente]
- Histórico: [conta nova / X campanhas anteriores]

## Estrutura Inicial Proposta
- Tipo: [ABO / CBO / misto]
- Estágios ativos: [TOFU / MOFU / BOFU]
- Orçamento por conjunto: R$ [valor]
- Públicos necessários: [lista]
- Criativos necessários: [lista]

## Próximos Passos
1. [Ação 1]
2. [Ação 2]
```

### Veto Conditions
- Iniciar campanhas sem Pixel instalado e disparando → VETO
- Iniciar BOFU sem público quente mínimo de 1.000 pessoas → VETO
- Definir CPL meta acima de R$20 sem justificativa de nicho → ALERTA
- Campanha mistura CORPO + FACE → VETO

### Completion Criteria
- Briefing documentado com todos os campos preenchidos
- Situação do tracking verificada
- Estrutura inicial proposta e validada
- Próximos passos definidos e comunicados ao @media-buyer
