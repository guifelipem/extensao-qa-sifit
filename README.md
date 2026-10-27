# Testes Manuais — Sifit Alfa

Repositório de **documentação e planejamento de QA funcional** do [Sifit Alfa](https://sifitalfa.centrion.com.br/dashboard), seguindo a organização Markdown do projeto de referência enviado na atividade.

> **Estado atual (27/10/2026):** exploração de interface realizada; **27 casos planejados, 10 executados ou tentados: 8 aprovados, 1 reprovado (MAT-02), 1 bloqueado (DASH-01), 17 não executados e 2 bugs confirmados**. CLI-02, MAT-01 e MAT-02 foram repetidos em outra URL; as tentativas anteriores continuam registradas.

## Objetivo

Organizar a análise exploratória, os requisitos candidatos, o plano de testes e os casos de teste manuais de um sistema de gestão de academia, sem inventar comportamento, evidências, defeitos ou conclusões.

## Estrutura do repositório

```text
sifit-alfa-qa/
├── README.md
└── Sifit-Alfa/
    ├── 0-Relatorio de exploracao.md
    ├── 1-Analise de requisitos.md
    ├── 2-plano de testes.md
    ├── 3-Relatorio-de-Bugs.md
    ├── 4- Relatorio dos testes.md
    ├── 5-Selecao de casos.md
    ├── Cenarios de testes/
    │   └── CT_RF01 ... CT_RF12 (12 arquivos, 27 casos)
    └── Evidencias/
        └── README.md (índice das evidências Jam)
```

## Escopo

A exploração relatou **44 rotas do menu principal**, além de formulários e detalhes adicionais. O levantamento inicial propôs 53 casos. Foram **mantidos 27** e **retirados 26** da bateria atual, com justificativas em `Sifit-Alfa/5-Selecao de casos.md`.

Os casos planejados incluem acesso, painel, clientes, matrículas, avaliações, turmas, check-in, presenças, financeiro, fichas de treino, planos, contratos e anamnese.

## Documentos

- [Relatório de exploração](Sifit-Alfa/0-Relatorio%20de%20exploracao.md)
- [Análise de requisitos candidatos](Sifit-Alfa/1-Analise%20de%20requisitos.md)
- [Plano de testes](Sifit-Alfa/2-plano%20de%20testes.md)
- [Relatório de bugs (BUG-001 e BUG-002)](Sifit-Alfa/3-Relatorio-de-Bugs.md)
- [Relatório de execução (em andamento)](Sifit-Alfa/4-%20Relatorio%20dos%20testes.md)
- [Seleção e exclusões](Sifit-Alfa/5-Selecao%20de%20casos.md)
- [Cenários de testes](Sifit-Alfa/Cenarios%20de%20testes/)

## Metodologia planejada

Exploração visual inicial e testes funcionais manuais com descrições no padrão DADO/E/QUANDO/ENTÃO. Cada caso tem pré-condições, passos resumidos, resultado esperado e campos de execução preenchidos somente após evidência real.

**Atenção ao ambiente:** ações que criam ou alteram dados precisam de autorização e registros descartáveis. Não executar cobranças ou mensagens reais sem ambiente isolado.

## Próximos passos

Conferir DASH-01 com dados de datas conhecidas, acompanhar BUG-001 e BUG-002, executar os 17 casos ainda não realizados e concluir os relatórios somente após a bateria.
