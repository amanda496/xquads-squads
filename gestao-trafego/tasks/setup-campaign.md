# setup-campaign

## Task: Setup de Campanha — Configuração Stark no Gerenciador

### Metadata
- **executor:** media-buyer
- **elicit:** true
- **mode:** sequential
- **output:** campanha configurada + gate aprovado

### Inputs Required
```
nome_cliente: Nome do cliente
produto: Procedimento ou serviço da campanha
funil: TOFU | MOFU | BOFU
objetivo_meta: Mensagens | Leads | Tráfego | Alcance (nunca Alcance para BOFU)
tipo_estrutura: ABO | CBO
orcamento: Valor diário (ABO = por conjunto, CBO = por campanha)
publicos_criados: Lista de públicos já criados pelo *build-audience
criativos_prontos: Lista de criativos aprovados
```

### Elicitation
```
Qual o funil desta campanha? (TOFU / MOFU / BOFU)
> [media-buyer informa]

Qual o objetivo Meta Ads? (Mensagens / Leads / Tráfego)
> [media-buyer informa]

Estrutura ABO (teste) ou CBO (escala)?
> [media-buyer informa]

Qual o orçamento diário total?
> [media-buyer informa]

Os públicos já foram criados? (sim/não)
> [se não → executar *build-audience primeiro → VETO]
```

### Execution Steps

#### Step 1: Nomenclatura da Campanha
Aplicar formato Stark: `[FUNIL][OBJETIVO][PRODUTO][TIPO][ORÇAMENTO]`

Exemplos:
- `BOFU_MENSAGENS_BOTOX_CBO_R150DIA`
- `TOFU_TRAFEGO_HARMONIZACAO_ABO_R50CONJ`
- `MOFU_LEADS_LIPO_ABO_R80CONJ`

#### Step 2: Configurar Campanha
- Criar campanha com nome padronizado
- Selecionar objetivo correto (nunca Alcance para BOFU)
- Definir tipo de orçamento: ABO ou CBO
- Desativar Vantagem+ de campanha

#### Step 3: Configurar Conjuntos de Anúncios
Para cada público, aplicar nomenclatura: `[NUMERAÇÃO-PÚBLICO][CONVERSÃO][GEO]`

Exemplos:
- `01_LAL1PCT_WHATSAPP_SP`
- `02_ENGAJ90D_WHATSAPP_SP`
- `03_SEGUIDORES_WHATSAPP_BRASIL`

Configurações obrigatórias por conjunto:
- Posicionamento: **MANUAL** — Feed IG + Stories IG + Feed FB + Stories FB
- Faixa etária: **25-55 anos** (manual)
- Advantage+ Audience: **DESATIVADO**
- Segmentação: apenas públicos criados pelo *build-audience

#### Step 4: Subir Criativos
Para cada anúncio, aplicar nomenclatura: `[DATA][NOME][FORMATO][VARIAÇÃO][TIPO]`

Exemplos:
- `20250510_DrCarla_REELS_V1_ANTES_DEPOIS`
- `20250510_Clinica_FEED_V2_DEPOIMENTO`

Configurações obrigatórias por anúncio:
- CTA: **MANUAL** (ex: "Agende Agora", "Enviar mensagem", "Saiba mais")
- URL: conferida e com UTM correto
- Conteúdo: depoimento / antes e depois / educativo

#### Step 5: Gate de Proibições (checklist obrigatório)
- [ ] Posicionamento MANUAL: Feed + Stories IG + FB
- [ ] Advantage+ Audience: DESATIVADO
- [ ] Faixa etária: 25-55 (manual)
- [ ] CTA: manual definido
- [ ] Nomenclatura Stark em campanha, conjunto e anúncio
- [ ] URLs conferidas com UTM

**RESULTADO: 6/6 aprovado → publicar. Qualquer reprovado → corrigir antes.**

### Output Format
```
CAMPANHA CONFIGURADA — [Nome do Cliente]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Campanha: [nome completo]
Objetivo: [objetivo]
Orçamento: R$ [valor] / [dia ou campanha]

Conjuntos criados:
  ✅ [nome conjunto 1] — público: [público] — R$ [orçamento]
  ✅ [nome conjunto 2] — público: [público] — R$ [orçamento]

Anúncios por conjunto: [quantidade]

Gate de Proibições: 6/6 ✅

Status: PRONTO PARA PUBLICAR
```

### Veto Conditions
- Publicar com Advantage+ ativo → VETO
- Posicionamento automático → VETO
- Objetivo Alcance para BOFU → VETO
- Nomenclatura incorreta → VETO (corrigir antes)
- Criativos sem CTA manual → VETO
- Campanha mistura CORPO + FACE → VETO
- Publicar sem gate 6/6 aprovado → VETO

### Completion Criteria
- Gate de proibições 6/6 aprovado
- Nomenclatura Stark em todos os níveis
- Todos os criativos com CTA e URL corretos
- Campanha pronta para publicação (não publicar sem confirmação do @traffic-chief)
