## Cenário 07: Registro de entrada.

**Módulo:** Check-in  
**Rotas observadas:** `/checkin`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados orientam os testes. Regras de negócio não confirmadas permanecem como hipóteses.

### Caso de Teste 01: Check-in manual válido.

**ID:** CHK-01
**Objetivo:** Registrar entrada de cliente elegível.
**Prioridade:** P0
**Situação:** Não executado

**Pré-condição:** Cliente elegível, código conhecido, unidade e autorização para teste.

**Passos:**
- **DADO** que a tela Check-in está aberta
- **E** a unidade e o código do cliente são selecionados
- **QUANDO** realiza o check-in
- **ENTÃO** o registro aparece no controle de presenças

**Resultado esperado:** Entrada registrada uma vez e refletida em Presenças/indicadores.

**Execução:** Não executado; sem resultado ou evidência.

---

### Caso de Teste 02: Check-in com código inválido ou duplicado.

**ID:** CHK-02
**Objetivo:** Verificar tratamento de código inexistente e entrada repetida.
**Prioridade:** P0
**Situação:** Não executado

**Pré-condição:** Código inexistente e cliente já presente identificados com segurança.

**Passos:**
- **DADO** que a tela Check-in está aberta
- **E** informa código inexistente ou tenta repetir o check-in de cliente já presente
- **QUANDO** confirma a entrada
- **ENTÃO** o sistema dá feedback sem criar presença indevida

**Resultado esperado:** Nenhum registro indevido ou duplicado; mensagem adequada à situação.

**Execução:** Não executado; sem resultado ou evidência.

---
