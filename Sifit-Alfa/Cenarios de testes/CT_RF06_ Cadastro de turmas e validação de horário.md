## Cenário 06: Cadastro de turmas e validação de horário.

**Módulo:** Turmas  
**Rotas observadas:** `/turmas`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados orientam os testes. Regras de negócio não confirmadas permanecem como hipóteses.

### Caso de Teste 01: Cadastro válido de turma.

**ID:** TUR-01
**Objetivo:** Criar turma com plano, horários e dias definidos.
**Prioridade:** P1
**Situação:** Não executado

**Pré-condição:** Plano de teste disponível e autorização para cadastro.

**Passos:**
- **DADO** que o cadastro de turma está aberto
- **E** informa nome, plano, horários e dias válidos
- **QUANDO** salva o cadastro
- **ENTÃO** a turma é apresentada na listagem

**Resultado esperado:** Turma exibida com horário, dias e status cadastrados.

**Execução:** Não executado; sem resultado ou evidência.

---

### Caso de Teste 02: Horário inválido em turma.

**ID:** TUR-02
**Objetivo:** Verificar datas/horários e dias obrigatórios.
**Prioridade:** P1
**Situação:** Não executado

**Pré-condição:** Modal de turma aberto.

**Passos:**
- **DADO** que o cadastro de turma está aberto
- **E** a hora final é anterior à inicial ou não há seleção de dias
- **QUANDO** tenta salvar
- **ENTÃO** a regra de horários/dias é aplicada

**Resultado esperado:** Cadastro inválido não persiste e há feedback conforme regras confirmadas.

**Execução:** Não executado; sem resultado ou evidência.

---
