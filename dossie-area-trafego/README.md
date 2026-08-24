# Dossiê da Área de Tráfego Pago · Stark Marketing

> **Confidencial — uso restrito da liderança.** Contém estrutura de carteira, réguas internas,
> nomes de cliente e situações de pessoal em aberto. Se este repositório for público ou vier a ser
> publicado, mover esta pasta para um local privado.

**Data de corte:** 21/08/2026. **Finalidade:** handover da **área** — como ela funciona, o que
entrega, com que método, com que réguas, em que ritmo e onde estão os gargalos. O handover das
**pessoas** está em [`../dossies-gestores-trafego/`](../dossies-gestores-trafego/README.md).

> **Como ler este documento.** É um **diagnóstico do estado atual da área**, não um plano a ser
> executado. Quem assumir **herda todas as atividades** — inclusive as que hoje dependem do OK da
> liderança e as que estão em construção — e **decide o que mantém, o que muda e o que descontinua**.
> Onde há sugestão ou ordem de prioridade neste dossiê, é leitura de quem sai, não instrução para
> quem entra.

**Fonte:** reuniões de área, reuniões de resultados (Blocos A/B e, a partir de agosto, por squad),
dailies de tráfego, dailies de líderes, X1s, o ciclo de PRA de julho, a pauta de resultados
apresentada ao CEO em 04/08 e a documentação de processo da área. Cobertura detalhada no final.

---

## 1. O que a área é

A área de Tráfego Pago da Stark opera **mídia paga para cirurgiões plásticos e especialidades
médicas correlatas** (face, corpo, ortognática, bucomaxilo, dermatologia, capilar) em **Meta Ads e
Google Ads**. Em julho/2026 a área geria **96 contas ativas** distribuídas entre 8 gestores.

A tese central do negócio, dita em uma linha: **audiência aquecida converte; sem volume de topo, o
fundo de funil perde eficiência.** É por isso que a métrica-mãe da área não é lead nem venda — é
**CPS, o custo por seguidor**.

> **Régua vigente — CPS ≤ R$ 2,00**
> `CPS = custo das campanhas de topo de funil ÷ seguidores pagos`
>
> **Régua anterior — CPS ≤ R$ 2,59**
> `CPS = custo total da conta ÷ variação de seguidores do Reportei`

**As duas mudanças andam juntas e mudam a leitura da métrica.** O numerador saiu do investimento
inteiro da conta para **só o topo de funil**; o denominador saiu da **variação líquida do Reportei**
(ganhos menos perdas, orgânico incluído) para o **seguidor pago**. Numerador menor e denominador mais
restrito — é por isso que a meta desceu de R$ 2,59 para R$ 2,00.

A lógica da régua anterior era a de que "todas as campanhas resgatam seguidores", então o custo
considerado era o total (06/02/2026). A régua atual isola o que o topo de funil efetivamente entregou.

> ⚠ **Consequência prática:** série histórica apurada na régua anterior **não é comparável** com a
> nova sem recálculo. Qualquer comparação com meses anteriores precisa refazer a conta na base nova.

### As 11 entregas da área

**Recorrentes (toda semana):**

| # | Entrega | O que é |
|---|---|---|
| 1 | **Teste de criativos** | Posts aprovados na Agenda de Postagem 3.0 subidos como testes ABO |
| 2 | **Análise de campanhas** | Diagnóstico de TOFU/MOFU/BOFU com status OK / Atenção / Crítico |
| 3 | **Otimização de campanhas** | Pausas e ajustes por benchmark; o que exige aprovação sobe para o estrategista |
| 4 | **Status Report** | Narrativa do que foi feito na semana — subido, ajustado, pausado e por quê |
| 5 | **Relatório de tráfego** | Métricas com diagnóstico causal e próximos passos |
| 6 | **Planilha mestre** | Métricas da semana anterior — prazo até quarta-feira |
| 7 | **Solicitação de ajuste em vídeos patrocinados** | Quando o criativo precisa de ajuste técnico ou de copy |
| 8 | **Solicitação e subida de posts patrocinados** | Impulsionamentos conforme demanda da conta |

**De onboarding (cliente novo):** 9) configuração da conta de anúncio · 10) pixel e tags GTM ·
11) fluxo ManyChat.

### O ciclo semanal

| Quando | O que acontece |
|---|---|
| **Segunda / terça** | Testar criativos da semana; solicitar ajuste de vídeo; subir patrocinados |
| **Durante a semana** | Monitorar e otimizar; documentar no Status Report |
| **Terça, 14h** | Relatório semanal automático enviado aos clientes |
| **Até quarta** | Preencher a planilha mestre com as métricas da semana anterior |
| **Segunda** | **Relatório da semana anterior (seg–dom) entregue ao cliente** — prazo alterado; era sexta da semana seguinte |

**Três dependências que travam o ciclo inteiro:** a **Agenda de Postagem aprovada antes de
segunda** (sem ela, o teste da semana atrasa e o dado chega tarde); os **dados do comercial do
cliente**, que chegam pelo estrategista e definem onde concentrar verba; e o **Reportei** — nenhuma
métrica é estimada, se o dado não existe a seção é omitida.

---

## 2. Pessoas e estrutura

### Quem responde pelo quê

| Papel | Quem | O que faz |
|---|---|---|
| **Head de Tráfego** | Amanda Neves (sai em 21/08/2026) | Método, réguas, metas, X1, cobrança de entrega, apresentação de resultados ao C-level |
| **Interinos** | Anderson Silva e Silvanio Guimarães | Assumem a área na transição (comunicado em 20/08) |
| **Gerente de Operações** | Silvanio Guimarães | Squads, alocação, decisões de pessoal, Daily Líderes |
| **Plataforma / Stark OS** | Anderson Silva | Desenvolvimento do OS, integrações, dashboards, feedbacks |
| **Método novo** | Lúcio Henrique | Autor do "novo método de tráfego" que a área adotou em agosto |
| **Gestores** | Mateus, Gustavo Radler, Vinicius, Thiago, Wallison, Luiz Eduardo, Nicole, Richard Tahara | Execução técnica das contas |
| **Estrategistas** | Bruno Marques, Breno Henrique, Samuel Barbosa, Roberta Endili, Gustavo Monteiro | Direção, posicionamento, dados do comercial, relação com o cliente |

**A escadinha Stark** (fluxo formal de escalonamento, do Playbook de abril):

1. **Analista de Tráfego** — tenta resolver o problema técnico ou a demanda do cliente.
2. **Coordenador de Tráfego** — acionado se o analista travar tecnicamente ou houver erro de
   processo/dados.
3. **Head de Tráfego** — acionado **apenas** se o problema impactar a meta semestral, a cultura do
   time ou a permanência do cliente (churn).

### Os squads de cliente (estrutura de agosto/2026)

Em agosto a área foi reorganizada em squads multidisciplinares por carteira. Cada squad tem reunião
de resultados semanal própria, e o gestor de tráfego entra nela junto com estrategista, copy, design
e social.

| Squad | Gestores de tráfego | Estrategista | Ritual |
|---|---|---|---|
| **A · Invictus** | Wallison, Gustavo Radler | Breno Henrique | Segunda, 15h |
| **B · Os Voldemorts** | Thiago Manoel, Nicole | Bruno Marques | Quarta, 15h |
| **C · JARVIS** | Mateus Borgo, Vinicius Lima | Gustavo Monteiro | Quarta, 16h30 |
| **ROI-as-unhas** | Luiz Eduardo, Nicole, Richard Tahara | Samuel Barbosa, Roberta Endili | Sexta, 16h |
| **Café, Caos e Resultado** | Vinicius Lima, Nicole | — | Segunda/terça, 16h30 |

Silvanio, Elaine Fedrigo, Daniela Cabral e Kenia Hahn circulam por vários squads; Amanda participava
de todos.

**Um sinal já registrado:** na reunião do Invictus de 17/08, Luciana Camargo pediu que os clientes de
tráfego fossem **diluídos entre as semanas, no máximo 1 por reunião** — com quatro contas de tráfego
na pauta, a reunião ficou longa demais. Vale como precedente: o formato de squad ainda está sendo
calibrado.

### Fora do time atual, mas no histórico recente

**Andreyves Cezário** (saiu da área), **Fábio Santos** (carteira redistribuída em julho),
**Alexander Santos** (entrou em fev/2026), **Raísa** (desligada em fev/2026 por ausências não
justificadas em reuniões de cliente — o precedente que a área usa para tratar presença como cláusula
contratual, não preferência).

---

## 3. O método

### 3.1 A estrutura de funil e a regra de verba

**70% TOFU · 10% MOFU · 20% BOFU.** O desvio é permitido, mas tem de ser decisão consciente entre
estrategista e gestor — não default.

| Etapa | Objetivo | Métrica-chave | OK | Atenção / Pausar |
|---|---|---|---|---|
| **TOFU** | Atrair, parar o scroll, ganhar seguidor | **CPS** | ≤ R$ 1,50 | R$ 1,50–2,59 atenção · > R$ 2,59 pausar |
| | | *(meta contratual hoje: **≤ R$ 2,00** na nova base — custo de topo ÷ seguidores pagos)* | | |
| **MOFU** | Quebrar objeção, aquecer | **CTR** | ≥ 1,5% | 1,0–1,5% atenção · < 1,0% pausar |
| **BOFU** | Levar ao agendamento | **CPL** | R$ 7–12 | R$ 12–20 atenção · > R$ 20 pausar |
| **Google** | Capturar demanda ativa | **CPA** | < R$ 30 | ≥ R$ 30 pausar |

**CPL de referência por especialidade:** cirurgia plástica R$ 6–15 · implante dental R$ 25–55 ·
cirurgia ortognática R$ 20–50.

### 3.2 Teste e escala

**Regra de ouro: testar em ABO, escalar em CBO.**

- **ABO de teste:** 1 criativo por conjunto, R$ 6/dia por conjunto, avaliação em 7 dias.
- **Escala:** só depois de validado, migra para a CBO definitiva.
- **Ciclo de 72h** (Checklist Operacional): analisar CPS de todos os anúncios → se algum ≤ R$ 1,50,
  escalar; se nenhum, **reduzir ao mínimo** (não pausar) os que estão acima de R$ 3,00 e realocar
  **67% para escala do melhor esforço, 33% para novos testes**; pausar de vez só quando os
  substitutos saírem do aprendizado.

### 3.3 Andrômeda — o método atual

Apresentado em maio/2026 como resposta à atualização do algoritmo do Meta. A lógica:

- **O algoritmo aprende com conversão real, não com engajamento.** Menos intervenção manual, mais
  confiança na IA. Alteração de orçamento no máximo **1× por dia**.
- **9 anúncios por semana — 3 de cada nível** (C1 topo, C2 meio, C3 fundo), todos **no mesmo conjunto
  de anúncios**: o algoritmo distribui conforme o estágio de cada pessoa.
- **Por que 9:** mais de 50% do resultado de leilão depende da qualidade do criativo (estudo
  Meta/Nielsen). O algoritmo desfavorece repetição — por isso a renovação é semanal.
- **Duas contas por cliente:** uma de **escala** (onde não se experimenta, só se sustenta o que
  funciona) e uma de **teste** (o laboratório). Protege o histórico da conta principal.
- **Públicos:** Advantage+ como recomendação principal, mais personalizados (interação com o IG,
  visitantes, lista de WhatsApp) e **exclusão de quem já agendou**.

> ⚠ **Ponto de alerta em aberto.** O uso do Advantage+ dentro do Andrômeda vem gerando **reclamação de
> seguidor desqualificado e de seguidor vindo de localização errada**. Detalhe no risco 4.

**Os três níveis de criativo:** C1 conteúdo de valor / quebra de padrão / exploração de dor · C2 hard
sell, demonstrativos, antes e depois, comparativos · C3 prova social, quebra das 5 objeções (preço,
tempo, confiança, adequação, urgência), urgência real. **CTA único no fundo: mensagem no WhatsApp.**

### 3.4 Nomenclatura — o que sustenta a medição

Padrão de três níveis, obrigatório. Não é burocracia: **o Stark OS extrai os resultados a partir do
nome da campanha. Nomenclatura errada = resultado errado do gestor.**

```
CAMPANHA:  [FUNIL][OBJETIVO][PRODUTO/EXPERT][TIPO][ORÇAMENTO]
           TOFU|MOFU|BOFU · Tráfego|Msgs|Leads|Engaj|RESPONDI · Lipo|Mama|Face… · TESTE|ESCALA · ABO|CBO
CONJUNTO:  [NUMERAÇÃO + PÚBLICO][CONVERSÃO][GEO]     ex.: [01-Int. Cirurgia Plástica_SITE_SP]
ANÚNCIO:   [DATA][NOME DO CRIATIVO][FORMATO][VARIAÇÃO][TIPO][DATA POST]
```

Tags em uso na prática: `[PRA]`, `[ANDROMEDA]`, `[ESCALA]`, `[TESTE]`, `[ADV]`/`Advantage`, `[IMP]`
(impulsionado), `[STARK 2.0]`, `respondi` (obrigatório para o OS puxar conversão personalizada).

**UTMs são obrigatórias em todos os anúncios**, sem exceção — Meta via parâmetros de URL, Google no
nível de conta.

### 3.5 Regras inegociáveis

**Meta Ads** — o gestor não pode alterar:

| Configuração | Regra | Motivo |
|---|---|---|
| Posicionamento | Proibido automático. Selecionar Feed e Stories manualmente | O Meta distribui para posicionamento de baixa qualidade |
| Idade | Proibida idade automática | Gasta verba em faixa irrelevante |
| CTA | Proibido CTA automático | O Meta troca para CTA genérico |
| Conteúdo | Proibido viral/dança/de terceiros | Foco total em autoridade médica |
| Criativos | Coerência corpo/face — não misturar | Confunde o lead |

**Google Ads:** proibida Rede de Display em campanha de Pesquisa · proibida correspondência ampla
(só frase ou exata) · obrigatório negativar termos ruins **antes** de subir · anunciar apenas
procedimentos que o médico opera de fato · **3 RSAs por grupo, 15 títulos + 5 descrições cada** ·
extensões de imagem obrigatórias · termos genéricos ("melhor cirurgião da cidade") em toda conta ·
Google Meu Negócio vinculado. Proibido em imagem: antes/depois com exposição de pele, cicatriz
aberta, centro cirúrgico.

### 3.6 Criativo e conteúdo

- **Framework de consciência (Schwartz), P0 a P5**, mapeado para funil e CTA: P0 inconsciente →
  "compartilhe com uma amiga"; P1 ciente do problema → "siga para mais conteúdo"; P2 ciente da
  solução → "comente FACE"; P3 ciente do produto → "fale comigo no direct"; P4-P5 → "agende sua
  consulta".
- **Sistema AROS** — o DNA do médico em três pilares: Personalidade, Público, Produto. Vem antes de
  qualquer template.
- **3 clusters de ICP:** facial em capital (nível 4-5 de sofisticação, saturado) · corporal em
  capital (3-5) · corporal em cidade menor (2-4, menos saturado).
- **Duas linhas de produção semanal:** 5 peças novas (criação) + 5 variações de hook/ritmo/cenário/CTA
  (otimização).
- **Regra de conteúdo antes de público:** "Se os resultados não estão bons, solicitar novo conteúdo
  ANTES de trocar públicos."

### 3.7 Decisões técnicas que entraram em 2026

| Quando | O que |
|---|---|
| **jul/2026** | **Regra de valor: lance negativo de 90% para público masculino**, em todos os conjuntos — para conter entrega e comentários inadequados, sobretudo em campanha Andrômeda |
| **jul/2026** | **Formulário nativo com perguntas condicionais** — na Concierge, taxa de agendamento subiu de **15% para 40%** |
| **jul/2026** | **Monitoramento diário** substitui a validação de 7 dias em CBO de orçamento alto (R$ 100/dia) |
| **jul/2026** | Direcionamento por dispositivo iOS deixa de ser regra e passa a sugestão |
| **jul/2026** | **Metodologia de otimização de lances para criativos validados** — ideia trazida pelo Mateus, adotada para toda a carteira |
| **jul/2026** | **"Operação segunda chance"** — reativar na campanha de escala criativos antes rejeitados; rendeu seguidor a R$ 1,32 |
| **ago/2026** | **Conversão offline obrigatória** em todo anúncio de fundo de funil — prazo **04/09**. Não é viável em campanha de topo direcionada ao perfil do IG (erro por ausência de objeto de destino) |
| **ago/2026** | **Mensagem de boas-vindas padronizada e não automatizada por IA**: origem (anúncio) + procedimento + CTA claro |
| **ago/2026** | **Metodologia do "porquê do porquê"** — cada dado apresentado exige justificativa técnica profunda, não descrição superficial; link direto do criativo obrigatório no relatório |

---

## 4. Réguas, metas e remuneração variável

### O sistema de 7 pilares (vigente desde fevereiro/2026)

A meta mensal e a semestral do gestor são calculadas sobre sete pilares:

1. **NPS** (quando existe) — precisa ser positivo
2. **Churn** — **anula a meta mensal**
3. **Status Report** — 100% ou zero
4. **Relatórios** — 100% de entrega
5. **Seguidores** — **CPS ≤ R$ 2,00** (custo de topo de funil ÷ seguidores pagos) em pelo menos 70%
   da carteira. Era R$ 2,59 na base antiga (custo total ÷ variação do Reportei)
6. **Fundo de funil** — ROI ≥ 1
7. **Custo por conversão do Google** — CPA

**Meta semestral:** a nota final somando os sete pilares precisa ficar **acima de 70%**. Por isso um
gestor que não bate a meta de seguidores ainda pode receber algo — relatório e status report em dia
puxam a nota para cima.

**ROI de fundo de funil = (agendamentos × valor da consulta) ÷ investimento total.** Precisa ser
≥ 1. O dado vem do comercial do cliente, coletado pelo estrategista, atualizado a cada 15 dias.
Quando o comercial não passa, cai-se na exceção: custo por lead simples.

**Exceções previstas:** dermatologia e bucomaxilo têm régua própria; clientes só-Google não entram na
perna de seguidores; clientes que só têm "Respondi" em vez de "Conversa iniciada" são tratados caso a
caso.

### A régua por orçamento

Da planilha de acompanhamento (mar/2026) — quanto se espera de cada faixa de verba. **A coluna de CPS
máximo foi calculada na base antiga** e precisa ser refeita para a nova (custo de topo ÷ seguidores
pagos, meta R$ 2,00):

| Orçamento | Novos seguidores (mínimo) | Alta performance | 70% em topo | CPS máximo | Criativos escalados |
|---|---|---|---|---|---|
| até R$ 1,8 mil | 23 | 30 | R$ 1.260 | R$ 1,40 | 2 |
| até R$ 3 mil | 39 | 50 | R$ 2.100 | R$ 1,40 | 5 |
| até R$ 5 mil | 64 | 80 | R$ 3.500 | R$ 1,46 | 9 |
| até R$ 8 mil | 103 | 110 | R$ 5.600 | R$ 1,70 | 14 |
| até R$ 9,5 mil | 122 | 130 | R$ 6.650 | R$ 1,71 | 15 |

Faixas de status: **Google CPA** < 20 excelente · 20–30 média · > 30 abaixo. **Respondi CPL** < 20
excelente · 20–50 média · > 50 abaixo. A planilha também acompanha "tempo lateralizado (21 dias)" e
"check de escala" por conta.

### O funil comercial completo e seus benchmarks

Os 7 estágios: Visitante (TOFU) → Base Social → Lead → **MQL** (lead score ≥ 51) → SAL → SQL →
Cliente.

| Métrica | Benchmark (cirurgia plástica Brasil) |
|---|---|
| Tráfego → Lead | 37% |
| Lead → Consulta agendada | 15–25% |
| Consulta → Procedimento | 40–60% |
| CAC médio | R$ 800 – R$ 2.500 |
| LTV médio | R$ 8.000 – R$ 25.000 |
| ROI esperado | 3:1 a 6:1 |
| Investimento mensal de referência | R$ 5.000 – R$ 15.000 |

---

## 5. Rituais e cadências

A área mudou de ritmo três vezes em seis meses. Vale conhecer a sequência, porque cada mudança
resolveu um problema e criou outro.

| Período | Ritual dominante | O que era |
|---|---|---|
| **fev–jul/2026** | **Daily de Tráfego** (diária, ~10h) | Amanda + todos os gestores. Alinhamento curto, avisos de método, mudanças de meta, redistribuição de carteira |
| **fev–jul/2026** | **Acompanhamento de Resultados — Bloco A e Bloco B** (semanal) | Revisão conta por conta com o Head. Cada gestor apresenta a carteira, ouve diretriz e sai com lista de ações |
| **jul/2026** | **Ciclo PRA** | X1 de PRA com cada gestor (02–07/07), Alinhamento PRA coletivo (22/07), prazo único: topo, meio e fundo de todos os clientes da lista até quinta, 23:59 |
| **ago/2026** | **Reunião de Área Tráfego Pago** (4× por semana, 11h) | Substituiu a daily. Pauta operacional + apresentação de otimizações + demonstração do Stark OS |
| **ago/2026** | **Reunião de Resultados por Squad** (semanal, por squad) | Substituiu os Blocos A/B. O tráfego passa a ser discutido junto com copy, design, social e estrategista |
| **contínuo** | **X1 individual** | Conduzido pela Amanda. Quinzenal com os seniores |
| **contínuo** | **Daily Líderes** (diária, 9h30) | Silvanio + líderes de todas as áreas. É onde entram decisões de pessoal, alocação e processo |
| **abr/2026** | **X1 técnico conduzido pelo Vinicius** | Varredura de CPS conta a conta com Thiago, Wallison e Luiz |
| **jun/2026** | **Orquestradores** | Amanda + Gustavo + Vinicius. Frente de automação e IA |

**O custo dessa densidade:** em agosto um gestor tem 4 reuniões de área + 1 de squad + daily + X1 +
reuniões de cliente na mesma semana. Foi reclamação explícita de Thiago ("você sai da reunião um
pouco mais cansado; para voltar e continuar o trabalho é mais difícil") e de Luciana no squad
Invictus. **É o item de agenda mais fácil de melhorar e o de maior retorno imediato.**

---

## 6. A estrutura do ClickUp — as listas do tráfego

O ClickUp é onde a operação é cobrada e verificada. O que importa em cada lista é **o prazo e a quem a
atividade se aplica** — porque não é a mesma coisa para todos os gestores. **São oito listas:** seis em
operação, uma criada e nunca iniciada, uma em construção. Inventário com status no final da seção.

### Quadro de prazos da área

O resumo para apresentar junto com a estrutura — cada atividade com o seu prazo:

| Atividade | Prazo | Quem |
|---|---|---|
| **Relatório ao cliente** (semana seg–dom) | **Segunda-feira** *(mudou — era sexta da semana seguinte)* | Todos |
| **Checagem de orçamento** | **Diária, de segunda a sexta**, com aprovação da liderança | Todos |
| **Envio de Pix / boleto** | **Data personalizada por cliente** | Só contas que não pagam com cartão |
| **Planilha mestre** | Até **quarta-feira** | Todos |
| **Registro de otimização no Stark OS** | Em até **24h** da ação | Todos |
| **Registro de otimização no ClickUp** (Lista 3) | Ao longo da semana; **revisão na sexta** | Todos |
| **Status Report** | Semanal, registro contínuo | Todos |
| **Atualização de públicos** (video view) | **1× por mês**, no mínimo | Todos, por cliente |
| **Teste de criativos da semana** | Segunda / terça | Todos |
| **Conversão offline em todo BOFU** | **04/09** *(atividade pontual, Lista 2)* | Todos |

### Lista 1 · Controle de Orçamento

Tem um documento próprio descrevendo o processo. Duas atividades:

| Atividade | Prazo | A quem se aplica |
|---|---|---|
| **Envio de Pix / boleto mensal** | **Data personalizada por cliente** — cada conta tem o seu dia | **Só os clientes que não pagam com cartão.** A maioria da carteira é cartão, então a atividade cai para alguns gestores, não para todos |
| **Checagem diária de orçamento** | **Todos os dias, de segunda a sexta** | **Todos os gestores** — cada gestor tem a sua checagem, cobrindo as contas dele |

**O que a checagem diária verifica:** se a conta tem **saldo suficiente** e se o gasto **não passou do
orçamento diário previsto**. Concluída a checagem, o gestor **coloca a tarefa em análise** para a
liderança dar o OK — ou seja, a atividade só fecha com aprovação, não por autodeclaração.

> É a única atividade da área com **cadência diária e revisão da liderança** no mesmo fluxo. Vale
> preservar o desenho: é o mecanismo que evita conta pausada por falta de saldo, que é o erro mais
> caro da operação (reinicia o aprendizado da campanha).

### Lista 2 · Atividades pontuais

**Tudo o que não é recorrente entra aqui.** É a lista que absorve o trabalho que não tem processo
próprio e não cabe na rotina semanal.

| Tipo de atividade | Exemplos |
|---|---|
| **Liberação de acesso** | Acesso ao MCP do Reportei; acesso a conta de cliente no Meta Ads ou no Google Ads; qualquer acesso que não seja parte de um processo formal |
| **Implantação com prazo definido** | "Ativar conversão offline em todos os anúncios" — a diretriz de 13/08 com prazo em 04/09 entrou aqui como atividade pontual |

**Como o prazo funciona nesta lista:** não há cadência fixa — **cada atividade carrega o seu próprio
prazo**, definido na criação. É a diferença fundamental em relação à Lista 1, onde a cadência é a
regra (diária ou data fixa do cliente).

### Lista 3 · Otimização de campanhas

**O registro de tudo o que foi mexido nas contas.** É onde ficam todas as modificações e otimizações
feitas em Meta e Google ao longo da semana.

| | |
|---|---|
| **Prazo / cadência** | Registro ao longo da semana; **revisão da liderança na sexta-feira** |
| **Quem** | Todos os gestores |
| **Fluxo** | O gestor registra e **coloca em revisão**; a liderança confere na sexta se foi feito corretamente — inclusive se a justificativa atende à régua do **"porquê do porquê"** |
| **Estrutura atual** | Uma **atividade-mãe da liderança** com uma **atividade-filha por gestor**, e dentro dela uma subatividade por processo de otimização, de Meta e de Google, **para cada cliente** |
| **Apoio** | A lista tem documentação anexa explicando como o registro deve ser feito |

**Está em transição.** O modelo atual continua valendo, mas há uma **versão 2.0 em construção**, com o
processo bem mais reduzido — a atividade de registro passa a ser a versão resumida da 2.0. Quem
assumir vai encontrar as duas coisas ao mesmo tempo: a lista antiga em uso e a nova sendo montada.

> **Atenção na transição:** este registro é a fonte que sustenta o Status Report, a auditoria de
> liderança e o pilar de metas ligado a otimização. Trocar o modelo sem migrar o histórico deixa um
> buraco justo no período de troca de liderança.

### Lista 4 · Biblioteca de anúncios

**É onde os criativos são solicitados.** O gestor abre a solicitação, ela vai para a **copy**, e o
criativo **volta** para ele subir. Tem documentação na aba de documentos da lista descrevendo o
processo de solicitação.

> ⚠ **Este processo não está otimizado, e a liderança sabe.** Foi criado um processo, depois foi
> criado outro por cima, e a reunião com a **Dani** para consolidar os dois **nunca aconteceu** — a
> pendência atravessou toda a gestão. **Precisa ser revisto com ela.**

É a única das cinco listas em que o próprio dono do processo declara que a documentação vigente não
serve. Para quem assume: não trate a documentação desta lista como fonte confiável antes dessa
conversa.

### Lista 5 · Atualizar públicos

Tem **POP** (procedimento operacional padrão) na aba de documentos da lista.

| | |
|---|---|
| **Atividade** | Atualização dos públicos da conta — **principalmente os públicos de vídeo (video view)** |
| **Prazo / cadência** | **Pelo menos uma vez por mês** |
| **Quem** | Todos os gestores — **uma atividade gerada por cliente**, com o gestor da conta como responsável |
| **Estrutura** | **Tarefa-mãe da liderança**, **tarefa-filha de cada gestor** |
| **Comprovação** | O procedimento exige **informar qual público foi atualizado**, não só marcar como feito |

### Lista 6 · Relatório semanal

Tem **POP** na aba de documentos da lista.

| | |
|---|---|
| **Atividade** | Envio do relatório semanal ao cliente — **uma atividade por cliente**, com o **template** anexo, para o gestor saber exatamente como enviar |
| **Prazo** | **Segunda-feira** *(prazo novo — era sexta da semana seguinte)* |
| **Quem** | Todos os gestores |
| **Comprovação** | **Print.** O gestor envia o relatório conforme o modelo, anexa o print e **coloca em revisão**; a liderança dá o OK confirmando se foi enviado ou não |

> **É daqui que vem a régua "relatório sem print não conta".** Vale saber ao ler os dossiês
> individuais: quando um gestor aparece com "quatro semanas de relatório sem evidência", o que está
> em aberto não é o relatório — é a comprovação exigida por esta lista. A entrega pode ter
> acontecido; sem o print ela é contabilizada como não entregue.

### Lista 7 · Teste Tráfego <sub>criada, nunca iniciada</sub>

**A ideia:** ser o lugar onde os **estrategistas** registram os testes que estão rodando nas contas
**e que fogem do padrão** da área.

**O estado real:** o processo **não foi desenhado** e a lista **não foi iniciada**. Existe no ClickUp e
está vazia.

> Vale conectar com o que foi apresentado ao CEO em 04/08: a proposta dos estrategistas Bruno e Breno
> era exatamente essa — "novos testes a partir da estrutura Andrômeda, gestores documentam, liderança
> monitora". **A lista para isso já existe; o que falta é o processo e alguém puxando.** É a
> oportunidade mais barata da estrutura: o container está pronto.

### Lista 8 · Otimização 2.0 <sub>em construção</sub>

É a substituta da Lista 3. Traz as **atividades resumidas**, já **geradas para cada cliente**, e
**passa a ser a lista de otimização de campanhas** quando entrar em operação.

---

### Inventário e status

| # | Lista | Status |
|---|---|---|
| 1 | **Controle de Orçamento** | Em operação |
| 2 | **Atividades pontuais** | Em operação |
| 3 | **Otimização de campanhas** | Em operação — **será substituída pela 2.0** |
| 4 | **Biblioteca de anúncios** | Em operação, **processo em conflito** (pendência com a Dani) |
| 5 | **Atualizar públicos** | Em operação |
| 6 | **Relatório semanal** | Em operação |
| 7 | **Teste Tráfego** | **Criada, nunca iniciada** — processo não desenhado |
| 8 | **Otimização 2.0** | **Em construção** — assume o lugar da Lista 3 |

### O que vem junto com as listas

**O papel de quem dá o OK.** Quatro listas — Controle de Orçamento, Otimização de campanhas,
Atualizar públicos e Relatório semanal — seguem o mesmo desenho: **tarefa-mãe da liderança +
tarefa-filha por gestor**, com fechamento **em análise / em revisão**, nunca por autodeclaração. Hoje
quem dá o OK é a Head; **esse papel passa para quem assumir**. É o mecanismo de verificação que
sustenta o pilar de metas — as tarefas ficam abertas até alguém aprovar.

**Três listas chegam em obra.** A Biblioteca de anúncios com dois processos sobrepostos, a Otimização
migrando para a versão 2.0 e a Teste Tráfego criada e nunca iniciada. **As três ficam abertas para
decisão de quem assume** — continuar, refazer ou descontinuar. O dossiê registra o estado em que
estão, não o caminho a seguir.

---

## 7. Processos documentados

A área tem **11 processos escritos** (documento "Processos Área de Tráfego", fev/2026, e o Playbook
de Onboarding v1.0, abr/2026). Resumo do que existe e onde está o risco de cada um:

| Processo | Essência | Risco |
|---|---|---|
| **Relatórios via Reportei** | Template Tráfego 2.0 → marco na Linha do Tempo → link no WhatsApp. **Prazo: segunda-feira** (era sexta da semana seguinte) | O módulo de relatórios do Stark OS deve substituir o Reportei — transição não concluída. **O prazo novo é mais curto: o gestor tem o fim de semana a menos** |
| **Recarga de saldo (boleto/PIX)** | Gasto diário × 5 = piso de segurança. PIX quando possível; boleto do Google com antecedência | Conta pausada por falta de saldo reinicia o aprendizado — já aconteceu com vários clientes |
| **Transição de gestor** | 9 etapas no ClickUp. O estrategista é a ponte: se o gestor muda e ele fica, o cliente sente que o "cérebro" continua | Nenhuma transição é oficial sem todas as subetapas concluídas no ClickUp |
| **Onboarding de cliente** | Diagnóstico → Cenário A (conta do zero, CBO 3 públicos) ou B (conteúdo validado, ABO 7 dias) → públicos → funil → criativos da biblioteca | 8 onboards simultâneos na fila em agosto |
| **Onboarding de gestor** | Playbook v1.0: cronograma D+0 a D+10, diagnóstico, públicos padrão, nomenclatura, UTMs, GTM, checklist final | Documento excelente e pouco citado nas reuniões — vale verificar se está de fato em uso |
| **Otimização semanal** | Verificar padronização → analisar ABO de 7–10 dias → escalar em CBO → renovar MOFU/BOFU → registrar no Status Report | Virou registro diário no Stark OS a partir de agosto |
| **Status Report** | Diário oficial da conta no ClickUp: ano > cliente > mês > semana | **Pré-requisito de bonificação.** Registro genérico é invalidado; semana sem registro é contada como não feita |
| **Tracking GTM/GA4/Google Ads** | Container modelo da agência (nunca do zero), 3 variáveis, teste no Tag Assistant, `generate_lead` como conversão | Depende do dev do cliente para instalar o código |
| **Tracking + Respondi** | Importação do container modelo, personalização de variáveis, validação do gatilho | — |
| **ManyChat** | Copy entrega textos e cards → gestor monta fluxo, planilha de leads, gatilhos, teste, documento de gatilhos | Fluxo não sobe sem validação final da copy |
| **Criativos patrocinados** | ClickUp: Agência > Comunicação > Patrocinados. Nome do médico no título é obrigatório; design entrega em "Subir no Ads"; líder designa ao gestor | Em agosto a pasta foi movida para dentro de Conteúdo > Patrocinados > Biblioteca de anúncios |
| **Edição de vídeos patrocinados** | Triagem → tarefa no ClickUp → briefing com checklist → roteiro da copy anexado → validação | Primeiros 3 segundos (hook) são o critério de aprovação |

**A frase que resume a filosofia de processo da área**, do Playbook: *"Padronização precede
refinamento. Performance precede escala. Processo precede sofisticação. Feeling sem estrutura é
chute; feeling com estrutura é expertise."*

---

## 8. Stack e a virada tecnológica de 2026

### O que a área usa

| Ferramenta | Para quê |
|---|---|
| **ClickUp** | Tarefas, Status Report, plano de ação, solicitação de criativo, transições. Migrando para o fluxo 3.1 |
| **Stark OS** | Plataforma própria: dashboard, importação de CSV do Meta, registro de otimizações, metas por cliente, feedbacks, relatórios (em POC) |
| **Reportei** | Relatórios ao cliente e a fonte oficial da variação de seguidores — em substituição gradual pelo OS |
| **Google Sheets** | Planilha mestre / de acompanhamento — substituída por CSV + OS a partir de agosto |
| **Meta Ads / Google Ads (MCC)** | Operação. Estrutura de acessos sempre via BM parceira e MCC da Stark |
| **GTM / GA4** | Rastreamento e prova de atribuição multicanal |
| **ManyChat · Respondi · CRM (GHL, Concierge)** | Captura e qualificação de lead |
| **Claude / Antigravity · MCPs** | Análise, relatório, automação. Sonnet 5 liberado para o time em julho |
| **Star Quest** | Estrategista sugere conteúdo de alto desempenho direto para o tráfego pago |

### O squad de agentes de IA (jun/2026)

Frente conduzida por Gustavo Radler e Vinicius, com repositório próprio (`gestor_trafego_stark`)
rodando localmente nas máquinas dos gestores. Agentes: `alerta_monitor` (monitoramento de contas),
`click_writer` (relatórios), `coletor`, `onboarding`, `publicador`, `redator`, `stark_shift`,
`task_monitor`, `validador`, mais a rotina `rotina_semanal`, capaz de analisar contas e preencher
relatório.

O objetivo declarado: **automatizar o manual para o time se concentrar em otimização e análise.** A
lição operacional registrada na sessão: *observação genérica não serve para a IA* — "cliente crítico"
não é contexto; é preciso descrever características, histórico de incidentes e ações tomadas.

### Stark OS — o item mais importante do handover técnico

- Entrou no ar por volta de **20/07/2026** ("22 dias de existência" em 11/08). Anderson projetou
  estabilidade plena em 10 a 15 dias a partir dali.
- **O score de desempenho do gestor passa a ser calculado pelas interações diárias e pelo
  preenchimento correto dos dados na plataforma.**
- **Janela de 24h:** a otimização deve ser comentada no sistema em até 24 horas. Depois disso o
  registro é aceito, mas marcado como fora do prazo.
- Funciona hoje: dashboard por cliente, importação de CSV do Meta, agrupamento de ajustes por tipo e
  horário, central de notificações, feedbacks com anexo, metas por cliente (inclusive trocar CPS por
  CPL quando o cliente não dá acesso ao Instagram), seleção de moeda, integração GHL.
- Ainda instável em: importação de CSV (a coluna de ID do anúncio desaparece quando se troca o
  período no Meta — falha do próprio Meta), divergência de números por janela de atribuição e atraso
  de 48h nos dados orgânicos, sincronização (cron 2× ao dia, indo para 30 min), prévia de criativo,
  filtros de etapa de funil (a análise de IA não rodou para todos os perfis).
- **Meta declarada ao CEO: 100% da operação dentro do Stark OS até 30/08** — otimizações, seleção de
  criativos, sinalização de testados e relatórios. Nada mais fora da plataforma.

---

## 9. Linha do tempo da área — out/2025 a ago/2026

| Quando | O que aconteceu |
|---|---|
| **set–out/2025** | Checklist Operacional Padrão escrito. Ciclo formal de **PDI & Avaliação** (Mateus e Gustavo). Reunião de feedback comportamental conduzida com o Silvanio |
| **nov–dez/2025** | PDIs de 60 dias em execução, com checkpoint em dezembro |
| **fev/2026** | **Novo sistema de metas (7 pilares)** comunicado. Desligamento de uma gestora por ausência em reuniões de cliente e redistribuição da carteira. Documento **"Processos Área de Tráfego"**. Sprint do Novo Onboarding |
| **mar/2026** | Nova **planilha de acompanhamento** com régua por faixa de orçamento. Auditorias de carteira. **Trilha de Performance Q1 — O Executor** escrita pelo Vinicius |
| **abr/2026** | **Playbook de Onboarding do Gestor v1.0**. X1s técnicos conduzidos pelo Vinicius. Treinamento de Orquestração de IA e de Liderança |
| **mai/2026** | **Método Andrômeda** apresentado e testado (Daily de Testes Andrômeda) |
| **jun/2026** | **Squad de agentes de IA**. Documento "O que a área faz e como o estrategista entra". Contratação da Nicole. Frente de Orquestradores |
| **jul/2026** | **PRA em toda a carteira.** **Stark OS entra no ar.** Regra de gênero (−90% masculino). Formulários condicionais. Carteira do Fábio redistribuída. Promoção do Mateus a Sênior |
| **ago/2026** | **Reorganização em squads de cliente.** Reunião de área 4×/semana. CSV substitui a planilha. Conversão offline obrigatória (prazo 04/09). Meta de 100% no Stark OS até 30/08. Novo método do Lúcio. **Saída da Amanda da liderança (21/08)** |

---

## 10. Gargalos e riscos estruturais

**1. O fundo de funil é o gargalo — e é conhecido.** 44,2% das contas concluíram a adequação de topo,
mas só **9,1% o meio e 6,5% o fundo**. Toda a energia de julho foi para o topo. É onde está o
resultado que o cliente percebe (agendamento) e é a etapa menos padronizada.

**2. A área depende de um dado que não controla.** O ROI de fundo de funil vem do comercial do
cliente, pelo estrategista, a cada 15 dias. Quando Richard questionou a confiabilidade em fevereiro,
a resposta foi honesta: *"a gente tem que confiar no que eles falaram. Não tem outro recurso."* Um
pilar de sete da remuneração do time depende de um dado de terceiro não auditável.

**3. Duas metodologias em paralelo.** Andrômeda + estrutura anterior, até a integração completa de
CRM + pixel. Foi decisão consciente e comunicada ao CEO, mas significa que **o padrão da área hoje
não é único** — e quem assumir vai encontrar contas em dois mundos.

Por trás disso há uma **virada de tese em curso**: cerca de **50 clientes já integrados ao CRM**
(≈30 no modelo Concierge) e **~40 com listas reais** prontas para upload de CSV no pixel, com a
proposta de priorizar **lead qualificado em vez de seguidor barato**. A área foi construída sobre CPS
e está migrando para uma régua de qualificação — as duas convivem hoje.

**4. Andrômeda e o Advantage+ estão gerando reclamação de qualidade de audiência.** É o ponto de
alerta mais recente do método. Com a entrega no automático, chegam **reclamações de seguidores
desqualificados** — gente que segue mas não tem perfil de paciente — e de **seguidores vindos de
localizações erradas**, fora da praça onde o médico opera.

O efeito é perverso para a régua da área: **o CPS melhora enquanto a qualidade da audiência piora.**
Seguidor barato na cidade errada continua contando como seguidor. É a mesma classe de problema que a
área já tentou remediar em julho com a **regra de lance negativo de 90% para público masculino**,
criada justamente para conter entrega e comentário inadequado em campanha Andrômeda — ou seja, o
primeiro remendo já existe, e o problema é maior que ele.

**Por que isso pesa agora:** a virada para qualificação via CRM (risco 3) e essa reclamação apontam
para o mesmo lugar — CPS sozinho não distingue seguidor bom de seguidor ruim. **Quem assumir decide se
mantém o Advantage+ como padrão, se restringe geografia manualmente, ou se troca a régua.** Vale
levantar o volume real de reclamações por conta antes de decidir.

**5. A documentação está atrás da prática — e o CPS é o caso mais grave.** A métrica-mãe da área
mudou de fórmula **e** de meta (de custo total ÷ variação do Reportei, meta R$ 2,59, para custo de
topo ÷ seguidores pagos, meta R$ 2,00), e nenhum dos documentos de método ou de régua foi atualizado:
o documento para estrategistas (jun) traz as bandas antigas, a planilha de mar/2026 calcula o CPS
máximo na base antiga, e o pilar de metas de fev/2026 fixa R$ 2,59. **É a correção mais urgente da
documentação, porque o número que remunera o time depende dela.**

Outros três exemplos do mesmo tipo: o Playbook (abr) proíbe posicionamento **Advantage+ automático**,
enquanto o roteiro Andrômeda (mai) recomenda **Advantage+ de público** como padrão — são coisas
diferentes, mas a leitura conjunta confunde; o Checklist manda avaliar em ciclo de 72h/7 dias, e em
julho a diretriz passou a ser **monitoramento diário** para CBO de verba alta; o Playbook fixa CPS
ideal ≤ R$ 1,50 como referência de anúncio, o que se sobrepõe à meta de conta.
**Nada disso está errado — está apenas em documentos que não conversam.** Consolidar em uma fonte
única é a dívida técnica de processo mais barata de pagar.

**6. O Stark OS é obrigatório, está ligado ao score e ainda é instável.** A combinação exige atenção:
enquanto houver divergência de número no dashboard, cobrar score pelo OS gera contestação legítima.

**7. Registro e comprovação é o gargalo humano recorrente.** Aparece em todo gestor, em todo mês, em
toda régua: print sem data, relatório sem evidência, otimização sem justificativa, link de criativo
ausente. Foi o tema de metade das reuniões de área de agosto. **Não é falta de clareza — é falta de
mecanismo de verificação.**

**8. Conhecimento concentrado em uma pessoa.** CRM e formulário nativo moram no Gustavo; ferramenta e
padrão no Vinicius; o Stark OS no Anderson. Nenhum tem backup formal.

**9. Carteiras desbalanceadas.** Vinicius 17, Luiz 15, Gustavo 15, Thiago 14 — contra Richard 2 e
Nicole 10 (com dois meses de casa). A distribuição não segue senioridade nem complexidade.

**10. Churn e onboarding simultâneos.** Saídas recentes (Rodrigo Gomide, a clínica da Nicole, Marcelo
Santos) e **8 onboards na fila** em agosto. A hipótese registrada para a saída do Rodrigo: falta de
resultado percebido nos três primeiros meses + acompanhamento interrompido. A proposta que saiu
disso: **antecipar o kickoff** para mostrar valor mais rápido e **pesquisa de saída** para todo
cancelamento.

**11. Agenda fragmentada.** Ver seção 6.

**12. A transição de liderança acumula com uma situação de pessoal em aberto.** Na Daily Líderes de
**20/08** foi discutida a situação do **Luiz Eduardo** — ausência em reuniões de cliente, distância,
reclamações de volume de leads em duas contas (Victor Augusto e Luciano Esteves) — e a
**redistribuição das 12 a 14 contas dele** entre Samuel, Nicole, Wallison e Gustavo, com a
possibilidade de saída tratada como cenário real. Isso **atualiza o dossiê individual dele**: até
11/08 o registro era um pedido de mudança de área feito por ele; em 20/08 já havia leitura de
desempenho da liderança e plano de redistribuição em andamento.

---

## 11. Pendências e decisões abertas na data de corte

| Pendência | Dono | Prazo | Situação |
|---|---|---|---|
| **Consolidar o processo de solicitação de criativos com a Dani** | Liderança + Dani | — | Dois processos sobrepostos na Biblioteca de anúncios; a reunião de ajuste nunca aconteceu e atravessou toda a gestão |
| **Atualizar a régua de CPS em toda a documentação** | Liderança | — | Fórmula e meta mudaram (R$ 2,00, custo de topo ÷ seguidores pagos); documento para estrategistas, planilha de acompanhamento e pilar de metas seguem na base antiga |
| **100% da operação no Stark OS** | Gestores + liderança | **30/08** | Meta apresentada ao CEO; migração em curso |
| **Conversão offline em todo BOFU** | Gestores | **04/09** | Combinada em 13/08; não viável em TOFU de perfil |
| **Força-tarefa CRM + pixel** em toda a carteira | Liderança + gestores | "esta semana" (04/08) | ~50 integrados, ~40 com lista pronta para CSV |
| **Avançar meio e fundo no rollout Andrômeda** | Gestores | agosto | Hoje 9,1% e 6,5% |
| **Adequação da estrutura do Gustavo** | Gustavo + liderança | — | Menor adesão do time (35,7%) |
| **Acompanhamento da Nicole** | Liderança | agosto | CPS subiu 25,6%; rotina de feedback e reporte |
| **Situação do Luiz Eduardo** | Silvanio | — | Redistribuição de 12–14 contas; continuidade em avaliação |
| **8 onboards na fila** | Squads | agosto | Exige mobilização de time |
| **Pesquisa de saída para churn** | Estrategistas | — | Proposta aprovada, não implantada |
| **Fonte das otimizações (coluna L — Base Andrômeda)** | Liderança + gestores | "esta semana" (04/08) | Indicador "otimizações dentro do modelo" sem dados até o fechamento |
| **Bots de higienização de lista e validação de relatório** | Liderança | "esta semana" (04/08) | — |
| **Rotina de feedbacks formais (mín. 2/mês, documentados)** | Liderança | contínuo | Compromisso assumido na pauta do CEO |
| **Fluxo ClickUp 3.1** | Daniela + líderes | agosto | Em teste por squad; vídeo de treinamento pendente |

---

## 12. O que está na mesa para quem assume

O que está aberto na data de corte, com a leitura de quem sai. **Todas as decisões abaixo são de quem
assume** — o que segue, o que muda e o que para.

1. **A prioridade que agosto já tinha, e é mensurável:** 100% da operação no Stark OS até 30/08,
   seguindo o método do Lúcio, com verificação gestor a gestor. É o compromisso que a área assumiu
   com o CEO em 04/08 — vale saber que ele existe antes de definir uma prioridade nova.
2. **O gargalo é o fundo de funil, não o topo.** A adequação ao método está em 44,2% no topo, **9,1%
   no meio e 6,5% no fundo**. É onde está o resultado que o cliente sente.
3. **A documentação do CPS é o item mais desatualizado.** A métrica que remunera o time mudou de
   fórmula e de meta (R$ 2,00 sobre custo de topo ÷ seguidores pagos) e a documentação inteira ainda
   descreve a base antiga — documento para estrategistas, planilha de acompanhamento e pilar de
   metas. Playbook, Processos, Checklist e roteiro Andrômeda têm divergências do mesmo tipo, de menor
   impacto.
4. **Enquanto o OS estiver instável, separe cobrança de score de cobrança de entrega.** O time aceita
   a régua; contesta — com razão — número divergente no dashboard.
5. **Reequilibre as carteiras antes de cobrar profundidade.** Vinicius (17) e Gustavo (15) não têm
   como fazer meio e fundo em todas as contas no ritmo pedido.
6. **Reduza a densidade de reunião.** Quatro reuniões de área por semana mais o squad é mais tempo de
   call do que de conta. O pedido já veio do time, por dois caminhos independentes.
7. **Duas decisões de pessoal chegam em aberto** — Luiz Eduardo e o pleito de mérito do Thiago — e as
   duas têm risco real de perda de pessoa. Detalhe em
   [`../dossies-gestores-trafego/`](../dossies-gestores-trafego/README.md).
8. **A qualidade de audiência do Andrômeda está em questionamento** — reclamação de seguidor
   desqualificado e de localização errada, com o Advantage+ no centro. Decisão de método em aberto.
9. **As oito listas do ClickUp são herdadas inteiras**, com o papel de aprovação que quatro delas
   exigem e as três que estão em obra. Nenhuma decisão sobre elas foi tomada por antecipação.

---

## Cobertura das fontes

Este dossiê foi montado a partir de **~70 documentos** do Drive da área, lidos entre out/2025 e
21/08/2026 — as fontes principais estão listadas abaixo. Os X1s individuais e o ciclo de PDI estão
citados no dossiê de pessoas.

**Governança e método**
- [Tráfego Pago — O que a área faz e como o estrategista entra](https://docs.google.com/document/d/1eRobyY_PnYKf4rhx8JZnQUSaHSzScxzR9sHVExBvERc/edit) (jun/2026)
- [Processos Área de Tráfego](https://docs.google.com/document/d/1d2jDoJLuzSpUVhM-OUNUocbXSBD8BIMb_1XDbmexSDQ/edit) (fev/2026) — 11 processos
- [Playbook de Onboarding — Gestor de Tráfego, v1.0](https://drive.google.com/file/d/1ns48HQk4YcipRPSuULE8kP_gmKuDIfxF/view) (abr/2026)
- [Roteiro — Estratégia Meta Andrômeda](https://docs.google.com/document/d/15TEuwIfIn6_azAtXC4DM6aNVbpT-QJ5UMZpevaptVKQ/edit) (mai/2026)
- [Checklist Operacional Padrão](https://docs.google.com/document/d/1Wu9hw-6RuJmM45QQv0nOrFjOQugebJ07m6dRq9ZMNC8/edit) (set/2025)
- [Trilha de Performance — Q1 · O Executor](https://docs.google.com/document/d/1wfP71fOvbfV3P5X_-8o_gsm4H-OvnBtX6FSHSX7CvoQ/edit) (mar/2026)
- [Acompanhamento de Resultados de tráfego — Nova](https://docs.google.com/spreadsheets/d/1tzoqRYkZOcuUPy2z8IZg26bAvc9PlPlgqympn9SdpvE/edit) (mar/2026) — réguas por orçamento

**Resultados e PRA**
- [PAUTA — Reunião de Área · Resultados de Julho/2026 para CEO](https://docs.google.com/document/d/1IwautPi22CZL4ezJKlq_J0TyVX486DWP2AjQOSyQFio/edit) (04/08/2026)
- [Resultados PRA](https://docs.google.com/document/d/1vLD07J8xa7Jfo7eZSsZOt8JmwB0DOpcojn1Ta8QGR50/edit) · [Base PRA por campanha](https://docs.google.com/document/d/1ECa9Hc4N9cokcxMIsvSD7nQ6lrGnD2WeDP4MfS2VK3U/edit) (jul/2026)
- [Alinhamento PRA](https://docs.google.com/document/d/1It9TtmqbxPuMhsHye6luEzJ780hecm1kzfq8sAGDrRU/edit) (22/07/2026)
- [Adequação de Campanhas ao Novo Modelo — Squad](https://docs.google.com/document/d/1QB0r3jbLLt8KyGPwLOccPxXsVsgIqSJTL1cUHOysXtY/edit) (17/07/2026)

**Reuniões de área (agosto/2026)**
- [06/08](https://docs.google.com/document/d/1MTrLfVMa2JDUXPpfKQvHe8ACEa7AHj3xSPUUCK32YCc/edit) · [11/08](https://docs.google.com/document/d/1sh1hPey59eQVhNIWhbGH_96FkEVWDlgWyW92qNRV0DE/edit) · [13/08](https://docs.google.com/document/d/1ezN928_MoL23hHM_iFKIuccFYAFYqChgCsejXdVCmH4/edit) · [18/08](https://docs.google.com/document/d/1Xly5vQFJoSdH70STUmQ04v6R_lv42Z5_Cp7KmCqy2cg/edit) · [20/08](https://docs.google.com/document/d/1DHbHM6YcB71e5fkRUY_PgdaywGZKI6vwycxrXxeYIh0/edit) · [Extraordinária 05/08](https://docs.google.com/document/d/1PueY68NVoYS_OTaajkIaXoOYjJUTIKbUUBMq2H7jqzY/edit)

**Squads (agosto/2026)**
- [A · Invictus 17/08](https://docs.google.com/document/d/16cGuIi6Q2SX2e6H_2DOk7UIKBwr28DVJ6Wu3S7Wajt4/edit) · [B · Os Voldemorts 19/08](https://docs.google.com/document/d/1ov4nXtAqeXkDEcS2zvcXZTt6xLbCSJpf0V-tUbeaNxQ/edit) · [C · JARVIS 19/08](https://docs.google.com/document/d/1iy15m9CyBwuPs1eNvPY6EAjYALNC4Xhw6YZUETV8Xgs/edit) · [ROI-as-unhas 21/08](https://docs.google.com/document/d/14_BmSy3xKykNEmf1eVPyIa3GBs7vz1cKB4FUNESuOaw/edit) · [Café, Caos e Resultado 17/08](https://docs.google.com/document/d/1QuhtE8Q55L13_dWvwD1VH70NzzET0AF1Z_yvuoNh2M4/edit)

**Rituais anteriores e liderança**
- [Daily de Tráfego 06/02/2026](https://docs.google.com/document/d/1S3afkPGMMRfE6st-vEUKp9bcgHPZ3wQQit2rP4Rvotc/edit) — sistema de metas de 7 pilares
- [Reunião de Resultados — Bloco B 02/07/2026](https://docs.google.com/document/d/1C56S_XgWhozRK9QPCamOTBmPWAWfzjFtTuZFcfGl1sU/edit)
- [Squad — Gestores de tráfego 09/06/2026](https://docs.google.com/document/d/1vmoIgCQiuXkfodEqyjyIyufMRNqAAirQsEXVpTENzEU/edit) — squad de agentes de IA
- [Orquestradores 22/06/2026](https://docs.google.com/document/d/1aDJVI20f2LFF0vN1M8ueUL9DzPRy6lc726W6SJk32JM/edit)
- [Daily Líderes 20/08/2026](https://docs.google.com/document/d/1TsXBBWnRsdPjXXLguhLTvAAXXvyM4N02yXUwHHsNo6k/edit)

### O que ficou fora — e por quê

- **~90 Dailies de Tráfego (fev–jul/2026)** e **~20 Acompanhamentos de Resultados Bloco A/B**: lidos
  por amostragem (uma daily de fevereiro, uma reunião de resultados de julho, a daily de Testes
  Andrômeda). São reuniões de execução conta a conta; o padrão e as diretrizes que saíram delas estão
  refletidos aqui, mas **não há garantia de que nenhuma decisão pontual tenha escapado**.
- **~60 documentos de Treinamento de Liderança e Treinamento de Orquestração de IA (mai/2026)**: são
  formações da empresa, não da área de tráfego. Não lidos.
- **Reunião de Área de 04/08**: usada pela pauta escrita (mais completa que as notas do Gemini).
- **Playbooks 1/2/3 da Stark, Playbook de Posicionamento e Playbook TikTok Ads**: identificados no
  Drive, não lidos — o TikTok não aparece na operação atual (só Meta e Google).
- **Reuniões de cliente individuais**: fora de escopo por volume.

Se algum desses blocos importar para a decisão de quem assume, vale uma segunda passada dirigida.
