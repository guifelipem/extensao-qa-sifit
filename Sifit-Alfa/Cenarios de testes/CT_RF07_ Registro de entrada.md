## Cenário 07: Registro de entrada.

**Módulo:** Check-in  
**Rotas observadas:** `/checkin`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Check-in manual válido.

| ID / Campo | Descrição |
| --- | --- |
| CHK-01 | Registrar entrada de cliente elegível. |
| Prioridade | P0 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Cliente elegível, código conhecido, unidade e autorização para teste. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que a tela Check-in está aberta |
| **E** a unidade e o código do cliente são selecionados |
| **QUANDO** realiza o check-in |
| **ENTÃO** o registro aparece no controle de presenças |

| Critérios de aceitação (propostos) |
| --- |
| Entrada registrada uma vez e refletida em Presenças/indicadores. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 02: Check-in com código inválido ou duplicado.

| ID / Campo | Descrição |
| --- | --- |
| CHK-02 | Verificar tratamento de código inexistente e entrada repetida. |
| Prioridade | P0 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Código inexistente e cliente já presente identificados com segurança. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que a tela Check-in está aberta |
| **E** informa código inexistente ou tenta repetir o check-in de cliente já presente |
| **QUANDO** confirma a entrada |
| **ENTÃO** o sistema dá feedback sem criar presença indevida |

| Critérios de aceitação (propostos) |
| --- |
| Nenhum registro indevido ou duplicado; mensagem adequada à situação. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---
