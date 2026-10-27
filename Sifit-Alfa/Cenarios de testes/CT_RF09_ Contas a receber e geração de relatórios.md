## Cenário 09: Contas a receber e geração de relatórios.

**Módulo:** Financeiro  
**Rotas observadas:** `/contas-receber, /relatorios`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados orientam os testes. Regras de negócio não confirmadas permanecem como hipóteses.

### Caso de Teste 01: Cadastro de conta a receber.

**ID:** FIN-01
**Objetivo:** Criar uma conta pendente de teste e verificar a consulta.
**Prioridade:** P0
**Situação:** Não executado

**Pré-condição:** Cliente e forma de pagamento de teste; gravação autorizada sem cobrança real.

**Passos:**
- **DADO** que Nova Conta a Receber está aberto
- **E** informa cliente, valor, vencimento e status pendente
- **QUANDO** salva e consulta a conta
- **ENTÃO** a conta aparece no módulo financeiro

**Resultado esperado:** Status e valores informados aparecem corretamente; resumo coerente.

**Execução:** Não executado; sem resultado ou evidência.

---

### Caso de Teste 02: Registro de recebimento.

**ID:** FIN-02
**Objetivo:** Verificar a atualização de uma conta pendente após recebimento.
**Prioridade:** P0
**Situação:** Não executado

**Pré-condição:** Conta pendente descartável de teste e operação autorizada, sem pagamento real.

**Passos:**
- **DADO** que há uma conta de teste pendente
- **QUANDO** registra o recebimento pela operação prevista e consulta o registro
- **ENTÃO** os dados de recebimento e status são atualizados

**Resultado esperado:** Status, valor e data coerentes, sem duplicidade de contabilização.

**Execução:** Não executado; sem resultado ou evidência.

---

### Caso de Teste 03: Validação de valores e datas financeiros.

**ID:** FIN-03
**Objetivo:** Testar valor negativo, recebido maior que o devido e data inválida.
**Prioridade:** P0
**Situação:** Não executado

**Pré-condição:** Modal Nova Conta aberto, sem transação financeira real.

**Passos:**
- **DADO** que o cadastro de conta está aberto
- **E** é inserido valor negativo, recebido maior que o devido ou vencimento inválido
- **QUANDO** tenta salvar
- **ENTÃO** a inconsistência é rejeitada ou tratada de acordo com regra formalizada

**Resultado esperado:** Sem persistência de lançamento incoerente; regra esperada deve ser confirmada.

**Execução:** Não executado; sem resultado ou evidência.

---

### Caso de Teste 04: Relatório PDF de clientes e contas a receber.

**ID:** FIN-07
**Objetivo:** Gerar dois dos sete tipos de relatório disponíveis.
**Prioridade:** P1
**Situação:** Não executado

**Pré-condição:** Dados conhecidos no período consultado e permissão de relatório.

**Passos:**
- **DADO** que a tela Relatórios está aberta
- **E** seleciona o relatório de Clientes e um período
- **QUANDO** gera o PDF e repete com Contas a Receber
- **ENTÃO** os documentos refletem as consultas escolhidas

**Resultado esperado:** PDF abre ou é baixado, com título, intervalo e dados coerentes para os dois modelos.

**Execução:** Não executado; sem resultado ou evidência.

---
