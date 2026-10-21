## Cenário 10: Ficha de treino.

**Módulo:** Treinamento  
**Rotas observadas:** `/fichas-treino, /exercicios`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Cadastro de ficha de treino.

| ID / Campo | Descrição |
| --- | --- |
| TRE-01 | Criar uma ficha com exercícios e consultar pelo cliente. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Cliente e exercícios de teste; cadastro autorizado. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o cadastro de Ficha de Treino está disponível |
| **E** associa cliente e exercícios |
| **QUANDO** salva e pesquisa a ficha |
| **ENTÃO** a ficha cadastrada aparece para o aluno |

| Critérios de aceitação (propostos) |
| --- |
| Ficha exibida com exercícios, validade/status e vínculo corretos. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---
