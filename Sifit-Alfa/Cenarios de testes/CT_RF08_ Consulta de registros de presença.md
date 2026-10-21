## Cenário 08: Consulta de registros de presença.

**Módulo:** Presenças  
**Rotas observadas:** `/presencas`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Consulta de presenças por período.

| ID / Campo | Descrição |
| --- | --- |
| PRE-01 | Comparar dois períodos conhecidos e os respectivos indicadores. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Presenças de teste conhecidas e sessão autenticada. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que a tela Presenças está aberta |
| **E** seleciona dois períodos com dados conhecidos, um por vez |
| **QUANDO** consulta os resultados |
| **ENTÃO** registros e indicadores acompanham o intervalo escolhido |

| Critérios de aceitação (propostos) |
| --- |
| Registros, total e indicadores correspondem a cada período. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---
