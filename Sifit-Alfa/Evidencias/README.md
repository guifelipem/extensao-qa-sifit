# Evidências de execução

As evidências são mantidas em links para os vídeos Jam. **Dez casos distintos foram executados ou tentados em 27/10/2026; os outros 17 casos ainda não têm execução registrada.** As três novas gravações foram feitas em `https://sifit.centrion.com.br`; as primeiras tentativas ocorreram em `https://sifitalfa.centrion.com.br`.

| Caso | Evidência | Resultado |
| --- | --- | --- |
| AUT-01 | [Jam — Login válido](https://jam.dev/c/0f8a7525-756a-4032-a231-00f3054e6de7) | Passou: navegação de `/login` para `/dashboard` após autenticação. |
| AUT-02 | [Jam — Acesso sem autenticação](https://jam.dev/c/8400de22-65e8-403f-8d4d-2a57b766576b) | Passou: tentativa de acesso a `/dashboard` em janela anônima terminou na tela de login. |
| AUT-03 | [Jam — Login com credenciais inválidas](https://jam.dev/c/aef36c3c-e641-4acb-a8dc-a5b463de65ee) | Passou: acesso negado com mensagem e permanência na tela de login. |
| DASH-01 | [Jam — Filtro por período](https://jam.dev/c/dd7f029c-a76d-4415-8cdc-8319cd93a39b) | Bloqueado para conclusão: indicadores mudaram, mas faltam dados de referência para verificar exatidão. |
| CLI-01 | [Jam — Pesquisa por nome e código](https://jam.dev/c/0932fb55-3358-4b11-bf58-cd634d4523a1) | Passou: busca por nome e por código retornou os clientes correspondentes; a listagem foi restaurada entre as buscas. |
| CLI-02 — primeira tentativa | [Jam — Tentativa de cadastro na URL anterior](https://jam.dev/c/38aa65e1-c52e-4235-bd99-c7618584fe7d) | Inconclusiva: retorno HTTP 500 com CPF fictício que não passou na conferência dos dígitos verificadores. |
| CLI-02 — nova URL | [Jam — Cadastro de cliente concluído](https://jam.dev/c/9811d224-f41b-4b86-9279-5218f4690782) | Passou: cliente criado, listado com código 427 e perfil aberto. |
| CLI-03 | [Jam — Data de nascimento obrigatória](https://jam.dev/c/524e6df2-45be-4e84-a6d3-04703926b6cf) | Passou: formulário exigiu o preenchimento da Data de Nascimento. |
| CLI-05 | [Jam — Seções do perfil](https://jam.dev/c/5baee9a4-77c7-4e5e-b0a0-00869685e638) | Passou para a consulta das seções do perfil; consistência com registros de origem não verificada. |
| MAT-01 — primeira tentativa | [Jam — Tentativa de cadastro na URL anterior](https://jam.dev/c/2f0ded45-dc0c-434b-99ed-993644db0bc5) | Inconclusiva: HTTP 400 ao salvar; mensagem incorreta registrada como BUG-001. |
| MAT-01 — nova URL | [Jam — Matrícula salva](https://jam.dev/c/a271ab64-c64f-459c-8045-063f779c70ed) | Passou: confirmação de matrícula salva e abertura da conta a receber 1619. |
| MAT-02 — primeira tentativa | [Jam — Tentativa com período invertido na URL anterior](https://jam.dev/c/d0d8ebf9-700c-4006-b688-3889e19809a8) | Inconclusiva: HTTP 400 sem confirmação da causa. |
| MAT-02 — nova URL | [Jam — Período invertido aceito](https://jam.dev/c/8e8d97e0-154e-4eae-9fc9-a05665f4e883) | Falhou: matrícula salva com data inicial posterior à final; BUG-002. |

Quando os testes forem realizados, salvar aqui apenas capturas ou documentos reais, referenciando o ID correspondente (por exemplo, `AUT-01` ou `CLI-03`). Não usar imagens ilustrativas como prova de execução.

Evitar registrar senhas, dados pessoais, informações financeiras reais ou dados de saúde de clientes.
