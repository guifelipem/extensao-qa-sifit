# Relatório de Acompanhamento de Testes — Sifit Alfa

**Situação:** execução em andamento (não é relatório final de resultados).
**Base:** exploração de 20/10/2026 e seleção de 27 casos.  
**Execuções registradas:** 27/10/2026, AUT-01, AUT-02, AUT-03, DASH-01, CLI-01, CLI-02, CLI-03, CLI-05, MAT-01 e MAT-02.
**Responsável:** Guilherme Morais (autor do Jam). **Ambiente da captura:** Windows 11, Chrome 156.0.8078.48.

**URLs de execução:** primeiras tentativas em `https://sifitalfa.centrion.com.br`; novas execuções de CLI-02, MAT-01 e MAT-02 em `https://sifit.centrion.com.br`. Os resultados são mantidos por URL no índice de evidências.

---

## Resumo do estado atual

| Planejados | Executados | Aprovados | Reprovados | Bloqueados | Não executados |
| ---: | ---: | ---: | ---: | ---: | ---: |
| 27 | 10 | 8 | 1 | 1 | 17 |

**Interpretar corretamente:** os dez casos são distintos; as novas gravações de CLI-02, MAT-01 e MAT-02 são repetições, não casos adicionais. CLI-02 e MAT-01 passaram na nova URL. MAT-02 falhou porque aceitou período invertido (BUG-002). DASH-01 continua bloqueado por falta de dados de referência. As tentativas inconclusivas na URL anterior foram preservadas, incluindo BUG-001. Os outros 17 casos não foram executados.

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

- **Bugs registrados:** 2 — BUG-001, mensagem de Avaliações no cadastro de Matrícula na URL anterior; BUG-002, período invertido aceito na nova URL.
- **Evidências de execução:** [AUT-01](https://jam.dev/c/0f8a7525-756a-4032-a231-00f3054e6de7), [AUT-02](https://jam.dev/c/8400de22-65e8-403f-8d4d-2a57b766576b), [AUT-03](https://jam.dev/c/aef36c3c-e641-4acb-a8dc-a5b463de65ee), [DASH-01](https://jam.dev/c/dd7f029c-a76d-4415-8cdc-8319cd93a39b), [CLI-01](https://jam.dev/c/0932fb55-3358-4b11-bf58-cd634d4523a1), [CLI-02](https://jam.dev/c/38aa65e1-c52e-4235-bd99-c7618584fe7d), [CLI-03](https://jam.dev/c/524e6df2-45be-4e84-a6d3-04703926b6cf), [CLI-05](https://jam.dev/c/5baee9a4-77c7-4e5e-b0a0-00869685e638), [MAT-01](https://jam.dev/c/2f0ded45-dc0c-434b-99ed-993644db0bc5) e [MAT-02](https://jam.dev/c/d0d8ebf9-700c-4006-b688-3889e19809a8).
- **Novas execuções em `sifit.centrion.com.br`:** [CLI-02 — passou](https://jam.dev/c/9811d224-f41b-4b86-9279-5218f4690782), [MAT-01 — passou](https://jam.dev/c/a271ab64-c64f-459c-8045-063f779c70ed), [MAT-02 — falhou](https://jam.dev/c/8e8d97e0-154e-4eae-9fc9-a05665f4e883). As evidências anteriores permanecem no [índice de evidências](Evidencias/README.md).
- **Resultado consolidado:** oito passaram, MAT-02 falhou e DASH-01 segue bloqueado. Os outros 17 casos não têm execução registrada.

## Pendências para relatório final

- Realizar a bateria autorizada e preencher o resultado real de cada caso.
- Classificar Passou, Falhou, Bloqueado ou Não Executado conforme critério do plano.
- Anexar evidências de execução e registrar os defeitos confirmados.
- Consolidar contagens e redigir conclusão **somente após a execução**.

## Conclusão provisória

A exploração permitiu mapear telas e estruturar 27 casos priorizados. Oito casos passaram, MAT-02 falhou e DASH-01 exige nova verificação. BUG-001 e BUG-002 foram registrados em URLs diferentes. **Ainda não existe base para concluir sobre a estabilidade geral do Sifit Alfa**.
