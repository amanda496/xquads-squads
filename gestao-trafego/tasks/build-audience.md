# build-audience

## Task: Criar Públicos — Segmentação Stark por Estágio de Funil

### Metadata
- **executor:** media-buyer
- **elicit:** true
- **mode:** sequential
- **output:** públicos criados e documentados no Gerenciador

### Inputs Required
```
nome_cliente: Nome do cliente
estagios_ativos: TOFU | MOFU | BOFU (quais estágios a campanha vai usar)
lista_clientes: Arquivo de lista de clientes para LAL (se TOFU)
pagina_instagram: @ da conta Instagram
pagina_facebook: Nome da Página Facebook
geo: Cidade(s) / Estado(s) alvo
```

### Elicitation
```
Quais estágios de funil serão ativados nesta campanha?
> [TOFU / MOFU / BOFU ou combinação]

O cliente tem lista de clientes para criar Lookalike? (ideal: mínimo 500 contatos)
> [sim — subir arquivo / não — usar apenas públicos comportamentais]

Qual a segmentação geográfica? (ex: São Paulo capital / Rio de Janeiro / Brasil)
> [media-buyer informa]
```

### Execution Steps

#### TOFU — Públicos Frios (Alcance fora da base)

**LAL (Lookalike) — se lista disponível:**
- LAL 1% da lista de clientes (mais preciso)
- Tamanho mínimo esperado: 100K+ pessoas
- Nome padrão: `LAL1PCT_LISTA_[GEO]`

**Interesses — se sem lista:**
- Interesses relacionados ao procedimento/nicho
- Combinar: profissões de alto poder aquisitivo + interesses de luxo/estética
- Exemplos: Dermatologia, Cirurgia Plástica, Moda, Viagens Internacionais
- Nome padrão: `INTERESSES_LUXO_[GEO]`

**Verificação TOFU:**
- [ ] Tamanho do público ≥ 100.000 pessoas
- [ ] Sem sobreposição com públicos BOFU

---

#### MOFU — Públicos Mornos (Já interagiram)

- Visitantes do perfil Instagram nos últimos 90 dias
  - Nome padrão: `PERFIL_VISITA_90D_[GEO]`
- Engajamento com posts/anúncios nos últimos 90 dias
  - Nome padrão: `ENGAJ_POSTS_90D_[GEO]`
- Visualizações de vídeo 75%+ nos últimos 90 dias
  - Nome padrão: `VIDEO_75PCT_90D_[GEO]`

**Verificação MOFU:**
- [ ] Tamanho do público ≥ 1.000 pessoas
- [ ] Período de 90 dias configurado corretamente

---

#### BOFU — Públicos Quentes (Alta intenção)

- Engajamento Instagram 180 dias
  - Nome padrão: `ENGAJ_180D_[GEO]`
- Seguidores da conta (incluir apenas para conta nova — remover após 30 dias)
  - Nome padrão: `SEGUIDORES_[GEO]`
- Engajamento com página Facebook 180 dias
  - Nome padrão: `ENGAJ_FB_180D_[GEO]`
- Visitantes do site (se Pixel com dados)
  - Nome padrão: `VISITANTES_SITE_30D_[GEO]`

**Verificação BOFU:**
- [ ] Tamanho do público ≥ 1.000 pessoas
- [ ] Se seguidores em público BOFU → registrar data de criação (remover após 30 dias)

### Output Format
```
PÚBLICOS CRIADOS — [Nome do Cliente]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TOFU:
  ✅ LAL1PCT_LISTA_SP — 250.000 pessoas
  ✅ INTERESSES_LUXO_SP — 180.000 pessoas

MOFU:
  ✅ PERFIL_VISITA_90D_SP — 8.500 pessoas
  ✅ ENGAJ_POSTS_90D_SP — 12.000 pessoas

BOFU:
  ✅ ENGAJ_180D_SP — 4.200 pessoas
  ✅ SEGUIDORES_SP — 3.100 pessoas ⚠️ Remover após 30 dias (conta nova)

Total: [N] públicos criados
Pronto para: *setup-campaign
```

### Veto Conditions
- Criar campanha sem públicos prontos → VETO
- Público com tamanho < 1.000 pessoas → VETO para segmentação (usar apenas se não houver alternativa e documentar)
- Usar Advantage+ Audience no lugar de públicos manuais → VETO
- Iniciar BOFU sem público quente ativo → VETO

### Completion Criteria
- Todos os públicos necessários para os estágios ativos estão criados
- Tamanho mínimo verificado para cada público
- Nomenclatura padronizada em todos os públicos
- Lista de públicos documentada e pronta para o *setup-campaign
