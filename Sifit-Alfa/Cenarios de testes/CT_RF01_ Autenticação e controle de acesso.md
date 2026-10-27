## Cenário 01: Autenticação e controle de acesso.

**Módulo:** Autenticação  
**Rotas observadas:** `/login, /dashboard`  
**Situação:** AUT-01, AUT-02 e AUT-03 executados em 27/10/2026.

> Os resultados esperados orientam os testes. Regras de negócio não confirmadas permanecem como hipóteses.

### Caso de Teste 01: Login com credenciais válidas.

**ID:** AUT-01
**Objetivo:** Abrir sessão com credenciais de demonstração válidas.
**Prioridade:** P0
**Situação:** Passou em 27/10/2026

**Pré-condição:** Credenciais de demonstração válidas e autorização de acesso.

**Passos:**
- **DADO** que o usuário está na tela de login
- **E** informa login e senha válidos
- **QUANDO** seleciona a opção de entrar
- **ENTÃO** a sessão autenticada abre e o painel/menu ficam disponíveis

**Resultado esperado:** Sessão aberta e painel/menu autenticados visíveis.

**Resultado observado:** Após informar as credenciais válidas e clicar em Entrar, a aplicação navegou de `/login` para `/dashboard`.
**Evidência:** [Jam AUT-01 — Login válido](https://jam.dev/c/0f8a7525-756a-4032-a231-00f3054e6de7)
**Status:** Passou

---

### Caso de Teste 02: Bloqueio de acesso sem autenticação.

**ID:** AUT-02
**Objetivo:** Impedir o acesso direto a páginas internas sem sessão.
**Prioridade:** P0
**Situação:** Passou em 27/10/2026

**Pré-condição:** Navegador sem sessão autenticada.

**Passos:**
- **DADO** que não há sessão autenticada
- **QUANDO** o usuário tenta acessar `/dashboard` diretamente
- **ENTÃO** a aplicação solicita autenticação

**Resultado esperado:** Redirecionamento ao login e ausência de exposição de dados internos.

**Resultado observado:** Em janela anônima, a tentativa de abrir `/dashboard` terminou na tela de login, sem exibir o painel interno.
**Evidência:** [Jam AUT-02 — Acesso sem autenticação](https://jam.dev/c/8400de22-65e8-403f-8d4d-2a57b766576b)
**Status:** Passou

---

### Caso de Teste 03: Senha incorreta.

**ID:** AUT-03
**Objetivo:** Verificar o tratamento de credencial inválida.
**Prioridade:** P1
**Situação:** Passou em 27/10/2026

**Pré-condição:** Usuário de demonstração conhecido e sessão encerrada.

**Passos:**
- **DADO** que o usuário está no login
- **E** informa identificador válido e senha incorreta
- **QUANDO** tenta entrar
- **ENTÃO** o acesso é negado com feedback

**Resultado esperado:** Acesso negado, com feedback, sem sessão autenticada.

**Resultado observado:** Após tentar entrar com senha incorreta, a tela de login permaneceu aberta e exibiu a mensagem “O nome de usuário e senha não correspondem.”
**Evidência:** [Jam AUT-03 — Login com credenciais inválidas](https://jam.dev/c/aef36c3c-e641-4acb-a8dc-a5b463de65ee)
**Status:** Passou

---
