## Cenário 03: Cadastro, busca e perfil de cliente.

**Módulo:** Clientes  
**Rotas observadas:** `/clientes, /adicionar-cliente, /visualizar-cliente/408 (rota observada)`  
**Situação:** CLI-01, CLI-02, CLI-03 e CLI-05 passaram em 27/10/2026; CLI-04 não executado. CLI-02 passou na nova URL após tentativa inconclusiva na URL anterior.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Pesquisa de clientes por nome e código.

| ID / Campo | Descrição |
| --- | --- |
| CLI-01 | Buscar clientes separadamente por nome e por código. |
| Prioridade | P1 |
| Situação | Passou em 27/10/2026 |

| Pré-condições |
| --- |
| Clientes conhecidos no ambiente de teste, com nome e código disponíveis para conferência. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que a listagem de Clientes está aberta |
| **QUANDO** pesquisa um cliente pelo nome |
| **E** limpa a busca e pesquisa outro cliente pelo código |
| **ENTÃO** cada resultado corresponde ao termo informado, e a listagem é restaurada entre as buscas |

| Critérios de aceitação (propostos) |
| --- |
| A busca por nome retorna o cliente correspondente; a busca por código retorna o registro de mesmo código; limpar a primeira busca restaura a listagem. Outros filtros não fazem parte deste caso. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| A pesquisa por “Rafael Santos” retornou o registro correspondente. Após limpar a busca, a listagem voltou; a pesquisa pelo código `2` retornou o cliente de código 2. Filtros adicionais não foram usados. | [Jam CLI-01 — Pesquisa por nome e código](https://jam.dev/c/0932fb55-3358-4b11-bf58-cd634d4523a1) | Passou |

---

### Caso de Teste 02: Cadastro válido de cliente.

| ID / Campo | Descrição |
| --- | --- |
| CLI-02 | Cadastrar um cliente fictício com os campos necessários. |
| Prioridade | P1 |
| Situação | Passou em 27/10/2026 na nova URL |

| Pré-condições |
| --- |
| Autorização para cadastro de dados fictícios e descartáveis. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o formulário Novo Cliente está aberto |
| **E** os campos obrigatórios estão preenchidos com dados fictícios válidos |
| **QUANDO** seleciona Salvar e pesquisa o cadastro |
| **ENTÃO** o novo cliente aparece na listagem |

| Critérios de aceitação (propostos) |
| --- |
| Cliente listado uma única vez com dados e status informados. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Em `sifit.centrion.com.br`, o formulário foi salvo e a listagem passou de 133 para 134 clientes, exibindo o novo cliente com código 427; o perfil `/visualizar-cliente/427` foi aberto. O vídeo não mostra preenchimento de CPF nem confere todos os dados do perfil. | [Jam CLI-02 — Cadastro na nova URL](https://jam.dev/c/9811d224-f41b-4b86-9279-5218f4690782) | Passou para criação e localização do cliente |

**Histórico preservado:** na tentativa anterior em `sifitalfa.centrion.com.br`, o [Jam CLI-02](https://jam.dev/c/38aa65e1-c52e-4235-bd99-c7618584fe7d) registrou HTTP 500. O CPF fictício usado nessa tentativa não passou na conferência dos dígitos verificadores; sua causa permanece indeterminada.

---

### Caso de Teste 03: Data de nascimento obrigatória.

| ID / Campo | Descrição |
| --- | --- |
| CLI-03 | Verificar a validação da data de nascimento obrigatória. |
| Prioridade | P1 |
| Situação | Passou em 27/10/2026 |

| Pré-condições |
| --- |
| Formulário Novo Cliente aberto. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o formulário Novo Cliente está aberto |
| **E** os demais campos necessários são preenchidos, mas a Data de Nascimento fica vazia |
| **QUANDO** tenta salvar |
| **ENTÃO** o sistema sinaliza a Data de Nascimento como obrigatória |

| Critérios de aceitação (propostos) |
| --- |
| Gravação impedida e indicação de que a Data de Nascimento deve ser preenchida. Este caso não cobre os outros campos obrigatórios. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Ao tentar salvar com a Data de Nascimento vazia, o formulário indicou “Preencha a Data de Nascimento” e não concluiu o cadastro. | [Jam CLI-03 — Data de nascimento obrigatória](https://jam.dev/c/524e6df2-45be-4e84-a6d3-04703926b6cf) | Passou |

---

### Caso de Teste 04: Formatos inválidos de CPF e e-mail.

| ID / Campo | Descrição |
| --- | --- |
| CLI-04 | Verificar tratamento de formatos inválidos nos campos do cliente. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Formulário Novo Cliente aberto. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o formulário Novo Cliente está aberto |
| **E** são informados CPF e e-mail com formatos inválidos |
| **QUANDO** é feita a tentativa de gravação |
| **ENTÃO** os valores inválidos não são aceitos como válidos |

| Critérios de aceitação (propostos) |
| --- |
| Feedback de formato inválido e ausência de persistência de dados inválidos como válidos. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 05: Consulta das seções do perfil de cliente.

| ID / Campo | Descrição |
| --- | --- |
| CLI-05 | Abrir o perfil de um cliente e consultar as seções relacionadas disponíveis. |
| Prioridade | P1 |
| Situação | Passou em 27/10/2026 |

| Pré-condições |
| --- |
| Cliente existente com perfil acessível. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que a listagem de Clientes está aberta |
| **QUANDO** o usuário abre o detalhe de um cliente e consulta as seções disponíveis |
| **ENTÃO** o perfil e as seções relacionadas são exibidos no contexto desse cliente |

| Critérios de aceitação (propostos) |
| --- |
| Perfil e seções relacionadas abrem no contexto do cliente selecionado. A consistência dos dados com registros de origem requer teste separado. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| O perfil do cliente selecionado abriu e exibiu informações de risco, financeiro e histórico de presenças. O histórico mostrou ausência de presenças registradas. A gravação não compara esses dados com registros de origem. | [Jam CLI-05 — Seções do perfil](https://jam.dev/c/5baee9a4-77c7-4e5e-b0a0-00869685e638) | Passou para a consulta das seções |

---
