## Cenário 11: Planos e contratos.

**Módulo:** Comercial  
**Rotas observadas:** `/planos, /modelos-contrato, /adicionar-modelo-contrato`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados orientam os testes. Regras de negócio não confirmadas permanecem como hipóteses.

### Caso de Teste 01: Cadastro de plano mensal.

**ID:** COM-02
**Objetivo:** Verificar o cadastro/cálculo de um plano mensal.
**Prioridade:** P0
**Situação:** Não executado

**Pré-condição:** Dados de cadastro e autorizações de teste definidos.

**Passos:**
- **DADO** que o formulário Novo Plano está aberto
- **E** é escolhida a modalidade mensal com valores e condições válidos
- **QUANDO** revisa o resumo e salva conforme fluxo autorizado
- **ENTÃO** os dados do plano correspondem ao configurado

**Resultado esperado:** Condições/valores coerentes e valores inválidos tratados pela validação prevista.

**Execução:** Não executado; sem resultado ou evidência.

---

### Caso de Teste 02: Modelo de contrato e variáveis.

**ID:** COM-03
**Objetivo:** Verificar modelo e prévia com variáveis aluno e plano.
**Prioridade:** P1
**Situação:** Não executado

**Pré-condição:** Modelo descartável e dados de demonstração necessários.

**Passos:**
- **DADO** que o editor de Modelo de Contrato está aberto
- **E** insere `{nome_aluno}` e `{plano_nome}` e atualiza a prévia
- **QUANDO** salva e verifica a saída correspondente
- **ENTÃO** a substituição das variáveis é conferida

**Resultado esperado:** Variáveis substituídas corretamente quando o documento é gerado; obrigatório validado.

**Execução:** Não executado; sem resultado ou evidência.

---
