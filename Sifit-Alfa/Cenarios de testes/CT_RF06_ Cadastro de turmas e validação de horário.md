## Cenário 06: Cadastro de turmas e validação de horário.

**Módulo:** Turmas  
**Rotas observadas:** `/turmas`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Cadastro válido de turma.

| ID / Campo | Descrição |
| --- | --- |
| TUR-01 | Criar turma com plano, horários e dias definidos. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Plano de teste disponível e autorização para cadastro. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o cadastro de turma está aberto |
| **E** informa nome, plano, horários e dias válidos |
| **QUANDO** salva o cadastro |
| **ENTÃO** a turma é apresentada na listagem |

| Critérios de aceitação (propostos) |
| --- |
| Turma exibida com horário, dias e status cadastrados. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 02: Horário inválido em turma.

| ID / Campo | Descrição |
| --- | --- |
| TUR-02 | Verificar datas/horários e dias obrigatórios. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Modal de turma aberto. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o cadastro de turma está aberto |
| **E** a hora final é anterior à inicial ou não há seleção de dias |
| **QUANDO** tenta salvar |
| **ENTÃO** a regra de horários/dias é aplicada |

| Critérios de aceitação (propostos) |
| --- |
| Cadastro inválido não persiste e há feedback conforme regras confirmadas. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---
