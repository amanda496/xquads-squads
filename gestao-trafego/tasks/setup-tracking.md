# setup-tracking

## Task: Configurar Tracking — Pixel, API de Conversões e GTM

### Metadata
- **executor:** media-buyer
- **elicit:** true
- **mode:** sequential
- **output:** tracking 100% operacional verificado

### Inputs Required
```
cliente: Nome do cliente
site_url: URL do site ou landing page
plataforma_site: WordPress | Wix | Shopify | Outro
pixel_id: ID do Pixel Meta (se já existir)
acesso_gtm: Acesso ao Google Tag Manager (sim/não)
evento_conversao: O que deve ser rastreado (Lead, Purchase, Contact, Schedule)
```

### Elicitation
```
O cliente já tem Pixel do Meta instalado?
> [sim — informar ID / não — criar novo]

Qual o evento de conversão principal? (Lead, Agendamento, Contato, Compra)
> [media-buyer informa]

O cliente tem acesso ao GTM configurado?
> [sim / não — precisará configurar]

Qual a plataforma do site?
> [WordPress / Wix / Shopify / outro]
```

### Execution Steps

#### Step 1: Pixel do Meta
**Se Pixel ainda não instalado:**
- Criar novo Pixel no Gerenciador de Eventos
- Instalar via GTM (recomendado) ou plugin nativo
- Verificar disparo na página principal

**Se Pixel já instalado:**
- Verificar se está disparando corretamente
- Verificar se o evento de conversão principal está configurado
- Usar Pixel Helper (extensão Chrome) para diagnóstico

**Verificação:**
- [ ] Pixel disparando na página principal
- [ ] Evento de conversão configurado e disparando
- [ ] Sem Pixel duplicado (um Pixel por conta)

#### Step 2: API de Conversões (CAPI)
Configurar API de Conversões para complementar o Pixel:
- Acessar: Gerenciador de Eventos → Configurações → API de Conversões
- Instalar via GTM ou integração direta da plataforma
- Ativar deduplicação (event_id) para evitar contagem dupla

**Plataformas com integração nativa:**
- Shopify: instalar pelo app oficial Meta
- WordPress: usar plugin Pixel Your Site Pro ou similar
- Wix: usar integração nativa em Marketing > Pixel do Facebook

**Verificação:**
- [ ] CAPI enviando eventos (verificar em Gerenciador de Eventos → Qualidade dos Eventos)
- [ ] Taxa de correspondência ≥ 7.0 (ideal ≥ 8.0)
- [ ] Deduplicação ativa

#### Step 3: Medição Agregada de Eventos (iOS)
Configurar eventos prioritários para usuários iOS:
- Acessar: Gerenciador de Negócios → Configurações → Medição Agregada de Eventos
- Adicionar domínio verificado
- Configurar prioridade dos eventos (máximo 8 eventos por domínio)
- Evento principal no topo da lista

**Verificação:**
- [ ] Domínio verificado
- [ ] Eventos configurados por prioridade
- [ ] Evento de conversão principal em posição 1 ou 2

#### Step 4: Google Tag Manager
- Verificar se GTM está instalado no site
- Verificar se o container está publicado e ativo
- Adicionar tag do Pixel via GTM (se não foi feito diretamente)
- Verificar via Preview do GTM

**Verificação:**
- [ ] GTM instalado e container publicado
- [ ] Tag do Pixel ativa via GTM
- [ ] Preview mostra eventos disparando

#### Step 5: Teste Final
- Acionar evento de conversão (ex: preencher formulário de teste)
- Verificar em Gerenciador de Eventos se evento chegou
- Verificar qualidade do sinal (alta / média / baixa)

### Output Format
```
RELATÓRIO DE TRACKING — [Nome do Cliente]
Data: [data]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Pixel Meta: ✅ ID [pixel_id] — disparando
Evento principal: ✅ [evento] — configurado
API de Conversões: ✅ Taxa de correspondência: [score]/10
Medição Agregada iOS: ✅ [N] eventos configurados
GTM: ✅ Container [ID] — ativo e publicado

Qualidade do Sinal: [ALTA / MÉDIA / BAIXA]

⚠️ Pendências:
  [lista de pendências se houver]

STATUS GERAL: [APROVADO / PENDENTE]
```

### Veto Conditions
- Lançar campanha sem Pixel instalado e verificado → VETO
- Pixel duplicado na página → VETO (remover duplicata antes)
- Evento de conversão não configurado → VETO para campanha de geração de leads
- Medição Agregada iOS não configurada → ALERTA (não impede lançamento, mas reduz eficiência)

### Completion Criteria
- Pixel instalado e disparando na página principal
- Evento de conversão principal configurado e testado
- API de Conversões ativa com taxa de correspondência ≥ 7.0
- Medição Agregada de Eventos iOS configurada
- GTM instalado e publicado
- Relatório de tracking gerado e aprovado pelo @traffic-chief
