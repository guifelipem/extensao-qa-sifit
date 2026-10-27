## Cenário 04: Registro e validação de matrícula.

**Módulo:** Matrículas  
**Rotas observadas:** `/matriculas, /adicionar-matricula`  
**Situação:** na nova URL, MAT-01 passou e MAT-02 falhou em 27/10/2026. As tentativas anteriores na URL antiga permanecem documentadas.

> Os resultados esperados orientam os testes. Regras de negócio não confirmadas permanecem como hipóteses.

### Caso de Teste 01: Criação de matrícula e conta a receber vinculada.

**ID:** MAT-01
**Objetivo:** Criar matrícula de teste e verificar a confirmação e a conta a receber aberta no fluxo.
**Prioridade:** P0
**Situação:** Passou em 27/10/2026 na nova URL

**Pré-condição:** Cliente, modalidade/plano e tipo de pagamento de teste existentes; autorização para escrita.

**Passos:**
- **DADO** que o cadastro de matrícula está aberto
- **E** cliente, modalidade/plano, período e valores válidos são informados
- **QUANDO** salva a matrícula
- **ENTÃO** a criação é confirmada e o fluxo abre a conta a receber vinculada

**Resultado esperado:** Confirmação de matrícula salva e abertura da conta a receber do cliente selecionado. Conferência na listagem e no perfil requer teste separado.

**Resultado observado:** Em `sifit.centrion.com.br`, após salvar, a interface exibiu “Matrícula salva” e abriu uma conta a receber vinculada ao cliente, com ID 1619. A gravação não confere a matrícula na listagem nem no perfil do cliente.
**Evidência:** [Jam MAT-01 — Matrícula salva na nova URL](https://jam.dev/c/a271ab64-c64f-459c-8045-063f779c70ed)
**Status:** Passou para criação da matrícula; conferência na listagem/perfil não realizada

**Histórico preservado:** na tentativa anterior em `sifitalfa.centrion.com.br`, o [Jam MAT-01](https://jam.dev/c/2f0ded45-dc0c-434b-99ed-993644db0bc5) registrou HTTP 400 e mensagem que citava Avaliações (BUG-001). A causa da rejeição não foi isolada.

---

### Caso de Teste 02: Período invertido na matrícula.

**ID:** MAT-02
**Objetivo:** Verificar se a data final anterior à inicial é rejeitada.
**Prioridade:** P0
**Situação:** Falhou em 27/10/2026 na nova URL — BUG-002

**Pré-condição:** Formulário de matrícula aberto, sem efetuar transações reais.

**Passos:**
- **DADO** que o cadastro de matrícula está aberto
- **E** a data final é anterior à inicial
- **QUANDO** tenta salvar
- **ENTÃO** a matrícula com período invertido é impedida com uma mensagem explicativa

**Resultado esperado:** Nenhuma matrícula com data final anterior à inicial é salva. Valor negativo não faz parte desta execução.

**Resultado observado:** Em `sifit.centrion.com.br`, o formulário mostrou Data Inicial 29/10/2026 e Data Final 27/10/2026. Após salvar, apareceu “Matrícula salva” e o fluxo abriu a conta a receber de ID 1620. A ordem inválida não foi impedida.
**Evidência:** [Jam MAT-02 — Período invertido aceito na nova URL](https://jam.dev/c/8e8d97e0-154e-4eae-9fc9-a05665f4e883)
**Status:** Falhou — BUG-002

**Histórico preservado:** na tentativa anterior em `sifitalfa.centrion.com.br`, o [Jam MAT-02](https://jam.dev/c/d0d8ebf9-700c-4006-b688-3889e19809a8) registrou HTTP 400 sem permitir atribuir a rejeição especificamente à ordem das datas.

---
