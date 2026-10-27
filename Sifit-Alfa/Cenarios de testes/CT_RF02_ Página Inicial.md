## Cenário 02: Página Inicial.

**Módulo:** Dashboard  
**Rotas observadas:** `/dashboard`  
**Situação:** DASH-01 executado em 27/10/2026; validação dos valores pendente por falta de dados de referência.

> Os resultados esperados orientam os testes. Regras de negócio não confirmadas permanecem como hipóteses.

### Caso de Teste 01: Consulta por período no painel.

**ID:** DASH-01
**Objetivo:** Consultar indicadores por intervalo selecionado.
**Prioridade:** P1
**Situação:** Bloqueado em 27/10/2026 para conclusão do critério completo

**Pré-condição:** Sessão válida e dados de datas conhecidas.

**Passos:**
- **DADO** que a Página Inicial está aberta
- **E** o usuário altera o período de consulta
- **QUANDO** aciona a busca
- **ENTÃO** os indicadores e as listas correspondem ao período selecionado

**Resultado esperado:** Indicadores e listas coerentes com o período selecionado.

**Resultado observado:** O período foi alterado e os indicadores visíveis mudaram (por exemplo, matrículas no período: 4 para 0; desistências no período: 3 para 2). A gravação não compara os valores com registros de datas conhecidas nem comprova a coerência de todas as listas.
**Evidência:** [Jam DASH-01 — Filtro por período](https://jam.dev/c/dd7f029c-a76d-4415-8cdc-8319cd93a39b)
**Status:** Bloqueado: falta base de dados conhecida para validar a exatidão

---
