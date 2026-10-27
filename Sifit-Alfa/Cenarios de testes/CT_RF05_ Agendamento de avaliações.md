## Cenário 05: Agendamento de avaliações.

**Módulo:** Avaliações  
**Rotas observadas:** `/avaliacoes`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados orientam os testes. Regras de negócio não confirmadas permanecem como hipóteses.

### Caso de Teste 01: Agendamento válido de avaliação.

**ID:** AVA-01
**Objetivo:** Agendar avaliação para aluno e personal.
**Prioridade:** P1
**Situação:** Não executado

**Pré-condição:** Aluno e personal válidos; permissão para gravar dados de teste.

**Passos:**
- **DADO** que o modal Cadastrar Avaliação está aberto
- **E** informa aluno, personal, data e hora válidos
- **QUANDO** salva o agendamento
- **ENTÃO** a avaliação aparece para aluno e responsável selecionados

**Resultado esperado:** Avaliação registrada como pendente para as partes informadas.

**Execução:** Não executado; sem resultado ou evidência.

---

### Caso de Teste 02: Avaliação com dados inválidos.

**ID:** AVA-02
**Objetivo:** Testar falta de aluno/personal ou data/hora inválida.
**Prioridade:** P1
**Situação:** Não executado

**Pré-condição:** Modal de avaliação aberto.

**Passos:**
- **DADO** que o modal de avaliação está aberto
- **E** há campo essencial não preenchido ou data/hora inválida
- **QUANDO** tenta salvar
- **ENTÃO** o sistema apresenta feedback de validação

**Resultado esperado:** Sem avaliação inconsistente persistida; validação conforme regra do sistema.

**Execução:** Não executado; sem resultado ou evidência.

---
