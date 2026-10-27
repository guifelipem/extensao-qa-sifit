## Cenário 02: Página Inicial.

**Módulo:** Dashboard  
**Rotas observadas:** `/dashboard`  
**Situação:** DASH-01 executado em 27/10/2026; validação dos valores pendente por falta de dados de referência.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Consulta por período no painel.

| ID / Campo | Descrição |
| --- | --- |
| DASH-01 | Consultar indicadores por intervalo selecionado. |
| Prioridade | P1 |
| Situação | Bloqueado em 27/10/2026 para conclusão do critério completo |

| Pré-condições |
| --- |
| Sessão válida e dados de datas conhecidas. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que a Página Inicial está aberta |
| **E** o usuário altera o período de consulta |
| **QUANDO** aciona a busca |
| **ENTÃO** os indicadores e as listas correspondem ao período selecionado |

| Critérios de aceitação (propostos) |
| --- |
| Indicadores e listas coerentes com o período selecionado. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| O período foi alterado e os indicadores visíveis mudaram (por exemplo, matrículas no período: 4 para 0; desistências no período: 3 para 2). A gravação não compara os valores com registros de datas conhecidas nem comprova a coerência de todas as listas. | [Jam DASH-01 — Filtro por período](https://jam.dev/c/dd7f029c-a76d-4415-8cdc-8319cd93a39b) | Bloqueado: falta base de dados conhecida para validar a exatidão |

---
