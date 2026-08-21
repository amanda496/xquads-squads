# Checklist de Setup de Conta — Proibições Inegociáveis Stark

Gate de configuração: verificar **antes de publicar**. Aplica-se a toda conta Stark.

Complementos: `validacao-ativos-meta.md` (R1–R6, antes do setup) ·
`onboarding-gestor-trafego.md` (checklist final do onboarding).

---

## Meta Ads

### Posicionamento
- [ ] Posicionamento MANUAL selecionado
- [ ] Feed Instagram ✅
- [ ] Stories Instagram ✅
- [ ] Feed Facebook ✅
- [ ] Stories Facebook ✅
- [ ] Advantage+ / Automático: **DESATIVADO** ✅

### Público
- [ ] Advantage+ Audience: **DESATIVADO** ✅
- [ ] Segmentação manual configurada
- [ ] Faixa etária MANUAL, definida pelo cliente-alvo real (referência padrão: 25–55) ✅
      — proibida Idade Automática
- [ ] Localização: configurada manualmente, no raio real de atuação ✅
- [ ] Públicos criados em sessão dedicada, **antes** de subir campanhas ✅
- [ ] Lista de exclusão de já convertidos carregada ✅

### Anúncios
- [ ] CTA: MANUAL definido (ex: "Agende Agora", "Enviar mensagem") ✅
- [ ] URLs conferidas em todos os anúncios ✅
- [ ] UTMs configuradas corretamente ✅ — ver `data/padroes-stark.md`
- [ ] Conteúdo: depoimento / antes e depois / educativo ✅
      — proibido viral, dança ou conteúdo de terceiros

### Tracking
- [ ] Pixel do Meta instalado e disparando ✅
- [ ] API de Conversões configurada ✅
- [ ] Medição Agregada de Eventos configurada (iOS) ✅
- [ ] GTM instalado, publicado e verificado com Tag Assistant ✅
- [ ] GA4 vinculado ao Google Ads, Google Signals ativo, `generate_lead` como conversão ✅

### Nomenclatura
- [ ] Campanha: `[FUNIL][OBJETIVO][PRODUTO][TIPO][ORÇAMENTO]` ✅
- [ ] Conjunto: `[NUMERAÇÃO-PÚBLICO][CONVERSÃO][GEO]` ✅
- [ ] Anúncio: `[DATA][NOME][FORMATO][VARIAÇÃO][TIPO]` ✅

### Coerência de Campanha
- [ ] Campanha foca em CORPO **ou** FACE — nunca ambos ✅
- [ ] Funil correto para o objetivo (não usar Alcance para BOFU) ✅
- [ ] Seguidores em público BOFU: apenas se conta nova (remover após 30 dias) ✅
- [ ] Anuncia apenas procedimentos que o médico de fato opera ✅

---

## Google Ads

### Rede e correspondência
- [ ] "Incluir a Rede de Display" **DESMARCADA** em toda campanha de Pesquisa ✅
- [ ] Correspondência apenas Frase (`"palavra"`) ou Exata (`[palavra]`) ✅
      — proibida Correspondência Ampla
- [ ] Palavras negativas configuradas **ANTES** de subir a campanha ✅
      (grátis, SUS, fotos bizarras, etc.)

### Estrutura
- [ ] Campanhas separadas por Corporal e Facial ✅
- [ ] Grupo de Termos Genéricos/Institucionais presente em todas as campanhas ✅
- [ ] Grupos por procedimento realmente operado ✅
- [ ] Técnica exclusiva do médico com grupo próprio + LP específica ✅

### Anúncios e ativos
- [ ] 3 RSAs por Grupo de Anúncios ✅
- [ ] 15 títulos + 5 descrições em cada RSA ✅
- [ ] Sitelinks (mínimo 4), Frases de Destaque, Snippets, Chamada ✅
- [ ] Extensões de Imagem ativas (3–5 imagens de qualidade) ✅
- [ ] Nenhuma imagem com exposição de pele, cicatriz aberta ou centro cirúrgico ✅
- [ ] Google Meu Negócio vinculado ✅

### Conta
- [ ] Estratégia de lances: Maximizar Conversões ✅
- [ ] Ação de conversão: botão WhatsApp ou formulário ✅
- [ ] Lista de clientes antigos carregada ✅
- [ ] Públicos de interesse em modo Observação ✅
- [ ] UTMs no nível de conta e nas extensões (inclusive link do WhatsApp) ✅

---

**RESULTADO:** Todos os itens aprovados antes de publicar.
Se qualquer item reprovado → corrigir antes de publicar. Sem exceção.
