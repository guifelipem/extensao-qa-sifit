## Cenário 01: Autenticação e controle de acesso.

**Módulo:** Autenticação  
**Rotas observadas:** `/login, /dashboard`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Login com credenciais válidas.

| ID / Campo | Descrição |
| --- | --- |
| AUT-01 | Abrir sessão com credenciais de demonstração válidas. |
| Prioridade | P0 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Credenciais de demonstração válidas e autorização de acesso. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o usuário está na tela de login |
| **E** informa login e senha válidos |
| **QUANDO** seleciona a opção de entrar |
| **ENTÃO** a sessão autenticada abre e o painel/menu ficam disponíveis |

| Critérios de aceitação (propostos) |
| --- |
| Sessão aberta e painel/menu autenticados visíveis. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 02: Bloqueio de acesso sem autenticação.

| ID / Campo | Descrição |
| --- | --- |
| AUT-02 | Impedir o acesso direto a páginas internas sem sessão. |
| Prioridade | P0 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Navegador sem sessão autenticada. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que não há sessão autenticada |
| **QUANDO** o usuário tenta acessar `/dashboard` diretamente |
| **ENTÃO** a aplicação solicita autenticação |

| Critérios de aceitação (propostos) |
| --- |
| Redirecionamento ao login e ausência de exposição de dados internos. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 03: Senha incorreta.

| ID / Campo | Descrição |
| --- | --- |
| AUT-03 | Verificar o tratamento de credencial inválida. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Usuário de demonstração conhecido e sessão encerrada. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o usuário está no login |
| **E** informa identificador válido e senha incorreta |
| **QUANDO** tenta entrar |
| **ENTÃO** o acesso é negado com feedback |

| Critérios de aceitação (propostos) |
| --- |
| Acesso negado, com feedback, sem sessão autenticada. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---
