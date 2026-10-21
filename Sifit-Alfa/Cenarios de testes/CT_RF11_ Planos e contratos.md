## Cenário 11: Planos e contratos.

**Módulo:** Comercial  
**Rotas observadas:** `/planos, /modelos-contrato, /adicionar-modelo-contrato`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Cadastro de plano mensal.

| ID / Campo | Descrição |
| --- | --- |
| COM-02 | Verificar o cadastro/cálculo de um plano mensal. |
| Prioridade | P0 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Dados de cadastro e autorizações de teste definidos. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o formulário Novo Plano está aberto |
| **E** é escolhida a modalidade mensal com valores e condições válidos |
| **QUANDO** revisa o resumo e salva conforme fluxo autorizado |
| **ENTÃO** os dados do plano correspondem ao configurado |

| Critérios de aceitação (propostos) |
| --- |
| Condições/valores coerentes e valores inválidos tratados pela validação prevista. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 02: Modelo de contrato e variáveis.

| ID / Campo | Descrição |
| --- | --- |
| COM-03 | Verificar modelo e prévia com variáveis aluno e plano. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Modelo descartável e dados de demonstração necessários. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o editor de Modelo de Contrato está aberto |
| **E** insere `{nome_aluno}` e `{plano_nome}` e atualiza a prévia |
| **QUANDO** salva e verifica a saída correspondente |
| **ENTÃO** a substituição das variáveis é conferida |

| Critérios de aceitação (propostos) |
| --- |
| Variáveis substituídas corretamente quando o documento é gerado; obrigatório validado. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---
