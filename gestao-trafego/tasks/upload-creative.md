# upload-creative

## Task: Upload e Nomenclatura de Criativos — Padrão Stark

### Metadata
- **executor:** media-buyer
- **elicit:** true
- **mode:** sequential
- **output:** criativos nomeados e configurados no Gerenciador

### Inputs Required
```
criativos_disponiveis: Lista de arquivos de criativos aprovados
conjunto_destino: Nome do conjunto de anúncios destino
tipo_criativo: REELS | FEED | STORIES | CARROSSEL
objetivo_conversao: WHATSAPP | DIRECT | FORM | SITE
cta_definido: CTA manual a ser usado
url_destino: Link de destino com UTM
```

### Elicitation
```
Quais criativos estão aprovados e prontos para subir?
> [lista de arquivos]

Qual o CTA deste anúncio? (ex: "Agende Agora", "Enviar mensagem", "Saiba mais")
> [media-buyer define]

A URL de destino tem UTM configurado?
> [sim/não — se não, configurar antes]
```

### Execution Steps

#### Step 1: Verificar Criativos
Checklist de verificação antes do upload:
- [ ] Arquivo no formato correto (MP4 para vídeo, JPG/PNG para imagem)
- [ ] Proporção correta: 9:16 para REELS/STORIES, 1:1 ou 4:5 para FEED
- [ ] Sem música protegida por direitos autorais
- [ ] Conteúdo aprovado: depoimento / antes e depois / educativo (sem viral ou dança)
- [ ] Sem texto em excesso na imagem (máximo 20% da área)

#### Step 2: Nomenclatura do Anúncio
Aplicar formato Stark: `[DATA][NOME][FORMATO][VARIAÇÃO][TIPO]`

**Campos:**
- DATA: `AAAAMMDD` (ex: 20250510)
- NOME: identificador breve do criativo (ex: DrCarla, Antes_Depois_Botox)
- FORMATO: REELS | FEED | STORIES | CARROSSEL
- VARIAÇÃO: V1 | V2 | V3 (para testes A/B)
- TIPO: ANTES_DEPOIS | DEPOIMENTO | EDUCATIVO | OFERTA

**Exemplos:**
- `20250510_DrCarla_REELS_V1_DEPOIMENTO`
- `20250510_Botox_FEED_V1_ANTES_DEPOIS`
- `20250510_Harmoniz_STORIES_V2_EDUCATIVO`

#### Step 3: Configurar Anúncio no Gerenciador
- Nome do anúncio: aplicar nomenclatura Stark
- Selecionar criativo correto
- Definir CTA: **MANUAL** (não deixar automático)
- Inserir URL com UTM
- Verificar preview nos formatos: Feed, Stories, Reels

#### Step 4: Verificar UTM
Formato padrão de UTM:
```
?utm_source=facebook&utm_medium=paid&utm_campaign=[NOME_CAMPANHA]&utm_content=[NOME_CONJUNTO]&utm_term=[NOME_ANUNCIO]
```

Verificar rastreamento em pelo menos 1 anúncio antes de publicar todos.

### Output Format
```
CRIATIVOS CONFIGURADOS — [Nome do Cliente]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Conjunto: [nome do conjunto]

Anúncios configurados:
  ✅ 20250510_DrCarla_REELS_V1_DEPOIMENTO
     CTA: Agende Agora | URL: conferida ✅
  ✅ 20250510_Botox_FEED_V1_ANTES_DEPOIS
     CTA: Enviar mensagem | URL: conferida ✅
  ✅ 20250510_Harmoniz_STORIES_V2_EDUCATIVO
     CTA: Saiba mais | URL: conferida ✅

Total: [N] anúncios configurados
Gate CTA manual: [N]/[N] ✅
Gate URL+UTM: [N]/[N] ✅
```

### Veto Conditions
- CTA automático (não manual) → VETO
- URL sem UTM para campanha com objetivo de tráfego → VETO
- Criativo com conteúdo viral/dança → VETO (rejeitar e solicitar substituto)
- Música protegida sem licença → VETO
- Anúncio sem nomenclatura Stark → VETO (renomear antes)

### Completion Criteria
- Todos os criativos nomeados com nomenclatura Stark
- CTA manual definido em todos os anúncios
- URLs com UTM verificadas
- Preview conferido nos formatos principais
- Pronto para publicação (aguardar gate final do @traffic-chief)
