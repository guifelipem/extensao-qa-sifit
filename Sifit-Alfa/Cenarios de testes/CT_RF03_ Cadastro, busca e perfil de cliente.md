## Cenário 03: Cadastro, busca e perfil de cliente.

**Módulo:** Clientes  
**Rotas observadas:** `/clientes, /adicionar-cliente, /visualizar-cliente/408 (rota observada)`  
**Situação:** CLI-01, CLI-02, CLI-03 e CLI-05 passaram em 27/10/2026; CLI-04 não executado. CLI-02 passou na nova URL após tentativa inconclusiva na URL anterior.

> Os resultados esperados orientam os testes. Regras de negócio não confirmadas permanecem como hipóteses.

### Caso de Teste 01: Pesquisa de clientes por nome e código.

**ID:** CLI-01
**Objetivo:** Buscar clientes separadamente por nome e por código.
**Prioridade:** P1
**Situação:** Passou em 27/10/2026

**Pré-condição:** Clientes conhecidos no ambiente de teste, com nome e código disponíveis para conferência.

**Passos:**
- **DADO** que a listagem de Clientes está aberta
- **QUANDO** pesquisa um cliente pelo nome
- **E** limpa a busca e pesquisa outro cliente pelo código
- **ENTÃO** cada resultado corresponde ao termo informado, e a listagem é restaurada entre as buscas

**Resultado esperado:** A busca por nome retorna o cliente correspondente; a busca por código retorna o registro de mesmo código; limpar a primeira busca restaura a listagem. Outros filtros não fazem parte deste caso.

**Resultado observado:** A pesquisa por “Rafael Santos” retornou o registro correspondente. Após limpar a busca, a listagem voltou; a pesquisa pelo código `2` retornou o cliente de código 2. Filtros adicionais não foram usados.
**Evidência:** [Jam CLI-01 — Pesquisa por nome e código](https://jam.dev/c/0932fb55-3358-4b11-bf58-cd634d4523a1)
**Status:** Passou

---

### Caso de Teste 02: Cadastro válido de cliente.

**ID:** CLI-02
**Objetivo:** Cadastrar um cliente fictício com os campos necessários.
**Prioridade:** P1
**Situação:** Passou em 27/10/2026 na nova URL

**Pré-condição:** Autorização para cadastro de dados fictícios e descartáveis.

**Passos:**
- **DADO** que o formulário Novo Cliente está aberto
- **E** os campos obrigatórios estão preenchidos com dados fictícios válidos
- **QUANDO** seleciona Salvar e pesquisa o cadastro
- **ENTÃO** o novo cliente aparece na listagem

**Resultado esperado:** Cliente listado uma única vez com dados e status informados.

**Resultado observado:** Em `sifit.centrion.com.br`, o formulário foi salvo e a listagem passou de 133 para 134 clientes, exibindo o novo cliente com código 427; o perfil `/visualizar-cliente/427` foi aberto. O vídeo não mostra preenchimento de CPF nem confere todos os dados do perfil.
**Evidência:** [Jam CLI-02 — Cadastro na nova URL](https://jam.dev/c/9811d224-f41b-4b86-9279-5218f4690782)
**Status:** Passou para criação e localização do cliente

**Histórico preservado:** na tentativa anterior em `sifitalfa.centrion.com.br`, o [Jam CLI-02](https://jam.dev/c/38aa65e1-c52e-4235-bd99-c7618584fe7d) registrou HTTP 500. O CPF fictício usado nessa tentativa não passou na conferência dos dígitos verificadores; sua causa permanece indeterminada.

---

### Caso de Teste 03: Data de nascimento obrigatória.

**ID:** CLI-03
**Objetivo:** Verificar a validação da data de nascimento obrigatória.
**Prioridade:** P1
**Situação:** Passou em 27/10/2026

**Pré-condição:** Formulário Novo Cliente aberto.

**Passos:**
- **DADO** que o formulário Novo Cliente está aberto
- **E** os demais campos necessários são preenchidos, mas a Data de Nascimento fica vazia
- **QUANDO** tenta salvar
- **ENTÃO** o sistema sinaliza a Data de Nascimento como obrigatória

**Resultado esperado:** Gravação impedida e indicação de que a Data de Nascimento deve ser preenchida. Este caso não cobre os outros campos obrigatórios.

**Resultado observado:** Ao tentar salvar com a Data de Nascimento vazia, o formulário indicou “Preencha a Data de Nascimento” e não concluiu o cadastro.
**Evidência:** [Jam CLI-03 — Data de nascimento obrigatória](https://jam.dev/c/524e6df2-45be-4e84-a6d3-04703926b6cf)
**Status:** Passou

---

### Caso de Teste 04: Formatos inválidos de CPF e e-mail.

**ID:** CLI-04
**Objetivo:** Verificar tratamento de formatos inválidos nos campos do cliente.
**Prioridade:** P1
**Situação:** Não executado

**Pré-condição:** Formulário Novo Cliente aberto.

**Passos:**
- **DADO** que o formulário Novo Cliente está aberto
- **E** são informados CPF e e-mail com formatos inválidos
- **QUANDO** é feita a tentativa de gravação
- **ENTÃO** os valores inválidos não são aceitos como válidos

**Resultado esperado:** Feedback de formato inválido e ausência de persistência de dados inválidos como válidos.

**Execução:** Não executado; sem resultado ou evidência.

---

### Caso de Teste 05: Consulta das seções do perfil de cliente.

**ID:** CLI-05
**Objetivo:** Abrir o perfil de um cliente e consultar as seções relacionadas disponíveis.
**Prioridade:** P1
**Situação:** Passou em 27/10/2026

**Pré-condição:** Cliente existente com perfil acessível.

**Passos:**
- **DADO** que a listagem de Clientes está aberta
- **QUANDO** o usuário abre o detalhe de um cliente e consulta as seções disponíveis
- **ENTÃO** o perfil e as seções relacionadas são exibidos no contexto desse cliente

**Resultado esperado:** Perfil e seções relacionadas abrem no contexto do cliente selecionado. A consistência dos dados com registros de origem requer teste separado.

**Resultado observado:** O perfil do cliente selecionado abriu e exibiu informações de risco, financeiro e histórico de presenças. O histórico mostrou ausência de presenças registradas. A gravação não compara esses dados com registros de origem.
**Evidência:** [Jam CLI-05 — Seções do perfil](https://jam.dev/c/5baee9a4-77c7-4e5e-b0a0-00869685e638)
**Status:** Passou para a consulta das seções

---
