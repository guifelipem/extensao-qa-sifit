# Relatório de Bugs — Sifit Alfa

**Sistema:** Sifit Alfa  
**Ambiente:** https://sifitalfa.centrion.com.br/dashboard  
**Base do planejamento:** exploração de 20/10/2026  
**Estado:** **2 defeitos confirmados; 10 casos distintos executados ou tentados, 8 aprovados, 1 reprovado, 1 bloqueado e 17 não executados**.

---

## Registro atual

**BUG-001** ocorreu na URL `sifitalfa.centrion.com.br`. **BUG-002** ocorreu na URL `sifit.centrion.com.br`. As tentativas anteriores e as novas execuções foram preservadas separadamente.

## BUG-001 — Mensagem cita Avaliações ao falhar cadastro de Matrícula

| Campo | Registro |
| --- | --- |
| Módulo / caso | Matrículas / MAT-01; URL `sifitalfa.centrion.com.br` |
| Data e ambiente | 27/10/2026; Windows 11; Chrome 156.0.8078.48 |
| Pré-condição | Formulário de nova matrícula aberto para cliente existente. |
| Passos | Selecionar cliente e demais dados do formulário; clicar em Salvar. |
| Resultado esperado | Se o cadastro for rejeitado, a mensagem deve identificar a matrícula e explicar o motivo aplicável. |
| Resultado obtido | A API retornou HTTP 400; o modal mostrou “Não foi possível concluir” e “Erro ao Cadastrar em Avaliações”. |
| Severidade / prioridade | Baixa / P2: mensagem do módulo errado, sem causa funcional determinada. |
| Evidência | [Jam MAT-01](https://jam.dev/c/2f0ded45-dc0c-434b-99ed-993644db0bc5) |
| Situação | Aberto; mensagem confirmada, causa do HTTP 400 a investigar. |

## BUG-002 — Matrícula aceita data final anterior à inicial

| Campo | Registro |
| --- | --- |
| Módulo / caso | Matrículas / MAT-02; URL `sifit.centrion.com.br` |
| Data e ambiente | 27/10/2026; Windows 11; Chrome 156.0.8078.48 |
| Pré-condição | Formulário de nova matrícula aberto, cliente de teste selecionado. |
| Passos | Informar Data Inicial 29/10/2026 e Data Final 27/10/2026; preencher os demais campos e salvar. |
| Resultado esperado | Impedir a matrícula com período invertido e informar o motivo. |
| Resultado obtido | A interface confirmou “Matrícula salva” e abriu a conta a receber de ID 1620. |
| Severidade / prioridade | Média / P1: permite criar registro com intervalo de datas incoerente. |
| Evidência | [Jam MAT-02 na nova URL](https://jam.dev/c/8e8d97e0-154e-4eae-9fc9-a05665f4e883) |
| Situação | Aberto. |

Os seguintes pontos seguem como **investigações**, sem outros defeitos confirmados:

- A opção inicial “Recebido” no modal Nova Conta a Receber (verificar intenção de negócio).
- Estados de carregamento e indicadores transitórios em páginas consultadas (aguardar dados finais).
- Informações Pagar.me com `--` e indicação de carregamento (integração não confirmada).
- [CLI-02: retorno HTTP 500 na tentativa de cadastrar cliente](https://jam.dev/c/38aa65e1-c52e-4235-bd99-c7618584fe7d). O CPF fictício usado não passou na conferência dos dígitos verificadores; repetir com massa válida antes de classificar a falha no fluxo de cadastro. A causa do HTTP 500 não foi determinada.
- [MAT-01 e MAT-02: retornos HTTP 400 ao salvar matrícula](https://jam.dev/c/2f0ded45-dc0c-434b-99ed-993644db0bc5). O motivo da rejeição não foi isolado. BUG-001 cobre apenas a mensagem que menciona Avaliações.

## Estrutura adotada para futuros registros

Quando uma falha real for observada, documentar:

| Campo | Informação necessária |
| --- | --- |
| ID do bug | Identificador atribuído quando surgir um defeito real |
| Caso relacionado | ID do teste que identificou o comportamento |
| Título / módulo | Resumo do problema e tela afetada |
| Pré-condições e passos | Como reproduzir |
| Resultado esperado | Critério previamente confirmado |
| Resultado obtido | Comportamento efetivamente observado |
| Severidade / prioridade | Classificação após análise |
| Evidência | Caminho do print, vídeo ou log real |
| Situação | Status definido no acompanhamento |

Nenhum desses campos é preenchido artificialmente enquanto não houver execução.
