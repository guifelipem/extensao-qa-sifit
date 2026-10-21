## Cenário 09: Contas a receber e geração de relatórios.

**Módulo:** Financeiro  
**Rotas observadas:** `/contas-receber, /relatorios`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Cadastro de conta a receber.

| ID / Campo | Descrição |
| --- | --- |
| FIN-01 | Criar uma conta pendente de teste e verificar a consulta. |
| Prioridade | P0 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Cliente e forma de pagamento de teste; gravação autorizada sem cobrança real. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que Nova Conta a Receber está aberto |
| **E** informa cliente, valor, vencimento e status pendente |
| **QUANDO** salva e consulta a conta |
| **ENTÃO** a conta aparece no módulo financeiro |

| Critérios de aceitação (propostos) |
| --- |
| Status e valores informados aparecem corretamente; resumo coerente. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 02: Registro de recebimento.

| ID / Campo | Descrição |
| --- | --- |
| FIN-02 | Verificar a atualização de uma conta pendente após recebimento. |
| Prioridade | P0 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Conta pendente descartável de teste e operação autorizada, sem pagamento real. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que há uma conta de teste pendente |
| **QUANDO** registra o recebimento pela operação prevista e consulta o registro |
| **ENTÃO** os dados de recebimento e status são atualizados |

| Critérios de aceitação (propostos) |
| --- |
| Status, valor e data coerentes, sem duplicidade de contabilização. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 03: Validação de valores e datas financeiros.

| ID / Campo | Descrição |
| --- | --- |
| FIN-03 | Testar valor negativo, recebido maior que o devido e data inválida. |
| Prioridade | P0 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Modal Nova Conta aberto, sem transação financeira real. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o cadastro de conta está aberto |
| **E** é inserido valor negativo, recebido maior que o devido ou vencimento inválido |
| **QUANDO** tenta salvar |
| **ENTÃO** a inconsistência é rejeitada ou tratada de acordo com regra formalizada |

| Critérios de aceitação (propostos) |
| --- |
| Sem persistência de lançamento incoerente; regra esperada deve ser confirmada. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 04: Relatório PDF de clientes e contas a receber.

| ID / Campo | Descrição |
| --- | --- |
| FIN-07 | Gerar dois dos sete tipos de relatório disponíveis. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Dados conhecidos no período consultado e permissão de relatório. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que a tela Relatórios está aberta |
| **E** seleciona o relatório de Clientes e um período |
| **QUANDO** gera o PDF e repete com Contas a Receber |
| **ENTÃO** os documentos refletem as consultas escolhidas |

| Critérios de aceitação (propostos) |
| --- |
| PDF abre ou é baixado, com título, intervalo e dados coerentes para os dois modelos. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---
