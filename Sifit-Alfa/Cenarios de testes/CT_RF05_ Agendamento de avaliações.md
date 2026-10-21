## Cenário 05: Agendamento de avaliações.

**Módulo:** Avaliações  
**Rotas observadas:** `/avaliacoes`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Agendamento válido de avaliação.

| ID / Campo | Descrição |
| --- | --- |
| AVA-01 | Agendar avaliação para aluno e personal. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Aluno e personal válidos; permissão para gravar dados de teste. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o modal Cadastrar Avaliação está aberto |
| **E** informa aluno, personal, data e hora válidos |
| **QUANDO** salva o agendamento |
| **ENTÃO** a avaliação aparece para aluno e responsável selecionados |

| Critérios de aceitação (propostos) |
| --- |
| Avaliação registrada como pendente para as partes informadas. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 02: Avaliação com dados inválidos.

| ID / Campo | Descrição |
| --- | --- |
| AVA-02 | Testar falta de aluno/personal ou data/hora inválida. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Modal de avaliação aberto. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o modal de avaliação está aberto |
| **E** há campo essencial não preenchido ou data/hora inválida |
| **QUANDO** tenta salvar |
| **ENTÃO** o sistema apresenta feedback de validação |

| Critérios de aceitação (propostos) |
| --- |
| Sem avaliação inconsistente persistida; validação conforme regra do sistema. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---
