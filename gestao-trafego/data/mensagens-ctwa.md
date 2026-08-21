# Biblioteca de Mensagens — WhatsApp CTWA

Mensagem automática exibida ao lead no WhatsApp quando ele clica em um anúncio Meta Ads
com destino "Enviar mensagem via WhatsApp" (Click-to-WhatsApp).

**Fonte:** POP-OPR-032-V01 — Personalização da Mensagem Automática do WhatsApp em Anúncios
CTWA (IT-1 e IT-2). Biblioteca mantida pelo **Head de Tráfego**; modelos salvos no
Gerenciador e personalização por anúncio são do **Gestor de Tráfego**.

---

## Regra não-negociável

> **Em nenhuma hipótese o campo de mensagem automática fica com a sugestão gerada por IA
> do Gerenciador de Anúncios como texto final.** Toda mensagem publicada nasce de um modelo
> desta biblioteca — ou de uma variação escrita manualmente a partir dela, mantendo o padrão.
> Isso vale mesmo quando a sugestão da plataforma "parece boa o suficiente", e mesmo quando
> não existe modelo para o procedimento (aí usa-se a genérica).

A mensagem é escrita **em primeira pessoa, como se o próprio lead estivesse falando**. Ele
pode editar antes de enviar, mas na prática a maioria envia como está.

**Tom obrigatório:** formal e direto. Sem emojis, sem gírias ("Oi", "pra", "vc"), sem frases
longas. Não trocar "gostaria" por formas informais ("queria", "tava pensando"). Não alterar
a abertura fixa de cada origem. O padrão é o único aprovado — não é ponto de partida
criativo para o gestor reinventar o tom.

---

## As duas origens

Cada origem tem sua abertura fixa; o resto da frase (procedimento + ação) segue a mesma
lógica nos dois casos.

| Origem | Quando usar | Estrutura fixa |
|---|---|---|
| **Origem 1 — Anúncio direto** | Lead clicou direto no anúncio (CTWA puro) | `Olá! Vi um anúncio no Instagram [sobre o procedimento] e gostaria de [ação].` |
| **Origem 2 — Formulário preenchido** | O anúncio tem etapa de formulário / Instant Form antes de abrir o WhatsApp | `Olá! Preenchi o formulário [sobre o procedimento] e gostaria de [ação].` |

> ⚠️ Não confundir com o **POP-OPR-017**: lá o formulário nativo do Meta direciona ao
> CRM/GHL e o lead nunca chega ao WhatsApp. Na Origem 2 o destino final continua sendo o
> WhatsApp.
>
> Em dúvida sobre a origem: verificar no Gerenciador se o destino da campanha inclui uma
> etapa de formulário/Instant Form antes do WhatsApp.

---

## Mensagens genéricas

Usar quando o procedimento ainda não tem modelo específico — **nunca como substituto
permanente**. Ao usar uma genérica, sinalizar ao Head de Tráfego para criar o modelo
específico.

| # | Contexto de uso | Origem 1 — Anúncio direto | Origem 2 — Formulário preenchido |
|---|---|---|---|
| G1 | Anúncio institucional / sem procedimento específico em destaque | "Olá! Vi um anúncio no Instagram e gostaria de agendar uma consulta." | "Olá! Preenchi o formulário e gostaria de agendar uma consulta." |
| G2 | Campanha/promoção sem procedimento nomeado no criativo | "Olá! Vi um anúncio no Instagram e gostaria de saber mais informações sobre a promoção." | "Olá! Preenchi o formulário e gostaria de saber mais informações sobre a promoção." |
| G3 | Conteúdo educativo (vídeo explicando um tema, sem oferta direta) | "Olá! Vi um anúncio no Instagram sobre [tema do anúncio] e gostaria de saber mais informações." | "Olá! Preenchi o formulário sobre [tema do anúncio] e gostaria de saber mais informações." |
| G4 | Avaliação/consulta em geral | "Olá! Vi um anúncio no Instagram e gostaria de agendar uma avaliação." | "Olá! Preenchi o formulário e gostaria de agendar uma avaliação." |

---

## Mensagens por procedimento

Cobertura inicial dos procedimentos mais comuns na carteira Stark. **A lista não é
exaustiva** e deve crescer conforme novos clientes e procedimentos entram.

Todas seguem o mesmo padrão: `Olá! Vi um anúncio no Instagram sobre [procedimento] e
gostaria de saber mais sobre o procedimento.` (Origem 1) / `Olá! Preenchi o formulário sobre
[procedimento] e gostaria de saber mais sobre o procedimento.` (Origem 2)

| Procedimento | Termo usado na mensagem |
|---|---|
| Rinoplastia | rinoplastia |
| Lipoaspiração / Lipo HD | lipoaspiração |
| Mamoplastia de Aumento (prótese de mama) | mamoplastia de aumento |
| Mamoplastia Redutora | mamoplastia redutora |
| Mastopexia (lifting de mama) | mastopexia |
| Abdominoplastia | abdominoplastia |
| Lipoenxertia (BBL / enxerto de gordura) | lipoenxertia |
| Harmonização Facial | harmonização facial |
| Blefaroplastia (pálpebras) | blefaroplastia |
| Otoplastia (orelhas) | otoplastia |
| Cirurgia Íntima (ninfoplastia) | cirurgia íntima |
| Facelift / Ritidoplastia | facelift |
| Botox / Preenchimento (não cirúrgicos) | botox |
| Bichectomia | bichectomia |

**Exemplo completo (Rinoplastia, Origem 1):**
> "Olá! Vi um anúncio no Instagram sobre rinoplastia e gostaria de saber mais sobre o
> procedimento."

---

## Personalização obrigatória por anúncio

O modelo-base nunca vai para o anúncio sem confirmar que **o procedimento citado é
exatamente o do criativo em veiculação**. Quando o criativo tem oferta específica, ajustar
a ação final da frase — mantendo sempre a abertura fixa da origem.

| Elemento do criativo | Ajuste no final da frase |
|---|---|
| Menciona condição/promoção (ex.: "avaliação gratuita") | "…e gostaria de saber mais sobre a avaliação gratuita." |
| Depoimento de paciente / antes e depois | "…e gostaria de saber mais sobre o procedimento." (manter simples — não citar o depoimento) |
| Menciona parcelamento/condição de pagamento | "…e gostaria de saber mais sobre as condições de pagamento." |
| Sem oferta específica além do procedimento | Usar o modelo-base sem alteração |

---

## Ice breakers (sugestões de perguntas)

Botões de resposta rápida que aparecem para o lead. Configurados junto com o modelo.

| Contexto | Ice breakers |
|---|---|
| Genéricas (G1–G4) | "Quais os valores?" · "Como funciona a avaliação?" · "Quero agendar uma consulta." |
| Por procedimento | "Quais os valores?" · "Como funciona a avaliação?" · "Sou uma boa candidata(o)?" |

Ajustáveis por procedimento se fizer sentido, mantendo o tom.

---

## Convenção de nome do modelo salvo

```
[Procedimento] — [Origem 1: Anúncio direto | Origem 2: Formulário]
```

Exemplos: `Rinoplastia — Anúncio direto` · `Genérica — Formulário` ·
`Mastopexia — Anúncio direto`

O texto não cita o nome da clínica, então o modelo salvo fica disponível para seleção em
anúncios de outros clientes também.

⚠️ **Nunca criar um modelo novo do zero se já existe um salvo** para aquela combinação
procedimento + origem — gera duplicidade e divergência de texto.

---

## Exceções frequentes

| Situação | Como resolver |
|---|---|
| Procedimento do anúncio não está na tabela | Usar a genérica (G1–G4) da origem correta + sinalizar ao Head de Tráfego para criar o modelo específico |
| Não está claro se é Origem 1 ou Origem 2 | Verificar no Gerenciador se o destino da campanha inclui etapa de formulário/Instant Form antes do WhatsApp |
| Anúncio cobre múltiplos procedimentos | "Olá! Vi um anúncio no Instagram sobre mamoplastia e lipoaspiração e gostaria de saber mais sobre os procedimentos." |
| A sugestão automática do Gerenciador "parece boa o suficiente" | Não usar mesmo assim — sempre substituir por um modelo desta biblioteca |
| Não encontro a seção "Modelo de mensagem" | Confirmar que o objetivo da campanha é "Mensagens" e o destino é "WhatsApp" — em outros objetivos essa seção não existe |
| A conta não mostra botão de "gerar com IA" | A regra segue igual: campo vazio ou com texto padrão da plataforma tem a mesma proibição |
| Não encontro a opção "Salvar modelo" | Verificar se está dentro do construtor "Criar novo"; se realmente não existir na conta, registrar como limitação e usar o texto direto por anúncio |
| Duplicar anúncio trouxe a mensagem do original | Revisar e reescrever a oferta específica antes de publicar — nunca publicar duplicado sem revisar o texto |
| Texto não aparece na pré-visualização após salvar | Atualizar a página/preview; se persistir, salvar novamente antes de publicar |

---

## Nota de manutenção

A Meta atualiza a interface do Gerenciador com frequência — nomes exatos de botões e seções
podem variar por conta ou por atualização. Procurar pela **função** descrita, não pelo nome
literal, e atualizar esta referência com print assim que confirmar na conta real.

## Quando escalar

- **Procedimento sem modelo na biblioteca** → o Gestor cria e salva o modelo a partir do
  genérico (não bloqueia o anúncio) e sinaliza ao Head de Tráfego para registrar aqui.
- **Campo de mensagem não aparece** mesmo com objetivo e destino corretos → Head de Tráfego
  (pode ser limitação da conta ou da versão).
- **Dúvida sobre qual modelo usar** → Estrategista (contexto do cliente) ou Head de Tráfego
  (biblioteca).
- **Desvio recorrente na auditoria** (mesmo gestor, múltiplos anúncios) → Head de Tráfego.

## Indicadores (POP-OPR-032)

| Indicador | Meta |
|---|---|
| Anúncios ativos com destino WhatsApp e mensagem personalizada | 100% — nenhum com sugestão de IA como texto final |
| Correção após desvio identificado na auditoria | Até 2 dias úteis do registro no ClickUp |
| Cadência e cobertura da auditoria | Mensal, 100% dos anúncios ativos (checagem completa, não amostragem) |
| Cobertura da biblioteca por procedimento | 100% dos procedimentos ativos na carteira com modelo próprio |
