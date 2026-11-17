# 📋 Gestão Ágil & Engenharia de Requisitos — Sistema MMTADS (Desafio DIO)

Documentação completa de gestão de projeto, levantamento de requisitos, modelagem de processos e garantia de qualidade (QA) aplicada ao **MMTADS** (Sistema de Manutenção de Equipamentos)[cite: 3].

---

## 🎯 Contexto
O projeto foi desenvolvido como entrega prática de um desafio da **DIO (Digital Innovation One)** com o objetivo de estruturar o ciclo de vida de desenvolvimento e testes de uma aplicação web voltada à manutenção de equipamentos (**MMTADS**)[cite: 3]. O cenário envolvia organizar desde a concepção do fluxo de trabalho da equipe até a especificação detalhada das regras de negócio e critérios de qualidade para as primeiras entregas (Sprint)[cite: 1, 2, 5, 6].

## ⚠️ Problema
Em projetos de software sem estruturação prévia, a equipe enfrenta gargalos críticos:
* **Falta de visibilidade:** Ausência de estados claros para acompanhar o progresso das tarefas e a resolução de defeitos (bugs).
* **Ambiguidade nos requisitos:** Regras de negócio mal definidas (como prazos de validade de orçamentos, obrigatoriedade de justificativas e permissões de usuários), gerando retrabalho entre desenvolvimento e validação[cite: 6].
* **Risco de falhas em produção:** Falta de cenários padronizados para validar comportamentos críticos antes da entrega ao usuário final.

## 🛠️ Solução (O que e como foi feito)
Para resolver esses gargalos, estruturei toda a esteira de planejamento, especificação e qualidade utilizando práticas ágeis e ferramentas de gestão:

1. **Modelagem de Fluxos (Workflows no Jira):**
   * **Fluxo de Tarefas:** `A Fazer` ➔ `Em Andamento` ➔ `Pronto` ➔ `Validação` ➔ `Teste` ➔ `Concluído`[cite: 1].
   * **Ciclo de Vida de Bugs:** `Novo` ➔ `Em Progresso` ➔ `Fix` ➔ `Testando` ➔ `Bug-Fixed`[cite: 1].
2. **Especificação de User Stories (`SCRUM-1` e `SCRUM-2`):**
   * Detalhamento de narrativas de usuário, requisitos técnicos, atores, interfaces, regras de negócio e critérios de aceite para os módulos de **Acesso/Autenticação** (Login, Cadastro e Redefinição de Senha) e **Gestão de Orçamentos** (criação em formato `R$`, aprovação/rejeição com motivo obrigatório, histórico auditável e expiração automática em 48h)[cite: 1, 3, 4, 6, 7, 8].
3. **Mapeamento Visual (MindMap):**
   * Construção de um mapa mental centralizando a visão geral, funcionalidades por perfil (Cliente e Funcionário), interfaces, regras adicionais e critérios de aceite do sistema de orçamento[cite: 9].
4. **Engenharia de Qualidade (Casos de Teste & BDD):**
   * Criação de **Casos de Teste Funcionais** passo a passo (`CT-SCRUM2-001` e `CT-SCRUM2-002`) com pré-condições, dados de entrada e resultados esperados[cite: 9, 10].
   * Escrita de cenários em **BDD (Gherkin)** cobrindo fluxos de aprovação, bloqueio de ações duplicadas e rotina de expiração automática de orçamentos[cite: 11, 12].

## 📊 Resultado (Antes x Depois)

| Aspecto | ❌ Antes | ✅ Depois |
| :--- | :--- | :--- |
| **Controle de Demandas** | Tarefas e bugs sem etapas definidas de revisão ou homologação. | Fluxos visuais padronizados separando esteira de **Tarefas** e **Ciclo de Bugs**[cite: 1]. |
| **Regras de Negócio** | Regras implícitas e sujeitas a falhas (ex.: orçamentos abertos indefinidamente). | Documentação formal com regras claras (expiração em 48h, motivo obrigatório de rejeição e histórico de ações)[cite: 6, 8]. |
| **Alinhamento Técnico** | Baixa rastreabilidade entre o que o cliente precisa e o que o dev codifica. | User Stories completas acompanhadas de **MindMap** estruturado por ator e interface[cite: 3, 6, 9]. |
| **Qualidade (QA)** | Testes informais e sem cobertura documentada. | **Casos de Teste** rastreáveis e especificações executáveis em **BDD (Given/When/Then)**[cite: 9, 10, 11, 12]. |

---

### 📂 Estrutura da Documentação
* `01.` Fluxos de Trabalho & Ciclo de Vida de Bugs[cite: 1]
* `02.` Backlog & User Stories (`SCRUM-1` e `SCRUM-2`)[cite: 1, 4]
* `03.` Mapa Mental — Sistema de Orçamento de Solicitações[cite: 9]
* `04.` Plano de Testes Funcionais & Cenários BDD[cite: 9, 11, 12]
