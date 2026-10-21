## Cenário 12: Modelo e aplicação de anamnese.

**Módulo:** Saúde / Anamnese  
**Rotas observadas:** `/anamnese/modelos, /anamnese/modelos/novo, /anamneses`  
**Situação:** planejamento; nenhum caso executado formalmente.

> Os resultados esperados são hipóteses de teste baseadas na interface, ainda dependentes de execução e, quando necessário, confirmação das regras de negócio.

### Caso de Teste 01: Modelo de anamnese com perguntas.

| ID / Campo | Descrição |
| --- | --- |
| SAU-01 | Criar modelo simples e verificar ordem e obrigatoriedade. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Perguntas/categoria de teste disponíveis e gravação autorizada. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que o editor de Modelo de Anamnese está aberto |
| **E** seleciona duas ou três perguntas, define ordem e marca obrigatoriedade |
| **QUANDO** salva e reabre o modelo |
| **ENTÃO** as definições são preservadas |

| Critérios de aceitação (propostos) |
| --- |
| Ordem/obrigatoriedade persistem; nome obrigatório não pode ficar vazio. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---

### Caso de Teste 02: Aplicação de anamnese.

| ID / Campo | Descrição |
| --- | --- |
| SAU-02 | Vincular respostas de uma ficha ao cliente. |
| Prioridade | P1 |
| Situação | Não executado |

| Pré-condições |
| --- |
| Cliente e modelo de teste existentes, sem dados pessoais reais de saúde. |

| Passos (BDD / Gherkin simplificado) |
| --- |
| **DADO** que a tela Nova Anamnese está aberta |
| **E** preenche respostas fictícias vinculadas a cliente e modelo de teste |
| **QUANDO** conclui a operação autorizada |
| **ENTÃO** a ficha corresponde ao cliente e mantém respostas e status |

| Critérios de aceitação (propostos) |
| --- |
| Respostas preservadas e cliente/modelo/status coerentes. |

| Resultado obtido | Evidência | Status de execução |
| --- | --- | --- |
| Não registrado | Não anexada | Não executado |

---
