## **Plano de Testes — Sifit Alfa (Demo)**

### 1. **Identificação**

- **Nome do projeto:** QA funcional do Sifit Alfa (gestão de academia).
- **Ambiente observado:** https://sifitalfa.centrion.com.br/dashboard
- **Tipo de teste planejado:** testes funcionais manuais com evidência por caso.
- **Exploração:** 20/10/2026 (America/Sao_Paulo).
- **Versão da aplicação:** não identificada no relatório de exploração.
- **Responsável pela execução e datas futuras:** ainda não definidos.
- **Status:** planejamento concluído; **nenhum caso executado formalmente**.

---

### 2. **Objetivo**

Validar um recorte representativo das principais funcionalidades identificadas na exploração do Sifit Alfa, com foco em acesso, cadastros, regras de validação, operações de academia, consistência financeira e consultas.

---

### 3. **Escopo**

**Incluído:** 27 casos dos módulos Autenticação, Página Inicial, Clientes, Matrículas, Avaliações, Turmas, Check-in, Presenças, Financeiro (Contas a Receber e dois relatórios em PDF), Treinamento (Ficha), Comercial (Plano mensal/Contrato) e Anamnese.

**Excluído desta etapa:** 26 casos identificados na seleção, incluindo navegação ampla já mapeada, cadastros auxiliares, caixa, contas a pagar, SifitBox, integração Pagar.me, automações, mudanças globais de configuração e notificações. Motivos individualizados em `5-Selecao de casos.md`.

**Limites:** a existência dos campos e botões não comprova validação, persistência nem regra de negócio. Nenhum bug está confirmado no momento.

---

### 4. **Ferramentas / registro**

- **Ferramenta de exploração utilizada:** controle de navegador integrado à sessão autenticada, conforme relatório fornecido.
- **Documentação:** arquivos Markdown para requisitos, cenários, acompanhamento e defeitos.
- **Ferramenta de captura de evidências na execução:** ainda não informada.
- **Navegador/versão e sistema operacional da futura execução:** ainda não informados.

---

### 5. **Técnicas previstas**

- Exploração orientada por interface.
- Cenários positivos e negativos.
- Validação de campos/formatos, datas e valores.
- Consulta de registros e consistência entre módulos.
- Verificação de transições de estado em check-in e recebimento.

---

### 6. **Critérios de avaliação e evidência**

1. **Passou:** comportamento real corresponde ao critério previamente confirmado, com evidência registrada.
2. **Falhou:** comportamento real diverge do critério confirmado, com passos e evidência reproduzíveis.
3. **Bloqueado:** execução impedida por falta de autorização, massa de dados, integração ou pré-condição.
4. **Não executado:** nenhum procedimento formal realizado.

**Atenção:** casos cujo resultado dependa de regra de negócio ainda não confirmada devem ser esclarecidos antes de serem classificados como falha.

---

### 7. **Condições para iniciar e encerrar a execução**

- Confirmar autorização para ações de gravação no ambiente compartilhado.
- Preparar clientes, planos e demais registros fictícios e descartáveis, com estado inicial conhecido.
- Evitar cobranças, pagamentos, envio de mensagens, check-ins indevidos e manipulação de dados reais.
- Recolher prints ou outra evidência por caso efetivamente executado.
- Registrar defeitos somente se observados, com resultado esperado e obtido.
- No encerramento, contabilizar aprovados, falhos, bloqueados e não executados sem preenchimento fictício.

---

### 8. **Cronograma**

| Atividade | Situação | Data |
| --- | --- | --- |
| Exploração da interface | Concluída | 20/10/2026 |
| Seleção e documentação de 27 casos | Planejada/documentada | Com base na exploração e seleção desta conversa |
| Execução formal dos casos | Não iniciada | Não definida |
| Coleta de evidências e registro de defeitos | Não iniciada | Não definida |
| Relatório de execução concluído | Pendente | Não definida |

---

### 9. **Módulos e casos selecionados**

| Código RF | Módulo | Qtde. planejada | Casos |
| --- | --- | --- | --- |
| RF01 | Autenticação | 3 | AUT-01, AUT-02, AUT-03 |
| RF02 | Dashboard | 1 | DASH-01 |
| RF03 | Clientes | 5 | CLI-01, CLI-02, CLI-03, CLI-04, CLI-05 |
| RF04 | Matrículas | 2 | MAT-01, MAT-02 |
| RF05 | Avaliações | 2 | AVA-01, AVA-02 |
| RF06 | Turmas | 2 | TUR-01, TUR-02 |
| RF07 | Check-in | 2 | CHK-01, CHK-02 |
| RF08 | Presenças | 1 | PRE-01 |
| RF09 | Financeiro | 4 | FIN-01, FIN-02, FIN-03, FIN-07 |
| RF10 | Treinamento | 1 | TRE-01 |
| RF11 | Comercial | 2 | COM-02, COM-03 |
| RF12 | Saúde / Anamnese | 2 | SAU-01, SAU-02 |

**Total:** 27 casos; **executados:** 0.

---

### 10. **Gestão de defeitos**

Usar `3-Relatorio-de-Bugs.md` para registrar apenas defeitos confirmados por execução, incluindo ID, módulo, caso associado, passos, comportamento esperado e real, severidade e evidência.

---

### 11. **Riscos / restrições identificados**

| Restrição identificada na exploração | Implicação no teste |
| --- | --- |
| Uso de ambiente de demonstração compartilhado | Alterações exigem autorização e registros fictícios. |
| Sem regras de negócio formalizadas | Critérios de aceitação são propostos e precisam de confirmação quando ambíguos. |
| Dados e indicadores carregados de forma assíncrona | Esperar o carregamento para interpretar valores. |
| Ações financeiras/externas e automações | Não testar em produção sem isolamento e autorização. |
| Permissões por diferentes perfis não exploradas | Escopo cobre apenas comportamento sob a sessão disponível. |

---

### 12. **Entregáveis disponíveis agora**

- Relatório de exploração e inventário visual.
- Análise de requisitos candidatos.
- Plano de testes e escopo reduzido.
- 27 casos planejados em 12 arquivos de cenário.
- Relatório de bugs sem ocorrências registradas (execução não iniciada).
- Relatório de acompanhamento pré-execução (sem resultados inventados).
- Diretório de evidências ainda vazio.
