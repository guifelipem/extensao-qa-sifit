# Relatório de Bugs — Sifit Alfa

**Estado:** 2 defeitos confirmados em 27/10/2026. O [relatório de execução](4-%20Relatorio%20dos%20testes.md) reúne os totais dos casos.

---

Os bugs ocorreram em URLs diferentes. As gravações das primeiras tentativas e das novas execuções estão preservadas no [índice de evidências](Evidencias/README.md).

## BUG-001 — Mensagem cita Avaliações ao falhar cadastro de Matrícula

**Onde:** cadastro de matrícula em `sifitalfa.centrion.com.br`, caso MAT-01.

**Como reproduzir:** abrir Nova Matrícula, selecionar um cliente existente, preencher o formulário e salvar.

**Esperado:** se o cadastro for rejeitado, a mensagem deve se referir à matrícula e explicar o motivo aplicável. **Observado:** a API retornou HTTP 400 e o modal mostrou “Não foi possível concluir” com o detalhe “Erro ao Cadastrar em Avaliações”.

**Severidade:** baixa (P2). A mensagem cita o módulo errado; a causa do HTTP 400 ainda não foi determinada. **Situação:** aberto. [Vídeo MAT-01 na URL anterior](https://jam.dev/c/2f0ded45-dc0c-434b-99ed-993644db0bc5).

## BUG-002 — Matrícula aceita data final anterior à inicial

**Onde:** cadastro de matrícula em `sifit.centrion.com.br`, caso MAT-02.

**Como reproduzir:** selecionar um cliente de teste, informar Data Inicial **29/10/2026** e Data Final **27/10/2026**, preencher os demais campos e salvar.

**Esperado:** impedir a matrícula com período invertido e informar o motivo. **Observado:** a interface confirmou “Matrícula salva” e abriu a conta a receber de ID 1620.

**Severidade:** média (P1), pois permite criar um registro com intervalo incoerente. **Situação:** aberto. [Vídeo MAT-02 na nova URL](https://jam.dev/c/8e8d97e0-154e-4eae-9fc9-a05665f4e883).

Os seguintes pontos seguem como **investigações**, sem outros defeitos confirmados:

- A opção inicial “Recebido” no modal Nova Conta a Receber (verificar intenção de negócio).
- Estados de carregamento e indicadores transitórios em páginas consultadas (aguardar dados finais).
- Informações Pagar.me com `--` e indicação de carregamento (integração não confirmada).
- [CLI-02: retorno HTTP 500 na tentativa de cadastrar cliente](https://jam.dev/c/38aa65e1-c52e-4235-bd99-c7618584fe7d). O CPF fictício usado não passou na conferência dos dígitos verificadores; repetir com massa válida antes de classificar a falha no fluxo de cadastro. A causa do HTTP 500 não foi determinada.
- [MAT-01 e MAT-02: retornos HTTP 400 ao salvar matrícula](https://jam.dev/c/2f0ded45-dc0c-434b-99ed-993644db0bc5). O motivo da rejeição não foi isolado. BUG-001 cobre apenas a mensagem que menciona Avaliações.

## Para os próximos registros

Registrar caso e URL, passos para reproduzir, resultado esperado e observado, severidade, situação e link da evidência. Não atribuir causa a erros HTTP sem confirmação.
