# Checklist — Validação dos Ativos Meta (R1–R6)

Reusa **IT-3.1** (POP-OPR-013 / ATI-3, também ATI-3 do POP-OPR-014 reduzido).
Executor: **Gestor de Tráfego**. Roda em paralelo com a criação da conta no CRM.

**Pré-condição:** o gestor precisa estar como **Administrador no Gerenciador de Negócios
(BM)** do cliente. Sem isso, nenhum passo abaixo é possível.

**Regra:** todos os 6 requisitos devem ser VERDADEIROS antes de o estrategista avançar
para o cadastro do cartão (ATI-4).

---

## Passo 0 — Acessar a BM
- [ ] Abrir `business.facebook.com` com o perfil que tem acesso Admin à BM do cliente
- [ ] Selecionar a BM do cliente no alternador de negócios (se houver mais de uma)

## R1 — Página do Facebook
`Configurações do negócio › Contas › Páginas`
- [ ] Página da empresa listada e sem restrição
- [ ] Se não estiver: Adicionar › Adicionar uma página › vincular à BM

## R2 — Instagram
`Configurações do negócio › Contas › Contas do Instagram`
- [ ] Conta comercial listada e sem restrição
- [ ] Se não aparecer: garantir que a conta é Profissional/Comercial e está vinculada
      à Página; depois adicioná-la à BM

## R3 — WABA (WhatsApp Business Account)
`Configurações do negócio › Contas › Contas do WhatsApp`
- [ ] WABA com o número dedicado do cliente registrado
- [ ] Se não existir: criar a WABA e registrar o número, validando por SMS ou ligação

## R4 — Conta de Anúncios
`Configurações do negócio › Contas › Contas de anúncios`
- [ ] Pelo menos 1 conta ativa e sem restrição
- [ ] Se não houver: criar dentro da BM

## R5 — Verificação da empresa
`Central de Segurança › Verificação da empresa`
- [ ] Status = **Verificado**
- [ ] Se "Em análise": pode seguir em paralelo, mas o encerramento (Handoff) exige Verificado
- [ ] Se a opção de verificação não aparecer: forçar criando um aplicativo dentro da BM
      (`Configurações › Apps`)

## R6 — Varredura de restrições
- [ ] Página — sem aviso, bloqueio ou alerta da Meta
- [ ] Instagram — sem aviso, bloqueio ou alerta
- [ ] WABA — sem aviso, bloqueio ou alerta
- [ ] Conta de Anúncios — sem aviso, bloqueio ou alerta
- [ ] Qualquer ativo com restrição ativa → abrir o recurso na BM, ler o aviso e tratar
      **antes** de avançar

## Comunicação ao cliente — qualidade do número
- [ ] Cliente informado: responder **≥ 80%** das mensagens recebidas
- [ ] Cliente informado: responder a **1ª mensagem em ≤ 24h**

---

## Exceções frequentes

| Situação | Como resolver |
|---|---|
| Opção de verificação não disponível | Forçar criando um aplicativo dentro da BM |
| Instagram não aparece | Conta deve ser Profissional/Comercial e vinculada à Página; depois adicionar à BM |
| Ativo com restrição/aviso | Abrir o ativo, ler o aviso, seguir a contestação da Meta; **não avançar** |
| Verificação travada em "Em análise" | Documentos legíveis + site no ar; > 7 dias úteis → acionar Tecnologia |

---

**RESULTADO:** R1–R6 verdadeiros e sem restrição + cliente informado dos critérios
80% / 24h. Qualquer item reprovado → tratar antes de avançar. Sem exceção.

> ⚠️ Ao final do onboarding, o **Estrategista** remove ou rebaixa o gestor de tráfego da
> posição de Administrador na BM (ATI-10) — só depois de públicos e UTMs concluídos.
