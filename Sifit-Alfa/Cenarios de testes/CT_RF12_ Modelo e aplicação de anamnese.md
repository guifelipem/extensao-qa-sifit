## Cenário 12: Modelo e aplicação de anamnese.

**Módulo:** Saúde / Anamnese  
**Rotas observadas:** `/anamnese/modelos, /anamnese/modelos/novo, /anamneses`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados orientam os testes. Regras de negócio não confirmadas permanecem como hipóteses.

### Caso de Teste 01: Modelo de anamnese com perguntas.

**ID:** SAU-01
**Objetivo:** Criar modelo simples e verificar ordem e obrigatoriedade.
**Prioridade:** P1
**Situação:** Não executado

**Pré-condição:** Perguntas/categoria de teste disponíveis e gravação autorizada.

**Passos:**
- **DADO** que o editor de Modelo de Anamnese está aberto
- **E** seleciona duas ou três perguntas, define ordem e marca obrigatoriedade
- **QUANDO** salva e reabre o modelo
- **ENTÃO** as definições são preservadas

**Resultado esperado:** Ordem/obrigatoriedade persistem; nome obrigatório não pode ficar vazio.

**Execução:** Não executado; sem resultado ou evidência.

---

### Caso de Teste 02: Aplicação de anamnese.

**ID:** SAU-02
**Objetivo:** Vincular respostas de uma ficha ao cliente.
**Prioridade:** P1
**Situação:** Não executado

**Pré-condição:** Cliente e modelo de teste existentes, sem dados pessoais reais de saúde.

**Passos:**
- **DADO** que a tela Nova Anamnese está aberta
- **E** preenche respostas fictícias vinculadas a cliente e modelo de teste
- **QUANDO** conclui a operação autorizada
- **ENTÃO** a ficha corresponde ao cliente e mantém respostas e status

**Resultado esperado:** Respostas preservadas e cliente/modelo/status coerentes.

**Execução:** Não executado; sem resultado ou evidência.

---
