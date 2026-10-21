## Cenário 03: Cadastro, busca e perfil de cliente.

**Módulo:** Clientes  
**Rotas observadas:** `/clientes, /adicionar-cliente, /visualizar-cliente/408 (rota observada)`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Pesquisa e filtros de clientes.

| ID / Campo | Descrição |
| --- | --- |
| CLI-01 | Buscar clientes por código/nome e combinar filtros. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Clientes conhecidos no ambiente de teste. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que a listagem de Clientes está aberta |
| **E** aplica busca por código e por nome, além de filtros disponíveis |
| **QUANDO** consulta os resultados e limpa os filtros |
| **ENTÃO** os registros correspondem aos critérios e a listagem é restaurada |

| Critérios de aceitação (propostos) |
| --- |
| Somente registros compatíveis; limpeza restaura a listagem. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 02: Cadastro válido de cliente.

| ID / Campo | Descrição |
| --- | --- |
| CLI-02 | Cadastrar um cliente fictício com os campos necessários. |
| Prioridade | P1 |
| Situação | Não executado |

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
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 03: Campos obrigatórios sem preenchimento.

| ID / Campo | Descrição |
| --- | --- |
| CLI-03 | Verificar validação dos campos marcados como obrigatórios. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Formulário Novo Cliente aberto. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o formulário Novo Cliente está aberto |
| **E** Nome, Sexo ou Data de Nascimento é deixado sem valor |
| **QUANDO** tenta salvar |
| **ENTÃO** o sistema sinaliza o preenchimento obrigatório |

| Critérios de aceitação (propostos) |
| --- |
| Gravação impedida e indicação dos campos faltantes. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

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

### Caso de Teste 05: Vínculos do perfil de cliente.

| ID / Campo | Descrição |
| --- | --- |
| CLI-05 | Consultar informações relacionadas a um único cliente. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Cliente existente com informações relacionadas disponíveis. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que a listagem de Clientes está aberta |
| **QUANDO** o usuário abre o detalhe de um cliente e consulta perfil, matrícula, presenças e financeiro |
| **ENTÃO** cada seção corresponde ao cliente consultado |

| Critérios de aceitação (propostos) |
| --- |
| Seções vinculadas ao cliente correto e coerentes com os registros existentes. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---
