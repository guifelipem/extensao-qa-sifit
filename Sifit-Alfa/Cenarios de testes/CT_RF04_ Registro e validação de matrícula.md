## Cenário 04: Registro e validação de matrícula.

**Módulo:** Matrículas  
**Rotas observadas:** `/matriculas, /adicionar-matricula`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Cadastro válido de matrícula.

| ID / Campo | Descrição |
| --- | --- |
| MAT-01 | Criar matrícula de teste e verificar seus vínculos. |
| Prioridade | P0 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Cliente, modalidade/plano e tipo de pagamento de teste existentes; autorização para escrita. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o cadastro de matrícula está aberto |
| **E** cliente, modalidade/plano, período e valores válidos são informados |
| **QUANDO** salva a matrícula e consulta seus registros |
| **ENTÃO** a matrícula aparece na listagem e no perfil do cliente |

| Critérios de aceitação (propostos) |
| --- |
| Matrícula e vínculos consistentes com valores e datas informados. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 02: Data ou valor inválido na matrícula.

| ID / Campo | Descrição |
| --- | --- |
| MAT-02 | Verificar tratamento de período invertido ou valor negativo. |
| Prioridade | P0 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Formulário de matrícula aberto, sem efetuar transações reais. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o cadastro de matrícula está aberto |
| **E** a data final é anterior à inicial ou um valor informado é negativo |
| **QUANDO** tenta salvar |
| **ENTÃO** a entrada inválida é impedida ou tratada conforme regra documentada |

| Critérios de aceitação (propostos) |
| --- |
| Nenhum registro com período/valor incoerente; confirmar a regra de negócio antes da avaliação final. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---
