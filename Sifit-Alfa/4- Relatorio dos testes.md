# Relatório de Acompanhamento de Testes — Sifit Alfa

**Situação:** execução em andamento, em 27/10/2026. **Responsável:** Guilherme Morais. **Captura:** Windows 11, Chrome 156.0.8078.48.

Os testes começaram em `sifitalfa.centrion.com.br`. CLI-02, MAT-01 e MAT-02 foram repetidos em `sifit.centrion.com.br`. O [índice de evidências](Evidencias/README.md) guarda os dois vídeos de cada um desses casos.

---

## Resultado até agora

| Planejados | Executados | Aprovados | Reprovados | Bloqueados | Não executados |
| ---: | ---: | ---: | ---: | ---: | ---: |
| 27 | 10 | 8 | 1 | 1 | 17 |

Os dez casos são **distintos**; as três novas gravações são repetições. CLI-02 e MAT-01 passaram na nova URL. MAT-02 falhou porque aceitou período invertido (BUG-002). DASH-01 continua bloqueado por falta de dados de referência. Os outros 17 casos ainda não foram executados.

## Cobertura por módulo

| Código RF | Módulo | Planejados | Executados | Pendentes |
| --- | --- | --- | --- | --- |
| RF01 | Autenticação | 3 | 3 | 0 |
| RF02 | Dashboard | 1 | 1 | 0 |
| RF03 | Clientes | 5 | 4 | 1 |
| RF04 | Matrículas | 2 | 2 | 0 |
| RF05 | Avaliações | 2 | 0 | 2 |
| RF06 | Turmas | 2 | 0 | 2 |
| RF07 | Check-in | 2 | 0 | 2 |
| RF08 | Presenças | 1 | 0 | 1 |
| RF09 | Financeiro | 4 | 0 | 4 |
| RF10 | Treinamento | 1 | 0 | 1 |
| RF11 | Comercial | 2 | 0 | 2 |
| RF12 | Saúde / Anamnese | 2 | 0 | 2 |

## Bugs e evidências

O [relatório de bugs](3-Relatorio-de-Bugs.md) documenta BUG-001 (mensagem de Avaliações no cadastro de matrícula, na URL anterior) e BUG-002 (período invertido aceito na URL nova). Todos os vídeos, inclusive as primeiras tentativas, estão no [índice de evidências](Evidencias/README.md).

## Próximos passos

Conferir DASH-01 com dados de referência, executar os 17 casos restantes e atualizar os resultados e evidências. A conclusão geral fica para o fim da bateria.

## Conclusão provisória

Oito casos passaram, MAT-02 falhou e DASH-01 exige nova verificação. Esses resultados ainda não permitem concluir sobre a estabilidade geral do Sifit Alfa.
